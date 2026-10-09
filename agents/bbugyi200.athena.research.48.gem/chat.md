# Chat History - ace-run (research.48.gem)

- **TIMESTAMP:** 2026-10-09 16:16:46 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.48.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261009_160056.md`

## Prompt

%id(gem, clan=research.48)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.48.cdx`, `research.48.cld`, `research.48.grk`, `research.48.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
would like to start showing the current pomodoro (if any) and all future pomodoros in
the preview shown by the bob-mac-capture app when no input text has been typed.

- This preview should therefore load by default when the panel first pops up.
- Since we will load this preview so often, we should make sure to cache it somehow when
  the daily file's contents haven't changed at all. IMPORTANT: The bob-mac-capture app
  MUST be blazing fast.
- For each task associated with a task link in a current or future pomodoro in today's
  daily file, we should always show as much of each task's contents as possible without
  causing the user to need to scroll the preview pane.
- This means that, if it all fits in the preview pane without the user needing to scroll
  (we should expand the height of the window as neccessary), we shoould show the full
  task definition for each task including all of its sub-bullets.
- Otherwise, we should support two folded views, which we will use in this order of
  priority, if necessary, to decrease the size of the contents in the preview pane:
  1. A view of each task that does not show the work log or schedule log for that task,
     but shows all other sub-bullets.
  2. A single-line view of each task.
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

# Independent Research Report: Default Pomodoro & Task Preview for Bob Mac Capture

**Researcher:** `research.48.gem`  
**Durable Snapshot:** [`research:202610/capture_panel_default_pomodoro_preview__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/capture_panel_default_pomodoro_preview__gem.md)  
**Artifact ID:** `explicit:03fdc2e354f9e6bc8dde037b`

---

## 1. Executive Summary & Assessment

### Is this a good idea?
**Yes, with critical architectural and UX adjustments.**

Currently, popping up [`bob-mac-capture`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-mac-capture) displays an empty text input with an idle preview pane. The user is capturing without immediate situational awareness. Introducing an ambient default preview of the **running Pomodoro** and **future queued Pomodoros** grounds Bryan in his daily plan with zero keystrokes. It accelerates common capture workflows (`@route+` sub-bullet capture, `=` session starts, and `=x` closes) because the user immediately sees the active session and its task hierarchy.

However, a naive implementation faces **five critical pitfalls** that require adjustments to the prompt's initial assumptions.

---

## 2. Critique of the Plan & Required Adjustments

### 2.1 The Multi-File Cache Invalidation Trap
* **The Issue:** The prompt suggests caching the preview *"when the daily file's contents haven't changed at all"*. However, in Bob's vault architecture (per [`today-is-read-from-the-ledger`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/memory/decisions/today-is-read-from-the-ledger.md)), the daily note (`YYYYMMDD.md`) contains only the **Task Links** (`[[Projects/bob-cli#^fix-cache]]`). The actual task body, checkbox status, sub-bullets, and `🛠️ **WORK LOG**` live in external notes (`Projects/bob-cli.md`). If Bryan edits a task in Obsidian, the daily note remains untouched. Keying the cache solely to the daily note would show **stale task definitions**.
* **Adjustment:** The cache invalidation must observe both the daily note and the referenced task notes. Fortunately, [`VaultTargetWatcher`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/VaultTargetWatcher.swift) in `bob-mac-capture` already monitors the vault root via macOS `FSEvents`. In addition, `bob-cli`'s response includes a manifest of touched files and their timestamps for precise cache validation.

### 2.2 Window Sizing Jitter & Keystroke Transitions
* **The Issue:** If the empty panel expands to ~650pt to show several Pomodoros and tasks, typing a single character `t` (e.g. `task: buy milk`) will replace the default preview with a ~140pt single-item draft preview. Without a steady-height transition policy, the window would abruptly shrink by 500pt on the very first keystroke.
* **Adjustment:** Implement smooth SwiftUI animations (`.animation(.snappy(duration: 0.2))`) during transitions between the default ledger overview and draft capture mode, preserving layout stability while typing.

### 2.3 The "All Future Pomodoros" Screen Overflow Dilemma
* **The Issue:** A user planning 8–10 Pomodoros with 12 linked tasks will easily exceed the screen's vertical budget on standard displays (e.g., MacBook laptop displays with ~800–900pt visible height), even in Folded View 2 (single-line per task). The "no scrolling" requirement cannot be met without bounding the planning horizon.
* **Adjustment:** Introduce a **Planning Horizon Cap**:
  - Show the **Current Pomodoro** in full fidelity.
  - Show the **Next 2 upcoming Pomodoros** with their tasks.
  - Collapse any further queued Pomodoros into a clean summary badge (`+ 5 more planned Pomodoros`) with an interactive expand toggle.

### 2.4 Asymmetric Folding Priority
* **The Issue:** A uniform global folding switch means that a large, multi-bullet task in a distant future Pomodoro would force the *active running task* to collapse to a single line.
* **Adjustment:** Use **asymmetric tiered folding**. Strip logs and collapse future tasks first, preserving the sub-bullet detail of the running task as long as possible before falling back to full single-line compression.

### 2.5 Integrated Session & Task Presentation
* **The Issue:** In `bob-mac-capture`'s current preview cards, task blocks and Pomodoro blocks render as separate, disconnected stacks. Rendering them separately would sever the relationship between each Pomodoro and its planned tasks.
* **Adjustment:** Nest task cards directly under their parent Pomodoro session header.

---

## 3. Technical Architecture & CLI Contract

In accordance with [`mac-capture-is-a-thin-client`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/memory/decisions/mac-capture-is-a-thin-client.md), `bob-cli` remains the sole authority for vault reading, link resolution, and markdown parsing, while `bob-mac-capture` owns presentation and window sizing.

### 3.1 New CLI Subcommand: `bob capture-default-preview`
```bash
bob capture-default-preview --format json [--bob-dir <DIR>]
```
- **Read-only and deterministic**, adhering to [`cli_rules.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/memory/cli_rules.md).
- Scans today's daily file using [`capture_pomodoros::scan`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/capture_pomodoros.rs).
- Extracts task links using [`capture_pomodoro_close::number_task_links`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/capture_pomodoro_close/selection.rs) and [`plan_budget::today::today_links`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/plan_budget/today.rs).
- Resolves note files via [`VaultLinkResolver`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/plan_budget/today.rs) and scans tasks via [`note_tasks::scan`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/note_tasks.rs).
- Generates pre-computed line tiers (`full`, `no_logs`, `headline_only`) using [`parse_managed_task_log_marker`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/capture/sub_bullet.rs) to detect and separate `🛠️ **WORK LOG**` and `🗓️ **SCHEDULE LOG**`.

### 3.2 JSON Response Schema (`schema_version: 1`)
```json
{
  "ok": true,
  "schema_version": 1,
  "day_file": "/home/bryan/bob/2026/20261009.md",
  "relative_day_file": "2026/20261009.md",
  "manifest": [
    { "path": "2026/20261009.md", "mtime": 1791578400000 },
    { "path": "Projects/bob-cli.md", "mtime": 1791578420000 }
  ],
  "plan_budget": {
    "themes": { "count": 2, "cap": 3, "over_cap": false },
    "links": { "count": 5, "cap": 10, "over_cap": false }
  },
  "current_pomodoro": {
    "ref": "46:ae8bb2f6",
    "name": "FIX",
    "time_range": "(**0920-0950** [t:: 30m])",
    "status": "running",
    "tasks": [
      {
        "relative_target": "Projects/bob-cli.md",
        "route": "bob",
        "line": 142,
        "block_id": "fix-cache",
        "status_symbol": "/",
        "status_name": "In Progress",
        "headline_text": "- [/] Fix memory leak in capture-pomodoros ^fix-cache",
        "sub_bullet_count": 4,
        "work_log_count": 2,
        "schedule_log_count": 1,
        "tiers": {
          "full": [ ... ],
          "no_logs": [ ... ],
          "headline_only": [ ... ]
        }
      }
    ]
  },
  "future_pomodoros": [ ... ],
  "warnings": []
}
```

---

## 4. Blazing-Fast Caching Architecture

To achieve zero popup delay (<0.5ms on frame 0):
1. **In-Memory Cache Actor (`CaptureLedgerPreviewCache`)**: Resident in `bob-mac-capture`. When [`show()`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelController.swift#L259) is called, the cached snapshot renders synchronously on frame 0.
2. **Event-Driven Prewarming & Invalidation**:
   - [`VaultTargetWatcher`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/VaultTargetWatcher.swift) observes vault file changes via `FSEvents`.
   - When a vault file changes, it asynchronously re-runs `bob capture-default-preview` in the background and populates the cache.
   - The user never waits on a process spawn when invoking the global hotkey.

---

## 5. Adaptive Sizing & Progressive Folding Algorithm

Using [`CapturePanelWindowSizer`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelWindowSizer.swift) and [`CapturePanelLayout`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift#L5), available height is calculated:
$$\text{AvailableHeight} = \text{ScreenVisibleHeight} - (2 \times \text{panelScreenMargin}) - \text{ChromeHeight} - \text{EditorHeight} - \text{FooterHeight}$$

The view evaluates content height across progressive stages:
1. **Stage 1 (Full Fidelity)**: Current task Full + Future tasks Full.
2. **Stage 2 (Strip Future Logs)**: Current task Full + Future tasks without Work/Schedule logs.
3. **Stage 3 (Strip All Logs)**: Current task without logs + Future tasks without logs.
4. **Stage 4 (Single-Line Future)**: Current task with sub-bullets + Future tasks single-line.
5. **Stage 5 (Single-Line All)**: All tasks single-line.
6. **Stage 6 (Horizon Truncation)**: Current + Next 2 Pomodoros, with remaining collapsed under a `+N more` badge.

Clicking any collapsed fold chip (e.g. `⋯ 2 work log entries hidden`) expands it inline using [`BlockDiffCard`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/BlockDiffCard.swift)'s existing fold expansion handler.

---

## 6. Recommended Next Steps

1. **Implement `src/native/capture_default_preview.rs` in `bob-cli`** with full unit test coverage.
2. **Implement `CaptureLedgerPreviewCache` and `DefaultLedgerPreviewView` in `bob-mac-capture`**.
3. **Verify window sizing and smooth draft-to-empty transitions** in the macOS menu-bar app.

The complete research report with full implementation details, Mermaid flowcharts, and architecture schemas has been saved and registered to [`sase/repos/research/202610/capture_panel_default_pomodoro_preview__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/capture_panel_default_pomodoro_preview__gem.md).
