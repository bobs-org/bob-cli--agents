- **PLAN:**
  [202610/in_progress_task_link_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/in_progress_task_link_marks.md)
- **AGENTS:**
  - [bbugyi200.apollo.5j--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5j.md)

Can you help me start adding an appropriate icon/symbol next to task links in daily
files that correspond with tasks that are in-progress?

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
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
