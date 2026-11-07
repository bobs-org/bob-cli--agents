# Chat History - ace-run (research.5x.gem)

- **TIMESTAMP:** 2026-11-07 17:34:04 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.5x.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261107_171600.md`

## Prompt

%id(gem, clan=research.5x)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5x.cdx`, `research.5x.cld`, `research.5x.grk`, `research.5x.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to add support for using `+<N>` at the end of the `<X>` in the `=<X>`,
`@file:id=<X>`, and (if you think its appropriate) the `x=<X>` capture syntaxes, where
`<N>` is some positive integer that defaults to 1 if not provided.

- This syntax should specify that the start of the pomodoro should be have `<N>`
  5-minute positive offsets added to it.
- For example, `=fix2+` should be equivalent to `=fix2 ++` and `@foo:bar=+3` should be
  equivalent to `@foo:bar= ++3`.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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

# Research Summary: Positive Pomodoro Start Offsets (`+<N>`)

**Research Report Path:** [`pomodoro_start_positive_offset__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/research/202611/pomodoro_start_positive_offset__gem.md)  
**Registered Artifact:** `research:202611/pomodoro_start_positive_offset__gem.md` (`explicit:6bbed6e83412d4822f57ff7b`)  
**Investigator:** Researcher `gem` (independent swarm study)

---

## 1. Executive Critique: Is This a Good Idea?

### The Strong "Yes": For `=<X>` and `@file:id=<X>`
Adding positive 5-minute start offsets (`+<N>`) to `=<X>` and `@file:id=<X>` is a **major usability and architectural win**:
1. **Solves an Impossible Chaining Gap:**  
   Currently, standalone starts can be chained (`=fix2 ++`), but task-link starts cannot. Typing `@work:task= ++3` captures `++3` as the task's title because `@route:id=` is a task-route token, not a session operator. Supporting `@route:id=+3` or `@route:id=fix2+` provides the **only syntactic mechanism** to atomically link a task and schedule its session in the future.
2. **Restores Mathematical Symmetry:**  
   The `<X>` timing suffix (mirroring Obsidian's `se<X>`) already supports negative offsets via `-` (e.g. `=-` for -5m, `=-2` for -10m, `=3-1` for 15m starting 5m ago). Supporting `+` completes the mental model (`[duration][sign][offset]`).
3. **Intentional Planning vs. Reactive Adjustment:**  
   The `++` shift operator requires an already-running session (failing if no session is active). `=+` or `=fix2+` allows users to author future intentions before work starts.

### The Decisive "No": Reject `+<N>` on `x=<X>`
Adding `+<N>` to `x=` is fundamentally flawed and must be rejected:
1. **Semantic Incoherence:** In Bob, `=` is present/future, `x` is present close, and `x=` is strictly for **past** records ("records what already happened"). A future start offset on a past session is an ontological contradiction.
2. **Existing Invariants:** `x=` already explicitly rejects `-` offsets (`x=3-1` teaches `x=3~1`). Permitting `+` while forbidding `-` on past records breaks consistency.
3. **Timeline Conflicts:** Past records stack backward from boundaries or pin via segment suffixes (`~n`, `~n+`).
4. **Grammar Collisions:** In `x=`, `+` is already actively used in segment pin indexing (`x=build~1+`) and compound themes (`x=bob+decks`).

---

## 2. Core Grammar Design

### Unified Grammar for `<X>`
Extend `<X>` from `[0-9]*(-[0-9]*)?` to:
```text
<X> := [ <duration_units> ] [ <offset_sign> [ <offset_units> ] ]
```
- `<duration_units>`: ASCII digits (omitted defaults to 5 units = 25 minutes).
- `<offset_sign>`: `+` or `-` (mutually exclusive; cannot mix `+` and `-`).
- `<offset_units>`: ASCII digits (omitted defaults to 1 unit = 5 minutes when a sign is present).

### Permutations Across Forms
- **Bare Starts:**
  - `=+` / `=+1`: 25m duration, start in +5m.
  - `=+3`: 25m duration, start in +15m.
  - `=3+`: 15m duration, start in +5m.
  - `=3+2`: 15m duration, start in +10m.
- **Named Starts (Leading Timing):**
  - `=+fix` / `=+2fix`: 25m FIX session starting in +5m / +10m.
  - `=3+2fix`: 15m FIX session starting in +10m.
  - `=+2#deep-work`: 25m DEEP-WORK starting in +10m.
- **Named Starts (Trailing Timing):**
  - `=fix+` / `=fix+2`: 25m FIX starting in +5m / +10m.
  - `=fix2+`: 10m FIX starting in +5m (exact equivalent to `=fix2 ++`).
  - `=fix2+3`: 10m FIX starting in +15m (exact equivalent to `=fix2 ++3`).
- **Routed Task Link Starts:**
  - `@foo:bar=+3`: Link `^bar` into today's ledger and start a 25m session in +15m.
  - `@foo:bar=fix2+`: Link `^bar` under FIX and start 10m session in +5m.
- **Multi-Theme Starts:**
  - `=bob+decks+`: 25m composite session `BOB+DECKS` starting in +5m.
  - `=bob+decks2+3`: 10m composite session `BOB+DECKS` starting in +15m.

---

## 3. Key Implementation Details in `bob-cli`

1. **Bare-Name Disambiguation:**
   Because `+` is also the Pomodoro theme separator (`is_pomodoro_selector_byte` includes `+`), the bare-name lexer (`bare_start_name_len`) previously swallowed `=fix2+` as a name (`FIX2+`).  
   *Fix:* Peeling trailing timing matching `[0-9]*([+-][0-9]*)?` before validating theme components cleanly preserves multi-theme names (`=bob+decks+`) while correctly isolating offsets.
2. **Start Minute Math:**
   In [`start_block_minute()`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture/meet_event_run.rs#L200-L225):
   ```rust
   let numerator = match spec.offset_direction {
       Some(StartOffsetDirection::Past) => now_minutes.checked_sub(offset_i64)?,
       Some(StartOffsetDirection::Future) => now_minutes.checked_add(offset_i64)?,
       None => now_minutes,
   };
   ```
3. **MEET Overlap & Calendar Sync:**
   `unnamed_start_target_with()` evaluates the offset start time. If `=+2` targets a block where an upcoming Google Calendar event begins, Bob automatically targets and joins that meeting.
4. **Backward-Compatible Data Structures:**
   `PomodoroStartSpec` and `PomodoroStartSummary` retain `offset_units: u64` and introduce an optional `offset_direction: Option<StartOffsetDirection>` (`past` vs `future`). Existing JSON consumers reading `offset_units` remain non-broken.

---

## 4. Next Steps & Recommended Action Plan

1. **Adopt the ADR Draft:** Incorporate the decision record from §7 of the report into `sase/memory/decisions/`.
2. **Implement in `bob-cli`:**
   - Update `start_timing_len` and `bare_start_name_len` in `capture_language`.
   - Update `parse_pomodoro_start_suffix` and `start_block_minute`.
   - Add rejection diagnostics for `x=+` in `parse_pomodoro_past`.
3. **Coordinate with `bob-plugins`:**
   - Update the `se<X>` snippet in `bob-ledger-tools` to expand `se+<N>`.
