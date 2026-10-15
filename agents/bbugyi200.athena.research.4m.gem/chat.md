# Chat History - ace-run (research.4m.gem)

- **TIMESTAMP:** 2026-10-15 17:55:35 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4m.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_174319.md`

## Prompt

%id(gem, clan=research.4m)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4m.cdx`, `research.4m.cld`, `research.4m.grk`, `research.4m.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
would like to add much better support to the `bob ref create` command for creating
beautiful PDF files from area notes / project notes. See the
~/bob/lib/chat/sase_blog_v1.pdf file (this PDF file might not be available on this
machine, but should be available on my macbook) for an example of how these look now
(not great).

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

# Research Report: Beautiful PDF Creation from Area & Project Notes

The independent research report has been written and registered as an audited SASE artifact:

- **Absolute Report Path:**  
  [`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/ref_create_area_project_note_pdf_rendering__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/ref_create_area_project_note_pdf_rendering__gem.md)
- **Artifact Label:**  
  `research:202610/ref_create_area_project_note_pdf_rendering__gem.md` (`file:explicit:01d2a7b1413bd24c52183696`)

---

## Key Findings & Ground Truth Analysis

We inspected `~/bob/lib/chat/sase_blog_v1.pdf` and its source note `~/bob/sase_blog.md`. The current Pandoc + XeLaTeX pipeline fails on Obsidian area and project notes in five key areas:

1. **Leaking Internal Dataview Plumbing**:  
   Raw internal metadata fields (`[fresh:: 2026-10-15]`, `[created:: 2026-06-11]`, `[id:: sase_blog__prj]`, `[dependsOn:: ...]`) and block IDs (`^prj`, `^intro-proposal`, `^ref-...`) appear verbatim as distracting clutter.
2. **Broken Transclusions & Images**:  
   Obsidian image embeds such as `![[img/20260802_144938.png|400]]` and note embeds (`![[ref/...#^ref]]`) are not parsed by Pandoc; they render as raw literal strings while the image files in `~/bob/img/` are ignored.
3. **Degraded Task Checkbox Semantics**:  
   Custom GTD task states (`[/]` In Progress, `[*]` Next, `[?]` Blocked, `[-]` Cancelled) are not recognized by standard Markdown readers, degrading into literal ASCII brackets or plain bullets. `- [ ]` and `- [x]` render as unstyled unicode boxes (`□`, `⊠`).
4. **Corrupted Table of Contents**:  
   Pandoc's `--number-sections` and `--toc` treat operational task groupings (`0.1.1 Next & In Progress`, `0.1.2 Blocked`, `0.1.3 Done & Canceled`) as numbered document chapters, cluttering the outline and burying substantive sections (`Requirements`, `Outline`, `Architecture`).
5. **Dated Academic Typography**:  
   Standard LaTeX serif output (`DejaVu Serif` / Computer Modern layout) is suited for academic papers, not an executive dashboard, project brief, or tablet annotation canvas.

---

## Critique of the Plan

### Is `bob ref create` the Right Tool?

- **The Good (The Highlights Review Cycle)**:  
  Bryan's primary motivation is to review active project and area notes away from the desk on an iPad using the Highlights app and Apple Pencil. In this workflow, creating a Highlights-ready PDF with a page-1 marker annotation that syncs highlights and comments back into Obsidian (`ref/chat/sase_blog_v1.md`) is an exceptionally tight and valuable GTD review loop.
- **The Friction (Reference Semantics vs. Vault State)**:  
  1. *Category Mismatch*: `bob ref create` defaults Markdown to `ref_type: chat` (`lib/chat/`). A living project note is not a chat log.
  2. *Parent Requirement Friction*: `bob ref create` requires `-P <parent>`. Forcing Bryan to type `-P sase_blog` when converting `sase_blog.md` (or for `sase.md`, which has no parent) is redundant.
  3. *Inability to Export Without GTD Side Effects*: A user who simply wants to generate a clean PDF for sharing or printing without creating an active reading task or page-1 marker is currently forced to use the Highlights intake pipeline.

### Recommended Architectural Separation

Decouple the **Note PDF Rendering Engine** from the **Highlights Reference Intake Pipeline**:
- **Core Engine**: A Rust-based Obsidian AST preprocessor + HTML/CSS print template.
- **`bob ref create` Integration**: Auto-detects vault notes (`type: "[[project]]"` or `"[[area]]"`), delegates rendering to the new engine, automatically sets `-P` to the note itself, routes to `lib/projects/` or `lib/notes/`, and stamps the Highlights page-1 marker.
- **Standalone Command (`bob note pdf <note>`)**: A direct command that exports the note to a beautiful PDF without Highlights marker stamping, intake moves, or reading task creation.

---

## Technology Evaluation

| Engine | Visual Styling | Emoji Support | Rendering Latency | System Dependencies | Code Reuse in `bob-cli` |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Pandoc + XeLaTeX** | Poor (academic) | Fragile | Slow (8–15s) | Heavy TeX Live | Low |
| **Headless Chromium + CSS** *(Recommended)* | **Exceptional** | **Native** | **Fast (<1s)** | **Zero new deps** (Chrome already required) | **High** (reuses web-clip assets & fonts) |
| **Typst (v0.15.1)** | Very High | Good | Instant (<300ms) | New binary dependency | None |
| **WeasyPrint** | Medium | Variable | Medium (3–5s) | Python C-extensions | None |

### Why Headless Chromium is the Recommended Engine:
1. **Zero New Dependencies**: `bob-cli` already requires and verifies Google Chrome / Chromium for `bob ref create` web clipping.
2. **Existing Assets**: `bob-cli` already bundles variable fonts (`Inter`, `JetBrains Mono`, `Source Serif 4`) directly into its binary, alongside `@page` print CSS logic in `scripts/web_clip/`.
3. **Obsidian Fidelity**: Obsidian is built on Electron/Chromium. HTML5/CSS3 flexbox, CSS grid, and callouts (`> [!info]`) allow pixel-perfect replication of modern note themes.
4. **Native Emoji**: Full native support for Bob task emojis (`🧱`, `⛓️`, `🗓️`, `🛠️`, `❌`, `🎲`, `⚪`, `🔵`, `🔴`, `🟢`) with zero LaTeX font mapping issues.

---

## Recommended Solution & Preprocessing Design

Implement a 4-stage pipeline in `bob-cli`:

1. **Project Hero Card**:  
   Extract the lead `^prj` task (`- [ ] #task #prj ...`) into a full-width **Project Hero Card** at the top of Page 1 displaying the project title, status badge (`WIP`, `Active`), parent area, target outcome statement, and KPI summary counters.
2. **GTD Task Sanitation & Card Transformation**:  
   - Strip internal plumbing (`[fresh::...]`, `[created::...]`, `[id::...]`, `[dependsOn::...]`, `^block-id`, `#task`, `#prj`, `#hide`).
   - Elevate `[priority:: high]` to a red priority badge and `[scheduled:: YYYY-MM-DD]` to a calendar pill.
   - Render task checkboxes as styled status icons (`★` Next, `◐` WIP, `?` Blocked, `✓` Done, `✕` Cancelled).
   - Format `BLOCKS:` and `DEPENDS ON:` as styled dependency pills.
   - Truncate and format `SCHEDULE LOG` and `CANCEL LOG` as compact, muted audit history boxes.
3. **Vault Asset Transclusion**:  
   Resolve `![[img/...|width]]` directly against the vault (`~/bob/img/`) and transclude referenced blocks (`![[note#^block]]`).
4. **TOC & Heading Hygiene**:  
   Exclude operational task lane headings (`Next & In Progress`, `Blocked`, `Done & Canceled`) from the PDF Table of Contents so the outline reflects actual document content (`Requirements`, `Outline`, `Architecture`).

Full architectural details, data schemas, and the phased implementation plan are available in the artifact above.
