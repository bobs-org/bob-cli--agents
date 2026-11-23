# Chat History - ace-run (fr--plan)

- **TIMESTAMP:** 2026-11-23 11:41:27 EST
- **MODEL:** claude/opus
- **AGENT:** fr--plan

**Plan:** /home/bryan/.sase/plans/202611/links_stage_event_tasks.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/links_stage_event_tasks.md`

> # Links stage: link to Event Tasks in daily notes
> ## Context
> **What the screencast shows.** On the job note's `Notion Software Engineer…` task,
> `Ctrl+Shift+L` opens `🪢 Links · …` ("searching 5115 tasks"). Typing `derrick blake`
> never surfaces today's meeting `1500-1530 Bryan Bugyi and Derrick Blakely`. That meeting
> is an Event Task in `2026/20261123.md`. Paging with `Ctrl+N` shows only unrelated
> subsequence matches.
> **Root cause.** The Links stage lives in bob-plugins `plugins/bob-navigation-hotkeys`.
> In `src/304-relation-stage-view.js`, `isRelationStageExcludedPath` drops every
> `YYYY/YYYYMMDD.md` path. Both pool builders call it:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me start showing event tasks in daily files from the linker panel
so we can link to them from other tasks? See the ~/tmp/screencasts/20261123_112516.mp4
screencast for context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

The screencast shows ⌃⇧L opening the linker on a job-note task, then a search for "derrick blake" that pages with ⌃N. I'm reading the frames now.

I found the Links panel source in `bob-navigation-hotkeys`. Next I'm tracing how it builds its task pool, to see why Event Tasks like the 1500-1530 Derrick Blakely meeting are left out.

Still mapping how bob scopes "active notes" for the reverse-link mirror. Once I know whether older daily notes count, I'll write the plan.

I'm sampling the vault's daily notes to separate real Event Tasks from other legacy `#task` lines. The panel should pick up only the meetings, not old daily-note clutter.

I'm checking where the Links panel's task cache comes from. It has to carry each row's `## Events` heading, or the panel can't tell a meeting from other daily-note tasks.

Capture's `~` relation target already accepts daily-note tasks. The gap is in the Obsidian plugin only. I'm checking where the Links-stage pool contract is documented.

I'm checking whether Bob Mac Capture's `~` picker lists Event Tasks today. If it doesn't, that's a separate gap I'll mention, not fold into this plan.

I have the full picture. I'll take one quick look at the canonical comparator so the ranking change in the plan stays a consistent sort order, then write and validate the plan.

The plan passes validation. I'm submitting it with `sase plan propose`.

The plan has been submitted and is waiting for your approval in the PlanApproval gate. Nothing has been changed in either repo yet.

**Why Event Tasks are missing:** the `Ctrl+Shift+L` Links panel lives in bob-plugins (`bob-navigation-hotkeys`). `isRelationStageExcludedPath` in `src/304-relation-stage-view.js` drops every `YYYY/YYYYMMDD.md` note from the search list. So typing `derrick blake` can never reach `1500-1530 Bryan Bugyi and Derrick Blakely`, and `⌃N` pages through unrelated loose matches. Nothing else needs fixing: bob already accepts relation targets in any daily note, and gcal sync keeps LINKS lines under Event Tasks. No bob-cli code changes.

**What the plan does:**
- **Event Tasks join the search:** rows in a daily note's `## Events` section that start with `**HHMM-HHMM**` become linkable. Other daily-note tasks, like the `^gtd` rows and old ledger rows, stay out.
- **Clean names:** rows read `1500-1530 Bryan Bugyi and Derrick Blakely` with their day, not the raw line with gcal URLs. The URLs also stop producing false matches, and typing `events derrick` narrows the list to meetings.
- **Ranking:**
  - When matches score equally, past meetings list newest day first.
  - With an empty search box, only today's open meetings show, so past ones don't pile up.
- **Linked from is unchanged:** it still doesn't offer daily-note tasks, consistent with capture's `~~`, which refuses them.
- **Yesterday's note:**
  - Linking to a meeting there works, but its reverse ("linked from") line can't be written yet because that note is read-only.
  - The notice will say so instead of the current, misleading "archived" wording.
  - Bob adds the reverse line once that note is no longer the previous day's.
- **Docs and tests:** new behaviour rules (LG25–LG29) go in bob-cli's `docs/task-relations.md`; the plan also updates the plugin docs, adds tests, and finishes with `bob plugins sync`.

**Three choices for you at approval**, with my defaults:
- **`daily_scope`:** only Event Tasks (default), or every daily-note task, which is what Mac Capture's `~` picker lists.
- **`day_window`:** meetings from every past day (default), or only today, future days and the last 30 days.
- **`chip_names`:** link chips also show meetings as `HHMM-HHMM Title` (default). This fixes the `1100-1130 Phone Call w/ Dan [📅](https:/…` chip in your screencast.
