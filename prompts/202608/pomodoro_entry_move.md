- **PLAN:**
  [202608/pomodoro_entry_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/pomodoro_entry_move.md)
- **AGENTS:**
  - [bbugyi200.athena.0el--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0el.md)

We recently added support to the `<ctrl+shift+m>` keymap in Obsidian for Pomodoro
sub-bullets. Can you now help me add support for using this keymap when the pomodoro
bullet itself is selected?

- If the user selects a different Pomodoro when prompted in this case, we should delete
  the current Pomodoro and move all of its sub-bullets to that Pomodoro.
- If the user types in the name of a new Pomodoro, however, we should just rename the
  current Pomodoro.
- See related git commits from earlier today for more context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
