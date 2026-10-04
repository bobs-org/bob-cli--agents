#gh:gh_bobs-org__bob-cli The point of the new `[fresh::<date>]` properties that we've added to ready
Obsidian tasks is to make it clearer which of those tasks are really ready.

- A new task or a rotten task (let's start using the term "rotten" instead of "stale")
  should not be shown in the "READY tasks" section of the ~/bob/dash.md file.
- Instead, we should show new tasks either in a new "NEW tasks" section, which should be
  shown above the "WIP tasks" section and show rotten tasks in a new ~/bob/rotten.md
  file (that the ~/bob/dash.md file links to with a new "ROTTEN" badge).
- We may need to preprocess these rotten tasks somehow in order to make this work. My
  first thought was that we could use the `bob task-status-hooks` command to add a
  `#rotten` tag to rotten tasks, but you should think hard about the best way to
  implement this.
- Review the freshness_gated_ready_dash.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the recommendations made by that research file.

Can you help me implement this? #plan %m:gpt-6-astra %auto