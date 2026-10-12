#gh:gh_bobs-org__bob-cli We already support pulling in successor tasks when closing a task link that
unblocks one or more tasks. Can you now help me make this work for project tasks too?

- In other words, if the final task in a project note is closed via its task link, then
  we should pull in a successor task link that points to the project task.
- The project task should be given a next (i.e. `[*]`) status when this happens.
- The `#hide` tag should also be auto-removed from the project task when this happens.
- The goal of this change it to make me immediately aware when the project corresponding
  with the task that I just finished no longer has any child tasks that can be worked.
- When this happens, I will then either close out the project task (if the project is
  really done) or add a new task (i.e. the next appropriate task to push that project
  forward) to that project note.
- Make sure this work does not conflict with the bob-cli-6s epic bead, which is
  in-progress. If it does, make sure you leave good notes on the appropriate beads.

#plan %m:@xlarge