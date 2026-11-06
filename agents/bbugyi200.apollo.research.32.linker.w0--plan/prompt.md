#gh:gh_bobs-org__bob-cli I want to make some improvements to the way we handle freshness updates using
the `<alt+f>` and `<ctrl+alt+f>` keymaps. Can you help me implement this?

- I want to generalize and unify the "task decay" supported by bob currently. We should
  add a new glossary term for "task decay" that does a good job of explaining this new /
  improved policy.
- We should add one more more appropriate config field to make this functionality
  flexible (I was thinking just allowed rolls for each task status, but I'll let you
  decide) and add them to my bob/config.yml file in my chezmoi repo (with good, but
  concise, comments).
- I would like my bob to allow 2 keeps in each status/priority before defaulting to
  rolling to the next status/priority. We already support this for priorities I believe,
  but it should be configured explicitly.
- We already support a way to decay ready tasks (after 3 keeps currently--this should be
  changed to 2).
  - There seems to be a problem with ready task decay right now though that you should
    look into.
  - Namely, it says that no priority ladder is configured (I think we should just always
    use P1, right?).
  - We should fix this issue as a part of this change.
  - See the ~/tmp/screenshots/20261102_134505.png screenshot for context.
- WIP tasks should decay to next tasks by default when their keep limit has been
  reached.
- Next tasks should decay to ready tasks by default when their keep limit has been
  reached.
- The user should have an option to keep the status the same for all of these
  transitions / prompts, which should reset the keep count for that task.
- Make sure the rotten log entries reflect all of these transitions appropriately.
- Let's stop prompting for a work log entry when marking WIP tasks as fresh in Obsidian.
  These WIP tasks should be considered rotten, which means that we should prompt for a
  rotten log entry instead.
- We should continue to prompt for a rotten log entry for next tasks (like we do now),
  but a rotten log entry should always be added (either explicitly or using a default).
- If the user does not give a rotten log entry, then a default one should be added which
  specifies the status that was kept (make sure it is clear how many times each task was
  kept in each status). We already do something like this for ready tasks I believe, but
  we might want to unify the process a bit (I'll let you decide on this one).
- Review the task_decay_ladder.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.32.linker