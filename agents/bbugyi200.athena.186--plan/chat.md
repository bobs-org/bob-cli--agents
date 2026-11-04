# Chat History - ace-run (186--plan)

- **TIMESTAMP:** 2026-11-04 14:18:05 EST
- **MODEL:** claude/opus
- **AGENT:** 186--plan

**Plan:** /home/bryan/.sase/plans/202611/goto_completed_only_toggle.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/goto_completed_only_toggle.md`

> # Go To picker: Command-X switches between open and completed tasks
> ## Context
> Epic `bob-cli-h3` (plan `plan:202611/goto_completed_toggle.md`, now closed) added
> **Command-X** to Bob Mac Capture's Go To picker (`/`, or `\` on a blank draft). Today
> the toggle switches between:
> - **off:** open tasks only, from `bob capture-complete --all-tasks … -- '/'`;
> - **on:** open tasks **plus** a trailing **Completed** section, from the same call with
>   `-C`/`--closed-tasks`.
> Bryan wants the on state to show **only** completed tasks. Command-X should flip between
> two disjoint views: open tasks only, and completed tasks only.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you actually make the `<cmd+x>` keymap toggle between not showing done
tasks and only showing done tasks? It currently toggles between not showing done tasks
and showing all tasks. See the bob-cli-h3 epic bead for context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the h3 epic and its plan. Next I'll go through the bob-cli and Mac app code behind the Command-X toggle and then write the plan.

I've read the Mac picker's grouping, ranking, caption, and hint code. Next I'm checking its panel-model toggle handling, docs, and test fixtures.

Both sides are mapped. Now I'm reading bob-cli's `--closed-tasks` tests and docs so the plan names exact edits.

Bob-cli and Mac are mapped; I'm checking a few remaining doc references before writing the plan.

I have what I need. Writing the plan now: bob's `-C` will return only closed rows, and the Mac Command-X will switch between the open and completed views.

I wrote a plan for this change. It passed validation and is now staged for your approval as a single-agent medium plan. Nothing has been implemented yet.

**What the plan changes:** Command-X in the Go To picker will flip between two views that never overlap: open tasks only, and completed tasks only.

**How it gets there:**
- **bob-cli first.** `bob capture-complete -C`/`--closed-tasks` will return completed tasks *instead of* open ones, rather than adding them after the open list. Without the flag, the output stays exactly as it is today.
  - The fix belongs in bob because the Mac app is meant to only display what bob returns. Filtering on the Mac side would leave bob with a mode nothing uses.
  - Changing what the flag means is safe: it was added today and hasn't been in any release yet (the latest is v0.4.0 from Oct 27). The implementing agent will re-check that before committing.
- **Mac app second.** The app still sends the same flag. Only its wording changes:
  - Header: `Go To · + Completed` becomes `Go To · Completed`.
  - Footer hint: `⌘X Hide Completed` becomes `⌘X Show Open`.
  - Screen-reader text and status messages change to match.
  - The plan also covers test fixtures and tests, the Mac docs, and a duplicated `## Go To Picker` heading in `docs/task-pickers.md`.
- **Unchanged:**
  - Completed tasks still come from the whole vault, including archives in `done/`.
  - Canceled tasks still appear, as you chose for that epic. I read "done tasks" in your request as both done and canceled tasks, so say so if you want canceled ones left out.
  - Each new Go To session still starts on open tasks, and Escape and reopening still keep your current choice.

**Two gates already fail on master for reasons unrelated to this work.** The plan tells the implementer not to fix them here, so each will still fail after this lands:
- `just docs-check` fails because `docs/develop/decisions.md` is out of date, which is already tracked on bob-cli-b6.
- `cargo fmt --all --check` fails on unformatted files that belong to the open bob-cli-h2 epic.
