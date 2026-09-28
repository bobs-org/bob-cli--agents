- **PLAN:**
  [202609/capture_pomodoro_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_pomodoro_close.md)
- **AGENTS:**
  - [bbugyi200.apollo.2i--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2i.md)

Can you help me add support for a new `=x` syntax to the `bob capture` command and the
corresponding bob-mac-capture app?

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
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
