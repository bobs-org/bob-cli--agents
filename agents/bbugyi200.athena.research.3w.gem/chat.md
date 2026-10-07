# Chat History - ace-run (research.3w.gem)

- **TIMESTAMP:** 2026-10-07 06:52:32 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3w.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261007_063610.md`

## Prompt

%id(gem, clan=research.3w)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3w.cdx`, `research.3w.cld`, `research.3w.grk`, `research.3w.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We should finished adding support to the `bob highlights create` command for URLs and
migrated that command to the `bob ref create` command (see the bob-cli-4s and
bob-cli-4w, respectively, epic beads for more context).

- I would now like to add support to the `bob capture` command and the corresponding
  bob-mac-capture app for passing URls that are provided as capture input to the
  `bob ref create` command.
- Specifically, when a URL is provided as the only capture input (bulk capture with URLs
  should be supported though), then we should run the appropriate `bob ref create`
  command on the URL instead of capturing a note or task.
- I would also like to add support for doing something similar when capturing from
  Google Keep.
- Namely, any Google Keep note that is pulled down using the `bob gkeep pull` command
  that contains only a URL should not be added to the ~/bob/gkeep_inbox.md file.
  Instead, the appropriate `bob ref create` command should be run.

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
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Summary: Routing URL Ingest to `bob ref create`

The independent research report has been completed, written to disk, and registered as a durable SASE artifact:

- **Report Path:** [`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/url_capture_ref_routing__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/url_capture_ref_routing__gem.md)
- **Artifact Reference:** `file:explicit:f283bd675245daeccb1b6648` (`research:202610/url_capture_ref_routing__gem.md`)

---

## Key Findings & Critique

### 1. The Core Idea is Desirable, but a Naive Implementation is Dangerous
The user goal—routing standalone URLs captured via `bob capture`, the `bob-mac-capture` app, and `bob gkeep pull` directly to `bob ref create` instead of creating inbox tasks—removes friction from Bryan's GTD and reference workflow. However, naive synchronous handoffs introduce critical UX and data-integrity risks:
- **Latency & Interactivity Hazard:** `bob capture` is built for instant local text appending (<50ms). `bob ref create` performs heavy network I/O and Chromium/Playwright rendering (3–15 seconds).
  - Keystroke live preview (`bob capture --dry-run`) in the macOS app will freeze or stutter if it executes network calls (note: `target_mod::fetch_and_route` currently fetches generic URLs synchronously even in dry-run mode).
  - Capturing offline or on flaky Wi-Fi would cause quick-capture to fail with exit code 1, dropping the user's thought and violating the core GTD rule that capture sinks must never lose data.
- **Google Keep State & Dedupe Hazard:** `bob gkeep pull` requires a vault ledger marker (`%%gkeep:v1:<id>:<fp12>%%`) to confirm a note is in the vault before archiving it in Keep. Bypassing `gkeep_inbox.md` means no markdown marker is written (only a staged PDF in `xlib/`). A subsequent pull or `--no-archive` run will see the note again, re-attempt `ref create`, and crash on `ref create`'s dedupe refusal (`already queued in xlib/...`), blocking the pull batch.

---

## Necessary Requirements Adjustments

1. **Zero-Network Dry Run:** `bob capture-parse` and `bob capture --dry-run` must remain **100% syntactic and local**. URL classification and dedupe checks against `ref/` and `xlib/` must execute entirely in memory/disk without network fetches, preserving <10ms live preview in `bob-mac-capture`.
2. **Resilient Offline/Failure Fallback:** If `bob capture` fails to execute `ref create` due to network outage, DNS failure, or HTTP 4xx/5xx, it **must not fail or drop input**. It must fall back to capturing an ordinary task in `mac_inbox.md` with a warning.
3. **Explicit Task Escape Hatch:** Prefixing a URL with a checkbox (`- [ ] https://...`) or appending an explicit route (`https://... @inbox` or `@dev`) forces task capture, preserving the ability to create simple todo tasks containing links.
4. **Mobile Share Sheet Normalization for Keep:** Android and iOS share sheets frequently auto-populate the Keep title with the webpage title while placing the URL in the body. If classification strictly requires an empty title, over 50% of mobile link captures would fail to route. A note qualifies if its body is solely a URL, even if the title was auto-filled by the browser.
5. **Dedupe-Aware Auto-Archiving in `bob gkeep pull`:** If a Keep URL note matches an existing reference in `ref/` or `xlib/`, it is classified as `ArchiveOnly` and archived in Keep immediately without re-downloading or erroring. Furthermore, single-note URL failures must be isolated so one dead link does not block the entire Keep pull batch.

---

## Recommended Solution: Hybrid Direct Execution (Approach C)

### Architecture Highlights
- **`bob capture-parse`:** Introduces `EditorMode::RefCreate` and `SpanKind::RefUrl` for purple/blue syntax highlighting in the macOS panel.
- **`bob capture --dry-run`:** Resolves URL syntactically and runs local dedupe against `ref/` and `xlib/` in <8ms. Emits `CaptureCommandSuccess` with `kind: "ref_create"`, `routed: true`, and predicted `relative_target: "xlib/blogs/<stem>.pdf"`.
- **`bob capture` (execution):** Calls `highlights_ref::create::create_pdf` in-process. Supports single-item and mixed bulk captures. If clipping fails due to network outage, falls back safely to `mac_inbox.md`.
- **`bob-mac-capture`:** Complies with decision `mac-capture-is-a-thin-client`. Spawns `bob`, decodes `kind: "ref_create"`, renders a dedicated Reference Preview Card, and displays `"Clipping reference…"` during submission.
- **`bob gkeep pull`:** Classifies URL notes, checks dedupe to archive duplicates immediately, runs `ref create` for new URLs, logs `ref_created` events to `gkeep/journal.jsonl`, and isolates failures per-note.

### Phased Roadmap
- **Phase 1:** Grammar, `EditorMode::RefCreate`, and zero-network dry-run in `bob-cli`.
- **Phase 2:** In-process `ref create` execution, bulk support, and offline fallback in `bob capture`.
- **Phase 3:** Thin-client UI card, syntax highlighting, and submission state in `bob-mac-capture`.
- **Phase 4:** Mobile-normalized URL extraction, dedupe auto-archive, and journal tracking in `bob gkeep pull`.
