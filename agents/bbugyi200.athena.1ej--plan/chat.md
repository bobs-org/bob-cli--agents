# Chat History - ace-run (1ej--plan)

- **TIMESTAMP:** 2026-11-20 09:04:22 EST
- **MODEL:** claude/opus
- **AGENT:** 1ej--plan

**Plan:** /home/bryan/.sase/plans/202611/record_card_ctrl_np.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/record_card_ctrl_np.md`

> # Record Card: Ctrl+N / Ctrl+P move the highlight like ↓ / ↑
> ## Problem
> Bryan's screencast (`~/tmp/screencasts/20261120_085557.mp4`, macOS) shows the Record
> Card editor on a `type: [[record]]` note. The **Status** choices stage is open with the
> **Filter choices** input focused and the highlight on the current choice (Draft). He
> presses `⌃P`, then `⌃N` three times, and the highlight never moves. He then presses `↓`
> three times (the highlight moves Draft → Ready → Placed → Later) and `↑` three times
> (back to Draft). Arrows work, but Ctrl+N and Ctrl+P do nothing. Every other Bob picker
> (relation card, bank subscription linker, bank category card, Emoji Slot, and
> `FilteredPickerModal` subclasses) already treats Ctrl+N / Ctrl+P as ↓ / ↑.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me fix the `<ctrl+n>` and `<ctrl+p>` keymaps on record cards? See
the ~/tmp/screencasts/20261120_085557.mp4 screencast for context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Ctrl+P/Ctrl+N leave the highlight on Draft in the screencast. Now I'm looking at the arrow-key frames to compare.

The screencast shows Ctrl+N/P doing nothing in the record card's choice picker, while ↓/↑ move the highlight. Next I'll open the bob-plugins repo to find the record card code.

I'm comparing how sibling cards (intention card editor, album schema card) handle Ctrl+N/P, to pick the convention the record card should follow.

I have what I need on the code side. Before planning a docs edit, I'm reading the project's docs rules.

I'm settling the last details (fragment build order, version-bump convention) before writing the plan.

Before writing the plan, I'm ruling out the other possible cause: some other plugin's global capture-phase handler swallowing Ctrl+N/P before the record card sees them.

No other plugin captures plain Ctrl+N/P (the capture-phase handlers all require Shift or other keys), so the record card simply ignores them. Writing the plan now.

Validation flagged missing `title`/`goal` and an over-long decision label and `why`. Fixing those.

Validation passed. Submitting the plan.

I've submitted a plan to fix Ctrl+N/Ctrl+P on the record card; it's waiting for your approval and no code has changed yet.

**What the screencast shows:** in the Status choices list, with "Filter choices" focused, ⌃P and three ⌃N leave the highlight on Draft. Three ↓ then move it to Later, and three ↑ bring it back.

**Root cause:** the record card's key handler never handled Ctrl+N/P. It's in `plugins/bob-ledger-tools/src/242r-plugin-record-card-typed-stages.js` in `bob-plugins`. Inside the filter box it only handles the arrow keys, so on macOS Ctrl+N/P just move the text cursor and the highlight stays put. The suggestion and link pickers have the same gap, and so does the field list when no picker is open. Nothing else is intercepting the keys; I checked the other plugins' global key handlers. Your other Bob pickers (relation card, bank pickers, Emoji Slot) already treat Ctrl+N/P like ↓/↑.

**The plan:**
- **Fix:** add a small check that recognises Ctrl+N and Ctrl+P. Variants with Shift, Alt or Cmd don't count, so Ctrl+Shift+P, which opens the card, is unaffected. Then make Ctrl+N/P do exactly what ↓/↑ do:
  - in the choice list, both inside and outside the filter box;
  - in the suggestion and link pickers;
  - in the field list, depending on your answer below.

  Text, date, number and URL inputs keep their normal behaviour.
- **Tests and docs:** add unit tests in `scripts/test-ledger-tools-record-card.cjs`, and update the key tables in `docs/record-card.md`.
- **Release:** bump the plugin's patch version, rebuild, run the full test suite, deploy with `bob plugins sync`, and commit in `bob-plugins`.

**Decision for you (`browse_ctrl_np`):** should Ctrl+N/P also move between fields when no picker is open? The default is yes, so the keys mean ↓/↑ everywhere on the card. The alternative limits them to the pickers.

The full real-Obsidian test run isn't part of the plan. It runs on Linux, which doesn't have the macOS cursor behaviour behind this bug, so it can't reproduce it; the unit tests are the gate. After the plugins sync, please check on your Mac that Ctrl+N/P move the Status highlight.
