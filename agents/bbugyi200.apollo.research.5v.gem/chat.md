# Chat History - ace-run (research.5v.gem)

- **TIMESTAMP:** 2026-11-22 12:34:40 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.5v.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261122_120049.md`

## Prompt

%id(gem, clan=research.5v)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5v.cdx`, `research.5v.cld`, `research.5v.grk`, `research.5v.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like for property cards to start taking over all properties defined in that
file's frontmatter.

- We should stop showing the built-in Obsidian "Properties" section for these notes
  completely.
- Instead, a read-only collapsable (collapsed by default) view of these properties
  should be able to be found at the bottom of the property card (it should be a part of
  the card).
- We should add a new `=-` keymap that allows me to expand/collapse this properties
  section of the property card.
- We should also add support for editing these properties via a new property editor,
  which should be triggered by a new `=+` keymap. This property editor should be at
  least as powerful as Obsidian's builtin "Properties" header (ideally more so and much
  easier to use via the keyboard).
- We should attemmpt to represent the `created` property somewhere concisely on all
  property cards even when the properties section of the card is collapsed.
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

Completed the independent research and design specification for Property Card frontmatter takeover and the keyboard-first Property Editor:

- **Report**: [property_card_frontmatter_takeover__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/property_card_frontmatter_takeover__gem.md)
- **Registered SASE Artifact**: `explicit:b2d7788dff4f3963e34cd0f0` (`research:202611/property_card_frontmatter_takeover__gem.md`, stored at [property_card_frontmatter_takeover__gem-33d4e3b036ac.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261122120055/property_card_frontmatter_takeover__gem-33d4e3b036ac.md))

### Verdict & Executive Summary

**Strongly endorse the proposal, with six concrete adjustments.** Across the live `~/bob` vault (1,473 property-card notes across 7 species vs. 5,216 other frontmatter notes), taking over `.metadata-container` removes partial row-hiding clutter (and Record Sheet's current three-layer overlap of sheet rows + bespoke `▸ N other properties` fold + native Properties) while unlocking a fast, Vim-native Property Editor.

### Six Justified Requirement Adjustments Called Out in the Report

1. **Retire Record Sheet's bespoke fold & `created` `<p>`** (`242j-plugin-record-sheet-dom.js`) and unify all 7 species on one shared kit **Properties Footer Bar + Drawer**.
2. **Smart `created` readout right-aligned on the collapsed footer bar (0 px extra height)**: show `Created 6:43 AM` on same-day Day cards (166/175 modern dailies share the title date), `Created Jun 11, 2026` on backfilled dailies and other species (fixing the space-separated `2026-08-06 07:35` format on `podcasts.md`), flag invalid `created` with an amber badge, and omit cleanly on the 80.6% of card notes where `created` is absent (Week/Quarter/Year, Zorg dailies, legacy records).
3. **1:1 drawer completeness without noise**: summarize nested mappings (`record:` on Albums, `bank:` on `bank.md`) as compact structural rows with a 1-click/`==` jump, subtly badge card-rendered keys (`in card`), and tuck historical Zorg migration keys (`generated_from_zorg`, `zorg_*`) behind a secondary sub-fold (`▸ 7 migration keys`).
4. **Make `=+` work vault-wide across all Markdown notes** (while keeping `=-` scoped strictly to notes with a mounted property card), and add a Reading-view `=` prefix window + Command Palette commands + card footer controls so `==`/`=-`/`=+` work outside Live Preview too.
5. **Include `bank.md` immediately** in whole-container hiding and the shared footer while leaving its eventual migration from body-mount to title-slot decoupled.
6. **Strict fail-open invariants**: never hide `.metadata-container` on malformed YAML, Source mode, embeds, hover popovers, Canvas, Print, mobile, or failed mounts; leave the right-sidebar File Properties pane untouched.

### Recommended Solution

- **Whole-Container Hiding**: Replace `240b`'s per-row `MutationObserver` (`subtree: true`) with a scope-level class (`bob-property-card-owns-properties`) backed by a Live Preview `StateField` (`EditorView.editorAttributes`, mirroring `240i`) and direct-child CSS (`display: none !important`), keeping `.metadata-container` in the DOM so `240e` title-slot anchoring continues working cleanly. Route `241d`'s `notebookFocusSummaryProperty` to `=+` when `.metadata-container` is card-owned.
- **Generalized `=` Chord Dispatcher**: Extend `248m-plugin-schema-double-equals.js` (since Vim treats `=` as `indentAuto` and `obsidian_vimrc.md` cannot bind `=-`/`=+`) to dispatch `==`, `=-`, and `=+` in capture phase — allowing `shiftKey` for `+`, rejecting counts/registers/Source/Insert/Visual/Replace, and adding an 800 ms Reading-view prefix window.
- **Hybrid Write Engine (Zero `bob-cli` breaking changes for v1)**:
  - **Verified JS Line-Span YAML Writer** (mirroring `bob-cli`'s `src/native/yaml_spans.rs` rules — never `processFrontMatter`): preserves BOM, CRLF, comments, quoting, and `bank.md` flow maps; refuses duplicate keys and anchors/tags; verifies every edit with `parseYaml()` round-trip checks; commits via `editor.replaceRange` (instant UI + native Undo) or preimage-guarded `vault.process` + in-modal multi-step Undo (`u` / `Ctrl+Z`).
  - **`app.metadataTypeManager`** for global `.obsidian/types.json` property types (with an explicit timezone-loss warning if converting `created` away from `text`).
  - **1-key `=` handoff** to existing Rust-backed `==` domain editors for `record:`/`bank:`/schema-managed fields, **`y` YAML excursion** with `242e`'s floating `Done` pill, **`proseField` v2 (`S16`)** + `bob-emoji`, and `Esc`/`q`/`Ctrl+[` close keys via `241xc`.
