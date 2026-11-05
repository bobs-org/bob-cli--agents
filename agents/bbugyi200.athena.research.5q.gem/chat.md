# Chat History - ace-run (research.5q.gem)

- **TIMESTAMP:** 2026-11-05 09:01:42 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.5q.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_083757.md`

## Prompt

%id(gem, clan=research.5q)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5q.cdx`, `research.5q.cld`, `research.5q.grk`, `research.5q.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Obsidian tasks should always have a type (either implicitly or explicitly) that matches
one of the task types of a pomodoro that contains a task link pointing to that task, but
we don't seem to do a good job of enforcing this currently. I would like to change that.

- The `bob task reconcile` command should be used as a fallback mechanism to ensure this
  is always the case (by removing or adding types to pomodoro lines as necessary).
- With that said, we should try to make sure that any keymaps that can currently break
  this constraint are fixed, so the `bob task reconcile` command is rarely needed to
  perform this cleanup.
- I think that the exception to this rule should maybe be custom pomodoro names, but I
  don't use these much so don't let them constrain the design too much (but don't break
  anything).

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

### Research Summary: Enforcing Task-to-Pomodoro Type Consistency

**Researcher:** `research.5q.gem`  
**Report Path:** [`pomodoro_task_type_alignment__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_33/sase/repos/research/202611/pomodoro_task_type_alignment__gem.md)  
**Artifact Registration:** `research:202611/pomodoro_task_type_alignment__gem.md` (`explicit:c55e8ced788cd2a1ee3bc5f1`)

---

### 1. Root Cause Analysis: Why Does Type Drift Occur Today?

In Bob's type architecture, tasks carry an intrinsic effective type (derived via `[type::]`, `#ref` reading rules, note frontmatter `task_type:`, or the global fallback `plan.default_type: CHORE`). Pomodoros in the daily ledger carry a name tail containing type components (`— COMP1 + COMP2`) from the configured vocabulary (`PLAN`, `BUILD`, `READ`, `CHORE`, `WRITE`, `FIX`, `MEET`).

An audit of `bob-plugins` and `bob-cli` reveals the primary leak points:

1. **The "Unlink Without Shedding" Gap (Primary Leak):**
   * Linking gestures (`Ctrl+Shift+Enter` and `((`) attempt to merge types on link insertion.
   * However, **every unlink and removal gesture ignores type shedding**:
     * `Alt+N` (`toggleTaskLaneOnLinks` in [`520-plugin-lane-links-and-review.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_33/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/520-plugin-lane-links-and-review.js#L140)) releases tasks to Ready via [`planDeferredPomodoroLinkCleanup`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_33/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/160-pomodoro-reorder.js#L568). It strips the link bullet, but leaves the Pomodoro name unchanged.
     * `Ctrl+Shift+Enter` on an already-linked task unlinks it via `planAllOpenPomodoroLinkCleanup`, but never sheds types.
     * Task rescheduling (`Alt+P`, `Ctrl+Shift+P reschedule`) and cancellation prune the link bullet but leave the type component in the Pomodoro name.
   * *Result:* Pomodoros accumulate orphaned, stale type components whose tasks have already been completed, released, or rescheduled.
2. **Untimed Placeholder Linking:**
   * Linking a task into an unnamed placeholder `- [ ] ()` classifies it as a container. The placeholder is not initialized with the task's type, leaving it untyped when started or named later.
3. **Task Move Relocation Abort:**
   * When moving a task (`Ctrl+Shift+M`) to a note without a `task_type:` default, [`gestureRetypeMoveShouldRelocate`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_33/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/650-plugin-move-commit.js#L33) returns `null`, stranding the live link under the old Pomodoro while the task's type resets.
4. **Direct In-Editor Modifications:**
   * Cutting/pasting link bullets in Vim (`dd`, `p`) or manually renaming Pomodoro entries in `YYYYMMDD.md` bypasses plugin hooks completely.
5. **No CLI Fallback in `bob task reconcile`:**
   * `bob task reconcile` previously treated Pomodoro names as strictly read-only never-writers (emitting only a read-only `type_mismatch` lint in `bob plan`), leaving drift uncorrected.

---

### 2. Plan Critique & Requirements Refinement

* **Is this a good idea?** **Yes.** Pomodoro names directly feed `bob stats`, Worked time, and Pomodoro catalogs. If a Pomodoro says `— FIX` but contains a `WRITE` task, time-tracking accounting is corrupted. Automating synchronization on the daily note ledger relieves cognitive burden while preserving task-side domain integrity.
* **Closed Pomodoros Boundary:** Reconcile must **never mutate closed (`[x]`) Pomodoro entries**. Closed sessions represent historical facts settled at completion. Retroactively renaming closed sessions when a project note's frontmatter changes weeks later would distort past logs. Reconcile must strictly target **open** Pomodoros in today's daily note.
* **Empty / Plain-Text Sessions:** If a Pomodoro has child list items that are purely plain-text notes/prose (ad-hoc work without formal task links), reconcile must **not** strip its type name. Type reconciliation applies only to Pomodoros that hold Task Links.
* **Custom Pomodoro Names Exception:**
  * **Pure Containers:** Entries with *zero* configured type components (e.g., `— INTERVIEW`, `— 1:1 WITH ALEX`, `— TAXES`, `— LATER`) must be treated as **exempt containers**. Reconcile must not append `+ TYPE` to pure containers, preserving human-titled events.
  * **Mixed Entries:** For entries with both labels and types (e.g., `— SASE + BUILD`), the label (`SASE`) is immutable, while the type component (`BUILD`) is synchronized against child tasks.
  * **`MEET` Entries:** Calendar-synced entries (`MEET`) are strictly exempt.

---

### 3. Recommended Solution

#### A. Authoritative Fallback in `bob task reconcile` (`bob-cli`)
Implement a new pass in `src/native/task_status_hooks/sync.rs` executing immediately after structural cleanup and empty-Pomodoro pruning:
1. Scan open Pomodoros (`[ ]`) in today's `## Pomodoros`.
2. Skip closed entries, `MEET` entries, and pure custom containers.
3. For each Pomodoro with live Task Links:
   * Compute the active task type set $\mathcal{T}_{tasks}$ from resolved tasks.
   * Separate existing name components into labels $\mathcal{L}$ and type components $\mathcal{T}_{pomo}$.
   * Shed types in $\mathcal{T}_{pomo}$ not in $\mathcal{T}_{tasks}$; append missing types from $\mathcal{T}_{tasks}$.
   * Reassemble the Pomodoro name: $\text{join}(\mathcal{L} \mathbin{\Vert} \mathcal{T}_{next}, \text{ " + "})$.
   * Rewrite the daily note line in-place, preserving timespans and inline metadata.

#### B. Proactive Keymap Hardening (`bob-plugins`)
1. **Link Cleanup Shedding:** Update [`planDeferredPomodoroLinkCleanup`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_33/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/160-pomodoro-reorder.js#L568) and `planAllOpenPomodoroLinkCleanup` to evaluate the remaining links of the owning Pomodoro. If all tasks of type $T$ have been removed, invoke `api.planShed` to prune $T$ from the Pomodoro header during `Alt+N`, unlinking, rolling, or cancelling.
2. **Move Fallback:** Update `gestureRetypeMoveShouldRelocate` in [`650-plugin-move-commit.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_33/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/650-plugin-move-commit.js#L33) to fall back to `plan.default_type` (`CHORE`) when moving to notes without `task_type:`, relocating the link rather than aborting.
3. **Placeholder Initializer:** In `block-id-prompt`, when linking a task to `- [ ] ()`, initialize the header with `- [ ] () — TASK_TYPE`.
