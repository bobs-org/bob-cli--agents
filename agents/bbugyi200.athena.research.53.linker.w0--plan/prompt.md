#gh:gh_bobs-org__bob-cli I would like to add support for directed links from one Obsidian task to
another. Can you help me implement this?

- I was thinking that we could display these links via a new `LINKS` task sub-bullet or
  somethiing like that.
- Tasks should also track their backlinks (via a new `BACKLINKS` sub-bullet?), which
  must always stay consistent and correct (i.e. this field needs to be kept up-to-date
  automatically somehow).
- I need to be able to easily specify links when capturing new tasks in the
  bob-mac-capture app. I was thinking I could use a new `~` syntax for that which
  triggers a completion menu / search interfact for other Obsidian tasks (which we will
  link the current task to).
- We also need a way to specify that another task should link to the current task in
  both Obsidian (via the `<ctrl+shift+p>` keymap?) and in the bob-mac-capture app (via a
  new `~~` syntax maybe?).
- The user should be able to specify an optional relation / link description when adding
  a link from one task to another.
- Review the task_relation_links.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.53.linker