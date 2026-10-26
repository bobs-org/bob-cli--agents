# Chat History - ace-run (research.5b.gem)

- **TIMESTAMP:** 2026-10-26 07:18:41 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.5b.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261026_070311.md`

## Prompt

%id(gem, clan=research.5b)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5b.cdx`, `research.5b.cld`, `research.5b.grk`, `research.5b.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for the ability to target (i.e. copy) code block contents
from the copy mode that is activated from the bob-mac-capture app's ref panel via the
`<cmd+y>` keymap.

- We will probably only be able to make this work for ref notes that were created by
  converting markdown files to PDFs (via the `bob ref create` command).
- We might need to start copying the markdown files that we used to generate the PDFs to
  some nearby location for this use-case (unless we can read the PDF directly). This is
  probably a good practice anyway so we always have access to the original markdown
  file.
- Think hard about what the best UX is for this is.
- As a part of this change, we should also add a new `<cmd+y>` keymap to the Highlights
  app that triggers the ref panel with copy mode activated for the current PDF.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
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

# Code Block Targeting in Ref Copy Mode & Highlights `<cmd+y>` Integration

The research report has been completed and registered as a durable SASE artifact:
- **Report File:** [`ref_copy_mode_code_blocks__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/ref_copy_mode_code_blocks__gem.md)
- **Artifact Ref:** `research:202610/ref_copy_mode_code_blocks__gem.md` (`explicit:bbdaf8e5d9541b0ad2f1f025`)

---

## Executive Summary & Plan Critique

### 1. Is this a good idea?
**Yes, strongly.** Reading technical PDFs in Highlights is a great experience for prose, but extracting code blocks is notoriously broken: PDF text selection mangles line breaks, strips leading whitespace indentation, splits syntax spans, and fragments code across page boundaries. Adding code block targeting to Bob's Copy mode bridges the gap between static PDF reading and active development.

### 2. Can we read code blocks directly from the PDF?
**No. Attempting PDF text extraction for code blocks is an anti-pattern.**
When pandoc and XeLaTeX compile Markdown into PDF, code fences (````` ``` `````) and language tags (`python`, `rust`, `bash`) are completely eliminated into LaTeX `Verbatim` environments. Re-extracting code from the PDF text layer requires fragile heuristics, breaks on soft-wrapped lines, loses language identifiers, and cannot survive page breaks.

### 3. Storing the Source Markdown File
**The user's intuition to store the source Markdown file is directly confirmed and supported by existing Bob infrastructure.**
Crucially, investigation of the codebase revealed that **Bob's intake pipeline already supports `.md` companion files**:
- In `src/native/highlights_ref/doctor.rs:1094-1104` (`intake_companion_moves`), Bob automatically scans for same-stem `.md` and `.textbundle` companions in `xlib/`, moves them alongside the PDF to `lib/`, and stages them for atomic Git commits.
- When `bob ref create <file.md>` runs, it currently compiles to PDF in `xlib/` but leaves the source `.md` behind.
- **The Solution:** Update `src/native/highlights_ref/create.rs` to copy the source Markdown (or projected Markdown for vault note snapshots) to `xlib/<type>/<stem>.md`. The existing intake engine will seamlessly carry it to `lib/<type>/<stem>.md` and version-control it.

### 4. Scope Adjustments: Support Vault Note Snapshots
The original prompt suggested this might only work for Markdown files converted via `bob ref create`.
- **Adjustment:** **Vault Note Snapshots** (`bob ref create <vault_note>`) must also be first-class targets! Vault notes are native Markdown files. When snapshotted, their projected Markdown can be saved as `lib/notes/<stem>.md`, providing identical code block extraction.
- **Graceful Degradation:** For non-Markdown PDFs (e.g., scanned arXiv papers), the Copy Card provides a graceful fallback notice: *"No code blocks on this reference"*, exactly like the existing highlight picker `[H]`.
- **Future Phase 2:** Web article captures (`bob ref create <URL>`) can later preserve their reader-mode Markdown to effortlessly extend code block copying to clipped articles.

### 5. Architectural Separation of Concerns
In accordance with `decisions:mac-capture-is-a-thin-client`, **Bob Mac Capture must not parse Markdown files directly**.
- `bob-cli` remains the parsing engine: `src/native/ref_library/show.rs` parses code blocks from companion `.md` files via `pulldown-cmark` and emits structured `code_blocks` in the `ShowRow` JSON.
- `bob-mac-capture` merely decodes `[RefsShowCodeBlock]` and renders the UI.

---

## UX & Visual Design

### 1. The Main Copy Card & Keycap `[C]`
- Within `RefsCopyKey`, the **`C`** keycap is completely unallocated.
- In `RefsCopyCardView`, an entry `[C] Pick a code block…` is rendered in the content section (displaying e.g. `4 blocks · python, bash`).
- Pressing `C` (or tapping the row) transitions the card into `RefsCodePicker`.

### 2. The Code Block Picker (`RefsCodePicker`)
Modeled after the existing `RefsHighlightPicker`, the code picker provides a 9-row window:
- **Keycaps `[1]` .. `[9]`:** Directly copies that block with a single stroke.
- **Language Badge:** High-contrast, monospaced pill badge (`PYTHON`, `BASH`, `RUST`, `JSON`, `SWIFT`).
- **Section Breadcrumbs:** Displays `§ Heading Name` when the code block sits under a Markdown heading.
- **2-Line Monospaced Preview:** Renders the first 2 lines in `RefsVisualTokens` monospace font.
- **Line Count Metadata:** Displays total line count (e.g. `L1–14`).

### 3. Dual Copy Payloads
| Action | Output Format | Purpose |
| :--- | :--- | :--- |
| **`1`..`9` / `Enter`** | **Raw Code** | Clean, unescaped code ready to run in terminal or paste in editor. |
| **`⌥1`..`⌥9` / `⌥Enter`** | **Fenced Markdown** | ````python ... ```` with attribution comment (`# From: <Title>, § <Section>`). |

### 4. Highlights `<cmd+y>` Integration
Highlights is a third-party app (`net.highlightsapp.universal`), but Bob Mac Capture already implements app-scoped Carbon hotkey takeover (`HighlightsTakeover.swift`) and active tab detection via Accessibility (`AXHighlightsTabsReader.swift`):
- We add `refsHighlightsCopyKey` (default `⌘Y`) to `HighlightsTakeover`.
- When Highlights is frontmost and Bryan presses `⌘Y`:
  1. `HighlightsTakeover` intercepts the keystroke.
  2. `AXHighlightsTabsReader` extracts the active document URL (`kAXDocumentAttribute`).
  3. `RefsLibrary` resolves the document to its `RefItem`.
  4. The Refs panel appears with Copy Mode already active.
  5. Bryan presses `C` $\rightarrow$ `1`.
  6. The code is copied to the clipboard, the Refs panel automatically dismisses, and focus smoothly returns to Highlights.

---

## Phased Implementation Roadmap

1. **Phase 1 (`bob-cli`):**
   - Stage companion `.md` files in `create.rs` for Markdown targets and vault note snapshots.
   - Use `pulldown-cmark` in `show.rs` to extract fenced code blocks, language tags, line counts, and section headers into `ShowRow.code_blocks`.
2. **Phase 2 (`bob-mac-capture` - RefsCore & UI):**
   - Decode `RefsShowCodeBlock` in `RefsShowRow`.
   - Add `.codePicker` to `RefsCopyKey` on glyph `C`.
   - Implement `RefsCodePicker` state machine and `RefsCodePickerView` in SwiftUI using `RefsVisualTokens`.
3. **Phase 3 (Highlights Takeover):**
   - Add `HotKeyAction.refsHighlightsCopy` (`⌘Y`) to `HotKeyRegistry.swift` and `HighlightsTakeover.swift`.
   - Implement `showRefsWithCopyMode()` in `BobPanelCoordinator.swift` with automatic dismissal on copy.
