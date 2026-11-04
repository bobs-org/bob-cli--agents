# Chat History - ace-run (17z--plan)

- **TIMESTAMP:** 2026-11-04 11:17:54 EST
- **MODEL:** claude/opus
- **AGENT:** 17z--plan

**Plan:** /home/bryan/.sase/plans/202611/gcal_past_events_born_done.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/gcal_past_events_born_done.md`

> # Born Done: `bob gcal sync` completes Event Tasks for meetings that already ended
> ## Problem
> When `bob gcal sync` first writes an Event Task after its meeting has ended (the
> **Past** phase), it already files the row under a closed
> `- [x] (**SSSS-EEEE** [t:: Nm]) — MEET` (or `[off:: Nm]`) entry with a `🍅 [[#^id]]`
> link. However, the row itself is born `[/]` (In Progress / Pending / WIP). Bryan's
> 2026-11-04 note shows the problem: the 08:15–08:30 `^swings` row was synced at 11:06.
> Its closed off-clock MEET was correct, but the `[/]` row sits in the Pending lane
> (already `PENDING 22/8`, over cap) until he completes it by hand.
> Root cause: `status_for_phase` in `src/native/gcal/plan.rs` maps `LinkPhase::Past` to

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make it so the `bob gcal sync` command creates event tasks with
a closed status when the event is in the past? We already seem to create the closed past
pomodoro properly, but the event task is created with a wip/pending status. See the
~/tmp/screenshots/20261104_110735.png screenshot for context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the `bob gcal sync` planner (`src/native/gcal/plan.rs`) to find where new Event Tasks get their status. It looks like ended meetings are hard-coded to `[/]`.

I'm checking the second place sync creates an Event Task: when a "Maybe" context row is upgraded in place to a task row.

Reading the `bob gcal sync` docs to find every place that documents ended meetings as `[/]`.

I'm checking the remaining docs and the existing past-phase tests that the plan must update.

The plan validates with no warnings. I'm submitting it now with `sase plan propose`.

The plan validated with no warnings and is staged for your review (`sase_plan_gcal_past_events_born_done.md`, tier `tale`, size `medium`). No code has changed yet.

**Cause:** `status_for_phase` in `src/native/gcal/plan.rs` gives `[/]` to any Event Task created for a meeting that has already ended. This was intentional: the accepted decision record `synced-meetings-link-by-phase` explicitly rejected `[x]` because "sync cannot know Bryan attended." Your request reverses that decision.

**What the plan changes:**
- **Ended meetings are created done.** New rows, and "Maybe" rows that turn into tasks, get `[x]` plus `[completion:: <note's day>]`. That date is the meeting's day, not the day sync ran, so `-D yesterday` counts as Done yesterday. Rows created before their meeting ends stay `[*]` as today.
- **The link under the closed MEET is struck at birth** (`🍅 ~~[[#^id]]~~`). That's the form `bob task reconcile` would rewrite it to anyway, and it's what reconcile already writes when it settles ended off-clock events. So sync's output won't be edited again by reconcile.
- **A parser fix that has to ship with it.** On a row without `[root::]`, `split_suffix` in `src/native/gcal/lifecycle.rs` would treat the completion field as part of Google's badges. Every later sync would then wrongly report "kept your edit to badges" and stop applying Google's title and time changes to that row. Rows completed today by a timed close, by reconcile, or by hand already hit this; the change would make it happen on every ended meeting.
- **Tests and docs:** existing tests that expect `[/]` get updated, and new ones cover the parser fix, reruns, and past days. `docs/gcal.md` and `docs/reference/vault-format.md` get updated to match.

**Two choices for you at approval, both on by default:**
1. Add a new decision record, `decisions:ended-synced-meetings-are-born-done`.
2. Mark `synced-meetings-link-by-phase` as partly superseded by it.

**Not covered:** rows already synced as `[/]` aren't migrated, since sync never changes a checkbox after creating it. That includes today's `^swings` row, so you'll need to complete it by hand.
