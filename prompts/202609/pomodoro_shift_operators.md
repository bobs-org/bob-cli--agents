- **PLAN:**
  [202609/pomodoro_shift_operators.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_shift_operators.md)
- **AGENTS:**
  - [bbugyi200.apollo.2k--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2k.md)

Can you help me add support to the `bob capture` command and the corresponding
bob-mac-capture app for the new `++[<N>]` / `--[<N>]` syntaxes?

- We already support the `+<N>` / `-<N>` syntaxes which emulate the `\p` / `\P` Obsidian
  keymaps.
- This new syntax is meant to emulate the related `\o` / `\O` keymaps.
- For example, using `++3` should have the same effect as pressing `3\o` when the
  currently running pomodoro is selected in Obsidian.
- `<N>` should be optional and should default to `1`. Make sure to fix this for the `+`
  / `-` syntaxes as well (so I can use just `-` instead of `-1`, for example).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
