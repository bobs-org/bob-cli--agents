#gh:gh_bobs-org__bob-cli Can you help me add support to `@file+` completion in the bob-mac-capture
panel for selecting any task in ~/bob/file.md instead of just tasks with block IDs?

- If the user selects a task that does not have an existing block ID, the user should be
  prompted to provide one.
- The block ID should immediately be added to that Obsidian task after the user submits
  the new ID name. At that point, the completion should expand (i.e. the new block ID
  should be appended to `@file+`).
- Make sure it is very clear (in a visually appealing way) which tasks have existing
  block IDs and which do not. Tasks with existing block IDs should also be sorted before
  tasks with no block IDs in the completion menu.
- #beau

#plan