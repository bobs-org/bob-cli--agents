# Chat History - tmp_261003_110656 (main)

- **TIMESTAMP:** 2026-10-03 11:16:13 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** main

## Prompt

Can you help me add support to our freshness logic for the special `^prj` and `^ref` tasks
that we use to track projects and references (i.e. things I want to read), respectively?

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

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and
author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.


## Response

I’m using the `sase_plan` and `sase_memory_read` skills to trace freshness and review ordering, then prepare and validate a plan before submitting it.


The main complication is that these tracking tasks normally carry `#hide`, which excludes them from freshness review today. I’m checking how to include them in review while preserving their visibility elsewhere, and how project readiness is counted.


I’m planning a PROJECTS review tier immediately after NEW. I’ll interpret “no ready tasks” as an empty Ready lane in that project note, counting NEW and ROTTEN tasks too, so aging alone doesn’t make a populated project appear empty.


Project sync uses a broader rule—any open task or subproject—to decide whether to hide `^prj`. Freshness therefore needs its own read-time check. The plan will also cover CLI/Obsidian parity, live queue updates when the last Ready task disappears, and refresh stamps that preserve `^prj` and `^ref`.


This fits a single `tale` plan with `medium` implementation size. One important edge case is project scheduling: `^prj` stores its schedule in note frontmatter, so the review check must honor that date when bypassing `#hide`. References will enter NEW without a stamp, then follow the existing freshness rules.


The plan is drafted. It covers the distinction between full review counts and dashboard counts, since hidden trackers need review without inflating a dashboard section that doesn’t show them. Validation found two missing metadata fields; I’m adding them and checking the tracker parsers before revalidating.


The `tale` plan passes validation with zero warnings. It covers the PROJECTS tier, reference freshness, scheduling and hidden-task handling, live queue updates, and parity tests. I’m submitting it for review now; no implementation files have changed.
