- **PLAN:**
  [202608/capture_task_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_task_sections.md)
- **AGENTS:**
  - [bbugyi200.athena.085--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.085.md)

Can you help me add support to the bob-mac-capture app and the `bob capture` command for
targeting task sections with `@file+id#section` syntax?

- We use the same definition of "task section" here that is used by the
  `<ctrl+shift+opt+n>` keymap when converting an Obsidian task to a project note (e.g. a
  bullet containing only capital letters).
- For example, `@foo+bar#requirements` should add the new note to the Obsidian task with
  a block ID of `^bar` in the ~/bob/foo.md file.
- Make sure the bob-mac-capture app has good completion for this new syntax (triggered
  by the `#` character).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
