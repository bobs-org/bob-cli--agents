#gh:gh_bobs-org__bob-cli #fork:bp Can you now help me add support for transforming `@file^id` into
`@file+id` with `+` and for creating new project notes using the `@file:id` syntax (not
just the `@file^id` syntax)?

- We will enable this by migrating the `@file^id+` syntax to `@file^id@` and adding
  support for a new `@file:id@` syntax.
- When the `@file:id@` syntax is used, we should show a project successor prompt to the
  user which has them select which tasks from the new project note should have task
  links created for them (a task link for the `^prj` task should not be created).
- Make sure to add excellent syntax highlighting for these new `@file:id@` / `@file^id@`
  syntaxes.
- #beau

#plan %m:@xlarge