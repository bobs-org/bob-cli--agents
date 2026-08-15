- **PLAN:**
  [202608/file_plus_any_task.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/file_plus_any_task.md)
- **AGENTS:**
  - [bbugyi200.athena.02a--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.02a.md)

Can you help me add support to `@file+` completion in the bob-mac-capture panel for
selecting any task in ~/bob/file.md instead of just tasks with block IDs?

- If the user selects a task that does not have an existing block ID, the user should be
  prompted to provide one.
- The block ID should immediately be added to that Obsidian task after the user submits
  the new ID name. At that point, the completion should expand (i.e. the new block ID
  should be appended to `@file+`).
- Make sure it is very clear (in a visually appealing way) which tasks have existing
  block IDs and which do not. Tasks with existing block IDs should also be sorted before
  tasks with no block IDs in the completion menu.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
