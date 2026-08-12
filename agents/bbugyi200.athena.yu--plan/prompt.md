#gh:gh_bobs-org__bob-cli Can you help me improve the `<ctrl+shift+opt+n>` Obsidian keymap by adding
support for specifying that certain sub-bullets should be added as notes to sections in
the new project file instead of added as tasks?

- Any sub-bullet that is all in caps (ex: `REQUIREMENTS`) and has sub-sub-bullets should
  be treated as a section title (converted to title-case).
- If that section already exists in the project file template, then we should add it to
  the existing section instead of adding a new one.

#plan #m_opus