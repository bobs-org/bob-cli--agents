- **PLAN:**
  [202610/subproject_cascade.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/subproject_cascade.md)
- **AGENTS:**
  - [bbugyi200.apollo.71--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.71.md)

Can you help me implement the `subproject_cascade` decision described in the
project_task_pull_in.md file in the plans sidecar repo that we initially chose not to
implement?

- Also, as a part of this change, let's have the `bob task reconcile` command start
  marking all sub-projects of blocked projects as blocked, recursively.
- The `<ctrl+shift+p>` keymap should also support this when marking a project task as
  blocked that corresponds to a project with sub-projects.
- Normal tasks AND the project task in these sub-project files should be given the
  `#prj_is_blocked` tag, as should already be done for normal tasks in blocked projects
  (see the bob-cli-6u epic bead for context).
- The `bob task reconcile` command and the `<ctrl+shift+p>` keymap should also support
  reversing this change when appropriate.
- Think hard about the best way to implement this without harming performance too much
  or breaking anything.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
