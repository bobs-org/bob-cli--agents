- **PLAN:**
  [202610/pomodoro_menubar_context.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_menubar_context.md)
- **AGENTS:**
  - [bbugyi200.athena.0vg--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vg.md)

Can you help me start always showing the current pomodoro's theme and its stop time (in
some visually appealing way) in the indicator that is shown in my macbook's menu bar?

- This indicator is defined by Hammerspoon in my chezmoi repo.
- We should even show this when >=10m past due. We currently show `OVERDUE POMODORO` in
  this case. We should still show `OVERDUE`, but let's drop the `POMODORO` to save
  space.
- We should continue to show `NO POMODORO` when there is no current pomodoro.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
