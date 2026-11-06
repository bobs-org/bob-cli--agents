#gh:gh_bobs-org__bob-cli I would like to add support for a new `^^` capture syntax that can be used with
the `@foo[^:]bar@` syntax. Can you help me implement this?

- See the bob-cli-gl epic bead for context on the recent support we added for pulling in
  child tasks from the parent project when using the `@foo[^:]bar@` syntax.
- When `^^` is found as the only contents of a capture bullet using this syntax, we
  should prompt the user to select one or more tasks from the parent project after they
  submit the capture.
- The selected tasks will be added as `^foo` / `:foo` bullets as if the syntax
  introduced by the bob-cli-gl epic bead was used directly.
- This task prompt should take inspiration from the successor prompt I'm thinking, but
  keep in mind that we need a way to support `:` as well as `^` (and not selected, which
  should be the default).
- Review the parent_task_move_choice.md file in the research sidecar repo for context
  and inspiration before planning. I agree with all of the requirements recommended in
  that research file (but keep in mind that you are responsible for planning and
  splitting up this work appropriately).
- #beau

#plan %m:@xlarge %w:research.37.linker