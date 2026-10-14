#gh:gh_bobs-org__bob-cli I would like to add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new `*` syntax. Can you help me implement this?

- This syntax should work a lot like the `&` syntax, which allows the user to specify
  that the new task should have a task dep link to a different task.
- This new syntax, however, should allow the user to specify that the new task blocks
  the specified task (i.e. specify a task dependency in the opposite direction).
- When we block a task that has a corresponding task link in today's daily file using
  this method, we should remove that task link (and the pomodoro iff that pomodoro
  section becomes empty after removing that task link).
- Review the capture_star_blocks_modifier.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).

#plan %m:@xlarge %auto %w:research.4g.linker