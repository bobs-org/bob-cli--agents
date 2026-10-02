- **PLAN:**
  [202610/remove_pomodoro_menubar_gradient.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/remove_pomodoro_menubar_gradient.md)
- **AGENTS:**
  - [bbugyi200.apollo.4b--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4b.md)

Can you help me completely remove the color gradient logic we recently added to the
macbook menu bar pomodoro indicator (defined by Hammerspoon in my chezmoi repo)? We
should still change the color of the countdown to red when the current pomodoro is
overdue and make it flash red when we show `OVERDUE` (i.e. when >=10 minutes overdue).
Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
