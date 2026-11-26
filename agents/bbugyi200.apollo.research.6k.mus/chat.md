# Chat History - ace-run (research.6k.mus)

- **TIMESTAMP:** 2026-11-26 11:27:22 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.6k.mus
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_111415.md`

## Prompt

%id(mus, clan=research.6k)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.6k.cdx`, `research.6k.cld`, `research.6k.grk`, `research.6k.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start rendering property cards at the top of prose (fka article) notes
and notebooks.

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qi and
  bob-cli-qj epic beads.
- These property cards should act like other property cards (e.g. the native Obsidian
  "Properties" should be hidden in these note files).
- Prose notes and notebooks do not currently support many custom frontmatter properties
  (just a summary?), but we should include rich, useful data related to the prose note /
  notebook in these cards. Think hard about what data would be most useful for us to
  show on these cards.
- As a part of this change, we should add excellent new glossary terms for "prose card"
  and "notebook card".
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__mus` suffix, i.e. `<stem>__mus.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Research complete. My report is at [prose_notebook_property_cards__mus.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202611/prose_notebook_property_cards__mus.md), registered as `research:202611/prose_notebook_property_cards__mus.md` (snapshot `explicit:9b68e98f571a2920dcfa2db3`).

Key findings:

- The idea is sound, with adjustments: inherit the existing fail-open mount gate unchanged, paint only from data bob already emits (no new frontmatter keys), and build prose detection on both `[[prose]]`/`[[article]]` spellings from day one rather than the `article` name.
- Parallel work is feasible with narrow coordination: reuse qi's real-Obsidian acceptance matrix instead of building a second harness, sequence display strings behind qj's rename, and note the one ordering constraint — prose notes report `note_kind: "note"` in the props contract while notebooks are already first-class `"notebook"`, so the prose card should key on frontmatter type rather than forcing a contract break.
- Recommended card contents: prose gets words/reading time, section/stub counts, numbering state, finding and inbound counts; notebook gets breadcrumb, note/section counts, `last_note` recency, summary health, and check findings. Draft `glossary:prose-card` and `glossary:notebook-card` definitions are in the report.
