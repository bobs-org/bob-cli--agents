#gh:gh_bobs-org__bob-cli Can you help me add support for a new `&foo:bar` syntax to the `bob capture`
command and its corresponding bob-mac-capture app that adds a task dep link for the task
specified by `foo:bar` (e.g. `[[foo#%^bar]]`)?

- The target task should be either the task that we are capturing (if the capture text
  looks like a task capture) or an explicitly targeted pre-existing task by using the
  `@file+id` syntax to specify that task.
- For example, `Buy Groceries! &foo:bar` will create a new `Buy Groceries!` task with a
  dep link to `[[foo#^bar]]`, whereas `&foo:bar @body:excercise` would add that dep link
  to the existing `^excercise` task in the ~/bob/body.md file.
- Pressing `&` at the beginning of a capture or after a space at the end of a line in
  the bob-mac-capture app should trigger an excellent completion menu that allows the
  user to fuzzy search for any task in their Obsidian vault. See how we do this when `:`
  is typed at the beginning of a capture for context and inspiration.
- #beau

#plan %m:gpt-6-astra %auto