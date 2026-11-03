# Chat History - ace-run (17c--plan)

- **TIMESTAMP:** 2026-11-03 10:45:22 EST
- **MODEL:** claude/opus
- **AGENT:** 17c--plan

**Plan:** /home/bryan/.sase/plans/202611/refs_copy_picker_scope.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/refs_copy_picker_scope.md`

> # Plan: Bob Refs Copy pickers always show how many, which one, and which are on screen
> All work happens in the linked **`bob-mac-capture`** repo. Open it with your
> `/sase_repo` skill (`sase repo open bob-mac-capture -r "<why>"`) and do every read and
> write in the path it prints. Read that repo's `AGENTS.md` first: it sets the compile,
> format, and docs rules this plan relies on. There are **no bob-cli changes**. This is
> presentation only, which the `decisions:mac-capture-is-a-thin-client` and
> `decisions:code-copy-reads-render-time-catalog` records leave to the app. Do not change
> what is copied or how `bob ref code` / `bob ref links` are read.
> ## 1. What is wrong today
> Bryan's screenshot shows the code picker (Command-B / `C`) for a 44-page PDF, with

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make some things clearer when using the bob-mac-capture app's
ref panel's copy mode to copy links or code blocks? Namely, how many links/blocks were
found in the PDF? Which link/block is currently selected and which links/blocks are
currently shown? See the ~/tmp/screenshots/20261103_103054.png screenshot for an example
of what this looks like now. I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the Mac app's copy-card code (the view, the preview wells, the key router, and the RefsCore models) so I can see how links and code blocks are listed and windowed today.

I have the full picture: the problems, both sizing bugs, and the test and docs harness. Now I'm writing the plan file.

The plan passes validation. Submitting it now.

I've submitted the plan for your approval. Nothing in the Mac app has been changed yet, and nothing has been compiled or tested.

Your screenshot shows two layout bugs that make the confusion worse:

- **The card is wider than the panel.** A long line in the code preview box stretches the whole Copy card past the inspector. That pushes each row's page label (`● p. 13`), the header's "p. 13 in Highlights" chip, and the "+N more lines" badge off screen, and row text runs to the panel edge without an ellipsis.
- **The link picker can overflow in short panels.** It sizes its rows as if its preview box weren't there, so in a short panel the rows and preview box run past the bottom of the card. It doesn't show in your screenshot, but it affects the same feature.

**The design:** the header says how many, a new line under the list says which one is selected and which are shown, and a slim bar on the right edge shows the same thing visually. Each fact appears as text in exactly one place.

1. **How many.** The header puts the number first: "13 CODE BLOCKS · ● 2 ON THIS PAGE". Today's "CODE BLOCKS 13" sits next to "p. 13/44" and reads as a page number as easily as a count.
2. **Which is selected, which are shown.** A new line under the list reads "Block 7 of 13 · showing 6–8", or "all shown" when everything fits. The word "Block" keeps the number from being confused with the 1–9 keys, which only number the rows currently on screen.
3. **The overview bar.** It appears only when some items are off screen:
   - a thumb covering the visible rows, like a scrollbar;
   - an accent-colored notch marking the selected item;
   - small accent ticks wherever an item is on the current Highlights page.

   It slides smoothly as you scroll, and the animations switch off under Reduce Motion.
4. **Honest key hints.** The hint line names the keys that actually work, like "1–3 pick" instead of "1–9 pick". Pressing a key past the visible rows says "Only 1–3 are showing · ↑↓ scrolls" instead of "No code block 7" when there are 13. VoiceOver hears the same count, position and range as the screen shows.
5. **Both layout bugs are fixed** as part of the same change.

What gets copied, the key bindings, and how ↑↓ moves (including wrapping from the last item to the first) stay the same. There are no bob-cli changes.

**Decision for you:**
- **Highlights picker:** should the `H` picker get the same header, position line and bar? It shares the same scrolling list and card, so I've defaulted to yes for consistency.

The plan targets the Bob Mac Capture repo and is sized medium for one coding agent. It includes:
- tests for the new count and position logic, which run on athena;
- a regression test that the card never grows wider than the panel;
- picker window-size checks;
- new light and dark preview images of a scrolled 13-block list;
- docs updates;
- a compile check of the Mac app on the Mac. The final report must say plainly if the Mac is offline and that check can't run.
