- **PLAN:**
  [202610/freshness_gated_ready.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/freshness_gated_ready.md)
- **AGENTS:**
  - [bbugyi200.athena.0uy--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uy.md)

The point of the new `[fresh::<date>]` properties that we've added to ready Obsidian
tasks is to make it clearer which of those tasks are really ready.

- A new task or a rotten task (let's start using the term "rotten" instead of "stale")
  should not be shown in the "READY tasks" section of the ~/bob/dash.md file.
- Instead, we should show new tasks either in a new "NEW tasks" section, which should be
  shown above the "WIP tasks" section and show rotten tasks in a new ~/bob/rotten.md
  file (that the ~/bob/dash.md file links to with a new "ROTTEN" badge).
- We may need to preprocess these rotten tasks somehow in order to make this work. My
  first thought was that we could use the `bob task-status-hooks` command to add a
  `#rotten` tag to rotten tasks, but you should think hard about the best way to
  implement this.
- Review the freshness_gated_ready_dash.md file in the research sidecar repo for context
  and inspiration before planning. I agree with all of the recommendations made by that
  research file.

Can you help me implement this? Think this through thoroughly and create a plan using
your `/sase_plan` skill. Choose and author the appropriate tier, validate and revalidate
until it passes, then submit it with `sase plan propose` (as the skill instructs) before
making any file changes.
