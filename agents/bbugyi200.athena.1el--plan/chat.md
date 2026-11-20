# Chat History - ace-run (1el--plan)

- **TIMESTAMP:** 2026-11-20 09:20:58 EST
- **MODEL:** claude/opus
- **AGENT:** 1el--plan

**Plan:** /home/bryan/.sase/plans/202611/picker_score_beats_status.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/picker_score_beats_status.md`

> # Plan: Task pickers rank by match score; status only breaks ties
> ## Problem
> Bryan's screenshot shows the Obsidian **Depends on** stage (Ctrl+Shift+B / Task Card
> `b`) with the filter `spike`. Eight Ready rows that match `spike` only as a scattered
> subsequence (score 0) fill RESULTS. The Blocked task
> `Spike S0: write the promise sentence…` matches as a field prefix (score 3), but it sits
> in a trailing **BLOCKED** section, below the fold. The best match should be first.
> **Rule (applies everywhere below):** match score always leads. Task status (open →
> Blocked → closed/done) only orders candidates whose scores are **equal**, followed by
> each picker's existing canonical order.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When linking to other tasks in Obsidian (and maybe in the capture panel, but
I'm not sure) we seem to group blocked (and done?) tasks in their own section at the
bottom. This makes it so, for example, typing "foobar" doesn't necessary immediately
reveal (the user has to scroll down) a blocked "Implement foobar component." task even
if it the best match.

- See the ~/tmp/screenshots/20261113_070944.png screenshot for an example of what I'm
  talking about.
- This is not correct.
- We should only preference open tasks over blocked/done tasks when the filter specified
  by the user matches those tasks equally well (so we fallback to sorting based on task
  status).

Can you help me fix this? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the Depends-on picker code in bob-plugins to find where blocked tasks get split into their own section.

I've found where the sections get built: the dependency, blocks, and relation stage views in `bob-navigation-hotkeys`. Next I'm reading how they rank and split rows.

I've confirmed the bob-cli capture `:` ranker sorts by match score first. Now I'm checking the other capture pickers, like the `&` dependency picker, for a blocked/closed split.

The Mac capture app has its own "Completed history" sections in several pickers. I'm reading how they build those sections from bob's candidate order.

I've mapped all the pickers that set blocked or done tasks apart. Now I'm reading the spec docs that encode the current rule, so the plan can update them too.

There's a prior plan, `links_stage_blocked_ranking`, that already fixed this for the Links stage. I'm reading it so this plan follows the same decisions.

Linked-from already ranks closed rows by score. So the remaining relation change is only the Links-to CLOSED split. I'm checking what else reads `firstInSection` before settling how headers render.

Settled: score first, then blocked/closed as the tie-break, with each row keeping its 🔒/closed styling. I'm checking the dependency spec's vector tables so the plan can add matching vectors.

I have the full picture. I'm reading the docs memory note (required before planning docs changes), then I'll write the plan.

I have what I need. Writing the plan now: one medium tale covering bob-cli and bob-plugins, with an embedded decision on empty-filter headers.

I've written the fix plan and submitted it for your review. No code has changed yet. You're right: blocked and done tasks are put below every open match no matter how well they match. Your screenshot shows the clearest case: `Spike S0: …` starts with "spike", but it lands under BLOCKED beneath eight Ready tasks that only contain the letters s-p-i-k-e scattered through them.

**Where status currently beats match quality:**
- **Depends on and Blocks stages (Obsidian):** blocked tasks always go into the trailing BLOCKED section. The roughly 60-row cap also cuts blocked rows first.
- **Links to stage (Obsidian):** closed and `done/` tasks always go into a trailing CLOSED section. An earlier plan already stopped this stage from setting Blocked tasks apart. Linked from already ranks everything by match.
- **The `((` task-link picker (Obsidian):** done tasks always come after open ones, under a "Completed history" divider.
- **Capture `&` and `((` (bob-cli):** done tasks always come after open ones. This is where your "and done?" hunch is right.
- **Bob Mac Capture:** already ranks by match when you type, so it needs no change.

**The fix:** match quality decides the order everywhere above. Task status (open, then blocked, then done) only orders tasks that match equally well. Blocked rows keep their 🔒 badge and muted text, and done rows keep their done look, so you can still tell them apart. Strong matches can no longer be cut off by the row cap.

While reading the code I found an existing bug: in those Obsidian stages, ties between equal matches currently come out in an essentially random order. The plan fixes that too.

The plan also covers tests in both repos, a shared ranking test case kept identical in both, the spec docs, a plugin sync, and a read-only check against your vault that `spike` puts the Spike task first.

**Two decisions for you at review:**
- **Empty-filter headers** (default: keep). With nothing typed, everything ties, so BLOCKED and CLOSED stay as headers at the bottom. Once you type, it becomes one ranked RESULTS list.
- **Decision record** (default: off). This would add an entry to the decisions memory recording this ranking rule.

**Left out:**
- In the Links stages, Blocked and Ready tasks stay treated as equals when tied, per the earlier accepted decision.
- The Mac `/` Go To picker still lists closed tasks after open ones regardless of match. It's for navigating, not linking, so I left it as a possible follow-up.
