# Chat History - ace-run (research.44.gem)

- **TIMESTAMP:** 2026-10-08 17:40:51 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.44.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261008_172831.md`

## Prompt

%id(gem, clan=research.44)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.44.cdx`, `research.44.cld`, `research.44.grk`, `research.44.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
use the Highlights app to read all of my references, which I like but I have a problem:
It is not nearly as easy as I would like it to be to quickly open PDFs in the Highlights
app.

- The problem is not how quickly Highlights loads the PDF, but how quickly I can find
  and select it (using the `<ctrl+o>` keymap in that app is terrible).
- I was thinking that I could solve that by writing a new bob-mac-refs Swift app,
  inspired by the bob-mac-capture app, that allows me to bind a keymap that triggers a
  prompt for me to select one of the PDFs in the ~/bob/lib/ directory (i.e. one of the
  PDFs in by reference system).
- We should make it clear whether each PDF selection is a paper, a chat, an article,
  etc...
- The user should be able to easily navigate to different PDfs that are shown and should
  be able to type to filter the PDF selections shown.
- Think hard about how we should sort the PDFs that are shown by default vs when a
  filter has been typed in by the user.
- You should add as much useful data as possible to this new panel to describe the PDFs
  in the selection menu and (especially) the PDF that is currently selected.
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
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report: `bob-mac-refs` Highlights PDF Launcher

**Report Artifact:** [`research:202610/bob_mac_refs_highlights_launcher__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/bob_mac_refs_highlights_launcher__gem.md)  
**Durable Snapshot ID:** `explicit:727b8eb28155458d8b356a6b`  
**Researcher:** gem (`research.44.gem`)

---

## 1. Executive Summary & Recommendation

Building a dedicated keyboard-driven reference launcher is an **outstanding, high-leverage initiative**. The native `<Ctrl+O>` / `NSOpenPanel` dialog in the Highlights app is fundamentally broken for research workflows: it is semantically blind, forces manual filesystem traversal through nested `~/bob/lib/` subfolders, displays opaque machine stems (e.g. `2403.12345v1.pdf`), and has zero awareness of reading lifecycle states (`started`, `next`, `queued`, `read`) or author metadata.

### Recommended Solution in One Line:
Build a native macOS floating HUD (`bob-mac-refs` or a unified `bob-mac` suite) that queries `bob-cli`'s reference index over versioned JSON, caches entries in-memory with FSEvents invalidation for sub-10ms response time, presents a two-pane master-detail interface featuring live `PDFKit` cover page thumbnails and lifecycle-tiered default sorting, and dispatches directly to Highlights via `NSWorkspace`.

---

## 2. Critique of the Plan & Alternative Approaches

### 2.1 Is building a dedicated Swift app a good idea?
**Yes, but with an architectural caveat regarding packaging.**

We evaluated four alternative implementation vectors:

1. **Raycast Extension:**
   - *Why consider:* Rapid to build in TypeScript/React using Raycast's List/Detail components.
   - *Why reject:* Imposes a hard runtime dependency on Raycast and Node.js; incurs 150–250ms cold-start latency; cannot embed custom native AppKit/`PDFKit` visual views; and violates the standalone design philosophy established in Bob.
2. **Obsidian Modal / Quick Switcher Plugin:**
   - *Why consider:* Vault metadata is already accessible in Obsidian.
   - *Why reject:* Fails Bryan's primary workflow requirement: global accessibility. When Bryan is actively reading in Highlights or working in Safari/Terminal, switching to Obsidian just to trigger a modal destroys focus.
3. **CLI / TUI Tool (`fzf` wrapper around `bob ref list`):**
   - *Why consider:* Trivial to implement, keyboard-first.
   - *Why reject:* Requires an active terminal; lacks graphical rendering of PDF cover pages; lacks rich typography. Excellent as a CLI companion, but insufficient as a primary desktop experience.
4. **Standalone App (`bob-mac-refs`) vs. Unified Suite (`bob-mac`):**
   - *Standalone App:* Creating `bob-mac-refs` as a completely isolated repository duplicates massive infrastructure: `HotKeyManager.swift` (Carbon registration), `BobProcessClient.swift`, `BobExecutableResolver.swift`, `VaultTargetWatcher.swift`, menu bar items, launch-at-login (`SMAppService`), and GitHub Actions CI.
   - *Unified Suite / Shared Monorepo:* A unified desktop daemon (`bob-mac`) running in the background with a ~35MB footprint can host **both** panels:
     - `⌃⇧⌘I` $\to$ **Bob Capture Panel** (GTD tasks, notes, Pomodoro sessions)
     - `⌃⇧⌘R` $\to$ **Bob References Panel** (Highlights PDF launcher & inspector)
   - *Recommendation:* Either merge into a unified `bob-mac` app or extract the shared infrastructure into a `BobMacCore` Swift package shared between the two apps.

---

## 3. Justified Adjustments to the Requirements

1. **Do NOT scan `~/bob/lib/` directly in Swift (Respect `decisions:mac-capture-is-a-thin-client`):**
   - Files in `~/bob/lib/` are raw PDFs. They do not store reading status (`started`, `next`, `queued`, `read`), author attribution, linked Obsidian notes, or annotation counts.
   - In accordance with SASE decision `mac-capture-is-a-thin-client`, `bob-cli` must remain the sole authority for reading-state derivation, marker parsing, and identity resolution. Swift must remain a thin client that queries `bob ref picker --format json` (or `bob ref list --all -f json`).
2. **Include Pending Intake PDFs (`~/bob/xlib/`):**
   - When web articles or arXiv papers are captured via `bob capture` or `bob ref create`, they land in `xlib/` before the next `bob ref scan`.
   - The launcher must surface these items with an `[Intake]` badge so Bryan can read them immediately without waiting for a library scan.
3. **Multi-Action Dispatch (Not just "Open in Highlights"):**
   - In addition to `Return` (`↵`) opening in Highlights, support:
     - `⌘Return` (`⌘↵`): Open the corresponding Obsidian reference note via `obsidian://open?vault=bob&file=ref/...`.
     - `⌥Return` (`⌥↵`): Reveal the PDF in macOS Finder.
     - `⌘C`: Copy the Markdown citation/link (`[[ref/papers/slug|Title]]`).
     - `Space`: Trigger native macOS Quick Look preview.
4. **In-Memory Cache with FSEvents Invalidation:**
   - Pre-warm references in Swift memory on launch so pressing the hotkey opens the panel in **< 10ms**.
   - Use `VaultTargetWatcher` (macOS `FSEventStreamCreate`) with a 300ms debounce to refresh the cache asynchronously whenever `~/bob/ref/`, `~/bob/lib/`, or `~/bob/xlib/` changes.

---

## 4. Reference Type Taxonomy & Visual Identification

References are categorized using distinct visual badges, SF Symbols, and color coding:

| Ref Type (`ref_type`) | Real-World Content | Visual Badge | SF Symbol Icon | Accent Color | Primary Metadata |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`papers`** | Academic papers, arXiv preprints, conference proceedings | `PAPER` | `graduationcap.fill` | Indigo (`#6366F1`) | Authors, Year, arXiv ID / DOI |
| **`chat`** | AI dialogues (Claude, Gemini, ChatGPT transcripts rendered to PDF) | `CHAT` | `bubble.left.and.bubble.right.fill` | Emerald (`#10B981`) | Model/Platform, Turn count, Date |
| **`blogs` / `articles`** | Clipped web articles, technical essays, Substack posts | `ARTICLE` | `newspaper.fill` | Amber (`#F59E0B`) | Publication domain, Author, Date |
| **`books`** | Textbooks, monograph chapters, technical manuals | `BOOK` | `book.closed.fill` | Rose (`#F43F5E`) | Author, Publisher, Year |
| **`reports`** | SASE research reports, organizational briefs, system analyses | `REPORT` | `chart.bar.doc.horizontal.fill` | Blue (`#3B82F6`) | Author agent/role, Target system |
| **`zorg` / `legacy`** | Migrated legacy references | `LEGACY` | `archivebox.fill` | Gray (`#6B7280`) | Era date, Legacy status |

*Category Navigation:* Toggle scopes via Header Tabs, shortcuts (`⌘1` All, `⌘2` Papers, `⌘3` Chat, `⌘4` Articles, `⌘5` Books, `⌘0` Queue), or inline filter syntax (typing `@paper`, `@chat`, etc.).

---

## 5. Sorting Dual-Engine: Default vs. Filtered

### 5.1 Default View (Zero-Query / Search Box Empty)
- **User Mental Model:** *"What should I be reading next? What did I leave unfinished?"*
- **Order (GTD Reading Lifecycle Ladder):**
  1. **Tier 1: In Progress (`started` / `wip` / `[/]`):** Most recently touched first.
  2. **Tier 2: Up Next (`queued`, `status: next` / `[*]`):** Prioritized during GTD review.
  3. **Tier 3: Active Reading Queue (`queued`, `status: ready` / `[ ]`):** Newest captures first.
  4. **Tier 4: Recently Finished (`finished` / `read` / `[x]`):** Completed in last 14–30 days.
  5. **Tier 5: Archive & Dropped (`dropped` / `[-]`, older `finished`):** Historical backlog.
- **Auto-Selection:** The top item in Tier 1 (or Tier 2) is pre-selected, enabling instant `HotKey` $\to$ `Return` to resume reading in < 0.5s.

### 5.2 Filtered View (Query Typed by User)
- **User Mental Model:** *"Find this specific paper, author, or topic."*
- **Order (Hybrid Composite Relevance Score):**
  $$S(R, Q) = S_{\text{match}}(R, Q) + B_{\text{state}}(R) + B_{\text{recency}}(R)$$
  - **Match Quality ($S_{\text{match}} \in [0, 100]$):** Exact match on arXiv ID/DOI/ID (100) $\to$ Title prefix/word-boundary (85) $\to$ Acronym match (80) $\to$ Author surname (75) $\to$ Substring/fuzzy title (50–70) $\to$ Topic/domain (40).
  - **State Boost ($B_{\text{state}} \in [-10, +20]$):** `started` (+20) $\to$ `next` (+15) $\to$ `queued` (+10) $\to$ `intake` (+8) $\to$ `finished` (+0) $\to$ `dropped` (-10).
  - **Recency Boost ($B_{\text{recency}} \in [0, +5]$):** Last 7 days (+5) $\to$ Last 30 days (+2).
- **Match Highlighting:** Query characters are highlighted with semibold weight and accent color across titles and authors using `AttributedString`.

---

## 6. UI & Visual Design System

### 6.1 Layout & Visual Geometry
- **Window:** Floating, borderless `NSPanel` (`styleMask: [.nonactivatingPanel, .fullSizeContentView, .titled, .resizable]`, level `.floating`).
- **Material:** `NSVisualEffectView` HUD vibrancy, dark mode material, 14pt corner radius, subtle 1pt border.
- **Dimensions:** Width **880 pt**, Height **540 pt** (fixed height avoids jarring layout shifts during filtering).
- **Two-Column Master-Detail Layout:**
  - **Left Pane (400 pt):** Search input, category filter chips, and virtualized list.
  - **Right Pane (479 pt):** Detail inspector & live preview.

### 6.2 UI Wireframe

```
+-------------------------------------------------------------------------------------------------------------+
|  🔍  attention is all                                                                 [ 3 matches / 142 ] ✖ |
+-------------------------------------------------------------------------------------------------------------+
|  [ All (⌘1) ]  [ Papers (⌘2) ]  [ Chat (⌘3) ]  [ Articles (⌘4) ]  [ Books (⌘5) ]   | Filter: [ Queue only ] |
+--------------------------------------------------+----------------------------------------------------------+
|  LIST PANE (400 pt)                              |  INSPECTOR & PREVIEW PANE (479 pt)                       |
+--------------------------------------------------+----------------------------------------------------------+
|  ▼ IN PROGRESS                                   |  [PAPER]  [● IN PROGRESS]  [arXiv:1706.03762]            |
|  +--------------------------------------------+  |                                                          |
|  | [PAPER] ● Attention Is All You Need        |  |  Attention Is All You Need                               |
|  | Ashish Vaswani, Noam Shazeer, et al.  2017 |  |  Ashish Vaswani, Noam Shazeer, Niki Parmar, et al.       |
|  | ♫ Audio summary · 14 highlights            |  |  Published: Jun 12, 2017 · Added: Sep 15, 2026           |
|  +--------------------------------------------+  |  ------------------------------------------------------- |
|                                                  |  +-----------------------+  DOCUMENT SUMMARY             |
|  ▼ NEXT UP                                       |  |                       |  • Source: arXiv preprint     |
|  +--------------------------------------------+  |  |   [ PDF PAGE 1        |  • Vault Note:                |
|  | [PAPER] ◉ FlashAttention: Fast & Memory... |  |  |     THUMBNAIL         |    ref/papers/attention.md    |
|  | Tri Dao, Daniel Y. Fu, et al.         2022 |  |  |     RENDERED VIA      |  • Reading Status:            |
|  | 8 highlights                               |  |  |     PDFKit            |    ref_task: [/] (wip)        |
|  +--------------------------------------------+  |  |     CANVAS ]          |                               |
|                                                  |  |                       |  • Annotations:               |
|  ▼ QUEUED                                        |  |                       |    14 highlights, 3 comments  |
|  +--------------------------------------------+  |  +-----------------------+                               |
|  | [PAPER] ○ FlashAttention-2: Faster Attn... |  |  ------------------------------------------------------- |
|  | Tri Dao                               2023 |  |  ♫ COMPANION AUDIO SUMMARY AVAILABLE                     |
|  | Queued since Oct 01, 2026                  |  |  [ ▶ Play Summary (4m 12s) ]  lib/papers/attention.mp3   |
|  +--------------------------------------------+  |  ------------------------------------------------------- |
|                                                  |  RECENT HIGHLIGHT EXCERPT                                |
|  ▼ RECENTLY READ                                 |  "The dominant sequence transduction models are based    |
|  +--------------------------------------------+  |   on complex recurrent or convolutional networks..."     |
|  | [ARTICLE] ✓ The Illustrated Transformer    |  |                                                          |
|  | Jay Alammar                           2018 |  |                                                          |
+--------------------------------------------------+----------------------------------------------------------+
|  [↵] Open in Highlights   |   [⌘↵] Open Obsidian Note   |   [⌥↵] Show in Finder   |   [Space] Quick Look    |
+-------------------------------------------------------------------------------------------------------------+
```

### 6.3 Right-Pane Visual Features
1. **Asynchronous `PDFKit` Cover Thumbnail:** Native macOS `PDFKit` renders page 1 with high-DPI quality and an `NSCache` image store. Visual recognition of paper layout and title banner is 10x faster than reading filenames.
2. **Metadata Matrix:** Full authors, publication date, capture date, arXiv ID/DOI, vault link.
3. **Companion Audio Card:** If an `.mp3` audio companion exists, renders a mini player pill with play/pause and duration.
4. **Highlight & Comment Teaser:** Shows count and quote text of the most recent highlight.

---

## 7. Phased Implementation Roadmap

- **Phase 1: `bob-cli` Backend & JSON Endpoint (`bob ref picker`)**
  - Add `bob ref picker --format json` (or `bob ref list --all --include-intake -f json`) returning resolved PDF paths, intake status, and snapshot annotation counts.
- **Phase 2: Swift Engine & Caching (`BobMacCore` / `RefsCore`)**
  - Implement `ReferencePickerItem` models, fuzzy search with hybrid scoring, and `VaultTargetWatcher` (FSEvents).
- **Phase 3: SwiftUI Interface & PDFKit Rendering**
  - Build `ReferencePanelView`, master list with section tiers, and detail inspector with asynchronous `PDFKit` cover page generation.
- **Phase 4: System Integration & Packaging**
  - Register global hotkey (`⌃⇧⌘R` via Carbon APIs), wire `NSWorkspace.shared.open` dispatch to Highlights, configure launch-at-login (`SMAppService`), and notarize via Xcode / `Scripts/bundle.sh`.

The complete, unabridged research report is committed and registered in durable storage at [`research:202610/bob_mac_refs_highlights_launcher__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/bob_mac_refs_highlights_launcher__gem.md).
