- **PLAN:**
  [202610/successor_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)
- **AGENTS:**
  - [bbugyi200.apollo.research.0p.linker.w0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md)

I would like to start automatically creating task links for tasks that depend on tasks
that we close in the current daily file. Can you help me implement this?

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
- Review the unblocked_successor_links_on_close.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
