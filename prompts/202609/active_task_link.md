- **PLAN:**
  [202609/active_task_link.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/active_task_link.md)
- **AGENTS:**
  - [bbugyi200.athena.0t3--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0t3.md)

Can you help me add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new solo (i.e. the only contents in a capture input)
`^file:id[#pomodoro]=<X>` syntax that works just like the solo `@file:id[#pomodoro]=<X>`
syntax except for a single twist?

- The twist is that `^` should only trigger completion for in-progress or next Obsidian
  tasks (i.e. the tasks associated with active task links) and should trigger
  full-completion (i.e. the `:id` part will be expanded as well).
- See the bob-cli-26 epic bead for context on the `=<X>` syntax.
- I'm not sure if the solo `@file:id` syntax even supports the `=<X>` yet, so you might
  need to add support for that.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
