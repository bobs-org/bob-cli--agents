# Chat History - ace-run (research.34.linker.w0--plan)

- **TIMESTAMP:** 2026-11-03 10:52:31 EST
- **MODEL:** claude/opus
- **AGENT:** research.34.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/period_notes_and_stats_strips.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/period_notes_and_stats_strips.md`

> # Plan: Period notes that add up
> ## Background
> Bryan's daily notes (`YYYY/YYYYMMDD.md`, created by core Daily Notes plus Templater from
> `_templates/daily.md`) set `parent` to `[[YYYY/YYYYMM]]`, a monthly note that is only
> created when someone clicks the dangling link (from the untemplated stub
> `_templates/monthly.md`). He wants the tree to be day → week → quarter → year → a new
> `all_time.md` → `org.md`. Each week, quarter, and year note should have a "stats strip"
> that breaks down working time, an automatic summary of its parts, and pre-written
> instructions so an agent asked to "update" the note needs nothing else. `gtd_daily.md`
> should run the reviews, and the glossary should gain "stats strip". He reviewed the

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Daily files in Obsidian currently link to a monthly file that uses no template.
I would like to start linking to weekly files as the parent of daily files instead. Can
you help me implement this?

- Weekly files should then link to quarterly files as their parents, which should link
  to yearly files as their parents, which should link to a new ~/bob/all_time.md file as
  their parent, which should link to the ~/bob/org.md file as its parent.
- Each of these weekly/quarterly/yearly files should contain a "stats strip" that breaks
  down the working time for the given time period.
- We should try to automatically summarize the units/parts that make up the whole of
  each of these files. For example, quarterly files should ideally show some kind of
  breakdown of each week.
- I'm also open to making it a routine to have an LLM / agent enrich these
  weekly/quarterly/yearly files with appropriate contents.
  - To support this use-case, each of thee files should be pre-generated with the
    appropriate instructions so an agent who is asked to update its contents doesn't
    need much more instruction than that.
  - Think hard about what instructions each of these (weekly/quarterly/yearly) files
    should contain.
  - We should update the weekly review task in the ~/bob/gtd_daily.md file and add
    appropriate quarterly/yearly tasks to that file.
- We should add a new glossary term for "stats strip" that adequately describes its
  relation to other existing glossary terms (for example, the "day strip" is the stats
  strip used for daily files).
- Review the period_note_tree_and_stats_strips.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.34.linker

## Response

Reading the research report first; the research sidecar isn't cloned in this workspace yet, so I'm opening it through `/sase_repo`.

Now the bob-cli code structure around stats and the CLI.

Still grounding the plan: I've reviewed the Day strip contract and the stats engine. Now checking the vault templates, `gtd_daily.md`, and the plugin's day-strip files.

Still exploring before writing the plan: now checking how `bob` registers commands and help sections, plus the nightly job.

Nearly done exploring. Before writing the plan, I'm loading the memory-write rules, because the plan adds glossary strands and decision records.

Exploration is done. Next I'll check an existing epic plan for house format, then write the plan.

Design is settled. Next I'll check the plan schema with the validator, then write the full epic.

Writing the epic plan now. It has nine phases, with the design contracts specified up front so each phase agent can work from them.

Validation passed with no warnings. Checking two numeric claims in the plan before revalidating.

Revalidation passed. Submitting the plan.

I've written the epic plan and submitted it for your approval. It passed validation with no warnings. Nothing has been implemented yet; work starts when you approve it. It builds on the research report's design and fills in the details the report left open.

**The tree.** Daily notes get their ISO week note as parent (`2026/2026-W45.md`). Weeks link to whole-week quarters (`2026/2026-Q4.md`, 13 weeks, or 14 when the year has a W53). Quarters link to the year (`2026.md`), years to a new `all_time.md`, and that to `org.md`. Because every period is made of whole weeks, the numbers and reviews at each level always add up to their parent. Every note title prints its real dates, so you never have to decode ISO week numbering.

**Creating the notes.** bob creates each note one week ahead, and never edits a note that already has content. The Obsidian plugin triggers this when a daily note is created and once a day. A one-time migration (a dry run first, then one commit) creates the ISO 2026 tree, re-parents the 2024–2026 year notes and the 2026 daily notes, and adds a week link to each daily note's prev/next line. It checks that your Stats totals and attribution are unchanged before committing. Existing monthly notes are left alone, and the monthly and yearly templates are retired.

**Stats strips.** Each period note opens with a stats strip built from the same parts as the Day strip:
- the same five facts, totalled over the period and marked "so far" while it's open;
- a "typical" comparison against the same kind of period before it;
- root-parent and type bars;
- a row of columns, one per child (days of a week, weeks of a quarter, and so on).

bob supplies every number, so nothing numeric is ever stored in the note.

**Automatic summaries.** Below the strip, a live table gives each child one row: its working time, review state, and either its Headline or an automatic line such as "bob-cli 42% · sase 21%". Quarters are summarized by their weeks even if no agent ever runs.

**Agent instructions.** Each note ends with a folded callout holding complete, versioned instructions. I wrote the final text for the weekly, quarterly, yearly, and all-time versions. An agent told "Update 2026/2026-W45.md":
- gets every number and all the context it needs from one bob command;
- writes only the Review section, describing, linking, and asking questions, with no scores, praise or advice;
- saves through a bob command that enforces the Headline and word limits, and refuses to overwrite your edits or your Reflection.

**Rituals.** Weekly prune becomes the Monday **Weekly review**. New **Quarterly review** (first Monday of each quarter, from 2027-01-04) and **Yearly review** (second Monday of January, from 2027-01-11) tasks are added. Both recurrence strings get checked against the Tasks plugin before the rows are edited.

**Glossary.** New **Stats Strip** and **Period Note** terms; the **Day Strip** term is reworded as the stats strip of a daily note. Three decision records capture the long-lived policies.

The work is split into nine phases across bob-cli, bob-plugins, memory and the vault, with explicit dependencies so some can run in parallel. The last phase does the live rollout and captures screenshots.

Five choices are open for you at approval:
- **Weekly Days table** (default yes): weekly notes also get the per-day summary table. This goes beyond the report, which gave weeks only the strip's columns.
- **Pilot drafts** (default yes): the rollout drafts the 2026-W44 and 2026-Q3 Reviews as worked examples for you to correct.
- **Off-clock detail in agent inputs** (default counts by area only): the alternative also shows event titles.
- **Glossary edits** and **decision records** (both default yes).

**After rollout:**
- The Mac needs a bob update and `bob plugins sync` before its notes get created automatically and its strips render. The rollout will list the steps for you rather than install anything there.
- Your own `bob.md` tasks (`^wqy-stat-strips`, `^prev-next-links`) are left for you to close.
- Running agent drafts automatically on athena is filed as a follow-up, to switch on only after four pilot weeks in which you keep or edit at least half the drafts.
