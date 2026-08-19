#gh:gh_bobs-org__bob-cli Can you help me add support to the bob-mac-capture app and the `bob capture` command for targeting task sections with `@file+id#section` syntax?

- We use the same definition of "task section" here that is used by the `<ctrl+shift+opt+n>` keymap when converting an Obsidian task to a project note (e.g. a bullet containing only capital letters).
- For example, `@foo+bar#requirements` should add the new note to the Obsidian task with a block ID of `^bar` in the ~/bob/foo.md file.
- Make sure the bob-mac-capture app has good completion for this new syntax (triggered by the `#` character).

#plan %m:grok-4.6