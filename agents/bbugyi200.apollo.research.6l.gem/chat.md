# Chat History - ace-run (research.6l.gem)

- **TIMESTAMP:** 2026-11-26 13:02:05 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6l.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_124105.md`

## Prompt

%id(gem, clan=research.6l)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6l.cdx`, `research.6l.cld`, `research.6l.grk`, `research.6l.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
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

I completed independent research on **Ref Cards** and registered the report as a durable SASE artifact:

- **Report:** [ref_property_cards__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/ref_property_cards__gem.md) (`research:202611/ref_property_cards__gem.md`)
- **Artifact:** `file:explicit:6b72c7def8080773f1d124df` (`~/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261126124110/ref_property_cards__gem-e0db5898467a.md`)

### Key Conclusions & Recommendations

1. **Verdict — Strongly Worth Building:** Ref Cards address the largest typed collection in the vault (**1,379** live notes under `ref/`: 775 modern PDF-backed + 604 legacy zorg-era) and eliminate the 17–21 row native Properties wall of SHA-256 hashes and sync plumbing on modern references.
2. **Six Justified Requirement Adjustments:**
   - **Path-confined eligibility:** Require **both** `ref/**/*.md` and exact `type: "[[ref]]"` — never `type: "[[ref]]"` alone, which would falsely claim 13 root-level legacy `*_ref.md` hub notes (`obsidian_ref.md`, `dev_ref.md`, etc.). Include both modern and legacy `ref/` notes (with a calm muted legacy treatment); keep `ref_history/` excluded.
   - **Harden `bob props` ownership in `bob-cli` (`roles.rs`):** `bob props show` currently classifies 15+ pipeline, sync-hash, and `^ref`-projected keys (`source_pdf_sha256`, `highlights_marker_*`, `pipeline_version`, `ref_type`, `audio`, `status`, `parent`, `id`) as editable `loose` rows. Lock them in `bob-cli` and emit an additive `props_ref_contract_v1` contract (`schema_version: 1`) while still gating Ref Card takeover on `props_v1` alone for clean version-skew fallback.
   - **Zero-spawn, local-first painting:** `bob ref show` (~1.09 s) and `bob ref list -R all -A` (~1.18 s / 1.48 MB) are far too slow to spawn on paint. Paint exclusively from local frontmatter, the note body (`## Highlights`, `[!summary|section]` cards), Obsidian's Tasks/Today/Snoozed/backlink caches, cached single-file `done/` task reads, and immutable `.bob/ref-sources/*/code.json`.
   - **Own only the redundant opening H1:** Keep Obsidian's interactive `![[parent#^ref-...]]` reading-task embed and `![[lib/...mp3]]` audio player visible directly below the card (mirroring how Project Cards keep `^prj`). Use a case/stem/managed-embed-aware H1 recognizer so editing `title:` never re-exposes a stale birth H1.
   - **Support `==` inside the shared Property Editor (not a bespoke modal):** Mirror Area/Project's settings-and-handoff architecture — `REFERENCE METADATA` (`title`, `author`, `published`, `source_url`/`url`, `topics`, `aliases`, with ghost rows and PDF-sync notices), `ON THE ^REF TASK` (validating and handing off straight to the `^ref` task's Task Card in its residence note), and `REFERENCE ACTIONS` delegating to Command Mode / Highlights (`Open PDF`, `Pull to Today`, `Rename`, `Sync PDF`, `Code/Links`), degrading to focus-or-add on `title` under older `bob`.
   - **Parallelize cleanly with `bob-cli-qm` via an isolated preview gate:** Use a Ref-Card-owned `refCardPreview: true` gate (independent of `qm`'s `cardPreviewKinds`, which `qm.7` deletes) across 6 phases: Phases 1 (`bob-cli` Rust) and 2 (pure JS model/body/DOM/fixtures) start immediately at T=0; Phase 3 waits only on `bob-cli-qm.1`; Phase 5 waits on `bob-cli-qi.4`; Phase 6 (go-live, docs, `glossary:ref-card`, `glossary:property-card` update, deploy) waits on `bob-cli-qi.6` and `bob-cli-qm.7`. Zero dependency on `bob-cli-qj`.
3. **Visual Design & Glossary:** Introduces a distinct vertical bookmark **`ribbon`** tile silhouette (bottom inverted-V notch) with `ref_type`-specific Lucide icons, root-area hue wash (5% filled for active, 2–3% outlined for terminal/legacy), archetype-aware provenance bylines, live reading state + blocked reasons + jumpable annotation section chips, silent missing `created`, `Managed · N` drawer folding, and a complete draft for `glossary:ref-card` plus the `glossary:property-card` delta.
