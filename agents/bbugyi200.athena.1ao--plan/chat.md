# Chat History - ace-run (1ao--plan)

- **TIMESTAMP:** 2026-11-09 18:15:16 EST
- **MODEL:** claude/opus
- **AGENT:** 1ao--plan

**Plan:** /home/bryan/.sase/plans/202611/mac_record_card_preview_fixes.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/mac_record_card_preview_fixes.md`

> # Fix Mac Record Card previews: set choices, status footer, route emoji
> ## Diagnosis
> The screenshot shows a restored canceled draft:
> ```text
> Hercules @movies/
> - status:: watched
> - [[abby]] liked this!
> ```
> The Record Card showed three defects:
> - The **Status** row showed both `🔖 To watch` and `✅ Watched` as identical gray

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Something seems wrong with the previews for record types when capturing from
the bob-mac-capture app. See the ~/tmp/screenshots/20261109_180335.png screenshot for
context. Can you help me diagnose the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Looking at the screenshot and the record docs to work out which part of the Record Card is wrong.

Reproducing the dry-run JSON bob returns for this draft (using a fresh title since Hercules already exists).

Found a likely culprit in `RecordCardView.valueContent`: a choice field with a set value still renders all schema choices. Checking the presentation layer and footer logic next.

Second culprit confirmed: the footer classifier treats any status text outside a short allowlist (including "Restored canceled draft") as a red refusal. Reading the row model now.

Now checking what `bob capture-parse` reports for the status field (state, display, choices).

Bob's parse is correct (`state: set`, `display: ✅ Watched`, plus the full `choices` list), so the Status row bug is on the Mac side. Let me zoom into the editor line to check the emoji overlay too.

Reading the original Record Card design plan to confirm intended behavior for set choice rows and the footer.

All three fixes are Mac-side (bob's JSON is correct and the mounted docs live in bob-mac-capture). Checking existing tests that pin the current behavior.

No open beads cover this. Checking existing panel tests for footer/stash patterns to point the implementer at, then writing the plan.

I have the full diagnosis. Writing the plan now.

The plan validates. Submitting it.

I found the cause of all three problems on the card, and the plan is now submitted for your approval. Bob's JSON is correct; every bug is in bob-mac-capture.

For your draft, `bob capture-parse -f json` reports `status` as set to `watched`, with the display `✅ Watched` and the full choice list. The dry-run plans the right Markdown, and `movies/hercules.md` was written with `status: watched`.

**Root causes**

1. **The chosen Status value never appears.** In `RecordCardView.swift`, the row code checks "is this a choice field with choices?" before it checks for Bob's display text. Bob always sends the full choice list, so every choice row shows all its options as identical gray pills, even when a value is set. It has been like this since the card first landed (8c13ac4). A test file already covers a set Status row, but nothing checks what the row actually shows.
2. **"Restored canceled draft" shows up in red.** The card's footer reads the panel's general status message and treats anything outside a short list (`Ready`, `Target cache stale`, `…`) as an error, painting it red in place of the `⇥ next field …` hint. That status line is set in about 200 places, and most of them are just information ("Inserted …", "Similar tasks changed", …). This particular message also survives later edits, so it stayed red while you typed.
3. **The 🎬 sits on top of the `@`.** The emoji is drawn over the `@` while the editor still draws the `@` in blue, so it shows around the emoji, and the emoji is wider than one character, so it covers part of the `m`. The saved test image draws the emoji without the text underneath, which is why review missed it.

**The plan's fixes**

- **Status row:** show Bob's display text whenever a value is set. The pills stay for unset or invalid choice fields.
- **Footer:** the app records explicitly when a status is an actual error ("Needs Status", preview or capture failures, Bob's errors). The footer turns red only for those, and other messages stay in the panel's bottom status line.
- **Emoji:** hide the `@` under the emoji and shrink the emoji to one character's width. The draft text itself doesn't change.

It also adds tests, an updated test image, and a short docs update, and runs the full Mac build and CI checks.

**Your choices at approval:**
- **Set Status row:** show only the value (my default), or keep all the pills and highlight the chosen one.
- **Emoji fix:** do it now (my default), or leave it and log it as a separate bug.

Once it lands and you reinstall Mac Capture, retest with a new title: `movies/hercules.md` already exists, so Bob would refuse that draft as a duplicate.
