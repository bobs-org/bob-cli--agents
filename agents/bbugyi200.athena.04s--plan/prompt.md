#gh:gh_bobs-org__bob-cli Can you help me add support to the `<ctrl+shift+opt+n>` Obsidian keymap for reversing its operation when a project note file's main `^prj` task is selected?

- In this case the keymap should convert the project file back into an Obsidian task and add it to the "Tasks" section of the parent node file.
- This operation should fail with a good error toast if the project note file does not have the expected format.

#plan