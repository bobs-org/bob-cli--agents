# Chat History - ace-run (research.1n.gem)

- **TIMESTAMP:** 2026-10-16 07:18:24 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.1n.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261016_070719.md`

## Prompt

%id(gem, clan=research.1n)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.1n.cdx`, `research.1n.cld`, `research.1n.grk`, `research.1n.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We
recently added support to the `bob capture` command and the corresponding
bob-mac-capture app for capture templates (see the bob-cli-7w epic bead for context).
Can you now help me add support for persisting templates to disk automatically when they
are used?

- We should then allow the user to access and modify the templates that have been saved
  in the bob-mac-capture app.
- This should work in a similar way to the capture stash.
  - We should use a new `<ctrl+t>` keymap that allows the user to view/modify saved
    templates.
  - Just like with the stash, we should pop a template when it is selected (it will just
    get re-added when the capture is submitted if the template is used).
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

# Research Findings: Capture Template Persistence & Library Design in Bob Mac Capture

**Report Artifact:** [`research:202610/capture_template_persistence_and_library_design__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/capture_template_persistence_and_library_design__gem.md)  
**Artifact ID:** `explicit:f89cdd54f5028af61ea8a28a`  
**Researcher:** `research.1n.gem` (Swarm Member)

---

## 1. Executive Summary & Critique of the Proposed Plan

Following the completion of epic [`bob-cli-7w`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/plans/202610/bulk_capture_templates.md) (`@@template:` bulk capture), you proposed adding automatic persistence for capture templates and a management library in `bob-mac-capture` modeled on the canceled draft stash (`<ctrl+s>`), featuring `<ctrl+t>` and a "pop on select" mechanic.

### Critique Verdict: Is This a Good Idea?

| Proposed Aspect | Evaluation | Critique & Risk | Recommended Adjustment |
| :--- | :--- | :--- | :--- |
| **"Pop on select"** (like the stash) | **Fatal Flaw (Critical Anti-Pattern)** | **Severe Data Loss Hazard:** Conflates an undo/shelving stash with a durable stencil library. Popping removes the template from disk. If the user hits `Esc`, dismisses the panel, cancels with `Ctrl-C`, experiences a crash, or hits a validation error, **the template is permanently erased**. Furthermore, modifying a template requires executing a capture batch, forcing dummy tasks into the live vault. | **Non-Destructive Apply:** Selecting a template loads it into the editor; the template remains securely in the store on disk. |
| **Persist upon use** | **Strong Concept** | If the entire raw draft is saved, transient data rows (past job URLs, names) pollute the template, requiring manual deletion upon every reuse and creating duplicate-capture hazards. | **Skeleton-Only Persistence:** Save only Zone A (`@@template:` + pattern block + children). Automatically strip data rows. |
| **`<ctrl+t>` Keymap** | **Excellent Ergonomics** | KeyCode 17 is completely unmapped in `CaptureKeyCommandRouter`. However, `@@template:` grammar strictly requires placement on line 1 of a draft. | Guard with `plainDraft.isEmpty` (identical to `<ctrl+s>`) to prevent clobbering active draft text. |
| **Access & Modify** | **Essential** | Stash only supports "Delete All" (`Shift-D`). A template library needs individual item retirement and in-place editing. | Provide **Single-Item Deletion (`d`)** and a dedicated **Template Edit Mode (`e`)** that saves without capturing. |

---

## 2. Recommended Solution & Design

### 2.1 The Template Lifecycle

```
  ┌───────────────────────────┐
  │  Capture Editor (Empty)   │
  └─────────────┬─────────────┘
                │  Press <ctrl+t>
                ▼
  ┌────────────────────────────────────────────────────────────────────────┐
  │  Template Picker HUD (<ctrl+t>)                                        │
  │  - Slot-colored placeholders ({0}, {1} in orange, teal, pink, ...)     │
  │  - Route badges (@job), field counts, and usage stats                  │
  ├────────────────────────────────────────────────────────────────────────┤
  │  [Return] / [1-9] Apply (Non-destructive)                              │
  │  [d] / [⌫] Delete Template from Store                                  │
  │  [e] / [⌃E] Enter Template Edit Mode                                   │
  └─────────────┬───────────────────────────────────────┬──────────────────┘
                │ [Return] Apply                        │ [e] Edit Mode
                ▼                                       ▼
  ┌───────────────────────────┐           ┌──────────────────────────────┐
  │  Editor Populated         │           │  Template Edit Mode          │
  │  - Header & pattern set   │           │  - Dedicated in-panel editor │
  │  - Cursor on row line     │           │  - [Return] saves to disk    │
  │  - Template STAYS in disk │           │  - ZERO vault pollution      │
  └─────────────┬─────────────┘           └──────────────────────────────┘
                │ Type rows & Return
                ▼
  ┌───────────────────────────┐
  │  Capture Executed         │
  │  - De-duplicates skeleton │
  │  - Increments useCount    │
  │  - Updates lastUsedAt     │
  └───────────────────────────┘
```

### 2.2 Beautiful & Intuitive Visual Design
1. **Live Slot Hues in Picker:** Placeholders `{0}`, `{1}`, `{2}` in the template picker HUD are styled using the exact 6-hue palette from `CaptureEditorPalette` (`field % 6`: Orange, Teal, Pink, Green, Purple, Brown), establishing instant visual coherence with the capture editor.
2. **Metadata Capsule Pills:** Each entry displays the target route pill (e.g. `@job`), field count pill (`3 fields: {0}..{2}`), and usage frequency (`Used 14x · 2h ago`).
3. **Footer Integration:** Added next to the Stash button in `CapturePanelView.swift`:  
   `Button { model.toggleTemplatePicker() } label: { Label("Templates \(count)", systemImage: "square.stack.3d.down.right") }`

### 2.3 Architecture & Data Storage
Following `decisions:mac-capture-is-a-thin-client` and `FileCanceledDraftStashStore` precedents:
- **Location:** `~/Library/Application Support/org.bobs.bob-mac-capture/capture-templates.json`
- **Security:** POSIX permissions `0o600` for file, `0o700` for parent directory.
- **Reliability:** Atomic file writes (`[.atomic]`), automatic quarantine of corrupt files (`capture-templates.corrupt.json`), and schema versioning (`schema_version: 1`).

---

## 3. Recommended Implementation Phases

1. **Phase 1: Persistence Core & Store (`CaptureCore`)**
   - Create `PersistedCaptureTemplate`, `CaptureTemplateFile`, and `FileCaptureTemplateStore`.
   - Implement MRU sorting, de-duplication, atomic writes, and corrupt file quarantine with unit tests.
2. **Phase 2: Automatic Skeleton Persistence (`CapturePanelModel`)**
   - Add deterministic Zone A skeleton extractor (extracting `@@template:`, pattern lines, child bullets, and trailing separator; stripping transient data rows).
   - Hook into `completeSubmit` to record template use upon verified capture success.
3. **Phase 3: Template Picker UI (`<ctrl+t>`)**
   - Route `KeyCode.t` (17) + Control in `CaptureKeyCommandRouter`.
   - Implement floating material `TemplatePickerView` with slot hues and 1-keystroke accelerators (`1`..`9`, `A`..`Z`).
   - Implement non-destructive Apply and empty-draft gating.
4. **Phase 4: Management & Template Edit Mode**
   - Implement single-entry deletion (`d` / `Backspace`) and `Shift-D` ("Clear All").
   - Implement dedicated in-panel **Template Edit Mode** (`e` / `Ctrl-E`) to update templates without capturing dummy vault tasks.

---

## 4. Audit & Verification Trail

- **Report Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/capture_template_persistence_and_library_design__gem.md`
- **Durable Snapshot:** Created via `sase artifact create` under label `research:202610/capture_template_persistence_and_library_design__gem.md`.
- **Final Declaration:** Submitted and accepted via `sase final submit -` with conventional commit message `docs(research): add capture template persistence research`.
