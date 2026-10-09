#gh:gh_bobs-org__bob-cli I would like to start automatically creating task links for tasks that depend
on tasks that we close in the current daily file. Can you help me implement this?

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
- Review the unblocked_successor_links_on_close.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file.
- #beau

#plan %m:@xlarge %auto %w:research.0p.linker