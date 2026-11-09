# Chat History - ace-run (research.3w.grk)

- **TIMESTAMP:** 2026-11-09 09:41:13 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** research.3w.grk
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_092439.md`

## Prompt

%id(grk, clan=research.3w)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.3w.cdx`, `research.3w.cld`, `research.3w.mus`, `research.3w.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to improve the way that we handle done notes with the goal of fixing any
existing bugs, making their management more reliable and intuitive, and making other
improvements where possible and desirable (think hard about what improvements we could
make that I would most likely find useful). I think we use `done/<name>_done.md` files
currently, which works OK I guess. I'm just curious how other systems handle this and
whether there is a better way to approach this problem.

Can you do some research with the goal of helping me with this? End your analysis with a
recommended set of changes that you think I should consider making (or recommend no
changes). 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__grk` suffix, i.e. `<stem>__grk.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I'll research how Bob currently handles done notes, then compare that with other systems and write an independent report. First I need the artifact, memory, and research-repo conventions so the write and registration stay in bounds.

I'll record the required skills, open the research sidecar, and pull the done-note memory and code in parallel.

I'll open the research sidecar and pull the memory, glossary, and current done-note code in parallel.

Research sidecar is open. Next I’ll map the current done-note implementation and check `202611/` so I don’t overwrite an existing report.

I'll pull the archive implementation, docs, and any existing done-note research so the report is grounded in the actual system.

The archive lives in `collect_done`. I’ll read that module next and fan out to bugs, vault layout, and how other systems archive completed work.

I have the archive planner. Next I’ll read link repair, tests, project-terminal handling, and the live vault, and I’ll look at how other systems archive completed work.

Live vault has 31 archive notes and a few known beads. I’ll sample those notes, inspect remaining closed tasks, and compare reopen/search behavior with other systems.

The archive path is free. I’ll draw the lifecycle figures, then write the independent report.

Figures read cleanly. Next I’ll write the full independent report.

Keep `done/<stem>_done.md`. Change what gets moved into it.

The independent report is at `sase/repos/research/202611/done_notes_task_archive/done_notes_task_archive__grk.md`, registered as `research:202611/done_notes_task_archive/done_notes_task_archive__grk.md` (`file:explicit:035d4520c1c6d52a590c3aa0`). The source file stayed in the research repo.

**What Bob already has.** `bob task archive` (nightly, default threshold 10) moves closed `[x]`/`[-]` `#task` blocks into `done/<stem>_done.md` with `type: [[done]]`, `parent:` back to the live note, and `done_tasks:` on the source, then rewrites wikilinks. That sidecar is Org’s `%s_archive` adapted to path+block-id identity. The live **Done & Canceled** group is the in-file recent store. Terminal *project notes* stay put with `status: done` — that is a different layer and should stay a status, not a move.

**What is wrong.** The hinge of “wait until this note has 10 closed tasks” is the problem, not the filename. In the live vault today: 31 archive files, 564 notes still holding 1–9 closed tasks (~900 rows), `gtd_daily_done.md` at 191 KB with 1,084 unheaded lines, and daily notes still eligible (Event Tasks are `#task`; a busy GCal day would empty `## Events`). Standalone archive has no `--dry-run`, no JSON, and no maintenance lock. Empty Done headings wait for reconcile, which nightly does not run. Reopen is blocked (`task move` refuses `done/`). `done_tasks:` lives in hidden YAML.

**Recommended changes (keep the files, fix the gate):**

1. Contract page `docs/task-archive.md`.
2. Never collect from canonical daily notes.
3. Recency rule: keep today’s completions plus the last five; archive the rest into the existing sidecar.
4. `--dry-run`, `-f json`, and the same lock as `bob task move`.
5. Rewrite status groups in the archive transaction.
6. Point the Done chip (or a 📦 line) at `[[done/stem_done]]`.
7. File dump rows under `## YYYY-MM-DD`.
8. Allow move-*from*-`done/` as reopen.
9. Ship open bead `bob-cli-em` (mint ids on archived mention sources).
10. Fail or repair ambiguous duplicate `^id`s instead of skipping link repair.
11. Self-heal archive path when the source was renamed (`20260528_day_done` is the live leftover).

Do not PARA-move finished project notes into `done/`, do not flatten to one `archive.md`, and do not drop the `_done` suffix (it keeps the `sase` basename unique).
