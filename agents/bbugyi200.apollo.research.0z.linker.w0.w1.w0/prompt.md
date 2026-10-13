#gh:gh_bobs-org__bob-cli I would like to migrate the `scheduled` and `depends_on` project task
frontmatter fields back to the project task in that file. Can you help me implement
this?

- I think this is more appropriate since I don't believe there is a need to use
  frontmatter fields (you should verify this doesn't break anything), it makes project
  tasks more consistent with every other Obsidian task, and it allows a nicer view of
  the scheduled date and dependencies (since we already have nice rendering of these for
  Obsidian tasks).
- I would also like to start adding a new `#prj_is_blocked` tag to any Obsidian task
  that is only marked as blocked because its parent is blocked. This way, after this
  change, it is clear from looking at any task exactly why that task is blocked.
- Also, make sure that a task that becomes unblocked because its parent is unblocked is
  always marked as needing a refresh somehow if left in a ready state / not pulled into
  today's daily file as a successor, which should cause the task's status to change to
  next (this may already be the case, but make sure). The goal here is to make sure that
  any task which is marked as unblocked (regardless of the reason--make sure we do this
  when a project note's `scheduled` date arrives too, for example) is always reviewed by
  me during my new GTD morning review at the very latest.
- Review the recently added related research file in the research sidecar repo for
  context and inspiration before planning.

#plan %m:@xlarge %w:research.0z.linker.w0.w1