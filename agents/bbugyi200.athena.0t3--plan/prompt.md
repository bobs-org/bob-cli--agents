#gh:gh_bobs-org__bob-cli Can you help me add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new solo (i.e. the only contents in a capture input)
`^file:id[#pomodoro]=<X>` syntax that works just like the solo `@file:id[#pomodoro]=<X>`
syntax except for a single twist?

- The twist is that `^` should only trigger completion for in-progress or next Obsidian
  tasks (i.e. the tasks associated with active task links) and should trigger
  full-completion (i.e. the `:id` part will be expanded as well).
- See the bob-cli-26 epic bead for context on the `=<X>` syntax.
- I'm not sure if the solo `@file:id` syntax even supports the `=<X>` yet, so you might
  need to add support for that.
- #beau

#plan %m:@xlarge %auto