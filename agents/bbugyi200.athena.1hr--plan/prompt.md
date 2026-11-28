#gh:gh_bobs-org__bob-cli The `<ctrl+shift+o>` keymap in Obsidian should always insert a note bullet into
a task when a task's headline (i.e. first line) is selected, which should always be
below any links/deps and should always be inside the "Notes" drawer if one currently
exists for the selected task. See the ~/tmp/screencasts/20261128_073223.mp4 screencast
for context. Can you help me fix this?

- As a part of this change, let's also change the `o` keymap so it creates a new task
  req for the current task, assuming that task's headline is selected.
- I rarely create tasks by hand in Obsidian (I use the capture panel), so the current
  functionality of the `o` keymap doesn't get much use.
- The `O` keymap should support this functionality only when a task req is currently
  selected.

#plan %m:@xlarge