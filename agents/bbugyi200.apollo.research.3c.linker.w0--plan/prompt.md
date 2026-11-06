#gh:gh_bobs-org__bob-cli We already support the `offclock` boolean area note / project note file
frontmatter field to specify that all tasks in an area/project, recursively, should be
treated as offclock. I would now like to add support for a new `offclock_types` property
that takes a list of task type names as values. Can you help me implement this?

- This field should work just like `offclock`, but only tasks which have one of the
  types listed by this field should be treated as offclock.
- As our first use-case I would like to migrate the area notes in my Obsidian vault that
  currently use `offclock` to start using `offclock_types` instead, with MEET being the
  only task type that they filter for.
- Review the offclock_types_area_type_clock.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

#plan %m:@xlarge %w:research.3c.linker