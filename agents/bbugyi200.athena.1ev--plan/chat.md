# Chat History - ace-run (1ev--plan)

- **TIMESTAMP:** 2026-11-21 10:07:55 EST
- **MODEL:** claude/opus
- **AGENT:** 1ev--plan

**Plan:** /home/bryan/.sase/plans/202611/intention_editor_footer_keeps_keys.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/intention_editor_footer_keeps_keys.md`

> # Plan: Keep the intention card editor's keymap footer on j/k
> ## Problem
> In the intention card editor (`==` on a daily or period note → "EDIT INTENTIONS"), the
> line under the rows starts as the keymap list:
> `j/k move · Enter edit · o add · r reflect · Alt+J/K reorder · Ctrl+D remove · u undo · [ ] = travel · y YAML`
> After one `j` or `k`, that line shows only the newly selected row's label ("Intention
> 2", "Reflection", …), and the keymap list does not come back while you keep browsing.
> The screencast `~/tmp/screencasts/20261121_100019.mp4` shows this (keys `j`, `j k k`,
> `j`, then `Ctrl+[`).
> ## Root cause (confirmed)

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When I use the `j` and/or `k` keymaps in the intentions panel, the footer that
shows me what all of the keymaps are goes away. See the
~/tmp/screencasts/20261121_100019.mp4 screencast for context. Can you help me fix this?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I checked the screencast. After `j`, the keymap hint footer is replaced by the focused row's label ("Reflection"). Next I'm finding the intentions panel code in the bob-plugins repo.

The footer is one status line, and it shows the `announce` text in place of the keymap hints. Next I'm finding where `j`/`k` sets `announce`.

Found the cause: `intentionSelect` puts the row's label into the status line, which replaces the keymap hints. Now I'm checking which tests and docs depend on that behavior.

I'm looking at the existing intention-card tests to choose where a regression test should go, then I'll write the plan.

Before writing the plan, I'll run a quick harness check to confirm that `j` really replaces the footer text.

I have the root cause and a reproduction, so I'm writing the plan now.

Validation passed. Submitting the plan.

I found the cause and staged a fix plan for your review. Nothing has been changed yet.

**Cause:** in the bob-plugins repo, `intentionSelect()` in `plugins/bob-ledger-tools/src/297c-plugin-intention-card-editor.js` writes the selected row's label into the status line. The status line only shows the keymap list when it has nothing else to show, so after a move it shows the label instead. That's why the footer turned into "Intention 2", "Reflection", and so on in your screencast. Arrows, Tab, the 1–9 keys and clicking a row go through the same function, so they hide the footer too. I reproduced it in the plugin's test harness: the footer shows the full keymap list when the panel opens, "Intention 2" after `j`, and "Intention 1" after `k`.

**Plan** (`sase_plan_intention_editor_footer_keeps_keys.md`, a small single-agent plan):
- **Fix:** selecting a row clears the status message instead of writing the label into it. The highlighted row already shows where you are, so the label adds nothing. All selection moves will keep the keymap footer. A message like "✓ Saved · u undo" stays until your next move, then the keymaps come back. Error and read-only messages are unchanged.
- **Tests:** add tests showing the footer stays through each kind of move, and that it comes back after a save or undo message.
- **Wrap-up:** add one sentence about the footer to `docs/intention-card.md`, bump the plugin's patch version, rebuild, run the tests and docs check, then `bob plugins sync`.

**One decision for you:** pressing `s` (select Summary) currently replaces the footer with "Summary selected · Enter explains ownership…". By default the plan keeps that message, and your next `j`/`k` brings the keymaps back. If you pick `footer` instead, `s` keeps the keymap footer like every other move.
