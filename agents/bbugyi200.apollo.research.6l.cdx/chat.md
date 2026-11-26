# Chat History - ace-run (research.6l.cdx)

- **TIMESTAMP:** 2026-11-26 12:56:21 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** research.6l.cdx
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_124105.md`

## Prompt

#gh:gh_bobs-org__bob-cli
%id(cdx, clan=research.6l)
%m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm.
The other researchers, `research.6l.cld`, `research.6l.grk`, `research.6l.mus`, `research.6l.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cdx.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to implement "ref cards", a new type of property card for ref notes.

- See how other property cards are implemented and the bob-cli-qm epic bead, which is
  in-progress and implements notebook cards and prose cards, for context and
  inspiration.
- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qm epic.
- Think hard about how this card should look. It should contain as much genuinely useful
  information about the reference as possible without cluttering the card.
- Also, think hard about whether or not ref cards should support the `==` keymap and, if
  so, what kinds of operations the schema editor that is triggered should support.
- As a part of this change, we should add an excellent new glossary term for "ref card".
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cdx` suffix, i.e. `<stem>__cdx.md` (double underscore before the
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

I’ll independently inspect the existing property cards, ref metadata, and the notebook/prose epic, then write a design recommendation that covers appearance, editing, and parallel implementation. I’ll use the SASE repo, memory, bead, and artifact workflows for the investigation and durable report.


The existing cards already share title, fold, refresh, and keyboard behavior. I’m checking how ref cards can reuse that shell while keeping reference data and edits owned by the CLI.


A key constraint is now clear: reading state and filing belong to the reading task, while source paths, IDs, and annotation snapshots have their own lifecycle rules. The card should expose those facts and offer navigation without turning them into ordinary editable fields.


I’ll use the Bob reference workflow for a read-only metadata sample, so the design reflects the mix of references in your library. My current direction is a compact identity card with useful navigation, plus a `==` editor limited to safe metadata changes and existing reference operations.


The metadata sample supports keeping the card sparse: many refs lack author or publication details, and legacy refs often lack PDFs or reading tasks. I also found a concrete overlap with `bob-cli-qm`: it owns the shared eligibility code and a temporary preview switch. Ref work can proceed independently, but activation must not depend on a switch that `qm` plans to remove.


My recommendation is a folded Ref Card that leads with identity, source access, and reading context, with less-used details behind expansion. I’ll include two explicit scope adjustments: `==` should reuse the Property Editor rather than introduce a schema builder, and retitling should wait for a transaction that can safely reconcile the metadata title and body heading. I’m writing the report now.


The report is written and its durable snapshot is registered. It includes the inventory of 1,377 references, card sketches, editing boundaries, parallel delivery guidance, and a proposed glossary entry. I’m finishing the report checks and SASE final declaration.


Created the independent [research report](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/research/202611/ref_cards_identity_metadata_and_parallel_delivery__cdx.md) and registered [durable snapshot `explicit:c6f2fb3e26bc02a2a95a3d4f`](/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261126124105/ref_cards_identity_metadata_and_parallel_delivery__cdx-c990e2fe8f92.md).

Recommendation: a compact Ref Card with bounded `==` metadata editing, progressive disclosure, and an independent activation gate for parallel delivery with `bob-cli-qm`. The report includes design sketches, requirement adjustments, and a proposed glossary entry.
