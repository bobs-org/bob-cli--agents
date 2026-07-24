#gh:gh_bobs-org__bob-cli We already have the `!` keymap in Obsidian, which toggles whether or not an Obsidian task associated with a block link on the current line is transcluded. Can you help me add a new `@` keymap, which should only be active when the cursor is on one of these lines and the block link is transcluded?

- This keymap should just toggle the task's state from open (i.e. `[ ]`) to in-progress (i.e. `[/]`).
- It's important that this keymap is only active when it should be because the `@` symbol is used to run macros in normal mode.

#plan %a:tale