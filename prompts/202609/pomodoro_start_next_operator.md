- **PLAN:**
  [202609/pomodoro_start_next_operator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_start_next_operator.md)
- **AGENTS:**
  - [bbugyi200.apollo.2s--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2s.md)

Can you help me add support for using `=<X>` as an input (by itself) to the
`bob capture` command and its corresponding bob-mac-capture app?

- This should only be valid when there are future pomodoro in the current Obsidian daily
  file but no current pomodoro.
- It should be used to indicate that we want to start the next future pomodoro.
- We should accept the same type of values for `<X>` as we do when using the
  `@file:id=<X>` syntax.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
