- **PLAN:**
  [202610/rotten_keep_streak.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_keep_streak.md)
- **AGENTS:**
  - [bbugyi200.apollo.4o--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4o.md)

I would like to start tracking every time an Obsidian task is explicitly refreshed (i.e.
its `fresh` property is updated by using the `<alt+f>` keymap) using a new
`refresh_count` property. Can you help me implement this?

- This property should be rendered as an appropriate icon (like we do with `fresh`).
- The goal of this change is to enable some sort of (user approved--at the time of
  decay) auto-decay for tasks that continue to be manually refreshed, but I haven't got
  that part worked out yet. We already support auto-decay for repeat priority rolls but
  not for repeat rotten task refreshes. Think hard about the best way to do this.
- Review the rotten_keep_streak_and_approved_decay.md file in the research sidecar repo
  for context and inspiration before planning. I agree with all of the recommendations
  made in that research file.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
