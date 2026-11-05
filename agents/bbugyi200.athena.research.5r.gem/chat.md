# Chat History - ace-run (research.5r.gem)

- **TIMESTAMP:** 2026-11-05 09:16:46 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.5r.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_090404.md`

## Prompt

%id(gem, clan=research.5r)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5r.cdx`, `research.5r.cld`, `research.5r.grk`, `research.5r.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

The `%c` capture directive works well when there is no index (i.e. we only fetch the
last clipboard entry), but when we attempt to fetch more than one clipboard entry, only
the first seems to ever be correct.

- I'm not really sure what's causing this, but I'm wondering if we maybe integrated with
  the wrong clipboard manager running on my macbook?
- Regardless of what the underlying root cause of this issue is, I would like to make
  the `%c` capture directive much more resiliant and reliable.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Summary: Clipboard `%c` Multi-Entry History Architecture & Resilience

The investigation into the `%c` capture directive and multi-entry history resolution (`%c<N>`) has been completed. The comprehensive research report has been written and registered as a durable SASE artifact:

- **Report Path**: [`clipboard_c_history_resilience__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_32/sase/repos/research/202611/clipboard_c_history_resilience__gem.md)
- **Artifact Label**: `research:202611/clipboard_c_history_resilience__gem.md`
- **Artifact Snapshot**: `file:explicit:b582eaeb02d010af5a162525`

---

## 1. Root Cause: Why Only the First Entry Is Correct

The symptom where `%c` (or `%c1`) works reliably while `%c<N>` (`N > 1`) only returns an accurate first entry stems from a fundamental divergence in how single vs. multi-clipboard values are fetched in [`clipboard.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_32/src/native/capture_clip/clipboard.rs#L10-L56):

1. **Single Entry (`count == 1`)**:
   - Calls `read_clipboard()`, which on macOS invokes `pbpaste` (`NSPasteboard.generalPasteboard`).
   - `pbpaste` communicates directly with the macOS window server via AppKit. It requires no background daemon, has zero latency, and always returns the current system clipboard.
2. **Multi-Entry (`count > 1`)**:
   - Calls [`read_clipboard_history(count)`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_32/src/native/capture_clip/clipboard.rs#L15-L33), which reads `current` via `pbpaste`, and then calls `read_history_candidates(count)`.
   - On macOS, `read_history_candidates` hardcodes reading from:
     `~/Library/Application Support/com.clipy-app.Clipy/sqlite.db` via [`read_clipy_history()`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_32/src/native/capture_clip/clipy.rs#L5-L47).
   - In [`merge_history_candidates()`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_32/src/native/capture_clip/clipboard.rs#L35-L55), `current` is prepended at index 0, and the top `count - 1` entries from the SQLite query are appended.

### Did We Integrate with the Wrong Clipboard Manager?
**Yes.** Clipy was hardcoded as the sole built-in macOS history backend in commit `e6b70be4` (July 2026).
- **The "Zombie Database" Trap**: If Clipy was ever run on your MacBook in the past, its `sqlite.db` remains on disk indefinitely. `bob-cli` only checks `database.is_file()`; it does not check if the `Clipy` process is alive or whether the database entries are fresh.
- When you copy items today and run `%c3`, `bob` takes the live copy from `pbpaste` (accurate entry #1) and pairs it with entries from July 2026 read from the dormant `sqlite.db` (stale entries #2 and #3).
- **Even if Clipy is running**, Clipy's internal Swift implementation introduces major hazards:
  1. **500ms Timer Lag**: Clipy polls `NSPasteboard.general.changeCount` every 500ms; rapid successive copies are not yet committed to SQLite when capture triggers.
  2. **1-Second Timestamp Resolution**: Clipy stores `updateAt` as whole integer seconds. Intra-second copies share identical timestamps, falling back to `ORDER BY id DESC` where `id` is a content hash or UUID—scrambling chronological order.
  3. **Duplicate Suppression**: When `allowsDuplicateHistory` is disabled, re-copying existing text does not bump the timestamp.
  4. **Process Interruptions**: Scripts such as `paste_parts` in `chezmoi` explicitly invoke `killall Clipy 2>/dev/null`.

---

## 2. Critique of the Plan & Architecture

- **Brittle Coupling to External SQLite Files**:
  Directly querying the unversioned private SQLite database of a third-party application without an IPC interface, process liveness check, or schema contract is fragile. It risks lock contention, silent stale reads, and breaks whenever the third-party app updates its schema or is replaced by the user.
- **Cognitive Volatility of Multi-Clipboard Capture**:
  While capturing multiple items in one stroke (`%c3`) eliminates repetitive app-switching, the system clipboard is a volatile global stack. Background utilities (password managers, linters, vim yanks) easily pollute history.
- **Flawed Strictness**:
  `bob` currently hard-fails the entire capture if `available < count`. When a user requests `%c3` but only 2 items are captured, failing the whole task without offering the available entries creates unnecessary friction.

---

## 3. Recommended Solution & Adjustments

Rather than writing adapters for various third-party clipboard managers (Maccy, Raycast, Alfred), **own the clipboard history through Bryan's native `bob-mac-capture` app**:

1. **First-Party History in `bob-mac-capture` (Primary Provider)**:
   - `bob-mac-capture` already runs 24/7 in the macOS menu bar and already monitors `NSPasteboard.general.changeCount`.
   - Have `bob-mac-capture` maintain an in-memory ring buffer (last 25 items) and persist it to `~/.local/state/bob/clipboard_history.json`.
   - `bob-cli` checks this first-party file first. This provides zero polling delay, exact millisecond timestamps, zero third-party dependencies, and full control over format and privacy.
2. **Fail-Fast Liveness & Staleness Guards (Immediate Safety Fix)**:
   - When reading any external database (Clipy or future fallbacks), check `pgrep -x Clipy`.
   - Enforce a staleness threshold: query `MAX(updateAt)`. If the newest entry is older than 15 minutes, reject the database with an actionable diagnostic rather than returning stale data.
3. **Provider Resolution Hierarchy**:
   ```
   1. BOB_CLIPBOARD_HISTORY_CMD (explicit environment override / CI mock)
   2. First-party history (~/.local/state/bob/clipboard_history.json from bob-mac-capture)
   3. External manager (e.g. Clipy/Maccy) ONLY if process is active and records are fresh
   4. Clear diagnostic error with remediation steps (never silent zombie fallback)
   ```
4. **Observability**:
   - Add a `bob clip status` diagnostic subcommand so you can instantly verify which clipboard history provider is active, its liveness status, and available entries.
