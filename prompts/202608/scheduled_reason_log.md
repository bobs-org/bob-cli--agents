- **PLAN:**
  [202608/scheduled_reason_log.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/scheduled_reason_log.md)
- **AGENTS:**
  - [bbugyi200.athena.tu--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.tu.md)

The `<ctrl+shift+p>` Obsidian keymap currently supports changing the `scheduled` property of an Obsidian task. Can you
help me make it so, after the user selects a new scheduled date, they are then prompted for a reason?

- This reason should be added as a sub-sub-bullet to some other appropriate sub-bullet (which should be added to the
  current Obsidian task if this sub-bullet does not already exist).
- Each sub-sub-bullet should clearly show the scheduled date that it is/was associated with.
- The user should be able to press enter without entering a reason. In which case, no reason sub-sub-bullet should be
  added (and the parent sub-bullet, if it does not already exist, should not be created).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last
  but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate tier,
validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs) before making
any file changes.
