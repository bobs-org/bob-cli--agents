# Chat History - ace-run (1gf--plan)

- **TIMESTAMP:** 2026-11-26 05:53:11 EST
- **MODEL:** claude/opus
- **AGENT:** 1gf--plan

**Plan:** /home/bryan/.sase/plans/202611/property_card_cursor_redraw.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/property_card_cursor_redraw.md`

> # Redraw the Vim cursor when a title-slot property card changes height
> ## Problem
> Screencast `20261126_053704.mp4` shows an Area card (`gtd_daily`) in Live Preview with
> Vim on. The cursor sits on the "Reflect on yesterday" task. When `-` collapses the
> card's Properties drawer, the card shrinks by about 330 px and the text moves up. The
> purple block cursor stays at its old screen row, which now covers "Check weather". The
> relative line numbers still place the real head on "Reflect on yesterday". `k` then
> lands on "Morning review", the line above, and the cursor repaints in the right place.
> So the selection is correct and only the painted cursor is stale. `_` (fold card
> details) changes the card height the same way.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When I use the `-` keymap to expand/collapse a property card's "Properties"
widget, the cursor appears to be positioned somewhere that it is not until I move it
(e.g. via the `j`/`k` keymaps). See the ~/tmp/screencasts/20261126_053704.mp4 screencast
for context. Can you help me diagnose the root cause of this issue and fix it? Make sure
that we apply the same fix to the `_` keymap (if applicable).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Found the `-` and `_` key handlers in bob-ledger-tools. Now I'm tracing `propertyCardToggleProperties` / `propertyCardToggleDetails` and where the card is mounted.

Still tracing: the gtd_daily card is an "area" Home card, so I'm reading how it's mounted in Live Preview (CodeMirror widget or DOM outside `.cm-content`) and how its toggle repaints.

Confirmed the main path: the card is "adopted" into the title slot, which sits outside `.cm-content`. Reading the title-slot code (240e/240k) next, since it already uses `requestMeasure`.

I'm checking Obsidian's bundled CodeMirror and vim cursor code to confirm why the cursor doesn't redraw when content moves.

Writing the plan next. Quick check on which docs describe the title-slot re-measure, so the plan updates the right ones.

I have the root cause and the fix design. Writing the tale plan now.

Validation passed. Submitting the plan.

The vim block cursor is drawn at a stale screen position after `-` or `_` resizes a property card. Your cursor never actually moves. I've written a plan to fix it, validated it, and submitted it for your approval; no code has changed yet.

**What the screencast shows:** after `-` collapses the card, the text moves up about 330 px but the block cursor stays at the same screen row, so it now sits over "Check weather". The relative line numbers still put the cursor on "Reflect on yesterday". When you press `k` it lands on "Morning review", the line above, and the cursor is drawn correctly again.

**Root cause** (checked against the CodeMirror and vim code bundled in Obsidian 1.15.1):
1. In Live Preview the card is mounted above the editor's text (inside `.cm-sizer`, before `.cm-contentContainer`), not inside the text area itself (`.cm-content`).
2. Obsidian's vim block cursor is a separate overlay at a fixed pixel position. It is only redrawn when the selection, editor geometry or visible range changes, or after vim runs a command.
3. Our handler in `248m-plugin-schema-double-equals.js` swallows `-` and `_` before vim sees them, so vim runs no command and never redraws.
4. The card then redraws itself a moment later. The title slot's resize watcher asks CodeMirror to re-measure, but CodeMirror only notices changes to the text area's size or padding, not to its position. That re-measure finds nothing changed and doesn't update the cursor, so it stays where it was until your next movement.

`_` goes through the same card redraw and the same resize watcher, so it has the same bug. So do mouse clicks on those controls and redraws triggered by new data, for every card type: album, record, bank, area, project and day/period.

**Planned fix** (in `bob-plugins`):
- **One change for every case:** in `240e-plugin-property-card-title-slot.js`, whenever a card is inserted or changes height in Live Preview, the code will also call vim's own cursor-redraw function (`blockCursor.scheduleRedraw()`). This covers `-`, `_`, clicks and data-driven redraws.
- **Fail-safe:** that function is internal to Obsidian, so the call is guarded and does nothing if it's missing. A future Obsidian update could therefore bring the bug back silently; the new real-Obsidian test would catch that. It isn't subject to the existing limit on re-measures per second, so pressing `-` or `_` quickly can't leave a stale cursor.
- **Rejected:** re-sending the current selection to force a redraw would wake about 30 selection-change handlers across the Bob plugins on every card resize.
- **Tests:**
  - Unit tests for the new redraw call.
  - New checks in the real-Obsidian Area/Project card walkthrough: the cursor must stay within 2 px of its text line after `-` open/close and `_` collapse/expand. They will be run once without the fix to confirm they catch the bug.
- **Shipping:** bump the bob-ledger-tools version to 1.166.5, update the docs, then run `bob plugins sync`.

**Decision for you:** whether to add the same cursor checks to the record-card walkthrough. The default is no: every card type goes through the one function being fixed, and the record-card walkthrough needs a bob built from bob-cli plus a longer run.
