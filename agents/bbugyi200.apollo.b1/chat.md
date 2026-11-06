# Chat History - ace-run (b1)

- **TIMESTAMP:** 2026-10-28 21:07:07 EDT
- **MODEL:** claude/opus
- **AGENT:** b1

## Prompt

#gh:gh_bobs-org__bob-cli Why do we excempt the PLAN theme? This is meant to be used anytime I need to
plan out more work for my day (see the ~/bob/2026/20261028.md file for an example use of
PLAN that does not involve my GTD morning review). End your analysis with a
recommendation for whether I should continue to exempt PLAN (include any tradeoffs /
decisions I need to make). 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete. %m:@xlarge

## Response

Tracing where `plan.exempt` is used (plan budget, Stats homes, themes, capture) and digging up the history behind it.

Found the origin: PLAN inherited GTD's exemption via the Oct 27 rename, on a research recommendation. Now reading that report's PLAN caveat and checking the actual minutes impact.

Checking two last code facts (duplicate-name lint and highlight), then writing the report.

Writing the report now.

Now registering the report as an artifact.

Registration succeeded. Now the final declaration.

The report is written and registered as an artifact (`file:explicit:2b30750a1359244593b9c794`, label `research:202610/plan_theme_exemption.md`). The research repo will commit it when this turn ends.

**Report:** `sase/repos/research/202610/plan_theme_exemption.md`

**Why PLAN is exempt:** PLAN inherited the exemption GTD had. Commit `f6287847` on Oct 27 changed `plan.exempt` from `[GTD]` to `[PLAN]`. The exemption was built for the morning ritual, for two reasons:
- **Plan budget (Sep 29):** the rule was "GTD plus ≤3 themes", and the 3-theme cap was set from the work you do outside review.
- **Stats (Oct 18):** "GTD sessions are review time", so the morning review wouldn't spread about 20% of the day into sase and bob.

The research behind the rename widened PLAN to cover project scoping too. It noticed the conflict and accepted it as about 10 hours over six months.

**Where it breaks:** `plan.exempt` does about ten things. Most of them are still right for planning in general: PLAN never counts as a theme, never becomes the ★ highlight, and never triggers the duplicate-name lint. The real problem is Stats. Every minute of a session named only PLAN goes to "PLAN review" (gtd area, shown as "GTD" in the Day Strip), and its links are ignored. In your Oct 28 example, Bob already forecasts the `sase_blog#^s0-spike` entry as `PLAN review`, with no tasks credited to `sase_blog`. There's a smaller leak too: tasks linked under PLAN don't count toward `max_links`. Tonight `bob plan` shows 1/13 links while Today lists 2 tasks.

**How much:** I scanned ledgers from Apr 27 to Oct 28. 21 PLAN sessions (475 min) linked no `^gtd` row at all, so they were planning outside the morning review. 16 of those (300 min) were in October, so the habit is growing.

**Recommendation: keep PLAN exempt from the plan budget, but change the Stats rule.** A PLAN-only session would count as review only when it links today's `^gtd` row. Otherwise its links decide where the minutes go, and the theme still reads PLAN. Morning reviews stay whole, and blog planning lands under `sase_blog`. Changing the Stats rule means a Rust change, a matching change in the Obsidian plugin and its shared test cases, doc updates, and a new decision record, since `f6287847` deliberately chose to go by the session's name.

Decisions for you:
1. **Should planning use one of your 3 theme slots?** I recommend no. If yes, drop the exemption and raise `max_themes` to 4.
2. **Should project-planning minutes count toward the project in Stats?** I recommend yes, via the rule change above.
3. **What should `review_time` measure?** Under the new rule it measures only the GTD ritual, and the PLAN theme becomes your total-planning number. Today it means every session named PLAN.
4. **Should tasks linked under PLAN count toward `max_links`?** I recommend yes, except the `^gtd` row. This is optional and low stakes.
5. **Color is a separate choice.** Keeping PLAN gray is fine. If you want color, setting `themes: PLAN: orange` overrides the gray without touching the exemption.
6. **Should linking a task under PLAN mark the task as a PLAN task?** I recommend keeping today's behavior, where it never does.

Whichever you choose, keep project planning in its own PLAN entry rather than inside the morning entry that links `[[#^gtd]]`. Also, PLAN-only sessions went from 24% of logged time over six months to 35% in October, and the exemption means the budget never pushes back on that.
