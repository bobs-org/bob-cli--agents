# Chat History - ace-run (research.03.gem)

- **TIMESTAMP:** 2026-10-03 09:26:53 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.03.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261003_091907.md`

## Prompt

%id(gem, clan=research.03)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.03.cdx`, `research.03.cld`, `research.03.grk`, `research.03.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start tracking every time an Obsidian task is explicitly refreshed (i.e.
its `fresh` property is updated by using the `<alt+f>` keymap) using a new
`refresh_count` property.

- This property should be rendered as an appropriate icon (like we do with `fresh`).
- The goal of this change is to enable some sort of (user approved--at the time of
  decay) auto-decay for tasks that continue to be manually refreshed, but I haven't got
  that part worked out yet. We already support auto-decay for repeat priority rolls but
  not for repeat rotten task refreshes. Think hard about the best way to do this.
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
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report Summary: Task Refresh Count Tracking & Auto-Decay for Rotten Tasks

**Researcher:** `researcher gem` (`research.03.gem`)  
**Report Path:** [`sase/repos/research/202610/task_refresh_count_and_auto_decay__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/task_refresh_count_and_auto_decay__gem.md)  
**Artifact Snapshot:** `research:202610/task_refresh_count_and_auto_decay__gem.md` (`file:explicit:fd979fd65deb37a93fe2b568`)

---

### Executive Overview & Critique of the Proposed Plan

Tracking consecutive refreshes is an essential antidote to the **"Rotten Review Treadmill"** (the tendency to repeatedly hit `<alt+f>` to defer an aging task without genuine intent to execute). However, our architectural analysis reveals three critical refinements needed for the initial plan:

1. **Storage Syntax & Sparsity (`[refresh_count:: N]`):**
   * *Lexical Collision:* In Bob's Dataview grammar, `[refresh:: N]` **already exists** to specify the custom review interval in days (e.g., `[refresh:: 14]`). 
   * *Sparsity:* Writing `[refresh_count:: 0]` or `[refresh_count:: 1]` on every task adds unnecessary markdown bloat. We recommend a **strictly sparse field**: omitted entirely on fresh or active tasks, appearing only on the **second consecutive rotten refresh** (`[refresh_count:: 2]`), and automatically stripped whenever real work occurs (Pomodoro link, status change to `[/]` or `[*]`, manual reschedule, or priority change).
   * *Placement:* Must sit directly alongside `[fresh:: ...]` and `[refresh:: ...]`, immediately preceding the trailing Tasks suffix (`created`, `priority`, `scheduled`, etc.), synchronized across Rust (`placement.rs`) and JavaScript (`bob-ledger-tools`).

2. **Visual Representation: Folded Mark Integration vs. Standalone Icon:**
   * Rendering `refresh_count` as an isolated standalone icon creates a cluttered "Christmas tree" effect on task lines already carrying status, description, freshness mark, priority, and date icons.
   * Following the precedent of interval folding (`docs/freshness.md` §11), `refresh_count` should **fold directly into the existing freshness mark widget**:
     * Clean state: `✓ today` or `(lease ring) 4d`
     * 1st/2nd rotten refresh: `[⟳ 8d · 2×]` with a quiet tabular count suffix
     * Decay threshold reached (e.g. 3×): `[⟳ 8d · 3× 🍂]` accented with an amber/decay warning border and tooltip alert.

3. **The Auto-Decay Architecture: Dual-Track Decay Ladder:**
   * **Prioritized Tasks (Priority Demotion Ladder):** Mirrors Bob’s existing Schedule Log priority decay (`docs/projects.md`):
     $$\text{P1 (high)} \xrightarrow{\text{decay}} \text{P2 (med)} \xrightarrow{\text{decay}} \text{P3 (low)} \xrightarrow{\text{decay}} \text{P4 (lowest)} \xrightarrow{\text{decay}} \text{Cancel } [-]$$
     Each step updates the priority field, resets `refresh_count` to 0, and records a Schedule Log entry (`- *YYYY-MM-DD* — 🍂 P2 → P3 decay after 3 refreshes`).
   * **Unprioritized Tasks (Interval Backoff Leash):** For tasks lacking explicit priority, decaying directly to cancellation is too destructive. Instead, the review interval lengthens ($7\text{d} \rightarrow 14\text{d} \rightarrow 30\text{d}$) to reduce review burden, before offering terminal cancellation or `#someday` tagging.

4. **Interaction Model: "Notice-Guided Review Chords":**
   * Modal dialogs destroy the rapid, single-keystroke cadence of morning review (`]s`).
   * When landing on a task that has reached its decay threshold, the **Review Jump Notice** explicitly displays the recommended decay before any key is pressed:
     ```text
     Review 4/12 · ROTTEN (3/3 refreshes) · confirmed Sep 20
     ⚠️ Refresh limit reached: Alt+F will DECAY (P2 → P3)
     Alt+F decay & confirm · Alt+Shift+F force fresh (keep P2) · Ctrl+D cancel
     ```
   * Striking `Alt+F` executes the recommended decay, resets the counter, and shows an instant undo prompt (`Ctrl+Z`). `Alt+Shift+F` remains available as an override to force a plain refresh without decay.

---

### Implementation Scope Across Repositories

* **`bob-cli` (Rust):**
  * `src/native/freshness/placement.rs`: Extend `TASKS_KEYS` and suffix scanners to recognize, preserve, and clean `[refresh_count:: N]`.
  * `src/native/config/freshness.rs`: Add `freshness.decay: { enabled: true, refreshes: 3, action: "priority" }`.
  * `src/native/freshness/cli.rs`: Expose `refresh_count` in `bob freshness list -f json`.
* **`bob-ledger-tools` (Obsidian plugin):**
  * Parser & normalizer support for `refresh_count`.
  * Update `buildFreshnessMarkElement` and `styles.css` to render count badges and decay threshold accents.
* **`bob-navigation-hotkeys` (Obsidian plugin):**
  * Implement `planTaskFreshnessRefresh` to evaluate decay thresholds on `Alt+F`.
  * Append Schedule Log and Cancel Log records on decay execution.
  * Update `buildReviewJumpNotice` to signal upcoming decays.

The full design doc, CSS specifications, state machine logic, and test vectors (P13–P15, M10–M11, D1–D2) are recorded in the durable research artifact at [`sase/repos/research/202610/task_refresh_count_and_auto_decay__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/task_refresh_count_and_auto_decay__gem.md).
