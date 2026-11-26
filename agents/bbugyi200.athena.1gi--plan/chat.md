# Chat History - ace-run (1gi--plan)

- **TIMESTAMP:** 2026-11-26 07:22:39 EST
- **MODEL:** claude/opus
- **AGENT:** 1gi--plan

**Plan:** /home/bryan/.sase/plans/202611/alt_p_review_walk_settle_identity.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/alt_p_review_walk_settle_identity.md`

> # Alt+P advances the `]s` walk again after settle regroups the row
> ## Goal
> Alt+P (and every other resolving Task Card commit) on a `]s` landing must advance the
> GTD review walk exactly once, even when the same-write task settle moves the answered
> task into another `## Tasks` group. This restores
> `decisions:answering-advances-the-walk`: "a resolving Task Card commit" advances once,
> and Reword, no-op writes, and refusals stay.
> All code changes are in the linked **bob-plugins** repo (`bob-navigation-hotkeys`). Open
> it with `/sase_repo` (`sase repo open bob-plugins`) and read its `AGENTS.md` first.
> bob-cli itself needs no change, and nobody edits `Cargo.toml` versions or

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli The `<alt+p>` keymap does not seem to reliably navigate to the next task in the
list of GTD review tasks. See the ~/tmp/screencasts/20261126_070911.mp4 screencast for
context. This seems related to the bob-cli-q4 epic bead? Can you help me confirm/deny my
suspicion, diagnose the true root cause, and fix the issue?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reviewing the 14-second screencast (two ⌥P presses at 0.7s and 9.5s) to see what the GTD review list did, then I'll trace the alt+p handler in code.

Tracing Alt+P → `applyTaskCardRecommendation` → the priority commit, to see where (if anywhere) it hands off to the review-walk advance after the write settles.

Confirmed the mechanism so far: the after-line lookup uses a Myers line diff. Now checking whether its alignment key can pair a task row that both changed and moved.

Same result for an ID-less row. I'll prototype the identity-first fix in a throwaway copy, not the repo, to confirm it works before writing the plan.

All six suites pass with the prototype. Now checking whether any other review-advance path uses the same alignment for identity.

The inbox-route gate reuses the same reader, so fixing it covers that path too. One more check: does settle also regroup *closed* tasks? If so, a Task Card cancel hits the same bug.

The merge path is separate: a merge that deletes the row stayed put before q4 as well, so it's out of scope. Reading the governing decision record to cite it in the plan.

I have enough to explain the screencast fully. Before writing the plan, checking how the existing quick-roll unit tests drive Alt+P, so the plan names a concrete entry point.

Diagnosis is complete and confirmed by reproduction, bisect, and a working prototype. Writing the tale plan now.

Validation passes. Proposing the plan.

Your suspicion is right: bob-cli-q4 caused it. I bisected it to commit `ca07830a` in bob-plugins (phase bob-cli-q4.10.1.3, "settle task card, schedule, priority, and quick-roll commits"). I've proposed a tale plan for the fix; nothing is changed yet, and the coder starts once you approve it.

**What the screencast shows:** ⌥P didn't advance the walk on either press. Neither press produced a walk toast, only the roll card.
- **First press** ("Fix unread flicker!"): it only looked like it worked. The task got Blocked and moved out of the way, so the next review task slid up into the cursor's line. The footer later read `Review 1/11` because the task index refreshed under the cursor, not because the walk landed there.
- **Second press:** since the walk never landed on that row, the press didn't count as answering a review landing. The cursor was left on an empty line above "Next & In Progress".

**Root cause:**
- Since `ca07830a`, Alt+P's write also tidies the note in the same step. A task that becomes Blocked moves to `### Blocked`; a cancelled one to `### Done & Canceled`; a Next one to `### Next & In Progress`.
- After the write, the Task Card finds the task again with a line-by-line diff of the note before and after (`readReviewOriginAfterLine`). That diff can't follow a block that moves past other lines.
- It loses the task when the moved block is shorter than the tasks it jumps over. The card then reports nothing changed and the walk stays put.
- When the moved block is longer, the diff does find it and the walk advances. That's why it seemed unreliable.

**How I checked it:**
- I reproduced it with the real settle code on a note with `## Tasks` groups, using both tasks with block IDs and tasks without.
- The nav-hotkeys build just before `ca07830a` advances; that commit and current HEAD don't.
- A later q4 fix (`8645ed55`) switched the walk's queue and landing tracking to block IDs but missed this one function.
- The tests didn't catch it either. The morning-review test never answers through the Task Card. The real-Obsidian Alt+P test uses a note without `## Tasks` groups, so nothing ever moves.

**The fix:** all of it is in bob-plugins; bob-cli needs no change.
- Find the answered task by its block ID first, then fall back to today's diff.
- If there's still no match, accept a single task line with the same title text (ignoring fields and checkbox).
- Duplicate titles and rewords stay put, as the walk rules require.

I tried this in a throwaway copy: both the block-ID and no-ID cases advance, and six existing review and settle test suites still pass.

**The plan:** medium size, in bob-plugins.
- Move the function out of `350-picker-task-card.js` (999 lines, at the 1000-line limit) into `538a-nav-settle-identity.js`.
- Add unit tests, and real-settle tests covering Alt+P roll and decay, picking a priority level, cancel, and the stay cases.
- Change the real-Obsidian Alt+P test to use a grouped note where the jump is bigger than the moved block, so it would have caught this.
- Bump the plugin version, add one sentence to `docs/develop/task-settle.md`, and run `bob plugins sync`.

The same fix also covers the other Task Card answers on a review landing: Ctrl+Enter, priority picks, schedule dates, Depends-on adds, cancel, and the inbox-route fallback.
