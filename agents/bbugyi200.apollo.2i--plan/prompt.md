#gh:gh_bobs-org__bob-cli Can you help me add support for a new `=x` syntax to the `bob capture` command
and the corresponding bob-mac-capture app?

- This syntax specifies that the currently running pomodoro (if there is none, we should
  produce a useful error/diagnostic for the user) should be closed/stopped.
- See how the `<ctrl+shift+enter>` Obsidian keymap handles this for inspiration (we
  should perform the same actions when closing a pomodoro using the `bob capture`
  command).
- This syntax should be able to be used like this, to first pull the Obsidian task with
  ID `^id` in the ~/bob/file.md file into the current pomodoro: `@file:id=x` (the
  `^file:id=x` syntax should also be supported)
- The `=x` syntax should also be able to be used on its own (i.e. it can be the only
  input) to just close/stop the current pomodoro.
- Make sure that when `=x` is typed in the bob-mac-capture app that the user is shown an
  excellent preview of the pomodoro that he/she is about to close.
- #beau

#plan %m:@xlarge %auto