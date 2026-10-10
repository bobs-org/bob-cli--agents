#gh:gh_bobs-org__bob-cli %w:6c Can you help me start using a consistent color scheme for the badges
shown at the top of Obsidian daily files and in the "WORK" section at the top of the
~/bob/dash.md file?

- When the count is 0 for a badge, we should color it grey.
- When the count is >=50% of the limit for a badge, we should color it green.
- When the count is >=75% of the limit for a badge, we should color it yellow.
- When the count is exactly equal to the limit for a badge, we should color it orange.
- When the count exceeds the limit for a badge, we should color it red.
- Otherwise (i.e. if the count is >0 but <50% of the limit), we should color it blue.
- The `TODAY` badge should use its task link count to calculate its color unless the
  theme count exceeds the theme limit, in which case the badge should be red.

#plan %m:gpt-6-astra %auto