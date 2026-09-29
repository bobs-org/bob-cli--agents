- **PLAN:**
  [202609/project_task_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/project_task_links.md)
- **AGENTS:**
  - [bbugyi200.apollo.35--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.35.md)

Can you help me add support to the `bob capture` command and its corresponding
bob-mac-capture app for a new ` :id` syntax that can be used at the end of sub-bullets
that will be turned into tasks in the new project note file we create when the
`@file^id+` / `@file^id#pomodoro+` syntax is used?

- This will allow me to easily name these tasks (e.g. append `^id` to them) and specify
  that they should have a corresponding task link added to the current/next pomodoro.
- We should start requiring that `@file^id+` be used instead of `@file:id+`, since we
  never want to add a task link for the special `^prj` task.
- Also, we will probably need to add support for the `@file^id#pomodoro+` syntax (the
  `#pomodoro` will only have meaning when at least one sub-bullet uses the `:id` syntax
  that this feature adds).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
