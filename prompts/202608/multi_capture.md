- **PLAN:**
  [202608/multi_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/multi_capture.md)
- **AGENTS:**
  - [bbugyi200.athena.024.w1--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.024.w1.md)

  Can you help me add support to the bob-mac-capture app for capturing multiple Obsidian
  tasks with the same input?

- This will be supported by treating a blank line as the separator for distinct
  tasks/notes.
- Currently, the `<ctrl+j>` keymap is used to insert a bullet on the next line. Let's
  keep this behavior but add a special case for when the current line's contents are
  just a bullet (and optional leading/trailing whitespace). Namely, in this case, we
  should remove the contents of the current line and insert a newline. The cursor should
  then be at the start of a new line after a single blank line (where the user can then
  start typing their next task/note).
- Also, we added support for sub-bullets recently, but never updated the `<ctrl+j>`
  keymap to respect the level of indentation of the current line when creating a new
  bullet line (i.e. if the current line is a sub-bullet, then the `<ctrl+j>` keymap
  should create a new sub-bullet). Fix this behavior as a part of this work.
- Let's also improve the mac notification that is displayed to the user by including a
  bit more information in the single task/note case and making sure to show info about
  all captured tasks/notes when multiple tasks/notes are captured.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
