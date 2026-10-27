# Chat History - ace-run (research.23.gem)

- **TIMESTAMP:** 2026-10-18 11:35:05 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.23.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261018_112744.md`

## Prompt

%id(gem, clan=research.23)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.23.cdx`, `research.23.cld`, `research.23.grk`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Can you help me review recent changes to Obsidian (see the
https://obsidian.md/changelog/ ChangeLog) that I just got access to by upgrading
Obsidian on my macbook (I think I went from v1.12 to v.1.14?)? Think hard about what I
would actually find useful based on my setup. End your analysis with a ranked list of
new features that you think I should be aware of / consider adopting in some way. 
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

# Research Report: Obsidian v1.12 to v1.14 Upgrade Analysis

**Report Artifact:** `research:202610/obsidian_v1_12_to_v1_14_upgrade_review__gem.md`  
**File Location:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/obsidian_v1_12_to_v1_14_upgrade_review__gem.md`  
**Durable Snapshot Reference:** `file:explicit:e6852d2452cca53351071906` (`artifacts[0]`)

---

## Executive Summary & Setup Alignment

Moving from **Obsidian v1.12** (Feb/Mar 2026) to **v1.14** (v1.14.4, Oct 2026) encompasses two major release cycles (**v1.13** and **v1.14**) and an Electron runtime upgrade (Electron v43.7.5). 

Rather than cosmetic surface changes, these releases introduce significant operational improvements that directly benefit your **macOS, terminal-adjacent, Vim-centric GTD vault (`~/bob`)**:

1. **Standalone Markdown & macOS Quick Look:** Obsidian can now open individual Markdown files outside your vault and provides native **macOS Quick Look** previews directly in Finder/terminal without launching the application.
2. **Keyboard-First & Vim Image Interactions:** Complete keyboard selection and resizing for images in Live Preview, plus a dedicated Vim `:image` Ex command (`:image grow`, `:image shrink`, `:image reset`), paired with a fullscreen pan/zoom lightbox.
3. **Daily Note / Ledger Paste Deduplication:** Pasting checklist or task items onto existing bulleted lines no longer doubles the markers (fixing the `- [ ] - [ ] ` issue).
4. **Vim-Navigable, Searchable Settings Panel:** Settings now run in a separate, searchable window with full `h`/`j`/`k`/`l` keyboard navigation and safe plugin debugging modes.
5. **Search Scalability & Word-Start Ranking:** Quick Switcher prioritizes word-start matching, retains fuzzy matching past 10,000 files, and sidebar search supports path matching and negative exclusion (e.g. `-done`).
6. **Multi-Color Highlighting:** Six native highlight colors (🔴, 🟠, 🟡, 🟢, 🔵, 🟣) using standard Markdown emoji syntax (`==🔴 text==`).
7. **Bases Kanban Views:** Native card columns with collapsible groups and disk-level folder moving capabilities.

---

## Ranked List of New Features to Adopt

### 1. macOS Quick Look & External Markdown Editing (v1.14) — *High Immediate Impact*
* **Why it fits:** You manage multiple code repositories, SASE workspaces (`bob-cli`, `bob-plugins`, `bob-mac-capture`), and research reports outside `~/bob`. Previously, viewing external `.md` files required launching another editor, while macOS Finder showed unrendered plain text.
* **How to use:**
  * **Quick Look:** Select any `.md` file in macOS Finder or terminal and tap `Space` (or `qlmanage -p file.md`) for instant Obsidian-styled rendering without opening the app.
  * **External File Editing:** Run the command `"Open file from outside the vault…"` to open standalone notes with full Outline and Outgoing Links sidebar support.
* **Prerequisite:** Download the latest installer (`.dmg`) from [obsidian.md/download](https://obsidian.md/download) to register the Quick Look extension in macOS.

### 2. Vim `:image` Ex Commands & Live Preview Keyboard Sizing (v1.13) — *High Daily Ergonomics*
* **Why it fits:** You run `vimMode: true` and avoid the mouse. Previously, adjusting images in reference notes (`ref/`) or capture attachments required manually editing raw `|width` dimensions or dragging corner handles.
* **How to use:**
  * In Live Preview, navigate to an image via Vim motions (`j`/`k`). The image focuses without expanding into raw syntax.
  * Run `:image grow`, `:image shrink`, or `:image reset` in Vim command mode (supports counts like `:4image grow`).
  * Alternatively, press `+`/`-` to resize, `0` to reset, or `Tab` to edit dimension numbers.
  * Press `Space` on a focused image to open the fullscreen lightbox viewer with pan/zoom.

### 3. List Marker Paste Deduplication & Smart Formatting (v1.14) — *Friction Removal*
* **Why it fits:** When managing daily note Pomodoro sessions, pasting task lines or captured bullets over an existing `- [ ] ` line frequently created doubled `- [ ] - [ ] ` markers that required manual backspacing.
* **How to use:** Native and automatic. Pasting onto a list line cleanly overwrites the target line's marker. In addition, bold/italic toggles now smartly respect selection boundaries without syntax fragments.

### 4. Word-Start Quick Switcher & Full-Path Sidebar Filtering (v1.14) — *Vault Scaling*
* **Why it fits:** Your vault contains an extensive backlog of daily notes, project notes, and archives under `done/`.
* **How to use:**
  * **Quick Switcher (`Cmd+O`):** Type initials (e.g. `bf` for `bob_freshness` or `dr` for `daily_review`); matches where characters start words now rank at the top.
  * **Sidebar Filter:** In the File Explorer or search panels, prefixing queries with a minus (e.g. `-done` or `-ref`) hides entire folder trees and their children.

### 5. Searchable Settings Panel with Vim Navigation (v1.13) — *Configuration Efficiency*
* **Why it fits:** Eliminates mouse scrolling when configuring hotkeys or plugin parameters.
* **How to use:** Settings opens in a dedicated window with built-in search across all core settings and plugins. Navigate tabs and rows using `j`/`k`, focus search with `Ctrl+F` (or `Cmd+F`), and dismiss instantly with `Esc`.

### 6. Semantic Multi-Color Highlighting (v1.14) — *Reading Queue Synthesis*
* **Why it fits:** When reviewing reading notes in `ref/` or Highlights PDFs in `lib/`, monochromatic yellow highlights lack semantic differentiation.
* **How to use:** Type `==` to trigger the color autosuggestion palette or author directly:
  * `==🟢 Key Finding / Takeaway==`
  * `==🔴 Flaw / Critique==`
  * `==🟡 Notable Quote==`
  * `==🟣 Action Item / Follow-up==`

### 7. Bases Kanban View (v1.14) — *Optional / Non-Task Pipelines*
* **Why it fits:** Your core task scheduling and dependencies belong in `bob-cli`. However, for high-level exploratory pipelines (e.g., article drafting pipelines or reading queue staging), Bases now offers native Kanban boards where dragging cards between `file.folder` columns physically moves files on disk.

---

## Breaking Changes & Housekeeping Audit

* **`--callout-color` CSS Variable:** Changed in v1.13 from RGB triplets (`255, 0, 0`) to valid CSS color strings (`#ff0000`).
  * *Audit Result:* Checked your custom snippets in `~/bob/.obsidian/snippets/` (`dataview-properties.css`, `inline-code.css`, `task-statuses.css`). No callout color variables are modified; your snippets are completely unaffected.
* **Base Font Sizing:** Base font sizes are now stored locally per-device and no longer sync across machines via `appearance.json`, preventing zoom-level drift between your MacBook retina display and other screens.
* **Installer Refresh:** To activate the macOS Quick Look extension and update to Electron v43.7.5, download and reinstall Obsidian from [obsidian.md/download](https://obsidian.md/download).
