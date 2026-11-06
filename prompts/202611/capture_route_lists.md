- **PLAN:**
  [202611/capture_route_lists.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_route_lists.md)
- **AGENTS:**
  - [bbugyi200.apollo.c1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c1.md)

Can you help me add support for a new bulk capture syntax for adding several tasks or
notes to the same project/area note by placing `@file` or `@file#drawer` on a line by
itself and using bullets below that line to specify which new tasks or (if `#drawer` was
specified) notes should be added to that note file / drawer?

- See how we did this in the bob-cli-fc epic bead for the `@file+id` syntax for context
  and inspiration.
- When this syntax is used without `#drawer` (i.e. tasks should be created), typing `^`
  or `:` should trigger a prompt for a block ID for the task defined by the current line
  (or parent line if in a sub-bullet).
- When the `:<id>` syntax is used to define the block ID for a line, the task that gets
  created for that line should have a task link added to today's daily file.
- Make sure this block ID prompt suggests a good default ID that the user is likely to
  accept.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
