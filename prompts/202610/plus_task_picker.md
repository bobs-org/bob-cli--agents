- **PLAN:**
  [202610/plus_task_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plus_task_picker.md)
- **AGENTS:**
  - [bbugyi200.athena.0vw--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vw.md)

The `@file:id` syntax supported by the `bob capture` command and the corresponding
bob-mac-capture app triggers a pop-up when `@file:` is typed that supports fuzzy
searching for tasks in the ~/bob/file.md file. Can you help me add equivalent support
for this for the `@file+id` syntax?

- Namely, when `@file+` is typed, an equivalent pop-up (use shared code where possible)
  should show that allows the user to fuzzy search for tasks.
- When selected, the text should expand to `@file+id` (assuming a atask with the `^id`
  block ID was selected).
- Also, let's start triggering a pop-up menu like this whenever the user presses `+` at
  the beginning of a capture input or after a space at the end of a line. This menu,
  however, should allow the user to fuzzy search for a task across the entire Obsidian
  vault. See how we do this when `:` is typed at the beginning of a capture input for
  inpsiration.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
