- **PLAN:**
  [202609/flash_overdue_pomodoro_warning.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/flash_overdue_pomodoro_warning.md)
- **AGENTS:**
  - [bbugyi200.apollo.2j--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2j.md)

We currently have a mac menu bar countdown for the current pomodoro (this is defined via
Hammerspoon in my chezmoi repo I believe). When the current pomodoro is >=10 minutes
overdue, we show `OVERDUE POMODORO` in bold red font instead of a countdown. This all
works good, but I'd like to make the `OVERDUE POMODORO` text stand out even more somehow
by animating it (maybe make it blink?). Think hard about what the best way to implement
this is / what the best UX for this is.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
