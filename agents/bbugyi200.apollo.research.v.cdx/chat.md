# Chat History - ace-run (research.v.cdx)

- **TIMESTAMP:** 2026-09-30 18:25:44 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** research.v.cdx
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_181054.md`

## Prompt

%id(cdx, clan=research.v)
%m:codex/gpt-5.6-sol@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cdx in a 5-researcher swarm.
The other researchers, `research.v.cld`, `research.v.grk`, `research.v.mus`, `research.v.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cdx.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

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
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cdx` suffix, i.e. `<stem>__cdx.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I’ll research this independently, using the epic only for project context and avoiding every peer report. I’m using the SASE repo, bead, memory-read, artifact, and final-declaration skills because the output lives in the research sidecar, the prompt cites a bead, and the completed report must be registered as a durable artifact.

The epic confirms the new model: Today is ledger-derived, while Pending/Next/Ready are mutually exclusive sticky lanes. I’m treating freshness as a separate review concern—not another execution status—so the design won’t undo that work. Next I’m tracing the current task schema, dashboard, hooks, and Obsidian keymaps, then comparing the mechanism against established GTD review and spaced-attention patterns.

A key design tension has emerged: the proposed date is defined as “last human confirmation,” so an automated unblock cannot truthfully advance it. I’m separating human acknowledgement from machine transitions in the recommendation. I’m also using the read-only Bob query skill to measure the present Ready backlog and age distribution; that will show whether a seven-day default is operationally plausible without touching the vault.

The live vault measurement changes the practical recommendation: the Ready lane currently has 186 tasks (176 non-recurring), including 65 in `gkeep_inbox.md`. A blanket seven-day cadence would mature about 26 tasks per day at steady state. I’m keeping seven days as the safe default, but the report will recommend a separate “never reviewed” queue, longer note-level intervals for low-volatility backlogs, and a cap that applies to periodic re-reviews—not to newly captured items.

The report is written and validated (4,998 words, clean Markdown diff). Its final recommendation preserves the exclusive lane dashboard, treats missing freshness as due, prevents automation from impersonating human review, and sizes the cadence against the live 186-task Ready population. I’m registering that exact file now as the requested durable snapshot.

Registration succeeded and the source remains in the research repository. Artifact reference: `file:explicit:cab9f84d4a176a3c8b5b9d37`. I’m now submitting the required SASE final declaration so the report is durably committed.

Research complete and independently authored.

- Report: [task_freshness_rolling_review_design__cdx.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/research/202609/task_freshness_rolling_review_design__cdx.md)
- Artifact: `file:explicit:cab9f84d4a176a3c8b5b9d37`
- Stored snapshot: `/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20260930181054/task_freshness_rolling_review_design__cdx-c9e339a5c378.md`

The report recommends task freshness with important adjustments: separate new/unreviewed tasks from expired tasks, never let automation claim a human review, exclude recurring tasks initially, preserve the exclusive lane dashboard, and use per-note intervals plus a bounded rolling review. Artifact registration and final declaration both succeeded.
