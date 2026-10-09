- **PLAN:**
  [202610/pomodoro_override.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_override.md)
- **AGENTS:**
  - [bbugyi200.apollo.61.w1.w0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.w0.md)

  Can you help me add support to the `bob capture` command and the corresponding
  bob-mac-capture app for a new `==` syntax that works just like the `=` syntax but
  allows you to override the current pomodoro? This will allow us to change the ledger
  used for the current pomodoro and/or, by using the `#pomodoro` suffix, make a
  different pomodoro in today's daily file the new current pomodoro (and migrate the old
  one to the first future pomodoro). By default, if `==#pomodoro` is used without
  specifying the start/end range (using a special syntax between the last `=` and the
  `#`), then we should keep the ledger as it is, but just make the targeted pomodoro the
  new current pomodoro. I want you to lead the design on this one. Make sure you design
  this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
