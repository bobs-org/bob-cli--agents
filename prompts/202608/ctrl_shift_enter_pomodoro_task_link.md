- **PLAN:**
  [202608/ctrl_shift_enter_pomodoro_task_link.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/ctrl_shift_enter_pomodoro_task_link.md)
- **AGENTS:**
  - [bbugyi200.athena.028--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.028.md)

Can you help me add a new `<ctrl+shift+enter>` Obsidian keymap that adds a task block
link to the current/next pomodoro associated with the current task (i.e. the one under
the cursor)?

- Make sure that we prompt the user for a block ID for the task if it does not already
  have one.
- Also the status of the task should be changed to next. If the task had a blocked
  status before and had a schedule log then we should add an appropriate entry to it.
- See how the special `^^` Obsidian functionality works when used to create a pomodoro
  sub-bullet task block link for inspiration.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
