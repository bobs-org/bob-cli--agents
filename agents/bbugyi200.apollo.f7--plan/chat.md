# Chat History - ace-run (f7--plan)

- **TIMESTAMP:** 2026-11-20 11:38:05 EST
- **MODEL:** claude/opus
- **AGENT:** f7--plan

**Plan:** /home/bryan/.sase/plans/202611/dataview_inline_prefix_collision.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/dataview_inline_prefix_collision.md`

> # Stop Dataview From Claiming Bob's `=` Code Spans
> ## Diagnosis
> **Symptom.** In `gtd_daily.md`, the GTD chores render Dataview parse errors in Live
> Preview: `` `==` `` becomes `Dataview (inline field '='): PARSING FAILED …` and
> `` `=` `` becomes `Dataview (inline field ''): … Got the end of the input`. The rows are
> vault-authored (vault commit `0402c21c1`, 2026-11-20), not bob-cli output.
> **Verdict on the suspicion ("these are inline Dataview queries; I don't use them; turn
> them off").**
> 1. _Inline Dataview queries cause it_ — **confirmed.**
>    `~/bob/.obsidian/plugins/dataview/data.json` has Dataview 0.5.68 defaults:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When tasks have a backtick before an equals, it causes Obsidian to attempt to
render it as an inline Dataview query. See the ~/tmp/screenshots/20261120_111935.png
screenshot for context. I don't think I use these, so they can probably be turned off,
but this is just my first thought. Think hard about the best way to fix this. Can you
help me confirm/deny my suspicion, diagnose the true root cause, and fix the issue?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Checking bob-plugins for any reliance on Dataview's inline prefixes.

Bob plugins don't depend on inline queries. Now checking bob-cli's own note-snapshot code, which mirrors the same `=` rule.

Diagnosis is solid. Before authoring the plan, reading the docs-change rules and the memory-write routing (the plan may add a decision record).

Writing the plan now. One last fact check: exact count of vault notes that the `=`/`$=` prefixes currently hijack.

Important: 119 real inline queries (`= durationformat(default(sum(n…`) exist. My earlier grep missed them (80-char limit). Investigating.

I have the full picture. Drafting the plan file now.

Plan validates; tightening the memory selector so the new record path is covered without a warning.

Validation passes (one non-blocking warning: the new memory record can't be resolved before it exists). Submitting.

You're right about the cause, but turning inline queries off won't fix what's in the screenshot, and you do have some old inline queries. I've submitted a plan for the fix and it's waiting for your review. Nothing has been changed yet.

**Your suspicion, checked against Dataview's code and your vault:**

1. **Inline Dataview queries cause it: right.** Your Dataview settings still have the defaults: inline queries on, triggered by `=`, and inline JavaScript on, triggered by `$=`. Dataview treats any inline code that starts with `=` as a query. So `` `==` `` and `` `=` `` in your chores get parsed and fail.
2. **"I don't use them": partly wrong.** 119 daily notes, from 2026-06-02 through 2026-09-28, have a heading like ``## Pomodoros (`= durationformat(…)`)`` that shows the day's total time. The Day Strip replaced that total, and an edit on 2026-10-25 already removed it from notes dated 2026-09-29 onward. Apart from those, the only one is an example in `lit/obsidian.md` (plus two generated copies of it). Nothing uses inline JavaScript, but it's switched on, so any `` `$= …` `` text in the vault would run.
3. **"So turn them off": not enough.** Dataview's editor (Live Preview) code runs whatever that setting says. With inline queries off, `` `==` `` would show "(disabled; enable in settings)" instead of the error. Only Reading view would be fixed, and your screenshot is Live Preview.

**Root cause:** Dataview's `=` trigger clashes with how Bob writes things in inline code: the `==` and `=` keys, close outcomes like `=x`, and the old `========================` headers from the zorg migration. Apart from the 119 headings, about 290 such bits of code in about 170 notes are being misread today. The fix is to change the trigger itself, not just switch the feature off.

**What the plan does:**
- **Dataview settings:** turn off inline queries and inline JavaScript, and change their triggers to `dv=` and `dvjs=`, which appear nowhere in the vault. Your `dataviewjs` blocks (`dash.md`, `rotten.md`) and the inline-field display keep working.
- **The 119 old headings:** rewrite them to plain `## Pomodoros`, matching the October cleanup. A one-off script does an exact-line replacement and stops if it doesn't find exactly 119.
- **bob-cli PDF snapshots of vault notes:** these currently turn a bare `` `=` `` into an "Open live query" link. They'll follow the vault's Dataview settings instead, with tests.
- **Docs:** add a vault requirement note and a row for Dataview's settings file in the vault-format table.
- **Left alone on purpose:** the Gmail import and compose safeguards against `=`/`$=` text. They're harmless and still protect you if the defaults ever come back.

**Decisions for you in the review:**
- **Old headings:** strip them (the default; those older notes lose the total in the heading, but `bob stats` still has it), or keep inline queries on under `dv=` so those totals keep showing.
- **PDF snapshots:** follow the vault setting (the default), or leave bob-cli as it is.
- **Memory:** whether to add a decision record that Dataview never claims Bob's `=` code. This is off by default because you didn't ask for it.

**What you'll need to do after it runs:** reload Dataview in Obsidian on the Mac once vault-sync has delivered the new settings. It doesn't notice changes to its settings file while running. Don't change any Dataview setting in a window you haven't reloaded first, or it will write the old `=` settings back.
