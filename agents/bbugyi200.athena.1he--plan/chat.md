# Chat History - ace-run (1he--plan)

- **TIMESTAMP:** 2026-11-27 14:33:47 EST
- **MODEL:** claude/opus
- **AGENT:** 1he--plan

**Plan:** /home/bryan/.sase/plans/202611/always_show_priority_bars.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/always_show_priority_bars.md`

> # Always show the priority bars on Blocked digit rows
> ## Goal
> Every task with a canonical `[priority:: …]` field shows its priority mark (the 1–4
> filled signal bars, or the urgent `!` for `highest`). The mark shows in Live Preview,
> Reading view, and Tasks query results, whatever blocked-reason mark its checkbox wears.
> The hollow digit inside a Blocked `[?]` box (`p1`–`p4` block marks) stays exactly as it
> is. Only the rule that hides the bars when the box shows a digit goes away.
> ## Why (root cause)
> bob-plugins commit `b64a4332` ("fold digit bars and project-blocked pills") made the
> priority bars fold to zero width on any Blocked row whose block-mark key is `p1`–`p4`,

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me start always showing the priority icon (1 to 4 vertical bars)
again in Obsidian? Sometimes the priority number isn't shown in-between the `[]`
characters (see the ~/tmp/screenshots/20261127_142354.png screenshot for context).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm digging into how the priority bars get drawn in the bob-plugins repo. Next I'll work out why they disappear when the checkbox holds a status character like `[?]`.

Found the cause: Blocked rows that show a priority digit in the box hide their priority bars. I'm now checking the cases where that digit doesn't show.

I've found all the places that hide the bars: two plugin code paths and two CSS rules. Next I'll check whether Tasks query results hide them too, then look at the tests.

I've confirmed the cause. Now I'm checking which bob-cli docs (`docs/blocked-marks.md` and others) describe the bar hiding and would need updating.

I've mapped the tests that check the bars are hidden. Next I'll look at the exact test changes from the commit that added the hiding, so the plan can list what to reverse.

I've got most of what the plan needs. Now I'm checking the end-to-end Tasks-results assertions that expect hidden bars, then I'll write the plan.

I have the full picture, so I'm writing the plan now. One last check first: whether the public priority-marks API exposes the "hidden" flag.

The plan passes validation. Submitting it now.

I've written a plan to bring back the priority bars and submitted it for your review. No code has changed yet; a coding agent starts once you approve.

**Why the bars disappear:** an earlier bob-plugins change (commit `b64a4332`) hides the bars on Blocked rows whose box shows a priority digit like `[2]`, on the theory that the digit already says it. But the digit isn't always on screen while the bars are hidden:

- **Cursor on the checkbox (your screenshot, row 143).** With the cursor at the start of the line, Obsidian shows the raw `[?]` text, so the digit is gone. The bars stay hidden, because whether to hide them is decided from the line's text alone, not from what's displayed. The row ends up with no priority showing at all.
- **Tasks query results.** For a recurring Blocked row with a priority, the box shows the recurrence loop instead of the digit, but the bars are still clipped.

**What the plan does:**
- **Show the bars everywhere:** it removes the bar-hiding from Live Preview, Reading view and Tasks results. The digit in the `[?]` box stays as it is.
- **Pills unchanged:** the `#prj_is_blocked` and `#awaiting_reply` tag pills still hide when the box already says the same thing.
- **Tests:** it updates the unit and end-to-end tests, and adds a regression case for the cursor-on-checkbox situation.
- **Docs:** it updates the plugin docs and the two bob-cli docs that define how these marks look (`docs/blocked-marks.md` and the "Priority marks" section of `docs/projects.md`).
- **Ship it:** it bumps bob-ledger-tools by a patch version, runs the checks, and deploys with `bob plugins sync`.

I sized it as `small`, since the cause is fully pinned down and the fix is mostly removing code. No existing decision record covers how priority or blocked marks are displayed, so the plan doesn't cite one.
