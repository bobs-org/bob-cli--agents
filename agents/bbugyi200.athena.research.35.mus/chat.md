# Chat History - ace-run (research.35.mus)

- **TIMESTAMP:** 2026-10-01 11:47:23 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.35.mus
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_112023.md`

## Prompt

Your previous attempt hit a model context limit or transient provider failure. Any file edits, new tests, and other on-disk changes you made are preserved. Before making additional changes, run `git status` and `git diff` to see what is already in place, then continue implementing the plan from wherever you left off. Do not re-apply edits that are already present.

%id(mus, clan=research.35)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.35.cdx`, `research.35.cld`, `research.35.grk`, `research.35.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

The point of the
new `[fresh::<date>]` properties that we've added to ready Obsidian tasks is to make it
clearer which of those tasks are really ready.

- A new task or a rotten task (let's start using the term "rotten" instead of "stale")
  should not be shown in the "READY tasks" section of the ~/bob/dash.md file.
- Instead, we should show new tasks either in a new "NEW tasks" section, which should be
  shown above the "WIP tasks" section and show rotten tasks in a new ~/bob/rotten.md
  file (that the ~/bob/dash.md file links to with a new "ROTTEN" badge).
- We may need to preprocess these rotten tasks somehow in order to make this work. My
  first thought was that we could use the `bob task-status-hooks` command to add a
  `#rotten` tag to rotten tasks, but you should think hard about the best way to
  implement this.

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

Research complete and registered.

Report: `sase/repos/research/202610/ready_new_rotten_split__mus.md` (registered as `research:202610/ready_new_rotten_split__mus.md`, snapshot `explicit:f9bfb28f0786393274825c8d`).

Top finding: do not preprocess anything — reject the `#rotten` tag. Freshness state is already computed at read time in both engines, so three Tasks `filter by function` predicates on the existing `api.freshness.state(task)` mirror deliver NEW / ROTTEN / READY with zero writer changes and zero midnight-rot. Six reasons are in the report (settled read-time-derivation rules, hooks running at the wrong times, the tag-removal problem across every writer, write-contract expansion into the trailing-field danger zone, tag-pane pollution, zero capability gain).

Recommendations: partition today's READY exactly into READY′=FRESH, NEW, and ROTTEN=STALE∪RESURFACED (resurfaced stays a named subgroup in rotten.md); place the NEW section after TODAY Tasks (no WIP section exists in dash.md — PENDING is the closest match); model rotten.md on blocked.md; rename stale→rotten atomically in one release with a `bob freshness` JSON schema bump; decline the sibling 1-day WIP/NEXT interval task (32 NEXT + 49 PENDING would flood the due set daily). Verified against the live vault: 199 fresh / 0 due today, native `filter by function` works headless, and all four dash blocks parse via `bob query --tasks-note dash.md`.

Declaration accepted for `commit` (research report `202610/ready_new_rotten_split__mus.md`). No further work this turn.
