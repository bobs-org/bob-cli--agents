# Chat History - tmp_261001_130059 (main)

- **TIMESTAMP:** 2026-10-01 13:09:08 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** main

## Prompt

The point of the new `[fresh::<date>]` properties that we've added to ready Obsidian tasks is to
make it clearer which of those tasks are really ready.

- A new task or a rotten task (let's start using the term "rotten" instead of "stale")
  should not be shown in the "READY tasks" section of the ~/bob/dash.md file.
- Instead, we should show new tasks either in a new "NEW tasks" section, which should be
  shown above the "WIP tasks" section and show rotten tasks in a new ~/bob/rotten.md
  file (that the ~/bob/dash.md file links to with a new "ROTTEN" badge).
- We may need to preprocess these rotten tasks somehow in order to make this work. My
  first thought was that we could use the `bob task-status-hooks` command to add a `#rotten` tag to rotten
  tasks, but you should think hard about the best way to implement this.
- Review the freshness_gated_ready_dash.md file in the research sidecar repo for context
  and inspiration before planning. I agree with all of the recommendations made by that
  research file.

Can you help me implement this? Think this through thoroughly and create a plan using
your `/sase_plan` skill. Choose and author the appropriate tier, validate and revalidate until
it passes, then submit it with `sase plan propose` (as the skill instructs) before making any file
changes.


## Response

I’ll use the `sase_plan` skill to build and validate the plan, starting with the research report, freshness rules, and dashboard implementation. I’ll use `sase_repo` and `sase_memory_read` for the required repository and memory access.


Freshness is already calculated when tasks are read, and human actions own the `[fresh:: …]` stamp. That points toward a dashboard filter rather than a `#rotten` tag managed by hooks. I’m checking the report and dashboard API to confirm how new, expired, and resurfaced tasks should be separated.


The report recommends NEW between TODAY and PENDING, with returned deferrals grouped separately in `rotten.md`. It also calls for matching badge counts and a safe fallback when the plugin is unavailable. I’ll use an epic plan to separate the plugin changes, dashboard rollout, and final terminology migration.

I’m also using `sase_memory_write` for the decision and glossary updates included in the recommendations you accepted.


The freshness-mark epic has now closed, so the terminology phase no longer needs to wait for it. I also found two details to cover in the plan: cached classifications must update when Today links change, and badges must refresh at midnight even if no task is edited. Recurring and daily-note tasks will remain exempt and visible in READY.


The draft now covers all three phases, the badge rules, the one-release compatibility window for `stale_daily_budget`, and the two-week trial. I’m validating the plan schema next, then checking it against the accepted recommendations before submitting it.


The epic plan passes validation with zero warnings. It covers cached freshness buckets and badges, the NEW/ROTTEN dashboard rollout, and the versioned “rotten” terminology migration. Only the scratch plan has changed.

I’m submitting it with `sase plan propose` for the approval handoff you requested.
