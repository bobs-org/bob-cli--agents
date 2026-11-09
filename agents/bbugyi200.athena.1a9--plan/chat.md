# Chat History - ace-run (1a9--plan)

- **TIMESTAMP:** 2026-11-09 06:18:26 EST
- **MODEL:** claude/opus
- **AGENT:** 1a9--plan

**Plan:** /home/bryan/.sase/plans/202611/successor_picker_ctrl_np.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/successor_picker_ctrl_np.md`

> # Plan: Fix Ctrl+N / Ctrl+P navigation in the successor offer picker
> ## Diagnosis (confirm / deny)
> **Confirmed:** Ctrl+N / Ctrl+P do not move the highlight in the successor offer picker
> ("Pull in successors of …", "Keep ‹project› moving", relation successor groups, the
> project-promotion card, and the relation-merge offer pick, which all open the same
> modal).
> **Denied, in part:** it is not intermittent. In this modal the keys _never_ work, on
> every platform and in every state. It only feels unreliable because:
> - `↓` / `↑` and `Tab` ("toggle and move") do move the highlight here, and a Ctrl+X /
>   Ctrl+Shift+X verdict also auto-advances it, so the highlight often moves near a Ctrl+N

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli The `<ctrl+n/p>` keymaps do not seem to reliably work to navigate to the
next/previous successor in the successor menu shown in Obsidian (see the
~/tmp/screenshots/20261109_060907.png screenshot for an example of what this look like).
Can you help me confirm/deny my suspicion, diagnose the true root cause, and fix the
issue?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm tracing the successor offer modal in the `bob-plugins` task-status-cycler to find where Ctrl+N/P is handled.

I found the likely root cause: the successor modal overrides the base picker's key handler and drops Ctrl+N/P. Now I'm checking the verdict patches to explain why it only fails sometimes.

I've confirmed the successor modal never handles Ctrl+N/P. Next I'm checking for other keydown handlers that could make it work some of the time.

Still checking: I'm looking at your vault hotkeys for any Ctrl+N/P bindings that could explain why it only fails some of the time.

I'm writing a quick throwaway reproduction (outside the repo) to confirm Ctrl+N/P never move the highlight in this modal.

No OS-level remaps either, so the bug is entirely in the plugin. Checking the reason-editor key path and release conventions before writing the plan.

The fix itself is small. I'm now auditing other pickers for the same pattern (an override that handles ArrowDown but drops Ctrl+N/P) so the plan covers the whole root cause, not just this one modal.

Patch bump plus regenerated `docs/index.md` is the convention for fixes. Reading the docs reference memory, since the plan touches plugin docs.

I'm checking whether the bob-cli successor-picker contract (`docs/task-dependencies.md`) lists the picker's keys, so the plan updates it if needed.

I have the full diagnosis. Writing the plan now.

Validation flagged missing `title`/`goal` and two over-long decision strings. Fixing them.

Validation passes. Proposing the plan.

Your suspicion is half right. Ctrl+N/P are broken in the successor picker, but they don't fail some of the time: in that modal they never move the highlight. I've proposed a fix plan, and nothing has been changed yet.

**Root cause:** the successor picker in the bob-navigation-hotkeys plugin (`plugins/bob-navigation-hotkeys/src/206-successor-picker-modal.js` in bob-plugins) replaces the shared picker's key handler with its own. Its handler covers Esc, Ctrl+X, Enter, Ctrl+A, Tab and ↑/↓, but never hands other keys back to the shared handler. Ctrl+N/P exist only in that shared handler (`200-filtered-picker-modals.js`), so they get dropped. The key then goes to the search box, where on macOS it just moves the cursor, so nothing visible happens. It has been like this since the picker was first added in `0d69a20`.

**Why it seemed intermittent:**
- In this picker ↑/↓ and Tab do move the highlight, and Ctrl+X moves it on automatically, so the highlight often moves near a Ctrl+N press.
- Nearly every other Bob picker supports Ctrl+N/P (the Task Card and its stages, the relation picker, the block-id-prompt pickers), so they work in the cards just before and after this one.

**How I checked:**
- A throwaway reproduction with the existing test harness and three rows: ↓ and Tab moved the highlight from row 0 to row 1. Ctrl+N and Ctrl+P left it on row 0 and weren't intercepted at all.
- About 20 other pickers build on the same shared picker and supply their own key handlers. Every one passes unhandled keys back to the shared handler except this one, so there's nothing else to fix.
- Nothing outside the plugin is involved: no Hammerspoon mapping, no plain Ctrl+N/P in your vault's `hotkeys.json`, and no third-party plugin remapping them.

**The fix plan (small):**
- **Code:** make the picker pass any key it doesn't handle back to the shared handler, which every sibling picker already does. Ctrl+N/P then behave exactly like ↓/↑, including wrap-around and landing on "+N more" rows.
- **Tests:** written to fail first, then pass. They cover moving, wrap-around, Enter pulling in the highlighted row, the collapsed "+N more" row, the mode where you're marking rows done or cancelled, and Cmd+N/Ctrl+Alt+N being left alone.
- **Release:** rebuild `main.js`, bump the patch version, add one line to the plugin's docs page, run the full test and docs checks, then `bob plugins sync`.

**One decision for you when approving:** whether the picker footer should also show a `^N ^P move` hint. The default is no, because the footer is already crowded and never showed ↑/↓ either.
