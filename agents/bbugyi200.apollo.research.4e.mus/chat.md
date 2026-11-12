# Chat History - ace-run (research.4e.mus)

- **TIMESTAMP:** 2026-11-12 11:09:10 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.4e.mus
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261112_110045.md`

## Prompt

%id(mus, clan=research.4e)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.4e.cdx`, `research.4e.cld`, `research.4e.grk`, `research.4e.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We currently always show the GTD review footer. I would like to start making this footer
only show when the GTD review walk is active (i.e. the `s` key is active and will be
triggered by the `[[` and `]]` keymaps).

- As a part of this change, we should add two appropriate new footers that are active
  only when the `w` walk or `n` walk is active.
- The `w` walk should have indicators that show how many pending/next/ready tasks are in
  that walk, for example.
- We should add an excellent new "walker footer" glossary term to describe these footers
  (note that a "review footer" should be considered a type of "walker footer").
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

Done. Report written and registered.

- File: [walker_footer_gated_design__mus.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/walker_footer_gated_design__mus.md)
- Artifact ref: `file:explicit:f402e3b04384210600be6a94`
- Recommendation: one walker-footer slot with s/w/n views (not three items); gate `s` content on active mode with `none → s`, keep an ambient `s`-due dot, `w` = lane counts/position, `n` = current note prev/next targets; ledger-tools owns views, new nav `api.bracketRepeat v1` for mode sync.
