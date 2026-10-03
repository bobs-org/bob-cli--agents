#gh:gh_bobs-org__bob-cli Can you help me add support for using `=<X>` as an input (by itself) to the
`bob capture` command and its corresponding bob-mac-capture app?

- This should only be valid when there are future pomodoro in the current Obsidian daily
  file but no current pomodoro.
- It should be used to indicate that we want to start the next future pomodoro.
- We should accept the same type of values for `<X>` as we do when using the
  `@file:id=<X>` syntax.
- #beau

#plan %m:@xlarge %auto %wait(bead=bob-cli-2a)