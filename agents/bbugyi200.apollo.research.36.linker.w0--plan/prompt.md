#gh:gh_bobs-org__bob-cli I would like to add better support for moving tasks from one note file to
another and add excellent (new) support for merging tasks to / creating new tasks from
bullets of other tasks. Can you help me implement this?

- We should add support for a new `@a+aid @b+bid > @c` capture syntax where any number
  of notes can be on the left-hand side of the `>` character and `@c` can have a
  `#drawer` suffix to specify that the tasks should be converted to notes and moved to
  that drawer (this drawer should be created if it does not already exist).
- We should also be able to use a target of the form `@c+cid` after the `>`, in which
  case we should merge the source tasks into the `^cid` task in the ~/bob/c.md file. We
  should also be able to use the `@c+cid#drawer` syntax to target a specific drawer in
  the `^cid` task (this drawer should be created if it does not already exist).
- When merging one task into another, we should not delete the source tasks. Instead, we
  should add a new "merged into" task relation that points from the source tasks to the
  destination task (and auto-cancels the source task). This "merged into" task relation
  should be able to be used on its own (in Obsidian via the `<ctrl+shift+l>` keymap, for
  example) to perform the same operation (see how we associate other task relations with
  specific operations for inspiration--this "merged into" relation should be
  configurable if possible/desirable).
- We should add a new `<ctrl+shift+t>` keymap to Obsidian that makes it easy to split
  out one or more top-level bullets from a task into new tasks. When this is done, the
  bullets (and their child bullets) should be replaced by some concise and useful text
  containing inline links to the new tasks that were created from the old bullets (the
  old tasks should wind up being given "linked from" mentions which are triggered by
  these inline links).
- Make sure that we have good command-line support for all of this new functionality.
- FYI: I already am in the process of adding support for the `@file+id` capture syntax
  multiple times on the same line (see the capture_multi_target.md file in the plans
  sidecar repo for context).
- Review the task_move_merge_split_design.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.36.linker