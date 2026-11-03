# Chat History - ace-run (17j--plan)

- **TIMESTAMP:** 2026-11-03 12:58:31 EST
- **MODEL:** claude/opus
- **AGENT:** 17j--plan

**Plan:** /home/bryan/.sase/plans/202611/refs_tabs_inspector_hydration.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/refs_tabs_inspector_hydration.md`

> # Plan: Fix Bob Refs inspector never hydrating after Command-T from Highlights
> ## Symptom
> When Bryan presses Command-T in Highlights to open Bob Refs in Tabs, the inspector
> sometimes shows only the list-item facts: a grey thumbnail box, the `Pages`/`Notes`
> counts, and no HIGHLIGHTS feed. There is no "Notes unavailable" line either, so
> `RefsInspectorContent` for the selected row is still `nil`; the load never ran. A
> panel-switch round trip to Capture and back fills it in. (Bryan described the key as
> Ctrl+Enter. In code the panel switch is Ctrl+Tab, `RefsKeyRouter.isPanelSwitch`; either
> way it is the same `BobPanelCoordinator.switchPanels` path.)
> ## Root cause (all paths are in the `bob-mac-capture` linked repo)

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Sometimes when I use the `<cmd+t>` keymap in the Highlights app to open the
bob-mac-capture app's ref panel, none of the annotations load. These show up after I use
the `<ctrl+enter>` keymap twice to jump to and then back from the capture panel. See the
~/tmp/screenshots/20261103_124708.png screenshot for an example of this issue in action.
Can you help me diagnose the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Opened the bob-mac-capture repo; now reading the ref panel's inspector loader and Cmd+T tabs path to find why annotations don't load.

Found a likely suspect: the inspector loader skips hydration when the panel isn't visible yet. Now tracing where selection changes call `inspectorRequested()` in the Tabs flow.

Root cause found. Writing the plan now.

I found the cause and wrote a fix plan for bob-mac-capture. It passed validation and is staged for your approval; no code has changed yet.

**What goes wrong:** in this app, only two things ask the ref panel's inspector to load a reference's annotations and thumbnail:
1. The code that runs each time the panel is shown, which loads whatever row is selected at that moment.
2. A UI hook (`.onChange(of: selected)` in `RefsPanelView.swift:263`) that fires when the selected row changes.

On ⌘T, the panel first builds its tab list from the *previous* tab read, then reads Highlights' open tabs in the background. When that read finishes, two things happen at once: the panel's loading state flips to loaded, and the selection jumps to the tab that's current now. The loading and loaded states draw the list and inspector in separate branches of the panel's view code. So the flip throws away the inspector and builds a new one. The new one's hook treats the new selection as its starting value, so it never fires. Nothing requests the load, which is why your screenshot shows a grey thumbnail box, counts that come from the list row, and no annotations or error message.

**Why only sometimes:**
- **It works** when the current Highlights tab is the same as at your last ⌘T. The row selected when the panel opened is already the right one, and that row was loaded.
- **It fails** on the first ⌘T after the app launches, and whenever you've switched tabs in Highlights since the last ⌘T.
- **The round trip fixes it** because coming back to the panel re-runs the show code with the right tab selected. In the code, the jump between the capture and ref panels is Ctrl+Tab, not Ctrl+Enter. Both go through the same switch-and-return path.

The same gap also stopped ⌘T from scrolling the inspector to the notes for your current page. The bug has been there since tab support was added on Oct 16 (`1b7ead4`).

**The planned fix (small, one agent):**
- **Load on every selection change:** in `RefsPanelModel.swift`, every change to the selected row will request the load, instead of relying on the view hook. The existing 120 ms wait and cancel-on-move still debounce rapid movement. A hidden panel still loads nothing until it's shown.
- **Remove the view hook:** take out the now-redundant hook in `RefsPanelView.swift`, so changing the view layout later can't bring the bug back.
- **Two regression tests** in `RefsPanelModelTests.swift`: one for the first ⌘T after launch, and one for "switched tabs since the last ⌘T". Both should fail on today's code and pass after the fix.
- **Checks:** `just portable-check` here (it can't compile the macOS app code). A best-effort compile of a scratch copy on the Mac, following the repo's AGENTS.md. The full test suite runs in CI, since the Mac has no XCTest.
- **Manual check for you after install:** press ⌘T on PDF A, Esc, switch Highlights to PDF B, press ⌘T again. B's annotations should appear right away, scrolled to the current page's notes.
