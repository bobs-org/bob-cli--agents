# Chat History - ace-run (research.v.image)

- **TIMESTAMP:** 2026-09-30 18:58:14 EDT
- **MODEL:** codex/gpt-6-sol
- **AGENT:** research.v.image
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_181054.md`

## Prompt

%id(image, clan=research.v) %m:gpt-6-sol
%wait:research.v.final %q(1.5x, w=0.25) #gh:gh_bobs-org__bob-cli 
%xprompts_enabled:false
# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first projections of exact continuation nodes; any historical source without recoverable node provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `1`

## Continuation Block `block:v1:b90024b3765957783fb72e099434f9c8`

- **Node:** `agent-delta:20260930181100:c75165a2b2f4483f`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:** `local:continuation/records/agent_delta/agent-delta:20260930181100:c75165a2b2f4483f.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update supersedes it.

%clan(research.v, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I'm
currently re-designing my GTD process a bit (see the bob-cli-2y epic bead for context),
but there is still one major requirement that is unmet.

- Namely, it is important that I at least glance at every task that I captured the
  previous day in case something is in there that should really get addressed today. For
  example, what if my wife and I are speed walking and she asks me to pick up our
  daughter in the morning? I'll add it to my Google Keep and sync that with my Obsidian
  the next morning using the `bob gkeep pull` command, but if I don't glance at that
  task, it does me no good.
- This is why I used to review the Ready section in the ~/bob/dash.md file every
  morning. This habit, where I would review every task in that section and attempt to
  reduce the number of ready tasks for each project to <=5, forced me to glance at inbox
  items every morning.
- The problem with this approach was that I was reviewing some tasks way more often than
  necessary, which wasted time and introduced friction into the process.
- I think we can solve this by using a new concept named "task freshness" (aka
  "freshness"), which should be added to the glossary memory web.
- This new policy/process will require that every ready task have some new property, say
  `fresh`, that has a date as a value. That date is meant to indicate the last time a
  human being looked at that task and confirmed it still needs to be done and should
  still look the way it does (e.g. same priority, description, parent project, etc...).
- By default, we should use 7 days as our task refresh interval, but tasks should be
  able to override this with a dataview property. Also, we should be able to
  configure/override the refresh interval for every task in a project by adding an
  appropriate frontmatter property to that project note file.
- Making any changes (e.g. via Obsidian keymaps we support--we do not need to actually
  monitor for manual task changes) to a ready task (including making it ready--going
  from blocked to ready, for example) should result in the freshness date being updated
  for that task automatically.
- Any task that is past due for a refresh should show up in my new freshness review
  process, which you should help me flesh out.
  - I should be able to see how many of my tasks our out-of-date as well as how many
    tasks I have refreshed today at a glance somehow during this review process.
  - I should have keymaps that allow me to easily jump to the next/previous out-of-date
    task. I should also have a keymap that allows me to refresh the currently selected
    task without making any other changes to it.
- This solution addresses the problem of me needing to glance at inbox tasks every
  morning (these should be out-of-date by default since they have never been marked as
  fresh), but it also minimizes the amount of work that I need to do during any kind of
  weekly review (which is not something that I currently do).
- It's possible that even this becomes too much work every morning but, if that becomes
  a problem, I can always limit myself to reviewing N out-of-date tasks per day (and
  then introduce a weekly review where I refresh all out-of-date tasks).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.v.final %m:@xlarge
%wait:research.v.cdx %wait:research.v.cld %wait:research.v.grk %wait:research.v.mus %wait:research.v.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I'm
currently re-designing my GTD process a bit (see the bob-cli-2y epic bead for context),
but there is still one major requirement that is unmet.

- Namely, it is important that I at least glance at every task that I captured the
  previous day in case something is in there that should really get addressed today. For
  example, what if my wife and I are speed walking and she asks me to pick up our
  daughter in the morning? I'll add it to my Google Keep and sync that with my Obsidian
  the next morning using the `bob gkeep pull` command, but if I don't glance at that
  task, it does me no good.
- This is why I used to review the Ready section in the ~/bob/dash.md file every
  morning. This habit, where I would review every task in that section and attempt to
  reduce the number of ready tasks for each project to <=5, forced me to glance at inbox
  items every morning.
- The problem with this approach was that I was reviewing some tasks way more often than
  necessary, which wasted time and introduced friction into the process.
- I think we can solve this by using a new concept named "task freshness" (aka
  "freshness"), which should be added to the glossary memory web.
- This new policy/process will require that every ready task have some new property, say
  `fresh`, that has a date as a value. That date is meant to indicate the last time a
  human being looked at that task and confirmed it still needs to be done and should
  still look the way it does (e.g. same priority, description, parent project, etc...).
- By default, we should use 7 days as our task refresh interval, but tasks should be
  able to override this with a dataview property. Also, we should be able to
  configure/override the refresh interval for every task in a project by adding an
  appropriate frontmatter property to that project note file.
- Making any changes (e.g. via Obsidian keymaps we support--we do not need to actually
  monitor for manual task changes) to a ready task (including making it ready--going
  from blocked to ready, for example) should result in the freshness date being updated
  for that task automatically.
- Any task that is past due for a refresh should show up in my new freshness review
  process, which you should help me flesh out.
  - I should be able to see how many of my tasks our out-of-date as well as how many
    tasks I have refreshed today at a glance somehow during this review process.
  - I should have keymaps that allow me to easily jump to the next/previous out-of-date
    task. I should also have a keymap that allows me to refresh the currently selected
    task without making any other changes to it.
- This solution addresses the problem of me needing to glance at inbox tasks every
  morning (these should be out-of-date by default since they have never been marked as
  fresh), but it also minimizes the amount of work that I need to do during any kind of
  weekly review (which is not something that I currently do).
- It's possible that even this becomes too much work every morning but, if that becomes
  a problem, I can always limit myself to reviewing N out-of-date tasks per day (and
  then introduce a weekly review where I refresh all out-of-date tasks).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.v.cdx`, `research.v.cld`, `research.v.grk`, `research.v.mus`, `research.v.gem` dependencies, matching by `wait_name` and the canonical research
   label's existing `__<suffix>.md` suffix. Never reassign suffixes from list order.
   Open the research repo with `/sase_repo`, then read each report through its canonical
   research reference (or the `ref` field's `file:<id>` reference if the original has
   moved) using `sase artifact read`. Do not read predecessor chat transcripts. If the
   records above do not identify exactly one report per expected suffix, stop and report
   the missing or ambiguous input instead of guessing.
2. Research the request yourself, prioritizing gaps, weak evidence, and disagreements
   between the reports.
3. Pick a descriptive stem `<name>` that collides with nothing in the month directory
   (do NOT end the name with `_consolidated` or `_<YYYYmmdd>` or anything similar unless
   it relates to the research topic), create `<month-dir>/<name>/`, and move each report
   inside it as `<name>__<suffix>.md`, preserving its existing suffix. Each report's
   `source_path` is provenance for where it lives in your own opened research checkout;
   resolve its canonical repo-relative path there before moving it. Never modify the
   other agents' checkouts or the stored snapshot recorded at `ref` — only the copy in
   your own checkout moves. Preserve every file and never overwrite: on any collision,
   pick a different stem first.
4. Write the consolidated report to `<name>/<name>__final.md`: merge the strongest findings
   from every report above and your own research, resolve conflicts, cut duplication,
   and add missing critical context without unnecessary length.

   Do not create `<name>/<name>.md`, not even as a placeholder, because the linker
   agent `research.v.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.v.linker`, can find it:

   sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

   Use the consolidated report's actual absolute path and its path relative to the
   research repo root, for example `research:202609/<name>/<name>__final.md`. Register
   only the consolidated report, and do not pass `--move`. If registration fails,
   report that failure; do not report the task as fully complete.

Final layout:

```text
<month-dir>/<name>/
├── <name>__cdx.md
├── <name>__cld.md
├── <name>__grk.md
├── <name>__mus.md
├── <name>__gem.md
└── <name>__final.md
```

### Assistant

Now reading each report through `sase artifact read`.

I've read all five reports and am now checking where they disagree against the source, the vault, and the decision records.

Checking key-binding conflicts in the plugin source now, then the live vault.

I'm re-checking the live vault numbers that the reports disagree on.

Local claims check out. Next I'm looking up outside prior art (Taskwarrior and OmniFocus review features).

Taskwarrior's `tasksh review` turns out to be almost exactly this design. Confirming the OmniFocus details, then writing.

Now verifying the capture-rate figure (it drives the size of the daily NEW queue), then I'll write the report.

Numbers confirmed (411 tasks created in September, about 13.7 a day). Moving the five reports into the new directory now.

Reports moved. Now writing the consolidated report.

Report written. Quick check that the suggested `review.md` name doesn't collide with an existing vault note, then I'll register the report.

`review.md` already exists in the vault, so I'll switch the suggestion to `freshness.md`.

Now registering the consolidated report as an artifact.

Registered. Now the final declaration.

I've merged the five reports and my own checks into one final report. My answer is yes, build task freshness, but with several changes to your plan. The report is registered as `research:202609/ready_task_freshness_review/ready_task_freshness_review__final.md` (`file:explicit:feae995d2c15fddd3b8acef3`). The five reports now sit beside it as `ready_task_freshness_review__{cdx,cld,grk,mus,gem}.md`, and the research repo is set to be committed.

**Verdict: build it.** Taskwarrior's `tasksh review` is almost exactly your design: a `reviewed` date on each task, a missing date counts as due, a one-week interval, and `review N` to limit a session. OmniFocus does the same thing per project. The key idea is that a task with no stamp means "never reviewed". Using the `created` date can't do that job, because `bob gkeep pull` writes the date the Keep note was created, not the date it was pulled.

**Changes to your requirements:**
1. **Where the field goes matters.** Obsidian Tasks 8.4.0 and bob-cli's own parser both read fields from the end of the line and stop at the first key they don't know. If `[fresh:: …]` is added at the end, which is what every current Bob writer does, `created`, `scheduled`, `priority` and `dependsOn` stop being read, and Blocked is no longer derived for that task. `fresh` has to go before the trailing Tasks fields, and one helper per language should own that rule.
2. **Only a person stamps.** When a task comes back from Blocked on its own (a `scheduled` date arrives or a dependency closes), it becomes due for review. It is not stamped. Creating a task never stamps it, whatever the capture path.
3. **Two tiers.** NEW (never stamped) comes first and is never capped. STALE (stamp expired, or back from a deferral) can be budgeted. Your "N per day" idea should apply only to STALE, and as a progress meter rather than a filter. A Tasks `limit N` block just shows the next N as soon as you clear the first N, so it never finishes.
4. **Ready tasks only in v1, recurring tasks excluded.** Next and Pending are already walked every morning and pruned weekly.
5. **Keep a small weekly check** inside the existing weekly prune chore: finish any leftover STALE and look for projects with no next action. Freshness can't notice tasks that don't exist.
6. **Seed stamps before switching over.** Without a seed, every existing task counts as NEW on day one and buries the one capture that matters. The seed covers every open non-recurring task: Ready ones spread over 7 days, grouped by note. Blocked, Next and Pending ones get the cutover date so they come back as STALE rather than NEW. None of the five reports caught that last case.

**Recommended setup:**
- **Fields:** `[fresh:: YYYY-MM-DD]` on the task, an interval override `[refresh:: N]` on the task, and `task_refresh: N` in the note's frontmatter, then a config value, then 7 days.
- **Review in the source notes:**
  - `]s`/`[s` (or Ctrl+Alt+J/K) jump to the next or previous task that needs review, across the whole vault.
  - **Alt+F** refreshes the task under the cursor. **Alt+Shift+F** refreshes it and jumps to the next one.
  - A status bar counter shows `⟳ 23 due · 3 new · ✓ 12 today`.
- **Dash:** gets one REVIEW chip linking to a `freshness.md` note (`review.md` is already taken). The accepted decision `today-is-read-from-the-ledger` keeps the TODAY/PENDING/NEXT/READY sections exclusive, so no new section.
- **Morning:** pull Keep, clear NEW, work STALE until it's empty or the budget is met, then plan from PENDING → NEXT.

**Load is the real risk.** With your 176 non-recurring Ready tasks on a 7-day interval, about 25 go stale each day. Returning deferrals and new captures add to that, so expect 30–45 glances a morning at first, roughly 5–8 minutes. That's far less than rereading all 186 Ready tasks, but it isn't free. The levers, in order: longer intervals for big slow notes like `sase.md`, deferring or cancelling during review, then the STALE budget.

**Decisions for you:**
- **`gkeep_inbox.md`:** do a one-time triage and then give it a 2-day interval (my recommendation), or keep it as a someday list with a long interval.
- **Desk captures:** keep "creation never stamps" for tasks you type or route yourself (recommended), or stamp them at creation to save 5–10 glances a day.
- **Scope:** Ready only (recommended), or include Next and Pending now.
- **Alt+Shift+F:** "refresh and jump to next" (recommended), or "refresh and see less often".
- **Names:** `fresh`, `refresh`, `task_refresh`, `freshness.md` and `]s`, or alternatives such as `reviewed`.

Land this after `bob-cli-2y.12` and the lane cleanup.

Sources:
- [Taskwarrior: Tasksh Review](https://taskwarrior.org/docs/review/)
- [tasksh(1)](https://www.mankier.com/1/tasksh)
- [Random Geekery taskrc](https://randomgeekery.org/config/shell/taskwarrior/)
- [OmniFocus 4 Reference Manual: Perspectives](https://support.omnigroup.com/documentation/omnifocus/universal/4.3.3/en/perspectives/)
- [OmniFocus at School: Reviews](https://www.omnigroup.com/blog/omnifocus-at-school-reviews)

---

%xprompts_enabled:true
# New Query

 Generate an infographic that illustrates the main points made in this research markdown
file. Write the image to `<stem>_infographic.png` in the same directory, where
`<stem>` is the source file's stem with any trailing `__final` removed (so
`topic__final.md` becomes `topic_infographic.png`; other stems are unchanged).
Create it without overwrite. If it already exists, stop and report the collision.


## Response

I’ll read the consolidated report, check that the output filename is free, then create the infographic beside it. I’m using the imagegen skill for the visual.

The report’s main recommendation is a daily two-tier review: clear every never-reviewed task, then work through older tasks as time allows. I’ll center the infographic on that flow, with the safeguards and expected review load alongside it.

The first draft has a misleading timeline: it marks days 5 and 6 stale, but the proposed default interval is 7 days. I’m correcting that before saving the image.

The corrected PNG is saved at the requested filename. I verified it’s a 1024 × 1536 image, and the earlier incorrect timeline is fixed.

Created the [task freshness infographic](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/research/202609/ready_task_freshness_review/ready_task_freshness_review_infographic.png) beside the research report. It shows the daily NEW → STALE review flow, the seven-day freshness rule, and the expected reduction in daily scanning.
