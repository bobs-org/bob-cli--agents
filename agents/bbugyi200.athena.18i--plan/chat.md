# Chat History - ace-run (18i--plan)

- **TIMESTAMP:** 2026-11-05 08:32:29 EST
- **MODEL:** claude/opus
- **AGENT:** 18i--plan

**Plan:** /home/bryan/.sase/plans/202611/gcal_refile_moved_meetings.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/gcal_refile_moved_meetings.md`

> # Re-file MEET Pomodoros When Google Moves An Event
> ## Why this plan exists (the answer to "is there a good reason?")
> No. The behavior that made Bryan fix the MEET by hand is a gap, not a safety rule.
> What happened in `2026/20261105.md` (vault commits `4d37dfdb8`, `3e9fa6667`,
> `8753da32a`):
> 1. 05:37: sync created `^swings` at `**0815-0830**` as `[*]` and linked `[[#^swings]]`
>    under the future `- [ ] () — MEET` placeholder.
> 2. 08:17: Bryan moved the event to 08:00–08:15 in Google and sync ran.
>    `apply_span_updates` (`src/native/gcal/plan.rs`) rewrote the bold span to
>    `**0800-0815**` and re-slotted the row. The event was already over, but the link

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli MEET pomodoros should always be corrected in response to Google Calendar event
updates when it is safe to do so (which should be basically always, right?). Is there a
good reason I had to just manually adjust the MEET pomodoros (i.e. close one with a time
range of 0800-0815) after rescheduling the "Swings" event from 0815-0830 to 0800-0815?
If not, use your /sase_plan skill to plan the appropriate changes.
 %m:@xlarge

## Response

Confirmed so far: when an event's time changes, sync rewrites the row's bold span in place but never moves its MEET link. Now reading the MEET-filing code to see where a re-file would go.

Investigation's done and I'm now drafting the plan. Reading the docs guidance first, then I'll start the plan skill.

Writing the plan file now. It covers re-filing MEET links when Google moves an event, the safety rules, tests, docs, and a decision record. Then I'll validate it and propose it.

Plan passes validation with no warnings. Submitting it now.

There was no good reason. It's a gap in `bob gcal sync`, not a safety rule. I've staged a plan to fix it for your review.

**What happened to Swings today:**
- **05:37:** sync created `^swings` at 0815–0830 and put its link under the future `- [ ] () — MEET` placeholder.
- **08:17:** you moved the event to 0800–0815 and ran sync. It changed the row's time, but left the row `[*]` and the link under the future placeholder, even though the meeting was already over.
- **08:18:** you closed a MEET by hand at 0805–0820, then edited it to 0800–0815.

**Why:** sync now keeps every other part of an event row in step with Google until you edit it: time, title, badges, `#off`, buffer, description bullets and root. MEET filing is the one exception. Sync files a link once, when it creates the row, and never moves it afterwards (the docs say sync "never… retimes… or moves an existing Pomodoro"). The recorded decisions only justify that for MEETs that are your record of what actually happened. They don't justify it for a link sitting in an untimed placeholder, or for a closed MEET that sync wrote and nobody has touched since.

Because Swings inherits off-clock from `love`, the 15-minute `bob task reconcile` would probably have closed it correctly by about 08:30. An on-clock meeting moved the same way is never corrected.

**Is it safe "basically always"?** Yes, with three limits the plan keeps:
- Sync never touches a running Pomodoro.
- Sync never touches a MEET or link you've edited. It reports those once as `kept_meet` instead.
- Sync only re-files after a change in Google. A meeting whose time simply passed without being started keeps today's missed-meeting handling.

**What the plan does (one medium-sized change):**
- **Planned link, event now over:** when Google changes an event's time or buffer, a link still in the placeholder moves to a closed MEET in the right time slot. The row becomes `[x]` with today's completion date. Today's Swings fix would have been automatic.
- **Sync-written closed MEET, event now later:** an untouched closed MEET is retimed if the event is still in the past. If the event moved into the future, the closed MEET is removed and the row reopens to `[*]` under the placeholder.
- **Tests:** a Swings regression test plus the edge cases above.
- **Reporting and docs:** sync output gets a `links_refiled` count, and `docs/gcal.md` is updated.

**Two choices for you when approving:**
1. **Closed MEETs:** whether to also correct closed MEETs that sync wrote (the second bullet above). Default is yes. Otherwise a meeting that sync had already marked done keeps its old span when moved.
2. **Decision records:** whether to add a new decision record, `meet-filing-follows-google-until-edited`, and mark three older records as partly superseded. Default is yes.
