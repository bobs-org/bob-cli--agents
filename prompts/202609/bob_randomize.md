- **PLAN:**
  [202609/bob_randomize.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/bob_randomize.md)
- **AGENTS:**
  - [bbugyi200.apollo.2q--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2q.md)

I want to implement a new `bob randomize` command. Can you help me implement this?

- This command would be used to re-schedule all of the currently due scheduled and
  prioritized Obsidian tasks (i.e. tasks that have a `scheduled` property equal to a
  date of today or earlier and have a `priority` property) using a random date.
- I use the `priority` field to mark lower priority (<P0) tasks. The goal of this change
  is to allow me to quickly re-schedule all of these lower priority tasks using random
  dates at once. This will be useful, for example, when I've gone several days/weeks
  without reviewing my tasks and need to focus all of my attention on getting P0 tasks
  done / organized.
- Each task's date should be randomized separately using the range of dates that is
  configured in the ~/.config/bob/config.yml file (based on the priority of that task).
- If possible, we should try to commit the file changes made by this command using a
  single commit. Make sure that our single commit doesn't cause issues with / conflict
  with the `bob vault-sync` command.
- Review the bob_randomize_backlog_reroll.md file in the research sidecar repo for
  context and inspiration before planning.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
