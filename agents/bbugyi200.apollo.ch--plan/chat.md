# Chat History - ace-run (ch--plan)

- **TIMESTAMP:** 2026-11-04 17:41:04 EST
- **MODEL:** claude/opus
- **AGENT:** ch--plan

**Plan:** /home/bryan/.sase/plans/202611/alt_p_footer_hint.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/alt_p_footer_hint.md`

> # Show the Alt+P recommendation in the footer off the review walk
> ## Background
> Research report `research:202611/alt_p_priority_contract/alt_p_priority_contract.md`
> (read it with `sase artifact read`) audited three constraints on the Obsidian `Alt+P`
> key (`bob-navigation-hotkeys:roll-by-recommendation`):
> 1. **No priority, so Alt+P acts like Task Card key `1`.** This holds. Since `14dc9d9`,
>    the shared planner `planPriorityRollRecommendation`
>    (`plugins/bob-navigation-hotkeys/src/040-priority-roll.js`) returns `kind: "assign"`
>    at `levels[0]`. A probe found byte-identical writes **and** notices on Ready rows.
>    The only test of this compares Alt+P with the card's Ctrl+Enter, not with key `1`.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me fix the `<alt+p>` Obsidian keymap as described by the alt_p_priority_contract.md file in the research sidecar repo? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Found the contract in the research sidecar; reading it through the audited artifact path now.

Reading the footer and freshness-status fragments in bob-plugins to verify the research before planning.

Now checking nav's `api.quickRoll.preview`, the footer tests, and how cursor tracking is wired.

Reading the remaining test context, docs, and the glossary strand the change would affect.

Now reading the glossary strand and checking the memory-write routing, since the footer's documented contract changes.

Checking how nav reads the current priority (project notes may keep it outside the line), which decides how cheap the footer's pre-check can be.

Let me quickly probe whether Alt+P and card key `1` also emit identical notices, so the plan's new parity test asserts the right thing.

Content and notices both match, so the new test can assert full `deepEqual`. Confirming the baseline footer and quick-roll suites pass before planning.

The bob-cli `docs/` tree mirrors the plugin docs. Reading the docs memory note to learn how that mirror is maintained.

Checking for an existing task-line helper in ledger-tools that the plan can point the coder to reuse for the cheap pre-check.

Checking the one-line strict-parity alternative the research mentions, since I'll offer it as a reviewer decision.

I have what I need. Writing the plan now.

Validation flagged frontmatter length limits, a missing `title`/`goal`, and the memory decision's shape (it must be a `memory:` toggle). Fixing.

Validation passes. Quick re-read of the final plan file before proposing.

Plan is valid. Submitting it.

I've written the plan and submitted it for your review. Nothing changes in either repo until you approve it.

**What the research found:** two of your three Alt+P rules already work.
- **No priority → same as pressing `1`:** this holds. I re-ran the check against bob-plugins `b9f47f3`: on Ready rows, Alt+P and card key `1` write the same note text and show the same notice.
- **Has a priority → do what the footer recommends:** this holds. Both read the same recommendation for the cursor's line.
- **The footer always shows that recommendation:** this fails. The footer only shows the Alt+P hint when the cursor is on a row that's due in today's review. Once the review is finished it hides completely, so for the rest of the day no task with a priority gets a hint.

**The fix is all in the bob-ledger-tools plugin:**
- **Off the review:** on any open task with a priority (any lane, not only Ready), the footer's `]s next` hint becomes the recommendation, e.g. `Alt+P roll P2 1/1`, with the full sentence in the tooltip.
- **When nothing is due:** on such a line the footer appears as just `⟳ Nothing due · Alt+P …`. On any other line it stays hidden as it does today.
- **Rows due in today's review:** unchanged.
- **Cost:** the footer only looks up a recommendation when the cursor is on a task line.
- **Tooltip fix:** the plan also fixes the tooltip not updating when two different rows produce the same short hint (e.g. two `Alt+P cancel?` rows).

**Also in the plan:**
- A new test that checks Alt+P against key `1` directly. Today's test only compares it with the card's Ctrl+Enter.
- Updated footer tests, a version bump to 1.99.0, the plugin docs, `docs/freshness.md`, and `bob plugins sync`.

**Decisions you'll make when approving:**
1. **Hint on tasks with no priority?** The default is no: those rows keep `]s next`, because Alt+P there always does what `1` does.
2. **Exact date match with `1`?** The default is to keep current behavior. The only difference is on Blocked tasks already scheduled inside P1's window: Alt+P always moves the date, while `1` can land on the same date (about 1 time in 6). It can never happen on a Ready task. Making them match exactly is a one-line change.
3. **Update the glossary note on the review footer?** The default is yes. Its line "hides when nothing is due" will no longer be true after this change.

The plan is a single-agent plan, sized medium. Before planning, the footer and Alt+P test suites all passed (55 of 55).
