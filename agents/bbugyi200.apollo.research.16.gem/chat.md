# Chat History - ace-run (research.16.gem)

- **TIMESTAMP:** 2026-10-14 07:52:57 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.16.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261014_074319.md`

## Prompt

%id(gem, clan=research.16)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.16.cdx`, `research.16.cld`, `research.16.grk`, `research.16.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
want to add a new `<ctrl+y>` keymap to the bob-mac-capture app's ref panel.

- This keymap should open a new menu that allows the user to select (with a single
  keypress) what they want to copy to their clipboard.
- Be creative about what options we put in this menu (e.g. the marker notes ID value,
  one of the notes/highlights, etc..). Think hard about what properties of a reference
  note / PDF file a user might want to copy to their clipboard.
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

# Research Report Summary: `<ctrl+y>` Clipboard Copy Palette for Bob Refs

**Author:** Researcher `gem` (`research.16.gem`)  
**Report File:** [`ref_panel_ctrl_y_copy_menu__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/ref_panel_ctrl_y_copy_menu__gem.md)  
**Registered Artifact:** `research:202610/ref_panel_ctrl_y_copy_menu__gem.md` (`file:explicit:3cc15fbf235ca690ff024f67`)

---

## 1. Critique of the Plan

### Is `<ctrl+y>` a Good Idea?
**Yes, with one key refinement.**
- **Why it fits:** In Vim, kakoune, tmux, and modern CLI environments, `y` stands universally for "yank" (copy). Furthermore, within Bob Refs' [`RefsKeyRouter.swift`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/Refs/RefsKeyRouter.swift), modifier roles are strictly partitioned: `⌘` handles system/window dispatch (`⌘↵`, `⌘K`, `⌘R`, `⌘S`, `⌘1–5`), while `⌃` (Control) is reserved for non-destructive in-panel inspection and navigation (`⌃P`/`⌃N`/`⌃J`/`⌃K` row movement, `⌃D`/`⌃U` half-page note scrolling, `⌃[` cancel). Assigning in-panel clipboard extraction to `⌃Y` matches this architectural convention.
- **The Cocoa conflict analyzed:** In standard Cocoa `NSTextField` controls, `Ctrl+Y` is bound to `yank:` (paste from kill ring). However, `RefsKeyRouter` has *already* overridden Cocoa text-editing defaults (`Ctrl+D` delete forward, `Ctrl+K` kill line, `Ctrl+U` kill line backward) in favor of panel navigation. Repurposing `Ctrl+Y` continues that deliberate design choice.
- **The adjustment:** Standard Mac users expect `⌘C`. We recommend that `⌘C` (when the search query has no text selected) acts as a direct alias to copy the default **Wiki Link** with a toast, while `⌃Y` invokes the full **Yank Palette**.

### Architecture: Native AppKit `NSMenu` vs. SwiftUI Glass HUD
**Do NOT build this as an AppKit `NSMenu`.**
- AppKit menus pause the event loop, cannot cleanly handle single unadorned letters (`w`, `m`, `p`) as immediate action triggers (macOS treats un-modified letters in `NSMenu` as type-ahead prefix search), and clash with Bob Mac Capture’s custom SwiftUI materials.
- **The Better Approach:** Implement a dedicated **SwiftUI Glass HUD ("Yank Palette")** overlay (analogous to [`CapturePullInChoiceCard`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePullInChoiceView.swift)). It renders inside the panel’s coordinate space on `.regularMaterial` with corner radius `12pt`, displays keycap badges with live previews of the exact text, and evaluates single keystrokes instantly.

---

## 2. Creative Copy Options Catalog

The research identified four distinct categories of reference properties:

```
┌────────────────────────────────────────────────────────────────────────┐
│  YANK TO CLIPBOARD                                      [esc] Cancel   │
├────────────────────────────────────────────────────────────────────────┤
│  [ W ]  Wiki Link              [[20261014_ref_panel|Bob Refs Panel]]   │
│  [ M ]  Marker ID              ref_panel_quick_open                    │
│  [ T ]  Reading Task           - [ ] [[20261014_ref_panel]] #task #ref │
│  [ P ]  PDF Path (Absolute)    ~/bob/lib/chat/20261014_ref_panel.pdf   │
│  [ R ]  PDF Path (Relative)    lib/chat/20261014_ref_panel.pdf         │
│  [ N ]  Note Path              ref/chat/20261014_ref_panel.md          │
│  [ U ]  Source URL             https://arxiv.org/abs/2610.12345        │
│  [ S ]  Summary / Abstract     "Examines the feasibility of adding..." │
│  [ Q ]  Latest Highlight Quote "The panel must open in under 50ms..."  │
│  [ K ]  Latest User Note       "Key design insight for the HUD..."     │
│  [ C ]  Citation (Markdown)    Bryan (2026). Bob Refs Panel.           │
│  [ B ]  BibTeX Entry           @article{bryan2026refs, ...}            │
└────────────────────────────────────────────────────────────────────────┘
```

1. **Vault & Knowledge Graph Links:**
   - **`[ W ]` Wiki Link (Aliased):** `[[ref/chat/stem.md|Title]]` — standard Obsidian linking.
   - **`[ M ]` Marker Note ID:** The semantic identifier from the PDF marker note (`FIELD_ID`) and frontmatter `id:`, crucial for capture syntax and `bob ref find <id>`.
   - **`[ T ]` Reading Task:** `- [ ] [[ref/chat/stem.md]] #task #ref` — instant task row for Area/Project notes.
   - **`[ O ]` Obsidian URI:** `obsidian://open?vault=bob&file=...` — deep links for external apps (Slack, Calendar).
2. **File Paths (System & Shell):**
   - **`[ P ]` Absolute PDF Path:** `/Users/bryan/bob/lib/...` — for terminal scripting, pandoc, CLI tools.
   - **`[ R ]` Relative PDF Path:** `lib/...` — standard vault-relative reference.
   - **`[ N ]` Relative Note Path:** `ref/...` — path for `bob ref show` and git.
3. **Web & Research Metadata:**
   - **`[ U ]` Source URL:** Original web/arXiv URL *(rendered conditionally when `urls` is non-empty)*.
   - **`[ D ]` DOI / arXiv ID:** Clean identifier string *(rendered conditionally)*.
   - **`[ C ]` Citation:** Formatted academic/Markdown citation (`Author (Year). Title. URL`).
   - **`[ B ]` BibTeX:** Standard BibTeX entry for LaTeX/Overleaf writing.
4. **Content Excerpts & Annotations:**
   - **`[ S ]` Summary / Abstract:** Extracted bottom-line bullet points or abstract text.
   - **`[ Q ]` Latest Highlight Quote:** The most recent quote highlighted in Highlights.
   - **`[ K ]` Latest User Comment:** The user's personal note on the highlight.
   - **`[ A ]` All Highlights as Markdown:** Formatted Markdown block of all highlights ready for embedding.

---

## 3. Recommended Technical Solution & Adjustments

### 3.1 Backend Requirement (`bob-cli`)
In [`src/native/ref_library/row.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/ref_library/row.rs#L47-L49), `RefRow.id` is currently annotated with `#[serde(skip_serializing)]`.
- **Change:** Un-suppress serialization using `#[serde(skip_serializing_if = "Option::is_none")]`.
- **Impact:** An additive change that exposes the marker/frontmatter ID to `bob ref list` and `bob ref show` JSON without breaking existing decoders.

### 3.2 Frontend Architecture (`bob-mac-capture`)
1. **Model:** In [`RefsCore/RefsDecoding.swift`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-mac-capture/Sources/RefsCore/RefsDecoding.swift) and [`RefsModel.swift`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-mac-capture/Sources/RefsCore/RefsModel.swift), decode `markerID` into `RefItem`.
2. **Router:** In [`RefsKeyRouter.swift`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/Refs/RefsKeyRouter.swift), map `KeyCode.y = 16` with `.control` to `.showCopyMenu`.
3. **State Machine:** When `isCopyMenuPresented` is active, printable keys are intercepted before the search field. A matching single key:
   - Writes the formatted string to `NSPasteboard.general`.
   - Posts VoiceOver announcement.
   - Dismisses the palette.
   - Fires a 1.5s footer toast confirmation (`Copied Marker ID`).
4. **Dual Interaction Mode:** Single-character keys provide instant muscle-memory execution, while arrow keys (`↑`/`↓`) and `Return` provide discoverability.
5. **Dismissal:** `Escape`, `⌃[`, or pressing `⌃Y` a second time cleanly dismisses the palette.

---

## 4. Verification & Artifact Registration

- **Research Document:** Written to `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/ref_panel_ctrl_y_copy_menu__gem.md`.
- **Audited Artifact Snapshot:** Created via `sase artifact create`:
  ```
  id: explicit:3cc15fbf235ca690ff024f67
  ref: file:explicit:3cc15fbf235ca690ff024f67
  label: research:202610/ref_panel_ctrl_y_copy_menu__gem.md
  ```
- **Finalizer Declaration:** Submitted and accepted for `sdd:research` repository.
