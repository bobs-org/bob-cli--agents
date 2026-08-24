#gh:gh_bobs-org__bob-cli %w:0c9 Can you help me add support to the `bob-capture` command and
bob-mac-capture app for using just the `@@foo` syntax to indicate that all tasks/notes
in this capture (for multi-capture, which requires blank lines in-between distinct
notes/tasks) be added to the same ~/bob/foo.md file?

- Make sure we also add support for the `@@foo+a_id` syntax, so we can specify that each
  capture should be added as its own sub-bullet of the Obsidian task with a block ID of
  `a_id` in the ~/bob/foo.md file.
- `@bar` / `@bar+b_id` instances found in individual notes/tasks should override this
  global declaration.
- Make sure completion, diagnostics, and notifications are all updated appropriately.
- #beau

#plan