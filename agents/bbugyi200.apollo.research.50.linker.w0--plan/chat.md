# Chat History - ace-run (research.50.linker.w0--plan)

- **TIMESTAMP:** 2026-11-16 14:55:48 EST
- **MODEL:** claude/opus
- **AGENT:** research.50.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/wf_checking_period_close.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/wf_checking_period_close.md`

> # Plan: Period closing balance for WF Checking on period notes
> ## Context
> Bryan wants to see his Wells Fargo checking balance at the end of each period on that
> period's note. For example, the 2026-11-15 balance should appear on `2026/2026-W46.md`.
> It must never appear on daily notes. The design brief is intuitive, reliable, and
> beautiful. Bryan accepted every recommendation in the consolidated research report. Read
> it first:
> ```bash
> sase artifact read "research:202611/wf_checking_period_close/wf_checking_period_close.md" "Closing-balance design context"
> ```

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to start showing the total balance of my Wells Fargo checking
account at the end of a given period in the corresponding period note (we should not do
this for daily files). Can you help me implement this?

- For example, I should be able to see what my Wells Fargo checking account balance was
  on 2026-11-15 in the ~/bob/2026/2026-W46.md file somewhere.
- Review the wf_checking_period_close.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.50.linker

## Response

I've read the research report and am now reviewing the bob-cli bank code and the bob-plugins Bank Charts host so I can plan the work.

Still exploring: bob-cli's bank journal/status code is understood; next I'm checking the report output, `bob bank check`, docs, and then the plugin's Bank Charts header.

Now the report command wiring in cli.rs, plus check.rs and the docs.

Now the plugin side: opening bob-plugins to inspect the Bank Period Charts host and header readout.

Reading the plugin's chart model and paint code next, to see where a resting closing-balance readout fits.

I've mapped the plugin's charts header, model, and decode path; checking styles, plugin docs, and the period-note/stats-strip hosts next.

Design is taking shape. Checking reference memory for docs conventions and the bank glossary terms before writing the plan.

Next, routing the planned glossary/decision memory updates through the memory-write skill.

Nearly done exploring — checking memory strand formats, then I'll write the epic plan.

I have the full picture. Checking the epic plan schema before writing.

Writing the epic plan now.

Validation passes. Re-reading the file since the validator reformatted it on disk.

The plan is valid. Submitting it.

Staged. Finishing through `/sase_final`.

I've submitted a four-phase plan for review. Nothing will be built until you approve it. It follows all of the research report's recommendations, plus a few changes where I took the design lead.

**What you'll see:** the balance sits on the right side of the existing Bank Charts header on week, quarter, ISO-year and all-time notes:

```
│ ▾ BANK CHARTS  ▪▪                      BALANCE  $1,234.56 · as of Fri Nov 13
```

- **The number:** the posted balance at the end of the period's last day. It is not the "available" balance the Wells Fargo app shows first.
- **Drawn, not written:** `bob` works it out from your imported bank statements each time the note is shown. It is never written into any note.
- **Daily notes:** the Bank Charts panel only appears on period notes, so daily notes can't show it.
- **The "as of" label:** right now, W46 can only honestly say "as of Fri Nov 13", because the last import ends Friday. Once a later import covers Sunday, the label drops away and it reads as the settled close. The amount itself doesn't change.
- **Quiet weeks:** weeks with no spending, including older weeks from before tracking started, show just a one-line `BANK … BALANCE $…` header. About 29 past weeks and Q2/Q3 will have balances straight away.
- **Terminal:** `bob bank report -D 2026-11-15` answers your exact example.

**Design changes beyond the research:**
1. **Separate element:** the balance is its own element with a small `BALANCE` label, rather than text in the hover readout. Hovering a chart bar temporarily replaces it; screen readers don't re-read it each time.
2. **Full dates:** "as of Fri Nov 13" rather than "Fri 13".
3. **Ledger-mismatch warning:** when your ledger rows differ from the bank, that note goes in the tooltip only. The balance comes from the bank either way.
4. **Disagreeing bank balances:** if two bank-reported balances disagree, only the days between them are hidden, not the whole history.
5. **Same-day downloads:** a statement downloaded mid-day can't mark a period as settled, and won't trigger false "unverified" warnings.
6. **CSV imports:** CSV imports are left out of the arithmetic, since their transactions can be told apart from the bank's QFX ones. A span is only hidden if one import run mixed CSV and QFX files.
7. **Clicking:** the balance opens that day in the bank month note. Where no month note exists, as on older weeks, it doesn't open anything.

**The phases:**
1. The `bob` calculation and two new `bob bank check` warnings.
2. Adding the balance to `bob bank report` (JSON and the terminal line), plus docs, checked read-only against your vault.
3. The Obsidian plugin display, including preview screenshots to judge the look, then a sync to your vault.
4. Glossary and decision-record notes for future agents. These are three toggles you can approve or reject; all default to yes because you agreed to the research's recommendations.

Your real balances will stay out of tests, docs and commits; everything there uses made-up amounts.

The plan leaves your 30-day "Update cash balance" chore alone. You can cancel it yourself once you've seen the balances appear; it's next due December 1.
