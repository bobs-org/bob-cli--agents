#gh:gh_bobs-org__bob-cli Can you help me start adding an appropriate icon/symbol next to task links in
daily files that correspond with tasks that are in-progress?

- We already use a tomato icon for task links which were worked in past pomodoros, so
  you should pick a different icon for this (which should only be shown next to current
  or future pomodoro task links).
- Every task corresponding with a task link in today's daily file should have either an
  in-progress or next status, so this new icon will allow us to tell which is which.
- As a part of this change, let's allow the `<alt+[>` and `<alt+]>` keymaps, which
  toggle task statuses, to work on task links.
- Users should only be able to toggle between two statuses when using these keymaps on
  task links: in-progress and next.
- If using one of these keymaps to toggle from in-progress to next, the user should be
  prompted for an optional work log entry.
- #beau

#plan %m:@xlarge %auto