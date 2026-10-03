#gh:gh_bobs-org__bob-cli The `@file:id` syntax supported by the `bob capture` command and the
corresponding bob-mac-capture app triggers a pop-up when `@file:` is typed that supports
fuzzy searching for tasks in the ~/bob/file.md file. Can you help me add equivalent
support for this for the `@file+id` syntax?

- Namely, when `@file+` is typed, an equivalent pop-up (use shared code where possible)
  should show that allows the user to fuzzy search for tasks.
- When selected, the text should expand to `@file+id` (assuming a atask with the `^id`
  block ID was selected).
- Also, let's start triggering a pop-up menu like this whenever the user presses `+` at
  the beginning of a capture input or after a space at the end of a line. This menu,
  however, should allow the user to fuzzy search for a task across the entire Obsidian
  vault. See how we do this when `:` is typed at the beginning of a capture input for
  inpsiration.
- #beau 

#plan %auto