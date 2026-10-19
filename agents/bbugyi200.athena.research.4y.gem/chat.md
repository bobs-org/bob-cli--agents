# Chat History - ace-run (research.4y.gem)

- **TIMESTAMP:** 2026-10-19 08:22:11 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4y.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261019_080823.md`

## Prompt

%id(gem, clan=research.4y)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4y.cdx`, `research.4y.cld`, `research.4y.grk`, `research.4y.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start rendering some kind of marker on tasks that are in today's daily
file when I view those tasks in Obsidian.

- We already do something similar to this for task links (to show which tasks are
  in-progress and which were unblocked today).
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

# Research Summary: Rendering Today Task Markers in Obsidian

**Researcher:** researcher gem (`research.gem`)  
**Report File:** [`today_file_task_markers_design__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/today_file_task_markers_design__gem.md)  
**Artifact Ref:** `research:202610/today_file_task_markers_design__gem.md` (`file:explicit:d0df41392a3ec6beeefa9e73`)

---

## 1. Critique & Verdict: Is This a Good Idea?

**Yes, this is an outstanding idea and a high-leverage UX enhancement.**

In Bob’s GTD workflow, the daily note serves as the execution cockpit, while project notes, area notes, and inbox files serve as backlogs. Under [`decisions:today-is-read-from-the-ledger`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/memory/decisions/today-is-read-from-the-ledger.md), tasks never carry written `#today` or `#now` tags. While this prevents write churn and sync races, it currently creates a **visibility asymmetry**:
- Looking at today’s daily note, Bryan can see which tasks are planned for today (and via [`plan:202610/in_progress_task_link_marks.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/plans/202610/in_progress_task_link_marks.md), an amber half-ring `◐` shows which linked targets are `[/]` In Progress, while `🔓` marks unblocked tasks).
- Looking at a project note, however, there is **zero ambient visual feedback** showing whether a task is already committed to today's Pomodoro ledger. Bryan must switch tabs or trigger Mac Capture to verify.

Rendering a display-only marker directly on tasks that appear on today's ledger resolves this asymmetry with zero markdown churn.

---

## 2. Recommended Adjustments to the Requirements

To ensure the design remains reliable, clutter-free, and aligned with Bob's architecture:

1. **Location Gating (Suppression inside Daily Notes):**
   The marker **must NOT render inside today’s daily note itself**. Inside the daily note, sub-bullets under `## Pomodoros` are already task links; rendering a "Today" marker there is redundant noise. The marker should render in project notes (`projects/*.md`), area notes (`areas/*.md`), inbox notes, and query blocks (Reading Board, Dataview/Tasks).
2. **Strict Ledger Semantics (`todayCache` Alignment):**
   "In today's daily file" must strictly mean: **the task has a dedicated plain Task Link under an OPEN Pomodoro session in today's daily file**. Tasks linked only under closed/past Pomodoros (`🍅` history lines) are completed sessions and should not show an active "Today" commitment mark.
3. **100% Display-Only (Zero Text Mutation):**
   The marker must be implemented purely as a CodeMirror 6 Live Preview widget and a Reading view Markdown post-processor in [`bob-ledger-tools`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/). It must never write tags, inline fields, or text to markdown files.
4. **User Controls & Accessibility:**
   Provide a command `Toggle today task marks` (body class `bob-today-task-marks`), full dark/light theme tokens, and `@media (prefers-reduced-motion)` support.

---

## 3. Recommended Design: The "Pomodoro Sun" Ledger Mark

### Visual Appearance & Placement
- **Glyph:** A bespoke, lightweight **16×16 vector outline of a Pomodoro silhouette** with a 3-lobed calyx, matching Bob’s 1.9-stroke line art house style.
- **Color:** Warm Ledger Accent (`var(--color-orange, #eb6834)` in light mode, `#d95926` in dark mode). This distinguishes it from In Progress amber (`[/]`, `--color-yellow`) and Next green (`[*]`, `--color-green`).
- **Placement:** Positioned immediately following the checkbox:
  `- [ ] 🍅 Fix parser crash in compiler ⏫ 📅 2026-10-19 ^t39a`
  Sized at `1.15em × 1.15em` with `margin-inline-end: 0.32em`. It feels like an integrated status badge rather than an indentation defect.

### Micro-Interactions & Navigation
- **Hover Tooltip:** Standard Obsidian 2-line hover card (`data-tooltip-position="top"`):
  ```
  🍅 On Today's Ledger · Rank #2
  Session: (0940-1010) — CLI REFACTOR
  Alt+Click → Jump to daily ledger
  ```
- **Click Behavior:** Plain click places the cursor at the start of the task description without interrupting typing. `Alt+Click` (or shortcut `Alt+Shift+T`) navigates directly to the corresponding Task Link line in today's daily file.

---

## 4. Technical Implementation Architecture

All changes reside cleanly in [`plugins/bob-ledger-tools`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/):

1. **Pure Model (`src/139-today-task-marks.js`):**
   - Extracts `^blockId` from task lines via regex (`/(?:^|\s)\^([A-Za-z0-9-]+)\s*$/`).
   - Resolves key `${filePath}#${blockId}` against `this.todayCache.rank` (O(1) lookup).
   - Generates tooltip metadata (rank and Pomodoro session).
   - Defines listener-free DOM builder and `TodayTaskMarkWidget extends WidgetType`.
2. **Live Preview Extension (`src/275-plugin-today-task-marks.js`):**
   - CM6 `ViewPlugin.fromClass` emitting `Decoration.widget({ side: 1 })`.
   - Inspects `view.visibleRanges` for high performance.
   - Rebuilds on document edits, viewport scrolls, and the `todayTaskMarksRefresh` StateEffect.
3. **Reading View (`src/276-plugin-today-task-marks-reading.js`):**
   - `registerMarkdownPostProcessor` injecting `span.bob-today-task-mark` into `li.task-list-item`.
4. **Cache & Event Synchronization:**
   - Hooked into `rebuildTodayCache(...)` in `290-plugin-today-and-location.js`: when today's daily file changes or rolls over at midnight, dispatches refresh effects to all open editor panes.

---

## 5. Artifact Snapshot

The full research report has been committed to the research repository and registered as a durable SASE artifact:
- **File:** [`today_file_task_markers_design__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/today_file_task_markers_design__gem.md)
- **Artifact Ref:** `research:202610/today_file_task_markers_design__gem.md` (`file:explicit:d0df41392a3ec6beeefa9e73`)
