# Chat History - ace-run (research.0z.gem)

- **TIMESTAMP:** 2026-10-12 07:00:22 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.0z.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261012_064148.md`

## Prompt

%id(gem, clan=research.0z)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.0z.cdx`, `research.0z.cld`, `research.0z.grk`, `research.0z.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
would like to add full support to prj tasks for task dep links.

- You can add a dependency to a prj task now (using the `<ctrl+shift+p>` keymap, for
  example), but the result is not intuitive (see the ~/bob/job_apply_to_databricks.md
  file, which should be auto-fixed by the `bob task reconcile` command after this
  change, for an example).
- When a prj task is given a dep link, it should be added as a `depends_on` frontmatter
  field on that project note, not in a "Depends On" sub-subullet. Make sure to update
  the `<cmd+ctrl+shift+n>` Obsidian keymap to support this change so project notes are
  converted from tasks correctly.
- Most importantly, any task that lives in a blocked project should also be blocked (in
  this case, because the project has an unmet dependency, but whenever a project is
  blocked this rule applies).
- We will need to make sure to update the `<ctrl+shift+p>` keymap so this occurs
  automatically when I add a dependency to a prj task using that keymap.
- Keep in mind that blocked tasks should not have corresponding task links, so those
  should be removed (along with the pomodoro section they live in if it becomes empty)
  if they exist.
- We should also update the `bob task reconcile` command to check for any tasks that
  should be blocked and/or have their corresponding task links removed.
- The "task dep links" glossary memory web term should be updated accordingly.

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

I have completed the research and recorded the full report at:
[`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/project_task_dependency_links_and_blocked_propagation__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/project_task_dependency_links_and_blocked_propagation__gem.md)

The artifact snapshot has been registered with SASE as:
`research:202610/project_task_dependency_links_and_blocked_propagation__gem.md` (Artifact ID: `explicit:41bbe2b9ff4adbfd2a581f2a`).

---

### Executive Summary & Key Findings

#### 1. Live Vault Case Study Analysis
Inspection of [`~/bob/job_apply_to_databricks.md`](file:///home/bryan/bob/job_apply_to_databricks.md) and [`~/bob/2026/20261012.md`](file:///home/bryan/bob/2026/20261012.md) confirmed the defects:
1. `job_apply_to_databricks.md` had `\t- ⛓️ **DEPENDS ON:** [[job#^update-linkedin]]` indented beneath `^prj`, which collides with project sub-block parsing (`src/native/projects/scan.rs::parse_prj_sub_block`).
2. The prerequisite `job#^update-linkedin` is open (`[/] In Progress`). While `^prj` was marked `[?]`, its two constituent tasks remained `[*] Next` in `### Next & In Progress` (with badge `🔵 2 next/wip · 🔴 0 blocked`).
3. In `20261012.md`, both blocked tasks were linked under today's open Pomodoro session `- [ ] (**0645-0710** [t:: 25m]) — JOB` alongside active tasks.

#### 2. Plan Critique & Architecture Evaluation
- **Is this a good idea?** Yes. Storing project-level dependencies in YAML frontmatter (`depends_on: ["[[note#^id]]"]`) mirrors how project schedules (`scheduled: YYYY-MM-DD`) work in [`docs/projects.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/docs/projects.md). Cascading blocked status to member tasks enforces finish-to-start dependency integrity.
- **Tension 1 (Sticky Lane Erasure on Recovery)**: Under [`decisions:task-lanes-are-sticky`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/memory/decisions/task-lanes-are-sticky.md), *lanes do not survive Blocked*. When a blocked project unblocks, its tasks will recover to Ready `[ ]` (unless linked today or in recent activity). This is GTD-correct (a waking project requires intentional triage via `Alt+N`), but the user must be aware that prior `Next` markers will not automatically reappear.
- **Tension 2 (Inherited Blocked vs. Field Stamping)**: Subtasks must derive Blocked dynamically at reconcile time (`has_derived_block = true`) rather than stamping `[dependsOn::]` on every line. This avoids graph bloat and R2 adoption churn.
- **Tension 3 (Pomodoro Pruning Scope)**: Task link pruning applies strictly to **open/planned** Pomodoros (`- [ ] ()` or `- [ ] (timespan)`). Completed/closed Pomodoro bullets (`- [x] (timespan)`) are immutable historical work logs and must never be pruned.

#### 3. Recommended Adjustments to the Requirements
1. **Frontmatter Grammar Tolerance**: Support YAML flow lists (`depends_on: ["[[...]]"]`), block lists (`depends_on:\n  - "[[...]]"`), and scalar strings (`depends_on: "[[...]]"`). Wikilinks in frontmatter must be quoted.
2. **Project Task Line Cleanup**: The `^prj` line must lose `[dependsOn::]` in favor of frontmatter `depends_on`.
3. **Definition of Blocked Project**: A project is blocked if: (a) frontmatter `depends_on` has open prerequisites, (b) frontmatter `scheduled` is future, (c) `^prj` is `[?]`, or (d) frontmatter `status` is `waiting` or `blocked`.

---

### Implementation Scope

1. **`bob-cli` (Rust Core)**:
   - `src/native/projects/scan.rs`: Add `parse_project_dependencies` to parse frontmatter `depends_on`.
   - `src/native/task_status_hooks/reconcile.rs`: Auto-fix legacy `⛓️ **DEPENDS ON:**` sub-bullets under `^prj` by promoting them to frontmatter `depends_on` and stripping `[dependsOn::]` from `^prj`.
   - `src/native/task_status_hooks/sync.rs`: Evaluate `blocked_project_files` and pass `in_blocked_project` into `has_derived_block = true` for all member tasks.
   - `src/native/task_status_hooks/structure.rs`: Prune open Pomodoro links pointing to blocked tasks in `plan_structural_changes`. Childless entries are automatically removed by `plan_empty_pomodoro_removals`.
2. **`bob-plugins` (Obsidian Hotkeys)**:
   - `<cmd+ctrl+shift+n>` (`createProjectNoteFromTask` / `convertProjectNoteToTask`): Seed source task dependencies into new frontmatter `depends_on`; restore them on reversal.
   - `<ctrl+shift+p>` Task Card (`set-bullet-property` → `b`): When cursor is on `^prj`, route updates to frontmatter `depends_on`, mark member tasks `[?]`, and prune matching open Pomodoro links via `planDeferredPomodoroLinkCleanup`.
3. **SASE Memory & Docs**:
   - Update `glossary:task_dep_link` to document project note frontmatter `depends_on`, cascading blocked status, and open Pomodoro pruning.
   - Update `docs/task-dependencies.md` and `docs/projects.md`.
