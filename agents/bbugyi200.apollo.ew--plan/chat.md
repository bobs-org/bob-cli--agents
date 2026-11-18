# Chat History - ace-run (ew--plan)

- **TIMESTAMP:** 2026-11-18 09:16:51 EST
- **MODEL:** claude/opus
- **AGENT:** ew--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_headline_label.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_headline_label.md`

> # Label the Daily Headline in the capture panel's idle agenda
> ## Problem
> The idle agenda in the Bob Mac Capture panel prints today's Daily Headline straight
> under the `Today · Wed 18 Nov · Nothing running` title, in semibold body text, with
> nothing that says what it is:
> ```text
> Today · Wed 18 Nov · Nothing running                 3 done · 50m  ┊15m off-clock┊
> Add 30 zettel to sase_blog_zettel album!
> ▍TODAY 13/13
> ▦ Lincoln Park w/ Abby at 19:00 · in 9h 55m       1 left · 1h 00m · ↻ 08:27

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make it much clearer to the user what the headline is in the
capture panel (via an icon or `HEADLINE:` prefix, for example)? See the
~/tmp/screenshots/20261118_090438.png screenshot for an example of what this looks like
now. I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the Mac app's agenda code to see how the headline renders today.

Still exploring: now reading the plan-budget chip, calendar header, and measurer code so the headline design matches the agenda's existing visual language.

Exploring the design tests and docs media next, so the plan can include a visual check of the result.

I have the design direction; checking the existing headline height tests before writing the plan.

Checking how `macos-ci-check` works, to decide when the coder can inspect the rendered PNGs.

Writing the plan: a run-in small-caps `HEADLINE` label, with no icon and no extra height.

Plan is staged; finishing the turn through `/sase_final`.

I've submitted the plan for your review; nothing changes in any repo until you approve it. It's a single-agent plan, all in bob-mac-capture.

**The design:** a small-caps `HEADLINE` label at the start of the headline line, on the same line as the text:

```text
Today · Wed 18 Nov · Nothing running            3 done · 50m  ┊15m off-clock┊
HEADLINE  Add 30 zettel to sase_blog_zettel album!
▍TODAY 13/13
```

If the headline wraps, the second line starts under the headline text, not under the label:

```text
HEADLINE  Converge take-home submitted and the zettel album's first draft
          published for Friday review
```

Why this over the other options:
- **A word, not an icon.** `HEADLINE` is the same word as the `**Headline:**` line you type in your daily note, so there's nothing to learn. The likely icons already mean something in Bob or are easy to misread: ★ is the type highlight, and a flag reads as "flagged".
- **No extra height.** The label sits on the headline's own line rather than above it, so the agenda keeps its space for tasks.
- **Plain grey text, no box or color.** In this agenda, grey boxes are buttons (`+1`, `4 tasks`), tinted boxes are type pills or the budget badge, and colors mean themes, warnings or links. Plain grey small caps can't be mistaken for any of those. It's also smaller than the full-size type names in rows like `WRITE · Review …`, so it doesn't read as a type.
- **Matches the badge below.** It uses the same small-caps style as the `TODAY 13/13` badge, so the left edge reads as one column: `Today` / `HEADLINE` / `TODAY 13/13`.

**What else the plan covers:**
- **Unchanged behavior:** hovering still shows the full text, VoiceOver still reads "Today's headline, …", and with no headline the line stays hidden.
- **Tests:** new height tests check that a short headline stays on one line and a very long one stops at two, at the normal and narrowest panel widths.
- **Visual check:** the implementing agent has to open the light and dark CI renders at both widths before landing.
- **Docs:** the idle-agenda page is updated, and its main screenshot will show the labeled headline. That screenshot is a second commit after CI passes.

Left out on purpose: an icon, a "write your headline" prompt when it's empty (an empty headline is valid), clicking it to open the daily note, and any bob-cli or memory changes.
