# Chat History - ace-run (18j--plan)

- **TIMESTAMP:** 2026-11-05 08:42:42 EST
- **MODEL:** claude/opus
- **AGENT:** 18j--plan

**Plan:** /home/bryan/.sase/plans/202611/off_clock_links_uncapped.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/off_clock_links_uncapped.md`

> # Off-clock Task Links leave the TODAY link budget
> ## Goal
> The Obsidian `bob-plan` / `dash.md` **TODAY** badge shows
> `budget.links.count / plan.max_links`: the number of distinct `(target, block_id)` Task
> Links under today's open, non-exempt Pomodoros. Today that count includes links to
> **off-clock** tasks (lunch, gym, school pickup), so off-clock life uses up the daily
> link cap (default 10) and can turn the plan `over`.
> Change the rule so that **a Task Link whose target task is off the clock is never
> counted toward the link budget**. It does not count toward the meter, cannot make the
> status `over`, never raises `plan_link_cap_exceeded`, and never fires capture's link-cap

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me stop counting offclock task links as a part of the tasks shown
by the `TODAY` badge in Obsidian? These tasks should not be constrained by the daily
task link limit.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the relevant decisions and searching for the TODAY badge and daily link limit code.

Found the Rust link-budget engine; now locating the off-clock resolver and the Obsidian badge code.

Reading the JS mirror (bob-ledger-tools plan budget, off-clock link chips, and the plan block badge).

Mapped the Rust consumers; checking the JS link resolver, conformance fixtures, and the dashboard badge next.

Still exploring: checking the tmux meter's call path and the Mac capture budget contract before drafting.

Looking at how the Today-roots code resolves a ledger link to its task line, so the plan can reuse it for the off-clock check.

Design is taking shape (vault-aware off-clock filter feeding the pure budget engine in Rust and JS). Checking the human meter renderers for a possible "off-clock" suffix.

Exploration is done. Before drafting, checking memory-write rules since the plan likely adds a decision record.

The plan is staged. Finishing the turn with the final declaration.

I've written the plan and submitted it for your review. No code has changed yet; the plan goes to a coding agent once you approve it.

**Where the number comes from.** The Obsidian TODAY badge (on the daily note and on `dash.md`) shows the link budget: how many different tasks are linked under today's open Pomodoros, out of `plan.max_links` (default 10). Right now that count only looks at link syntax. It never checks whether the linked task is off-clock, so lunch, the gym and similar links use up the cap and can push the plan over.

**What the plan changes**
- **The rule (`docs/plan.md`, the official definition):** each link is checked with the same off-clock test Pomodoro sessions already use:
  - `#on` beats `#off` (and its old spellings).
  - Otherwise the nearest area or project note's `offclock:` setting applies, including through `[root::]`.
  - Event Tasks in the daily note are checked too.
  - An off-clock link isn't counted, can't make the plan "over", and never triggers the link-cap warning.
  - A link that can't be resolved still counts, so mistakes err toward the cap.
  - The number left out is reported in a new JSON field, `links.off_clock`.
- **What stays the same:** off-clock tasks are still Today tasks. The 🍅 marks, the dashboard TODAY section and the Today roots line don't change. If they left Today, they'd fall into the NEXT and PENDING sections and count against those caps instead.
- **bob-cli:** the link check reuses the existing session off-clock code, so a session and the budget can't disagree about a link. Every place that shows the budget follows: `bob plan`, `bob task reconcile`, the capture meter and its warnings, the Mac app's TODAY badge (no Mac code changes), and the tmux `plan L/Lc` meter.
- **bob-plugins (bob-ledger-tools):** the plugin's copy of the counting code gets the same check, using the same lookup as the existing "off" chip on ledger links. The `api.planBudget` callers (the link-to-today picker footer and notices) pick it up automatically. The badge redraws once a linked note's text has loaded.
- **Tests:** a new set of 13 shared test cases runs against both the Rust code and the plugin, plus capture, agenda and tmux tests. Docs are updated in both repos, followed by `bob plugins sync`.

**Two choices for you when you approve:**
- **`off_clock_count_display`** (default: shown). The TODAY tooltip and the `bob plan` meter add "N off-clock uncapped", so a smaller count doesn't look like a bug.
- **`decision_record`** (default: off). Adds a new decisions memory record for this rule. It's off by default because no existing memory note becomes wrong.

It's a single medium-sized plan for one agent: the bob-cli change lands first, then the plugin change, with the shared test cases copied across.
