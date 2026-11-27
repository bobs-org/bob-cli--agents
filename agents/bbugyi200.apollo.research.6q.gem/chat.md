# Chat History - ace-run (research.6q.gem)

- **TIMESTAMP:** 2026-11-27 14:10:19 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6q.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261127_135226.md`

## Prompt

%id(gem, clan=research.6q)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6q.cdx`, `research.6q.cld`, `research.6q.grk`, `research.6q.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

When I use the `<ctrl+j/k>` keymaps in Obsidian to jump to the next/previous markdown
section header, it is easy to lose my place (e.g. forget which section is after/before
the one I just jumped to).

- I would like to mitigate this by displaying a brief, non-intruisive (but clearly
  visible) outline of the file's markdown sections when one of these keymaps is used.
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

I have completed the independent design research and written the full report to [obsidian_section_jump_outline_hud__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_24/sase/repos/research/202611/obsidian_section_jump_outline_hud__gem.md) (registered as durable artifact `file:explicit:1cf0aa3af8b52b1e250a68ae`, label `research:202611/obsidian_section_jump_outline_hud__gem.md`).

### Critique & Key Findings
- **The core idea is right:** A jump-triggered, ephemeral outline avoids the permanent multi-split clutter of sidebar outlines (Core Outline / Quiet Outline), the mouse-first hover friction of floating edge TOCs, the sibling blindness of parent breadcrumbs, and the focus-stealing interruption of modal heading pickers.
- **Why Obsidian's `Notice` is the wrong primitive here:** Unlike `]w`/`]b` walk toasts, a section outline is **pane-local**. `.notice-container` is fixed to the global window top-right (detached from left/middle splits), collides with sync/task/walk notices, and replays enter/exit animations on every rapid `<ctrl+j>` tap.
- **Four root causes an outline alone would miss:**
  1. **Silent boundary wrapping** in `getSectionHeaderJumpLine` (`130-fences-and-status.js:58-81`).
  2. **Near-EOF scroll clamping with no landing highlight** when `scrollEditorLineToTop` hits max scroll (`610-plugin-jumps-and-counted-keys.js:178-205`).
  3. **Bob Live Preview hidden headings:** `bob-ledger-tools` hides title-owned opening H1s (`240i-plugin-property-card-title-ownership.js`) and absorbed catalog H2s (`## Projects`, `## Areas`, etc., `240wg-plugin-cabinet-absorb-editor.js`), which raw-text `<ctrl+j/k>` currently jumps right into.
  4. **No burst `<C-o>` return point or `N<ctrl+j/k>` counts** (plus a double-scroll frame from calling `setEditorCursor` before `scrollEditorLineToTop`).

### Justified Adjustments to the Requirements
1. **Adaptive sliding window (`≤ 12` full list; `> 12` centered 9-row window + pinned `↳` ancestor breadcrumb + 6 px right-edge full-file progress spine)** so long Highlights/research notes stay compact and scannable.
2. **Activity-aware smart lifecycle** instead of a blind timer: opens immediately on jump, morphs *in place* with zero flicker during rapid bursts, dwells `2.0 s`, pauses on deliberate pointer hover or held `Ctrl` (with a 6 s failsafe), and fades out (`180 ms`) immediately on edit, cursor move, pane/file switch, blur, or passive `Esc` (without stealing focus or hijacking `q`, respecting `decisions:q-and-ctrl-bracket-mirror-esc`).
3. **Companion orientation fixes:** 700 ms CM6 heading landing flash (reusing `.bob-landing-flash`), explicit `↻ wrapped` header pill + edge bump (and `only section` badge on 1-heading notes), fold/hidden-heading filtering in Live Preview, `N<ctrl+j/k>` counts, and burst-coalesced `<C-o>` jump recording.
4. **Optional Phase 2:** Reading-mode parity via `checkCallback` + `metadataCache.headings` + `previewMode.applyScroll`.

### Recommended Solution
Build a **pane-anchored, non-modal, theme-native Section Outline HUD** directly inside `bob-navigation-hotkeys` using the same 3-layer split as `Ctrl+W` window keys (`131-section-outline-model.js`, `474-section-outline-view.js`, `611-plugin-section-outline.js`, and `.bob-so-*` styles):
- **Anchored top-right of the active leaf's `.view-content`** (same eye band as the top-aligned heading, sitting in empty right margin under Readable Line Length, with automatic `.notice-container` overlap offset, popout `ownerDocument` support, and `< 520 px` compact mode).
- **O(1) doc-identity heading cache** keyed on immutable CM6 `state.doc`, single reused DOM host, full `prefers-reduced-motion` compliance, and a headless Chromium visual preview script (`scripts/preview-section-outline.cjs`) for light/dark sign-off.
