#gh:gh_bobs-org__bob-cli Can you help me improve the way the `<ctrl+shift+m>` keymap works when used
on a pomodoro (e.g. to rename or move that pomodoro)?

- We should add support for merging pomodoros by selecting that pomodoro (e.g. using the
  `<ctrl+n/p>` keymaps) and using a new `<ctrl+x>` keymap.
- When we merge on pomodoro into another, the bullets from the one being merged into
  (i.e. appended to) the other should be added to the end of that pomodoro's bullets.
  The name of the old pomodoro should be appended to the name of the one we merge into,
  separated by a `+`.
- Future pomodoros should always be merged into (i.e. appended to) the pomodoro that the
  user selects. For current pomdoros, however, the selected pomodoro should be merge
  into the current one.

#plan %m:@xlarge