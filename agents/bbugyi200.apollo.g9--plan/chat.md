# Chat History - ace-run (g9--plan)

- **TIMESTAMP:** 2026-11-28 10:37:09 EST
- **MODEL:** claude/opus
- **AGENT:** g9--plan

**Plan:** /home/bryan/.sase/plans/202611/gg_reveals_note_header.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/gg_reveals_note_header.md`

> # Plan: Vim `gg` runs `zb` after landing at the top of a note
> Bob task `bob#^gg-runs-zb`: "Make it so `gg` always runs `zb` after scrolling to the top
> of the file in Obsidian!" The attached recording (`vid/20261128_101917.mp4` in the
> vault) shows this on today's daily note, starting well down the note. `gg` puts the
> cursor on the first body line, but the Day card stays above the viewport. A manual `zb`
> then scrolls to the very top and reveals the whole card.
> All work happens in the **bob-plugins** linked repo (open it with `/sase_repo`, read its
> `AGENTS.md`). bob-cli does not change. Do not edit the vault's `obsidian_vimrc.md` or
> `bob.md`.
> ## Root cause (verified)

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me complete the work associated with the ^gg-runs-zb task in the
~/bob/bob.md file? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I found the task. Its attached recording shows `gg` and then `zb` being pressed. Next I'll look at the frames to see what `zb` changes.

Opened the bob-plugins repo. Now looking for where the vim keys (`gg`, `zb`) are defined in the plugins and the vault's vimrc.

I'm checking how the property cards already handle vim keys near the top of a note, since that's where `gg` lands. There are existing card vim-navigation fragments to read.

I'm going through the existing real-Obsidian e2e harnesses so the plan can require verification in an actual Obsidian instance. Next I'll check the dev docs on where those e2e runs happen.

I'm reading the CodeMirror Vim code bundled with Obsidian on athena to see exactly how `gg` and `zb` scroll, so the plan is based on the real code.

Still researching. I'm checking the plugin version-bump policy and where the card docs describe Vim navigation, so the plan points at the right files.

I've confirmed the Vim APIs the fix needs (`defineMotion`, `mapCommand`, `Pos`) on athena's Obsidian 1.15.1. Last checks: existing unit tests for ledger-tools' Vim mappings, then I'll write the plan.

The plan passes validation. Submitting it now.

I've written the plan for `^gg-runs-zb`, it passed validation, and it's submitted for your review. Nothing changes until you approve it, and I haven't edited any files.

**Why `gg` hides the card.** Bob's cards, Obsidian's inline title and native Properties all sit above the editor's text area, though they scroll with the note. After `gg`, Obsidian's Vim scrolls only until line 1 is visible, which leaves everything above line 1 off-screen. Your recording shows this on today's daily note. `zb` fixes it because Obsidian measures its scroll from the very top, card included, so on line 1 it scrolls all the way up. I confirmed this in the Vim code bundled with Obsidian 1.15.1 on athena.

**Why the vimrc isn't enough.** `nnoremap gg ggzb` would cover most notes, but not Area/Project notes. On those, bob-ledger-tools intercepts the second `g` before Vim sees it. The mapping would also run `zb` after counted jumps like `120gg`, and only in normal mode.

**What the plan does (tale, medium):**
- **New `gg` override:** bob-ledger-tools replaces `gg` in normal and visual mode with a motion that lands exactly where stock `gg` does. This also covers `dgg`, `ygg`, `cgg` and Ctrl+O. Once the landing settles, it scrolls the way `zb` would.
- **Result:** the whole card, or the inline title and Properties, is visible. In a pane too short for the header, the cursor line stays visible at the bottom edge instead.
- **Card notes:** the existing `gg` handling on Area/Project and Ref Card notes requests the same scroll after it places the cursor.
- **Nothing else changes:** no note edits, no undo entries, `G`/`k`/Up untouched, and the mapping is removed cleanly when the plugin unloads.
- **Testing:**
  - Unit tests.
  - A real Obsidian run on athena, starting several screens down, on:
    - a plain note;
    - a Day card note;
    - an Area/Project note;
    - a Ref Card note;
    - a short split pane.
- **Shipping:** docs in `docs/bob-ledger-tools.md`, a minor version bump for bob-ledger-tools, then `bob plugins sync`.

**Decision for you (`counted_gg`):** I set it so only `gg` and `1gg` (the ones that land on line 1) scroll the card into view. The other choice is to have every `gg` do it; then `120gg` would leave line 120 at the bottom of the window.

None of the recorded project decisions cover Vim `gg` scrolling. The plan doesn't touch bob-cli, your vimrc, or `bob.md`.
