#gh:gh_bobs-org__bob-cli I would like to add support for auto-adding "linked from" task relation bullets
to tasks that are referenced (via Obsidian markdown links like `[[foo#^bar]]`j) by other
tasks. Can you help me implement this?

- We should make it very clear to the user (in a visually appealing way) why an inline
  "linked from" task relation is shown.
- We should not show a "linked to" bullet on the other task, since it already references
  the target task via an inline link.
- Review the inline_task_mention_backlinks.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.2v.linker