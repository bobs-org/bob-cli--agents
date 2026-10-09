#gh:gh_bobs-org__bob-cli I would like to re-imagine the way that we track ref tasks. Can you help me
implement this?

- I have been treating ref tasks as normal Obsidian tasks in practice, but our
  implementation does not support this well or encourage it.
- Namely, the fact that we store ref tasks inside of ref notes is not intuitive or
  consistent with how we treat other tasks, which all live in either area notes or
  project notes.
- I would like to fix this by requiring that all future and currently open ref notes
  have a project note or area note listed as their parent.
- We should then be able to define the ref task for each ref associated with an
  area/project in the "Tasks" section of the corresponding note file like we do for all
  other Obsidian tasks.
- You should migrate any existing ref notes that are associated with open ref tasks to
  use this new policy and move their ref tasks to the appropriate area/project note
  file.
- This complicates syncing the ref note status with the ref task a bit since we need to
  account for the possibility that the ref task gets moved to a "done" note file in the
  ~/bob/done/ directory at some point.
- Also, I think there is a lot of logic that currently treats ref tasks as special /
  something to filter out. We don't show them when pressing `^` to show today's /
  pending / next tasks in the bob-mac-capture app, for example. Just about all (probably
  all, but think hard about this so we don't break any invariants that I currently rely
  on) of this logic should be removed so we start treating ref tasks like any other
  task.
- This change will also require that we start prompting the user for a project / area
  note file when capturing new ref URLs (via the bob-mac-capture app or the
  `bob gkeep pull` command, for example) so we know which project / area note file to
  use.
- This project / area name should then be passed to the `bob ref create` command's new,
  required `-p|--parent` option.
- I currently use a sase (a GitHub project in the sase-org organization) file hook that
  uses this `bob ref create` command. We will need to start passing in the project name
  (e.g. "sase", "bob-cli") to the `-p|--parent` option.
  - I'm not sure that sase injects the project name into this file hook command string
    right now, so you might need to add support for that.
  - Also note that it is not guaranteed that the project name that gets passed in will
    exactly match the project note's name. For example, the "bob-cli" project name
    should actually map to the ~/bob/bob.md file. To work around this, we should add
    support for a new `project_name_aliases` frontmatter field to project notes that
    allows them to specify alternative names that will be matched by the `bob` command
    when searching for a project by name. We should set this field to `["bob-cli"]` for
    the ~/bob/bob.md project note.
- We will need to start giving ref tasks a different block ID since `^ref` will no
  longer be guaranteed to be unique. In order to make ref tasks stand out a bit more, we
  should also start rendering an appropriate icon/symbol instead of `#ref` when these
  tasks are rendered in Obsidian.
- Review the ref_tasks_move_into_parent_notes.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file.
- #beau

#plan %m:@xlarge %auto