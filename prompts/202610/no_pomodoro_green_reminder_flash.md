- **PLAN:**
  [202610/no_pomodoro_green_reminder_flash.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/no_pomodoro_green_reminder_flash.md)
- **AGENTS:**
  - [bbugyi200.athena.0wk--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0wk.md)

The pomodoro indicator in the menu bar on my macbook (defined by Hammerspoon in my
chezmoi repo) has `OVERDUE` text that is shown when the current pomodoro is overdue >=10
minutes and flashes red. I would like to do something like this (flash) for the
`NO POMODORO` text that is shown when there is no current pomodoro, but it can't flash
all of the time because that would be annoying. Instead, can you help me make the
`NO POMODORO` text flash green for 60 seconds on every 10th minute?

- This way I'll wind up remembering that I should set a pomodoro more often (sometimes I
  close the current one and then forget to set a new one).
- Make sure that the `NO POMODORO` text always flashes green for the first 60 seconds
  that it is shown (and then for 60 seconds every 10 minutes atter that). This way I'm
  always reminded to set a new pomodoro right after closing the current one.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
