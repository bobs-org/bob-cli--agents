#gh:gh_bobs-org__bob-cli Can you help me add support to the `bob capture` command and the corresponding
bob-mac-capture app for the new `++[<N>]` / `--[<N>]` syntaxes?

- We already support the `+<N>` / `-<N>` syntaxes which emulate the `\p` / `\P` Obsidian
  keymaps.
- This new syntax is meant to emulate the related `\o` / `\O` keymaps.
- For example, using `++3` should have the same effect as pressing `3\o` when the
  currently running pomodoro is selected in Obsidian.
- `<N>` should be optional and should default to `1`. Make sure to fix this for the `+`
  / `-` syntaxes as well (so I can use just `-` instead of `-1`, for example).
- #beau

#plan %m:@xlarge %auto %wait(bead=bob-cli-29)