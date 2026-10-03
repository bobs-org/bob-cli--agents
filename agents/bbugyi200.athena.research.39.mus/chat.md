# Chat History - ace-run (research.39.mus)

- **TIMESTAMP:** 2026-10-01 16:21:02 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.39.mus
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_161410.md`

## Prompt

%id(mus, clan=research.39)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.39.cdx`, `research.39.cld`, `research.39.grk`, `research.39.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

One of my goals while reviewing my Obsidian tasks during my morning GTD is to make sure
that no area/project note file contains more than N ready tasks (this number should be
configurable, but should default to 5).

- The idea is that if I have more than N ready tasks in a area/project, then I should
  probably look into creating a new project from some of those tasks and/or
  de-prioritizing (using the `<ctrl+shift+p>` keymap, for example) some tasks in that
  area/project note file.
- I would like to make it clearer which project files have more ready tasks than they
  should.
- We should show some kind of notification / toast in Obsidian anytime we use any one of
  the Obsidian keymaps that would cause this constraint to be violated (for example,
  when moving a task to a project note file that already has >=N ready tasks).
- We should show a badge and/or diagnostics in the ~/bob/dash.md file and/or in project
  note files that makes it clear how many area/projects violate this contraint currently
  (and which ones).
- I should also have the ability to view this information from the command-line. Namely,
  I should have the ability to review the number of ready tasks in each area/project
  note file from the command-line and should be able to see (in some visually appealing
  way) when this constraint is being violated (and in which area/project note files).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__mus` suffix, i.e. `<stem>__mus.md` (double underscore before the
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

Done. Top finding: a **per-note ready-task cap (default 5 for projects) is worth building as a soft limit** — it fills the gap between the global READY cap (100) and daily plan caps, and restates Bryan's own `^prj-task-count-warn` task.

Report written to [ready_tasks_per_note_budget__mus.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/research/202610/ready_tasks_per_note_budget__mus.md) and registered as durable snapshot `research:202610/ready_tasks_per_note_budget__mus.md` (artifact `explicit:98820626641536df668b10c2`).

Key points (all verified against repo/docs/live commands, not inferred):

- **Define "ready" as dashboard-READY-per-file** (TODO, visible, unblocked, due, not-Today, freshness-confirmed-or-exempt) so note counts sum to the dash count. Pragmatic v1 may reuse the already-native SHOWN predicate, clearly labeled.
- **Adjustments called out in the report:** split N by kind (projects 5, areas 8) + per-note `task_budget:` override; toast only on upward threshold crossings, never modal, never blocking; scope = `capture-targets` routable set minus inboxes/dailies.
- **Recommended solution:** new `ready:` config block, read-only `bob ready` CLI (TTY-colored table + JSON `schema_version: 2`) with capture/hooks warnings, then ledger-tools `api.ready` + dash over-budget section, then keymap toasts (`Ctrl+Shift+M`, capture routing, `Ctrl+Shift+P` unschedule) and per-note `READY n/cap` badge — phased so phase 1 ships in this repo alone.
- **Critique:** yes, good idea, but notification fatigue is the #1 risk and the metric is gameable via `#hide`; alternatives (review-query-only, lowering global `max_ready`, auto-split, hard blocks) are evaluated with hard blocks rejected.

Declaration submitted: commit for `sdd:research` report `202610/ready_tasks_per_note_budget__mus.md`.
