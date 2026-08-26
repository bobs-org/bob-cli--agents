- **PLAN:**
  [202608/pomodoro_bullet_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/pomodoro_bullet_move.md)
- **AGENTS:**
  - [bbugyi200.athena.0eb--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0eb.md)

Can you help me add support to the `<ctrl+shift+m>` keymap for moving pomodoro
sub-bullets and also add support for "named pomodoros"?

- Named pomodoros are pomodoros that have an em-dash followed by a name (may be one or
  more words). See the pomodoros at the bottom of the ~/bob/2026/20260826.md file for an
  idea of what these should look like.
- When the `<ctrl+shift+m>` keymap is used on a pomodoro sub-bullet, then the user
  should be prompted to select from one of the other open (named or unnamed) pomodoro in
  this file. They may also type in the name of a new pomodoro that should be created and
  added below the current pomodoro instead (the name provided by the user should have
  all of its letters capitalized).
- This keymap should also accept a count. For example, `2<ctrl+shift+m>` would specify
  that we should move this pomodoro sub-bullet and the 2 below it to the same other/new
  pomodoro specified by the user.
- Update the pomodoro glossary entry to reflect these changes. Make sure this glossary
  definition is excellent but also concise. Remember that every token in context either
  helps or hurts us.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
