# Chat History - ace-run (research.6l.grk)

- **TIMESTAMP:** 2026-11-26 13:10:03 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** research.6l.grk
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_124105.md`

## Prompt

%id(grk, clan=research.6l)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.6l.cdx`, `research.6l.cld`, `research.6l.mus`, `research.6l.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

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
`__grk` suffix, i.e. `<stem>__grk.md` (double underscore before the
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

I'll start by opening the research repo and loading the skills and memory this design needs.

Next I’ll open the research checkout and pull the artifact, memory-write, and beads skill context.

The repo-open command is still running; I’ll wait for it to finish before continuing.

Research checkout is open. I’ll load AGENTS.md, the decisions roster, and the glossary plus artifact memory next.

The glossary selector needed kebab-case. I’ll reread memory, then pull the epic plan, existing research, and the 202611 folder.

The glossary load worked. Next I’ll extract the relevant strands, then open plans and bob-plugins.

I’ll extract the glossary and artifact rules, then open plans and bob-plugins in parallel.

Repos are open. I’ll load the plugins AGENTS file, the epic plan, and the property-card kit next.

The epic plan is the right template. I’ll read the rest of it, the adopted research report, and the kit code.

I’ll keep reading kit fragments and ref-note code while the artifact read finishes.

I have the sibling-epic pattern. Next I’ll inspect ref-note shape, `bob ref` JSON, and the `==` dispatcher.

I have enough evidence to write the design. Next I’ll add the figures and the report, then register the artifact.

The equals-editor figure is too wide. I’ll tighten the labels and rerender.

I'll pick up from the compacted session: re-render the equals-editor figure, then write and register the research report.

The research checkout path from last turn is gone, so I’ll reopen that repo and load the artifact-memory rules before writing.

Figures are already in the research checkout. I’ll measure them, load glossary and analog report structure, then write the report.

The notebook/prose epic names may have shifted; I’ll confirm live beads and finish the remaining evidence before writing.

Chat refs expose the same loose pipeline keys. Next I’ll re-render the equals-editor figure, then write the report.

The equals-editor figure fits. I’ll write the full research report next.

**Do it as a sibling epic beside `bob-cli-qm`, with a citation-plate Ref Card and a pipeline-key lock that can start today.** Do not merge into `qm`. Do not give refs an album schema editor.

Report: `research:202611/ref_property_cards/ref_property_cards__grk.md`  
Artifact: `file:explicit:ebf69bf5e9dc0d3f7fa94412` (source left in the research repo)

### Recommended product
One species, `ref`, on the existing ledger-tools kit. Folded by default. A `plate` tile, `REF` kicker, parent crumbs in the home hue, title, a type pill (`CHAT` / `BLOG` / `PAPER` / …), and chips only when the facts exist. Absorb the managed H1 and reading-task embed at render; do not delete them. Painting never spawns bob. Native Properties hide under the family `props_v1` gate.

`==` yes, after the lock: Property Editor focused on `title`. No add/remove/reorder/type. Rename, Today, parent refile, and reading-state stay on the commands and the `#task #ref` checkbox they already have.

### Why this, not the request as written
Refs are the largest typed family without a card: **1,377 listed notes**, 52% chats, 92% of *modern* notes chats. A paper-thumbnail inspector would overfit the minority and fight Bob Refs plus the note body.

The live reliability bug is already there: `bob props` treats `id`, `status`, `parent`, hashes, and `highlights_*` as **loose**. Generic `+` can trash pipeline keys today. Lock those as identity/derived in bob-cli first (`feat(props)!` if the JSON role change is a contract break). That track does not wait for `qm`.

### Parallelism
Coordination at three plugin seams, not everywhere:
- **Now:** lock pipeline keys in bob-cli
- **After `qm.1`:** species, `plate` tile, T1 silence, preview gate (new species default-gated), card fragments
- **After `qm.6`:** extend the takeover harness
- **After `qm.7`:** docs, `glossary:ref-card`, family glossary, deploy

Invariant: always-live kinds stay the pre-`qm` set. If `ref` is added to `PROPERTY_CARD_KINDS` while the gate only special-cases notebook/prose, `qm.7` deleting that gate would ship ref cards by accident.

### Glossary
Draft for `glossary:ref-card` is in the report, plus sequenced “not the Ref Card” clauses on `glossary:ref-panel` and `glossary:reference-note`. Family-edit `glossary:property-card` only after `qm.7`.
