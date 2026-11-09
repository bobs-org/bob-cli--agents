# Chat History - ace-run (research.3u.mus)

- **TIMESTAMP:** 2026-11-09 07:11:40 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.3u.mus
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_070553.md`

## Prompt

%id(mus, clan=research.3u)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.3u.cdx`, `research.3u.cld`, `research.3u.grk`, `research.3u.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I like the set up we have now where I ask agents to add useful context to period note
files at the end of that period (an agent just updated the ~/bob/2026/2026-W45.md file
today, for example). I want to improve the agent instructions contained in these files
to try to make the summaries/context produced by agents even more useful, but I'm not
sure what changes to make.

Can you do some research with the goal of helping me decide if this is a good iea and
(if so) what changes to these period note agent instructions would be most useful? 
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

Report written and registered.

- File: [period_note_agent_instructions__mus.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202611/period_note_agent_instructions__mus.md)
- Artifact: `research:202611/period_note_agent_instructions__mus.md`
- Verdict: yes, iterate with small versioned deltas. Top recommendations: standalone-Headline rule, numbered question taxonomy with carry-forward slot, silent-omission rule for empty parts — paired with a `draft`-side link check and a 4-week question-answer-rate measurement.
