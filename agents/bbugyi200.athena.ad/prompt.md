#gh:gh_bobs-org__bob-cli Can you help me add a new custom Obsidian task status for blocked
tasks?

- The `bob mark-next-tasks` command should start automatically setting this
  status for any tasks that have open dependencies (i.e. one or more of the
  tasks that they link to via the `dependsOn` property are still open).
- Make sure the tasks query in the ~/bob/dash.md file still works.
- We should also change the `!` Obsidian keymap, which already sets `dependsOn`
  in some cases, to also mark the parent task as blocked if the task that the
  current sub-bullet's block link points to is still open.
- #beau

#plan