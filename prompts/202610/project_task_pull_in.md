- **PLAN:**
  [202610/project_task_pull_in.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_task_pull_in.md)
- **AGENTS:**
  - [bbugyi200.apollo.6z--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.6z.md)

We already support pulling in successor tasks when closing a task link that unblocks one
or more tasks. Can you now help me make this work for project tasks too?

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

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
