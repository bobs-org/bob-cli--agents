#gh:gh_bobs-org__bob-cli The `<ctrl+shift+m>` Obsidian keymap currently allows the user to move one
or more pomodoro sub-bullets to a new pomodoro of the same name using `+` as input. Can
you help me change this to `=` instead of `+`? Also, we need a way to split pomodoros
that were merged together (these have pomodoro names separated with the `+` character).
To support this, let's allow the `=foobar` syntax to be used to specify that we should
split all targeted pomodoro sub-bullets out into a new pomodoro named `FOOBAR` and
remove any `FOOBAR` (and the associated `+`) part from the current pomodoro's name.

#plan %m:grok-4.6