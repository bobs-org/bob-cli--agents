- **PLAN:**
  [202610/consistent_work_badge_colors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/consistent_work_badge_colors.md)
- **AGENTS:**
  - [bbugyi200.apollo.6c.w1--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.6c.w1.md)

  Can you help me start using a consistent color scheme for the badges shown at the top
  of Obsidian daily files and in the "WORK" section at the top of the ~/bob/dash.md
  file?

- When the count is 0 for a badge, we should color it grey.
- When the count is >=50% of the limit for a badge, we should color it green.
- When the count is >=75% of the limit for a badge, we should color it yellow.
- When the count is exactly equal to the limit for a badge, we should color it orange.
- When the count exceeds the limit for a badge, we should color it red.
- Otherwise (i.e. if the count is >0 but <50% of the limit), we should color it blue.
- The `TODAY` badge should use its task link count to calculate its color unless the
  theme count exceeds the theme limit, in which case the badge should be red.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
