#gh:gh_bobs-org__bob-cli I would like to add full support to prj tasks for task dep links. Can you help
me implement this?

- You can add a dependency to a prj task now (using the `<ctrl+shift+p>` keymap, for
  example), but the result is not intuitive (see the ~/bob/job_apply_to_databricks.md
  file, which should be auto-fixed by the `bob task reconcile` command after this
  change, for an example).
- When a prj task is given a dep link, it should be added as a `depends_on` frontmatter
  field on that project note, not in a "Depends On" sub-subullet. Make sure to update
  the `<cmd+ctrl+shift+n>` Obsidian keymap to support this change so project notes are
  converted from tasks correctly.
- Most importantly, any task that lives in a blocked project should also be blocked (in
  this case, because the project has an unmet dependency, but whenever a project is
  blocked this rule applies).
- We will need to make sure to update the `<ctrl+shift+p>` keymap so this occurs
  automatically when I add a dependency to a prj task using that keymap.
- Keep in mind that blocked tasks should not have corresponding task links, so those
  should be removed (along with the pomodoro section they live in if it becomes empty)
  if they exist.
- We should also update the `bob task reconcile` command to check for any tasks that
  should be blocked and/or have their corresponding task links removed.
- The "task dep links" glossary memory web term should be updated accordingly.
- Review the project_dependency_blocking.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

#plan %m:@xlarge %w:research.0z.linker