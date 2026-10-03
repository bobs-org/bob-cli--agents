# Chat History - ace-run (research.3a.grk)

- **TIMESTAMP:** 2026-10-01 17:32:44 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** research.3a.grk
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_171714.md`

## Prompt

%id(grk, clan=research.3a)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.3a.cdx`, `research.3a.cld`, `research.3a.mus`, `research.3a.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We
recently seeded the `fresh` property for all ready Obsidian tasks with fake freshness
dates in order to chunk these up a bit so I am not overwhelmed. I don't think we'll need
to do that anymore if we refine my morning GTD review process a bit more.

- Namely, the `[s` / `]s` and `<ctrl+alt+j/k>` keymaps should always walk through new
  tasks first, then pending tasks, then next tasks, and then ready tasks in order based
  on which ready tasks have the lowest refresh interval and then (if refresh intervals
  are equal) based on which was refreshed earlier (i.e. is more overdue) and then (if
  they have the same `refresh` property value) based on which was created later. For
  example, we should review a task with a 1d refresh interval before we review a task
  with a 7d refresh interval that is 1d overdue but we should review a task with a 7d
  interval that is 3d overdue before that one and we should review a task with a 7d
  interval that is 3d overdue but was created a few days later even sooner .
- We should also change the way refresh intervals are determined by adding new
  configuration fields that control the refresh interval used for pending/next tasks.
  Also, any task that has a `scheduled` property should have a default refresh interval
  that is configurable as well. All of these should default to 1 (i.e. they need to be
  refreshed every day--in the case of scheduled tasks, this just means they need to be
  refreshed on the day they are due).
- This should have the effect of me always reviewing my new tasks, pending tasks, next
  tasks, due scheduled tasks, and other ready tasks in that order.
- Once that is done, we should remove all of the artificial `refresh` properties that we
  added previously.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__grk` suffix, i.e. `<stem>__grk.md` (double underscore before the
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

I'll research the GTD review/refresh design independently and write a `__grk.md` report. First I'll load the relevant skills and inspect the current task-walk and freshness implementation.

The workspace is bob-cli with a linked research repo. I’ll open that repo, then read freshness, task-lane, and keymap sources before forming a recommendation.

Keymaps and interval logic live across bob-cli and bob-plugins. I’ll open both repos and the research sidecar, then read the current walk/sort and config contracts.

Repos are open. Next I’ll map the walk keymaps, interval config, and seeded `refresh`/`fresh` fields so the critique is grounded in the actual code.

I found the review-jump implementation. Next I’ll read its sort, vim mappings, interval evaluation, and how the vault currently stores seeded `refresh` fields.

The gated-READY plan deferred Next/Pending freshness and walk order. I’ll pull vault counts, the vimrc bindings, and the prior research that scoped this out.

I have the live numbers and the contract split. Next I’ll write the independent `__grk` report, then register it as an artifact.

The report is on disk. I’ll register it as a durable snapshot, then submit the turn.

The walk order is a good idea. Implement it as one queue behind the existing `]s` / `[s` / Ctrl+Alt+J/K keys, with Pending/Next defaulting to a 1-day lease and Ready staying at 7.

Report: `research:202610/gtd_review_walk_lane_intervals/gtd_review_walk_lane_intervals__grk.md`  
Snapshot: `file:explicit:12edfbda5a6bc400a7902b6f`

**Do this**
- Walk **NEW → PENDING → NEXT → due scheduled (RESURFACED) → other Ready-due**.
- Add `freshness.pending_interval` and `freshness.next_interval`, both default **1**. Keep Ready `freshness.interval` at **7**.
- Sort Ready-due by **interval ASC, then more overdue, then newer `created`**.
- Keep dash / `rotten.md` / `counts.due` **Ready-only**. Pending/Next belong in the keymap queue, not on `rotten.md`.

**Adjustments**
- Do **not** give every task with a `scheduled` field interval 1. “Refresh on the day it is due” is already RESURFACED. Naive `scheduled_interval: 1` would daily-leash **59** already-confirmed Ready tasks.
- Do **not** strip `[fresh::]` seed dates. The vault has **zero** `[refresh::]` fields. Deleting stamps recreates a ~199-task NEW flood.
- Pending **50** / Next **30** vs caps **10** / **15**. Interval 1 without a release pass is ~107 glances on 2026-10-02. Release to cap before measuring the 10-minute ritual.

Sort lives in `api.freshness.queue()` (Rust + JS). `planReviewJump` already walks that list. Land it before the 2026-10-05 trial so the trial measures this ritual.
