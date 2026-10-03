#gh:gh_bobs-org__bob-cli Can you help me add support to our freshness logic for the special `^prj` and
`^ref` tasks that we use to track projects and references (i.e. things I want to read),
respectively?

- `^prj` tasks should only need to be refreshed when the corresponding project note
  contains no ready tasks. These should be reviewed after NEW tasks when using the `]s`
  keymap to walk through tasks that need review. These tasks should require a refresh
  every 7d (same as normal tasks--use the same config field we already use to determine
  the number of days allowed in-between refreshes).
- `^ref` tasks should require refresh immediately (i.e. they should be treated as NEW
  when first created) and should then be treated like normal tasks after that (e.g.
  require refresh every 7d).
- The goal of this change is to make sure that I don't forget to add tasks to projects
  and to make sure that I don't forget about or (more likely) forget to mark reference
  tasks as done.

#plan %m:gpt-6-astra %auto