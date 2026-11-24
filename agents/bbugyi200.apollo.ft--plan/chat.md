# Chat History - ace-run (ft--plan)

- **TIMESTAMP:** 2026-11-24 06:57:52 EST
- **MODEL:** claude/opus
- **AGENT:** ft--plan

**Plan:** /home/bryan/.sase/plans/202611/bare_minus_plus_property_keys.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/bare_minus_plus_property_keys.md`

> # Plan: Bare `-` and `+` replace the `=-` and `=+` property-card chords
> ## Goal
> In Obsidian Live Preview, Vim normal mode, Bryan presses one key instead of a two-key
> chord:
> - `-` toggles the mounted property card's read-only **Properties** drawer. It replaces
>   `=-`.
> - `+` opens the **Property Editor** on the active Markdown note. It replaces `=+`.
> - `==` is unchanged. It still opens the species card editor.
> - `=-` and `=+` are retired. After a pending `=`, `-` and `+` go back to Vim, as `=`
>   followed by any other motion does.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me change the `=-` and `=+` Obsidian keymaps to `-` and `+`,
respectively? See the bob-cli-pf and bob-cli-pl epic beads for context. The `-` has
another behavior currently that I don't really need or use (it can be removed).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the two epics and their plans; next I'll open bob-plugins to find the `=` gate and what `-` does today.

Found the `=` gate in `248m`; now checking what bare `-` and `+` are mapped to in Vim (plugin `mapCommand`s and the vault vimrc).

Docs don't mention `-` → today's daily anywhere, so retiring it is a one-line vault vimrc change. Reading the vault conventions memory to plan that edit correctly.

Writing the plan now: a single medium tale (bob-plugins gate + tests + hints + docs, the one-line vault vimrc removal, and coordination notes on the pf/pl epics).

Plan validated cleanly. Submitting it.

I wrote the plan, it passed validation, and it's now submitted and waiting for your approval. I haven't changed any files yet; the coder starts once you approve.

**What `-` does today:** your vault vimrc has `nnoremap - :bob_daily<CR>`, which opens today's daily note. The plan deletes that line. `:bob_daily` and the "Today's daily note" command stay available.

**What the plan does:**
- **New keys:** in Live Preview with Vim in normal mode, `-` toggles the card's Properties drawer and `+` opens the Property Editor. Both are added to the existing `=` key handler in `bob-ledger-tools` rather than to the vimrc. That way `-` and `+` still behave as normal Vim keys when there's no card or no editor to open, and they keep the existing safety checks.
- **Old chords:** `==` is unchanged. `=-` and `=+` stop working, and Vim treats them like any other `=` followed by a motion.
- **Where the keys never act:** they only fire when you're typing in the note body with nothing else pending. With a count (`3-`), after an operator (`d-`), after a prefix key (`g+`, `f-`), or with a register, they keep their normal Vim meaning. The old `=` chords never needed this check, because they only acted after a pending `=`. Bare keys would otherwise grab `-` and `+` typed into Vim's `/` search box, the built-in Properties fields, or the inline title. Both test suites (unit and real-Obsidian) cover these cases.
- **Hints:** the tooltips become "Toggle properties (-)" and "✎ Edit all (+)".
- **Tests and docs:** existing tests switch to the new keys, plus a new test that `=-`/`=+` no longer act. Every doc page that mentions the old chords gets updated.

**Overlap with the two epics:** bob-cli-pf and bob-cli-pl are still in progress, and pl's remaining phases plan to say `=+` in many places. So after landing, the coder adds a note to both epics telling remaining phases to use `-`/`+`. No memory note mentions the chords today, so the plan changes no memory. If a later phase adds one, the coder files a task to fix it.

**After it lands:**
- Restart Obsidian (or reload the vimrc plugin) on each machine so the removed `-` mapping takes effect.
- The vimrc edit is left for vault sync to commit, not committed by hand.
