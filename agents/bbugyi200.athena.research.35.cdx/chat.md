# Chat History - ace-run (research.35.cdx)

- **TIMESTAMP:** 2026-10-01 11:30:55 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** research.35.cdx
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_112023.md`

## Prompt

%id(cdx, clan=research.35)
%m:codex/gpt-5.6-sol@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cdx in a 5-researcher swarm.
The other researchers, `research.35.cld`, `research.35.grk`, `research.35.mus`, `research.35.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cdx.md`.

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

I’ll independently trace the current freshness/status/dashboard implementation, review the project’s freshness and artifact rules, then write and register the `__cdx.md` report. I’ll avoid all peer reports and transcripts. I’m using the repository, memory-read, and artifact/finalization skills because the destination is a linked research repo and the snapshot must be audited and durable.

The canonical model already draws an important boundary: freshness is review metadata and must not change a task’s lane, schedule, priority, or Today state. I’m now checking whether the dashboard query layer can classify tasks directly, which will determine whether a derived `#rotten` mutation is necessary or merely denormalized state.

I’m using the read-only Bob query skill to inspect the live dashboard’s parsed task blocks and current freshness population without modifying the vault. This should reveal both the exact query constraints and whether “NEW” and “rotten” are large enough to justify separate surfaces.

The live data exposes two edge cases the requirements should name explicitly: `dash.md` currently has 210 READY rows, while the freshness evaluator has 199 in-scope fresh rows; 11 READY rows are outside freshness review scope (likely recurring or daily-note tasks). A dashboard filter must preserve those intentionally exempt tasks unless the product decision is to hide them too. Also, today’s queue is empty because the rollout stamped 391 tasks today, so rollout-day counts cannot validate long-term volume.

The implementation path is becoming clear: no preprocessing is needed. `bob-ledger-tools` already exposes synchronous `freshness.state/isDue/rank/counts` APIs, memoizes the whole-vault queue, and invalidates it on edits, frontmatter/config changes, and midnight rollover. The main engineering work is keeping the READY badge/count and native/headless query semantics aligned with the new filtered section—not inventing another source of truth.

I’m drafting the report around a derived-view design. The main requirement adjustments I’ll call out are: preserve recurring-task exemptions; route resurfaced tasks to the rotten page under a distinct RETURNED group; use ROTTEN only as user-facing terminology while retaining the existing `"stale"` machine value for compatibility; and replace the now-redundant REVIEW dashboard chip rather than accumulating overlapping badges.

The report is written and passes whitespace validation. It contains the live-count evidence, evaluates the hook/tag and generated-note alternatives, specifies the query/badge partition, and ends with the recommended derived-view solution. I’m now registering that exact file as the requested durable research artifact.

The snapshot registration succeeded as `file:explicit:d5a3d0d4c838e183160b2dfa`. I’ve also confirmed that only the new research report is dirty; the bob-cli and bob-plugins checkouts remain unchanged. I’m finalizing the research-repo commit declaration now.

Research completed and registered.

- Report: [task_freshness_dashboard_ready_rotten__cdx.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/research/202610/task_freshness_dashboard_ready_rotten__cdx.md)
- Artifact: `file:explicit:d5a3d0d4c838e183160b2dfa`
- Label: `research:202610/task_freshness_dashboard_ready_rotten__cdx.md`

Core recommendation: derive NEW/READY/RETURNED/ROTTEN views through the existing freshness API; do not materialize a `#rotten` tag with `task-status-hooks`.
