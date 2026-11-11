# Chat History - ace-run (research.44.mus)

- **TIMESTAMP:** 2026-11-11 06:51:24 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.44.mus
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261111_064505.md`

## Prompt

%id(mus, clan=research.44)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.44.cdx`, `research.44.cld`, `research.44.grk`, `research.44.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We already show a little key with a count next to task links that would free dependents.
I would now like to start adding a similar icon that hows how many other
ready/pending/next tasks exist in that task's leaf project which do not currently have
task links associated with them in today's daily file (so I know how many tasks will
appear in the successor offer when completing that task).

- This icon should only be shown for task links that correspond with tasks that live in
  leaf projects.
- For example, in the ~/tmp/screenshots/20261111_063929.png screenshot of the
  ~/bob/2026/20261111.md file, the `[[job_email_recruiters#^bryan-stephen-luzern-risk]]`
  task link should show this icon with a 4 next to it, since the
  ~/bob/job_email_recruiters.md file contains 4 next tasks that have no task links in
  today's daily file associated with them.
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
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Research complete. Report: `202611/leaf-task-keep-moving-icon__mus.md` (registered as `research:202611/leaf-task-keep-moving-icon__mus.md`).

Top finding: the worked example contradicts the leaf-only rule. `job_email_recruiters.md` is a top-level project (parent is the `job` area), not a leaf, so completing its linked task yields `"keep_moving":[]` today — I proved this with a scratch-copy dry-run. An icon showing 4 there would promise a picker that never appears.

Recommended solution: reparent the note under `job_2026` (one frontmatter line, making it a true leaf with exactly 4 offers), then build a display-only `⏭ N` ledger mark in bob-ledger-tools mirroring the frees-marks architecture (compact pill, `link 🔓 🔑 ⏭` order, honest "N more in ‹note›" tooltip, session toggle, KL/KC/KT/KP conformance vectors). No Rust, no decision change. Full design, count rule, alternatives, and three open questions for Bryan are in the report.
