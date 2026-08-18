- **PLAN:**
  [202608/capture_pomodoro_note_last_completed.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_pomodoro_note_last_completed.md)
- **AGENTS:**
  - [bbugyi200.athena.06v--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.06v.md)

Can you help me change the behavior of the special `#` syntax used with the
`bob capture` command (added earlier today I believe) when there is no current pomodoro?
Namely instead of adding the bullet to the next Pomodoro, we should add the bullet to
the last completed Pomodoro in today's daily file. Unless there is no completed Pomodoro
then we should add it to the first future Pomodoro. Think this through thoroughly and
create a plan using your `/sase_plan` skill. Choose and author the appropriate tier,
validate and revalidate until it passes, then submit it with `sase plan propose` (as the
skill instructs) before making any file changes.
