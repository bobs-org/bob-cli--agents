# Chat History - ace-run (research.0p.gem)

- **TIMESTAMP:** 2026-10-09 10:34:48 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.0p.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261009_101739.md`

## Prompt

%id(gem, clan=research.0p)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.0p.cdx`, `research.0p.cld`, `research.0p.grk`, `research.0p.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
would like to start automatically creating task links for tasks that depend on tasks
that we close in the current daily file.

- We should support this behavior when a task link's task is closed via the
  `<ctrl+enter>` keymap in Obsidian or via the `bob capture` command's `=x!` / `=!`
  syntax.
- We should display a good toast to the user in Obsidian or via the bob-mac-capture app
  (depending on how the task was closed) to let the user know which new task links were
  added and why.
- These task links should be added to the same pomodoro that the closed task was in or
  the newly created pomodoro if the entire pomodoro that the old task was in was closed.
- It is important that we are able to perform this operation quickly so this doesn't
  effect performance too much. The bob-mac-capture app, in particular, needs to remain
  blazing fast.
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

# Independent Research Report Summary: Automatic Task Link Creation for Dependent Tasks on Close

**Researcher:** `research.0p.gem`  
**Report File:** [`auto_link_dependent_tasks_on_close__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/auto_link_dependent_tasks_on_close__gem.md)  
**Registered Artifact:** `research:202610/auto_link_dependent_tasks_on_close__gem.md` (`explicit:97213606a44a5ffa94d4ebc0`)

---

### 1. Executive Summary & Thesis

Automatically linking newly unblocked dependent tasks into today's Pomodoro ledger transforms task dependencies from **passive status metadata** (moving from Blocked `[?]` to Ready `[ ]`) into an **active execution conveyor belt**. It eliminates friction between completing prerequisites and advancing multi-stage projects.

However, an unconstrained implementation introduces severe architectural hazards:
1. **The "Hydra" Fan-Out Problem:** A single foundational prerequisite (e.g., database schema or architecture RFC) frequently unblocks 5–10 downstream tasks. Dumping all of them into a 25-minute Pomodoro explodes the session and immediately breaches the 10-link daily ledger budget (`plan.max_links_per_day`).
2. **Sticky Lane Irreversibility:** Under [`decisions:today-is-read-from-the-ledger`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/memory/decisions/today-is-read-from-the-ledger.md) and [`decisions:task-lanes-are-sticky`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/memory/decisions/task-lanes-are-sticky.md), placing a task link under an open Pomodoro **permanently raises the task to Next (`[*]`)**. Because Next is a sticky lane, unlinking or deleting the task does not revert it to Ready; only manual `Alt+N` can do so. Auto-linking is therefore an irreversible commitment to Today.
3. **Context / Theme Smear:** Closing a task in a `— DEV` Pomodoro when an unblocked dependent belongs to documentation, code review, or personal admin pollutes the focused session.
4. **Subprocess Latency Degredation:** In Bryan's vault (6,208 markdown files), an unoptimized full-vault dependency scan takes **~420ms**. In `bob-mac-capture`, where live preview runs `bob capture --dry-run` on keystrokes, 420ms violates the thin-client performance contract (`decisions:mac-capture-is-a-thin-client`).

---

### 2. Critique & Recommended Adjustments to the Plan

| Raw Requirement | Critique & Failure Risk | Recommended Adjustment |
| :--- | :--- | :--- |
| **Link all unblocked tasks** | High fan-out risk (1 task unblocks 5+), ledger bloat, budget violation (`over: true`). | **Cap auto-linking to primary dependents (max 1–2).** Prioritize same-project / highest-priority tasks. Unblock remaining tasks in their project notes (`[?]` -> `[ ]`) and report them in the toast as "unblocked in backlog". |
| **Only support `=x!` / `=!` syntax** | Inconsistent UX: completing all tasks auto-links, but completing a specific task (`=x!1`, `=!1`, `=x1!2`) ignores dependents. | **Generalize to all completion operations** in `pomodoro_close` where one or more tasks transition to Done. |
| **Add to same or newly created pomodoro** | If the entire Pomodoro was closed, dumping unblocked tasks into an existing *different* planned theme (e.g. `— REVIEW`) contaminates context. | **Thematic Continuation Routing:** When closing an open Pomodoro session, append to a newly created continuation placeholder matching the closed session's theme (`- [ ] () — THEME`). |
| **Unblocked task lacks block ID** | Tasks can be Blocked via `⛓️ **DEPENDS ON:**` without having an authored `^block-id`. A wikilink `[[note#^id]]` cannot be created. | **Block ID Guard:** Tasks without block IDs recover to Ready `[ ]` on disk, but are skipped for auto-linking; toast reports `Unblocked (no block ID; unlinked)`. |
| **Already linked today** | Multiple closed tasks could unblock a task already queued in today's daily file. | **Deduplication Guard:** Do not create duplicate links if already present under any open Pomodoro today. |

---

### 3. Performance Architecture: Keeping `bob-mac-capture` Blazing Fast

Empirical measurements on Bryan's active 6,208-file Bob vault revealed:
- Full-vault scan and read (`staged_snapshot_for_recovery`): **419 ms**.
- **Crucial Sparsity Finding:** Only **29 files** in the entire vault contain `⛓️ **DEPENDS ON:**` and only **36 files** contain `[dependsOn::]` (99.4% of notes contain zero dependencies).

#### Recommended Dual-Engine Optimization:
1. **Rust (`bob-cli`): Inverted Dependency Index Cache**
   - Maintained during `bob task-status-hooks` / `reconcile` runs in `~/.cache/bob-cli/dependency_index.json`.
   - On capture close (`=x!`), look up completed task IDs in the cached inverted index in **$O(1)$ time (< 0.1ms)** and read *only* the 1–2 candidate dependent files.
   - Total preview execution time drops from **419ms to < 10ms**, keeping Bob Mac Capture instantly responsive.
2. **Obsidian (`task-status-cycler`): In-Memory Backlink Cache Lookup**
   - Leverage Obsidian's native `app.metadataCache.getBacklinksForFile()` instead of iterating over `vault.getMarkdownFiles()`.
   - Only notes linking to the closed task's file are evaluated, eliminating main-thread UI jank (< 1ms).

---

### 4. Visual & Interaction Design: Intuitive, Reliable, Beautiful

#### 1. Obsidian In-Editor Notice (DOM Fragment)
When `<ctrl+enter>` strikes a task link and unblocks a dependent:
```text
┌──────────────────────────────────────────────────────────────┐
│  ✓ Completed: Better ^ref task tracking!                     │
│  ⛓️ Next Task Unblocked & Queued:                            │
│     ↳ [[bob#^auto-dep-task-link]] Auto-add task links...     │
│       Added to 🍅 1000-1025 — BOB (Raised to Next [*])       │
└──────────────────────────────────────────────────────────────┘
```
Styled with emerald checkmark, theme accent chain glyph (`⛓️`), monospace link pill, and muted destination metadata (5000ms auto-dismiss).

#### 2. Bob Mac Capture Preview Card & HUD
- **Live Preview Window (keystroke mode):** Typing `=x!` dynamically highlights the prospective unblocked dependent under the next Pomodoro with an `[UNBLOCKED]` badge before pressing Enter.
- **Native macOS Toast / Notification:**
```text
┌──────────────────────────────────────────────────────────────┐
│ 🍅 Closed BOB (25m) · 2 tasks completed                      │
│ ⛓️ Unblocked & Queued in Next Session:                       │
│   ↳ Auto-add task links on close                             │
└──────────────────────────────────────────────────────────────┘
```

#### 3. CLI Terminal Human Output
```text
✓ closed BOB 1000-1025 (25m) · 2026/20261009.md line 31
  1 [*] → [x] Better ^ref task tracking! bob.md ^better-refs
  2 [*] → [x] Add `bob mac` command bob.md ^mac-cmd
  ↳ unblocked & queued [?] → [*] Auto-add task links on close bob.md ^auto-dep-task-link
next: BOB (created) at line 36 · carries 1 unblocked link
```

---

### 5. Implementation Roadmap Across Repositories

1. **`bob-cli`:**
   - [`src/native/capture_pomodoro_close/linked_tasks.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/src/native/capture_pomodoro_close/linked_tasks.rs): Run dependent recovery after `complete_embedded_trees`, filter valid unblocked tasks, apply the link budget cap, append links to `ledger.carried_lines`, and promote targets to Next `[*]`.
   - [`src/native/capture/output.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/src/native/capture/output.rs): Expose `auto_linked` in `PomodoroCloseSummaryJson` and render tree-indented lines in CLI human output.
   - [`src/native/task_complete/recovery.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/src/native/task_complete/recovery.rs): Add cached sparse dependency candidate filtering.
2. **`bob-plugins` (`task-status-cycler`):**
   - [`plugins/task-status-cycler/src/080-dependencies.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/plugins/task-status-cycler/src/080-dependencies.js): Enhance `buildBlockedDependentRecoveryPlan` to return recovered task metadata.
   - [`plugins/task-status-cycler/src/130-plugin-references.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/plugins/task-status-cycler/src/130-plugin-references.js): Add backlink cache lookup to `recoverBlockedDependentsNow`.
   - [`plugins/task-status-cycler/src/160-plugin-completion.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/plugins/task-status-cycler/src/160-plugin-completion.js): Append unblocked task links to the active Pomodoro and trigger the rich `new Notice`.
3. **`bob-mac-capture`:**
   - Decode `auto_linked` from the JSON response, render badges in `PreviewCardView`, and dispatch native HUD alerts upon close.

The full, unabridged research document is available at:  
[**`sase/repos/research/202610/auto_link_dependent_tasks_on_close__gem.md`**](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/auto_link_dependent_tasks_on_close__gem.md).
