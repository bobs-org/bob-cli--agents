- **PLAN:**
  [202609/priority_roll_decay.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/priority_roll_decay.md)
- **AGENTS:**
  - [bbugyi200.athena.0um--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0um.md)

Can you help me make some improvments to the way Obsidian task priorities work currently
by adding support for tasks that auto-decay as they continue to get rolled over?

- To start, let's always allow the user to select the roll date recommended by the
  prompt that pops up when the `<ctrl+shift+p>` Obsidian keymap is used by hitting
  `<ctrl+enter>` instead of `<enter>` to select `scheduled`. Make sure that the roll
  date is displayed near `scheduled` somehow.
- By default, a task will recommend the current priority for a roll the first time a
  task is rolled for that priority but, after that, a roll to the priority one level
  higher will be recommended.
- After the user has already rolled once at priority P4, hitting `<ctrl+enter>` while
  `scheduled` is selected should cancel the corresponding task (so tasks eventually get
  cancelled if the user continues to roll them over using the recommended roll).
- This behavior should be configureable (to allow for 3 rolls of the same priority
  level, for example).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
