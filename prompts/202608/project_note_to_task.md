- **PLAN:**
  [202608/project_note_to_task.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/project_note_to_task.md)
- **AGENTS:**
  - [bbugyi200.athena.04s--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.04s.md)

Can you help me add support to the `<ctrl+shift+opt+n>` Obsidian keymap for reversing
its operation when a project note file's main `^prj` task is selected?

- In this case the keymap should convert the project file back into an Obsidian task and
  add it to the "Tasks" section of the parent node file.
- This operation should fail with a good error toast if the project note file does not
  have the expected format.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
