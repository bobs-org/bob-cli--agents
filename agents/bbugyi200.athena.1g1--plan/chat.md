# Chat History - ace-run (1g1--plan)

- **TIMESTAMP:** 2026-11-25 11:19:45 EST
- **MODEL:** claude/opus
- **AGENT:** 1g1--plan

**Plan:** /home/bryan/.sase/plans/202611/property_card_autosave_flicker.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/property_card_autosave_flicker.md`

> # Plan: Stop property cards from flickering when a note autosaves
> All code changes are in the linked `bob-plugins` repo (plugin `bob-ledger-tools`). Open
> it with `/sase_repo` (`sase repo open bob-plugins -r "..."`) and read its `AGENTS.md`
> before editing. There are no bob-cli code or memory changes.
> ## Symptom
> Bryan's screencast types into the Live Preview body of a record note,
> `sase_blog_zettel/what_came_before.md`. The record card flickers three times in 7
> seconds. Each flicker coincides with Obsidian's ~2 s autosave, not with a keystroke.
> There are two distinct looks:
> - **Flicker A** (at 2.5–2.8 s and 6.9–7.0 s). The card stays put, but Obsidian's native

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Something seems to be wrong with property cards. Namely, there seems to be a
flicker of some sort when I type in record notes. See the
~/tmp/screencasts/20261125_105619.mp4 screencast for context. Can you help me diagnose
the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I found the flicker in the screencast: Obsidian's native Properties block briefly shows up under the custom record card. Next I'll find the exact frames, then trace the cause in the code.

The screencast shows two kinds of flicker, each right when Obsidian autosaves. Now I'm reading the bob-plugins card code to trace why.

Measuring exact flicker timing per frame, then reading the record sheet's refresh path.

Writing a small standalone probe (in /tmp, outside the repo) that reuses the harness to type into a record note in real Obsidian and log, frame by frame, what is visible.

Still on the rarer whole-card flicker: re-running the probe with every Bob plugin loaded, since your vault runs them all and my first runs loaded only bob-ledger-tools.

Neither run reproduced the whole-card teardown. Checking git history for why the metadata "changed" handler releases ownership unconditionally, so the fix keeps whatever that guards.

Day-note cards show both flickers too, so the fix belongs in the shared card kit, not just the record adapter. Mapping every card path that reads the metadata cache.

Both causes are confirmed. Checking the docs and memory for statements the fix would make false, then I'll write the plan.

I have enough to plan. One last check: does the card's own text (e.g., the "Properties · 7" foot) change during an autosave? `recordSheetOnMetadata` drops the cached source before re-reading it.

Card text stays stable across saves, so only the two causes remain. Writing the plan now.

Plan validates. Proposing it.

I found two root causes, both confirmed in a real Obsidian, and proposed a fix plan. It's waiting for your approval; nothing has been changed yet.

Both flickers in your screencast happen at Obsidian's ~2s autosave, not on a keystroke. I reproduced them in a throwaway vault with Obsidian under Xvfb on athena. I used your real `sase_blog_zettel` album, the current bob-ledger-tools (1.157.1) and every Bob plugin, and logged frame by frame what was on screen during real typing.

**1. Native Properties flash under the card (at 2.5s and 6.9s in the video).** On every metadata "changed" event, the card code gives up its hold on the native Properties block, even when the save only touched the body. In `240q-plugin-property-card-frontmatter-ownership.js`:

```js
bindEvent(plugin.app?.metadataCache, "changed", (file) => {
  propertyCardFrontmatterCoordinatorReleasePath(plugin, file?.path);
});
```

The rows the card doesn't cover (`parent`, `type`, `created`) then show until the next refresh takes the block back, about 100ms on athena and longer on your Mac. This happened on 12 of 12 autosaves. It came in yesterday with commit 57bcb470; that work's plan said to let go of the block only when the save makes it stale, and the code does it on every change. A unit test currently locks in the buggy behavior.

**2. The whole card vanishes (at 4.83s).** Between Obsidian writing the note and finishing its re-read, `getFileCache(file)` briefly returns `null`. Any card rebuild in that gap reads null as "this isn't a record note" and tears down the card, title hiding and row hiding. Every save also schedules a card refresh 100ms out, so a gap longer than ~100ms produces this flicker. Your large Mac vault plausibly has gaps that long. On athena the gap is ~5ms, so it never happened naturally. When I simulated a 150ms gap, it reproduced your 4.83s frame exactly: card gone, inline title back, all seven native rows visible.

Day-note cards have both problems too. The second cause also affects album cards.

**The plan (medium tale, all in bob-plugins):**
- On a metadata change, re-check whether the note's frontmatter still matches Obsidian's cache, and only give up the Properties block when it doesn't.
- Add a small shared helper that serves the last good cache for up to 2s while Obsidian re-reads a saved note. Card drawing and the Properties-block check read through it, for record, album, day/period and home cards.
- Rewrite the bad unit test and add new ones.
- Add two checks to the real-Obsidian takeover test: one types through an autosave, the other simulates a slow re-read. Both must fail on the current build and pass after the fix.
- Update the docs, bump the version, build, and run `bob plugins sync`.
