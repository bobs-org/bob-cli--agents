#gh:gh_bobs-org__bob-cli %w:research.0z.linker.w0 I would like to migrate the `scheduled` and
`depends_on` project task frontmatter fields back to the project task in that file.

- I think this is more appropriate since I don't believe there is a need to use
  frontmatter fields (you should verify this doesn't break anything), it makes project
  tasks more consistent with every other Obsidian task, and it allows a nicer view of
  the scheduled date and dependencies (since we already have nice rendering of these for
  Obsidian tasks).
- I would also like to start adding a new `#prj_is_blocked` tag to any Obsidian task
  that is only marked as blocked because its parent is blocked. This way, after this
  change, it is clear from looking at any task exactly why that task is blocked.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research %m:@xlarge