#gh:gh_bobs-org__bob-cli I would like to start automatically adding a new sub-bullet to tasks that other
tasks depend on to indicate that the task blocks one or more other tasks. Can you help
me implement this?

- We already use a "Depends On" sub-bullet on the dependent tasks.
- This should happen automatically when dependencies are added to tasks (via the
  `<ctrl+shift+p>` keymap, for example).
- The `bob task reconcile` command should ensure the appropriate sub-bullets all exist
  and are consistent.
- Review the prerequisite_blocks_line.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.4d.linker