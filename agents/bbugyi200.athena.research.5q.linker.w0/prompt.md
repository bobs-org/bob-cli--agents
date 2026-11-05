#gh:gh_bobs-org__bob-cli Obsidian tasks should always have a type (either implicitly or explicitly) that
matches one of the task types of a pomodoro that contains a task link pointing to that
task, but we don't seem to do a good job of enforcing this currently. I would like to
change that. Can you help me implement this?

- The `bob task reconcile` command should be used as a fallback mechanism to ensure this
  is always the case (by removing or adding types to pomodoro lines as necessary).
- With that said, we should try to make sure that any keymaps that can currently break
  this constraint are fixed, so the `bob task reconcile` command is rarely needed to
  perform this cleanup.
- I think that the exception to this rule should maybe be custom pomodoro names, but I
  don't use these much so don't let them constrain the design too much (but don't break
  anything).
- Review the pomodoro_names_follow_task_types.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

#plan %m:@xlarge %w:research.5q.linker