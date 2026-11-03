# Chat History - ace-run (17m--plan)

- **TIMESTAMP:** 2026-11-03 14:39:23 EST
- **MODEL:** claude/opus
- **AGENT:** 17m--plan

**Plan:** /home/bryan/.sase/plans/202611/mac_today_badge.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/mac_today_badge.md`

> # Plan: Bob Mac Capture's "Links N/C" capsule becomes Obsidian's TODAY badge
> ## Goal
> Bob Mac Capture shows today's Task Link budget as a green/red `Links 9/13` capsule.
> Obsidian's daily `bob-plan` block shows the same number as a `TODAY 9/13` chip. That
> chip has its own shape and a seven-step color ladder. Make the Mac badge closely mirror
> the Obsidian chip: the same label, the same color ladder with the same exact-integer
> thresholds and the same default-theme colors, and the same chip shape. Apply it on every
> Mac surface that shows the link budget.
> Bob already reports the numbers (`plan_budget.links.count` / `.cap`), and they are the
> same numbers the Obsidian chip shows. The ladder is a presentation state, not a lint or

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli The "Links" badge shown by the brief rendered by the bob-mac-capture app by
default should actually closely mirror the "TODAY" badge we show in daily files in
Obsidian (including the label and the color ladder). See the
~/tmp/screenshots/20261103_142837.png screenshot for an idea of what this badge looks
like now. Can you help me fix this? I want you to lead the design on this one. Just make sure it looks beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Tracing where the "Links 9/13" pill comes from in the Mac app and how Obsidian's TODAY badge is colored.

Found the shared TODAY tone ladder in bob-ledger-tools; now reading its label format and CSS colors.

Confirmed the ladder is specified in bob-cli `docs/plan.md`. Checking the thin-client decision record before deciding where the tone is computed.

Pulling the exact default-theme hex values out of the installed Obsidian bundle so the Mac badge matches pixel-for-pixel.

Got the exact default-theme colors (light and dark). Now checking every other place the Mac app shows "Links N/M", plus docs and tests that describe it.

Mapped all three "Links N/M" surfaces (idle agenda, capture preview, pull-in picker). Checking memory notes and the mac repo's CI/check commands before writing the plan.

Found CI design-render tests that produce PNG fixtures — I'll use those as the visual check in the plan. Peeking at how they render, then writing the plan.

I have everything I need. Writing the plan now.

The plan passes validation. Submitting it.

I've written a plan for this and submitted it for your approval. Nothing has been changed yet; implementation starts once you approve. One visible effect: your screenshot's `Links 9/13` would become `TODAY 9/13` in **yellow**, because 9 of 13 is between 60% and 80% of the cap. Today it shows green.

**What it covers.** "Links N/C" appears in three places in the Mac app: the idle agenda (the brief), the capture preview, and the pull-in chooser. The last one has its own copy of the capsule. All three would use one shared badge.

**Design, matched to the Obsidian chip:**
- **Label:** `TODAY n/L`, or `TODAY –` when the budget data is missing (Obsidian never shows a fake `0/L`).
- **Color ladder:** same rules and exact cut-offs as the plugin:
  - grey at 0
  - blue below 40% of the cap
  - green from 40% to 60%
  - yellow from 60% to 80%
  - orange from 80% up to the cap
  - magenta exactly at the cap
  - red over the cap
- **Colors:** taken from your installed Obsidian's default theme (your vault uses it, and no snippet overrides these colors), with separate light and dark values. Magenta is the plugin's own pink/purple mix.
- **Shape:** a rounded rectangle instead of a capsule, with a thin colored stripe down the left edge, a faint border and tint in the badge color, and normal dark text rather than colored text. The text uses small caps in SF Pro, the same font Obsidian uses on the Mac.
- **Polish:**
  - The number animates when it changes, except when Reduce Motion is on.
  - The pull-in chooser's `+N` chip gets the same shape in neutral grey.
  - VoiceOver reads "at cap" or "over cap", so color is never the only signal.
  - A hover tooltip explains the count.

**Why only the Mac app changes.** Bob already sends both numbers. The Obsidian plugin works out the color itself, and so will the Mac app. So there's no change to bob-cli code or its output, and no Bob release is needed. The one bob-cli change is a sentence in `docs/plan.md` saying the Mac badge uses the same color rules, so future edits to them land in both places.

**How it gets checked.** New tests copy every color-rule case from the plugin's tests, and the existing "Links" tests get updated. A new render test draws all the badge states in light and dark mode. The implementer will look at those images from a macOS CI run and tune spacing if anything looks off. Mac-capture docs that still say "Links capsule" get updated too.
