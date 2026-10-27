# Chat History - ace-run (research.28.gem)

- **TIMESTAMP:** 2026-10-21 07:39:34 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.28.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261021_072819.md`

## Prompt

%id(gem, clan=research.28)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.28.cdx`, `research.28.cld`, `research.28.grk`, `research.28.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start rendering nice appropriate icons in-place of `#gtd #pre` and
`#gtd #post` (i.e. the tags that specify which Obsidian tasks belong to our PRE and POST
GTD morning review groups, respectively).

- I would also like to start doing something about the `repeat` task property to make it
  look nicer and take up less space when rendered in Obsidian, but I'm not sure what (if
  anything) we should do for this one.
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

# Research Report: GTD Review Group Icons & Compact Repeat Marks Design

**Report Artifact:** [`research:202610/gtd_review_icons_and_compact_repeat_marks__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202610/gtd_review_icons_and_compact_repeat_marks__gem.md)  
**Artifact ID:** `explicit:d4c4ddfcb0ee7114b4e6c018`  
**Researcher:** `research.28.gem` (Gemini)

---

## 1. Executive Summary & Visual Progression

This research investigated the visual design, UX ergonomics, and technical architecture for rendering dedicated icons in place of `#gtd #pre` / `#gtd #post` tags, and transforming bulky `[repeat:: ...]` inline properties into compact, intuitive marks within Obsidian.

```text
RAW MARKDOWN (Storage):
- [?] #task #gtd #pre Brush teeth  [repeat:: every day when done]  [created:: 2026-10-21]  [scheduled:: 2026-10-22]

CURRENT OBSIDIAN RENDERING:
- [?] ⌗ [#gtd] [#pre] Brush teeth  REPEAT│every day when done  + Oct 21  ⧗ tomorrow
(Visual width: ~85 characters; tags and Dataview pill dominate the line)

RECOMMENDED RENDERING:
- [?] ⌗ 🌅 Brush teeth  🔁 daily  + Oct 21  ⧗ tomorrow
(Visual width: ~48 characters; 44% width reduction; description elevated to primary focus)
```

---

## 2. Critique of the Plan & Required Adjustments

### Is this a good idea?
**Yes, it is exceptionally high-value.** The GTD morning review in [`gtd_daily.md`](file:///home/bryan/bob/gtd_daily.md) is an everyday ritual. Currently, active checklist chores suffer from heavy visual clutter:
1. `#gtd` and `#pre` / `#post` appear as bright accent-colored (violet) tag pills right at the start of tasks, pushing task descriptions to the right.
2. `[repeat:: every day when done]` takes 30 physical characters and renders as a massive two-tone Dataview pill (`REPEAT | every day when done`), often 3× wider than the task description itself.
3. Because `#task` (`⌗`), priorities (`▮▮`), and dates (`+ Oct 21  ⧗ tomorrow`) are already decorated, these two properties are the **final remaining visual bottlenecks** on Bob task lines.

### Critical Adjustments to the Requirements:
1. **Single-Slot Replacement for Tag Pairs (Do NOT render two separate icons):**
   * *Adjustment:* Collapse `#gtd #pre` into a single compound **PRE glyph**, and `#gtd #post` into a single **POST glyph**.
   * *Rationale:* Replacing `#gtd` with a gear/checklist icon and `#pre` with a sun icon would cause icon clutter (`⌗ ⚙️ 🌅 Brush teeth`). Treating `#gtd #pre` as a single semantic identity mirrors the proven [`#task #ref` → `📖`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/task-tag-marks.md#L223-L250) precedent in [`docs/task-tag-marks.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/task-tag-marks.md).
2. **Icon + Compact Cadence Label for Repeat (Do NOT make it icon-only):**
   * *Adjustment:* Pair a recurring loop icon (`🔁`) with a humanized terse cadence string (`daily`, `Mon`, `30d`, `monthly · 1st`).
   * *Rationale:* A pure icon-only approach (`🔁`) obscures whether a task recurs daily, weekly, or monthly without hovering. Adopting the [`docs/date-marks.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/date-marks.md) pattern (`hourglass` + `tomorrow`) preserves instant operational awareness while still eliminating ~77% of the horizontal footprint.
3. **Strict Display-Only Architectural Boundary (Zero Storage Mutation):**
   * *Adjustment:* Markdown files must never be modified by the renderer. All decorations are rendered in memory via CodeMirror 6 ViewPlugins (Live Preview) and Markdown Post-Processors (Reading View).
   * *Rationale:* [`bob-cli`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18) (Rust), Pomodoro ledger parsers, Bob Mac Capture, and Dataview DQL rely strictly on exact `#gtd #pre` tokens and Dataview bracket syntax.
4. **Frictionless Cursor Reveal & Reversibility:**
   * Touching the mark with the cursor or clicking it immediately unfolds the underlying raw markdown for editing, preventing caret entrapment. A session toggle command (`Toggle GTD review marks` / `Toggle repeat marks`) allows instant restoration of native pills.

---

## 3. Recommended Design Specifications

### 3.1 GTD Review Group Icons

| Review Tier | Semantic Metaphor | Lucide Glyph | Ink & Tone | Hover Tooltip |
| :--- | :--- | :--- | :--- | :--- |
| **PRE** | Morning opening ritual, prelude chores, startup commitments | **`sunrise`** (🌅)<br>Horizon line + rising half-sun + 3 radial morning rays | **Dawn Amber / Gold**<br>`--bob-gtd-pre-hue`<br>(60% orange, 40% yellow mix) | `GTD PRE · morning review opening checklist`<br>`Ctrl+Enter to complete` |
| **POST** | Review conclusion, commitments verification, weekly prune milestone | **`flag`** (🚩)<br>Slender staff + flying pennant milestone flag | **Milestone Violet**<br>`--bob-gtd-post-hue`<br>(75% purple mix) | `GTD POST · morning review closing checklist`<br>`Ctrl+Enter to complete` |

* **Completed / Cancelled Tasks:** On lines with `[data-task="x"]` or `[data-task="-"]`, the inks rest faint (blended 40% toward `--text-faint` at 0.75 opacity), perfectly matching `task-tag-marks` and `date-marks`.

### 3.2 Repeat Cadence Grammar

* **Glyph:** 16×16 stroked geometric dual cycle arrows (`🔁`), defined once as an SVG CSS mask.
* **Ink:** Interface monochrome (`var(--text-muted)` at 0.85 opacity), matching Date Marks.
* **Grammar Normalization:**

| Stored Markdown Spec | Rendered Label | Tooltip Content |
| :--- | :--- | :--- |
| `[repeat:: every day when done]` | `🔁 daily` | `Repeats: every day when done (from completion date)` |
| `[repeat:: every day]` | `🔁 daily` | `Repeats: every day (from scheduled date)` |
| `[repeat:: every week on Monday when done]` | `🔁 Mon` | `Repeats: every week on Monday when done` |
| `[repeat:: every week on Sunday]` | `🔁 Sun` | `Repeats: every week on Sunday` |
| `[repeat:: every 30 days when done]` | `🔁 30d` | `Repeats: every 30 days when done` |
| `[repeat:: every 28 days]` | `🔁 28d` | `Repeats: every 28 days` |
| `[repeat:: every month on the 1st]` | `🔁 monthly · 1st` | `Repeats: every month on the 1st` |

---

## 4. Implementation Architecture in `bob-ledger-tools`

The implementation maps cleanly into the existing plugin structure in [`bob-plugins/plugins/bob-ledger-tools/src/`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src):

1. **Pure Cores:**
   * [`src/140-gtd-review-marks.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src): Token pair matcher (`#gtd` + `#pre` / `#post`), range calculations, code exclusion, and DOM element builders.
   * [`src/147-repeat-marks.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src): Field detection, whitespace folding, cadence label normalization, and tooltip builders.
2. **CodeMirror 6 ViewPlugins & Reading Post-Processors:**
   * [`src/263-plugin-gtd-review-marks.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src): CM6 `Prec.highest` decoration replacement with cursor proximity reveal, plus markdown post-processor for reading view and canvas embeds.
   * [`src/262-plugin-repeat-marks.js`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src): CM6 decoration replacement with whitespace folding, plus reading view post-processor.
3. **CSS Mask Definitions:** Added to [`styles.css`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/styles.css) with zero-leak classes (`body.bob-gtd-review-marks`, `body.bob-repeat-marks`).
4. **Test Harness:** Unit test suites in `scripts/test-ledger-tools-gtd-review-marks.cjs` and `scripts/test-ledger-tools-repeat-marks.cjs` executing conformance vectors against all vault edge cases.

---

## 5. Artifact Details

* **Research Report Path:** [`sase/repos/research/202610/gtd_review_icons_and_compact_repeat_marks__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202610/gtd_review_icons_and_compact_repeat_marks__gem.md)
* **Registered Artifact:** `sase artifact show file:explicit:d4c4ddfcb0ee7114b4e6c018`
* **Artifact Label:** `research:202610/gtd_review_icons_and_compact_repeat_marks__gem.md`
* **Final Declaration:** Submitted and accepted for host commit.
