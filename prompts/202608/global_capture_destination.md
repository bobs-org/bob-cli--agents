- **PLAN:**
  [202608/global_capture_destination.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/global_capture_destination.md)
- **AGENTS:**
  - [bbugyi200.athena.0c9.w0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0c9.w0.md)

  Can you help me add support to the `bob-capture` command and bob-mac-capture app for
  using just the `@@foo` syntax to indicate that all tasks/notes in this capture (for
  multi-capture, which requires blank lines in-between distinct notes/tasks) be added to
  the same ~/bob/foo.md file?

- Make sure we also add support for the `@@foo+a_id` syntax, so we can specify that each
  capture should be added as its own sub-bullet of the Obsidian task with a block ID of
  `a_id` in the ~/bob/foo.md file.
- `@bar` / `@bar+b_id` instances found in individual notes/tasks should override this
  global declaration.
- Make sure completion, diagnostics, and notifications are all updated appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
