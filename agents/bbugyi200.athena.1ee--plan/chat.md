# Chat History - ace-run (1ee--plan)

- **TIMESTAMP:** 2026-11-19 08:19:10 EST
- **MODEL:** claude/opus
- **AGENT:** 1ee--plan

**Plan:** /home/bryan/.sase/plans/202611/successor_tab_space_keys.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/successor_tab_space_keys.md`

> # Plan: Tab marks and advances in the Mac Pull-In card; empty-filter Space in the Obsidian successor picker
> ## Goal
> Make the capture panel's successor choice card (the Mac "Pull-In" card) work like the
> Obsidian successor picker:
> 1. **Mac:** add a `Tab` key. It toggles the mark on the highlighted offer, then moves
>    the highlight to the next visible offer. If the highlighted offer is the last one,
>    the highlight stays where it is. `Space` keeps its current behavior: the same toggle,
>    but the highlight does not move.
> 2. **Obsidian:** add a `Space` key to the successor picker. It toggles the mark on the
>    highlighted offer without moving, and works only while the filter input is completely

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make the capture panel's sucessor panel work more like the
successor panel in Obsidian?

- Namely, I would like to add a new `<tab>` keymap that selects the current successor
  and then focuses the next one in the list (if any).
- We should keep support for the `<space>` keymap, which does the same thing but without
  focusing the next successor.
- As a part of this change, we should also add a new `<space>` keymap to the Obsidian
  successor panel that is only active when the user has not typed any text (to filter
  the successors shown).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Exploring the Mac capture Pull-In card and the Obsidian successor panel to plan the keymap changes.

Reading the Mac successor-offer docs and key handling next.

Now the key handling in the Pull-In choice view/model.

Found the Mac Space handler; now checking what Tab currently does on the Pull-In card and how the card's filter works.

Mac side mapped. Now looking at the Obsidian successor panel in bob-plugins.

Mac side is clear. Now checking the Obsidian picker base class, its tests, and its docs.

Checking the Obsidian test harness and docs for the successor picker keys.

Drafting the plan details now; one last check on the Mac README and the Mac docs-check gate.

Checking the latest Mac commit, which unexpectedly touches the Pull-In UI.

I have what I need. Writing the plan now: one tale covering both repos, plus one embedded decision about Shift-Tab.

The plan passes validation. Submitting it.

I've written the plan and submitted it for your review. It passed validation as a single-agent plan (size medium) and is staged now. Nothing gets implemented until you approve it, and no files in any repo have been changed yet.

**Capture panel's successor card (bob-mac-capture)**
- **New `Tab`:** marks or unmarks the highlighted successor, then moves to the next visible one. On the last one, the highlight stays put rather than wrapping, as you described ("if any"). Holding Tab down does nothing extra, the same as Space and Ctrl-X there.
- **Tab with filter text:** Tab works even when the filter has text. If your cursor is in the filter, it stays there, so you can filter, Tab, change the filter, Tab again, and press Return without the mouse. Marks you can't currently see still get submitted.
- **Tab on a Done/Cancel row:** it turns that row into a pull-in mark, the same as Space does today.
- **`Space` is unchanged:** it still marks or unmarks without moving.
- **Footer:** gains a `tab Mark & Next` hint, the spoken-description text mentions Tab, and `docs/keyboard.md` and `docs/capture-previews.md` describe it.
- **One side effect:** today, Tab on that card moves keyboard focus around the window, possibly into the filter. After this change you'd reach the filter by clicking it.

**Obsidian successor picker (bob-plugins)**
- **New `Space`:** marks or unmarks the highlighted successor without moving, but only while the filter box is completely empty. Once you've typed anything, Space types into the filter as it does now.
- **Ignored cases:** Space with Shift, Ctrl, Alt or Cmd held, a held-down Space, and Space in the Cancel reason box all behave as before.
- **Other keys and footer:** Tab is unchanged (it still wraps from the last row to the first), and the footer still advertises only Tab.
- **Version and deploy:** the plan bumps the plugin to 2.89.0, rebuilds it, and deploys with `bob plugins sync`.

**One choice for you when reviewing**
- **Shift-Tab on the Mac card:** by default, Shift-Tab moves up one row without marking, like Obsidian. Otherwise, once the card owns Tab, Shift-Tab would move focus out of the list. The alternative is to leave Shift-Tab as it is now.

The plan also requires compiling the Swift on the Mac and watching the macOS CI run go green after the push. If the Mac is offline, the final report has to say the Mac build is unverified.
