- **PLAN:**
  [202608/capture_id_only_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_id_only_marker.md)
- **AGENTS:**
  - [bbugyi200.athena.022--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.022.md)

The `bob capture` commands input text already supports a special `@file:id` syntax that
allows the user to specify the block ID of the task that gets added and add a task block
link as a sub bullet under a Pomodoro. Can you help me add a new `@file::id` syntax that
allows the user to specify that a block ID should be added only (no pomodoro
sub-bullet)? Make sure you add support for this syntax to the bob-mac-capture app as
well. Think this through thoroughly and create a plan using your `/sase_plan` skill.
Choose and author the appropriate tier, validate and revalidate until it passes, then
submit it with `sase plan propose` (as the skill instructs) before making any file
changes.
