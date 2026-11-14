# Chat History - ace-run (research.4m.linker.w0--plan)

- **TIMESTAMP:** 2026-11-14 09:32:13 EST
- **MODEL:** claude/opus
- **AGENT:** research.4m.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/bank_period_charts.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/bank_period_charts.md`

> # Plan: Bank Period Charts on period notes
> ## Summary
> This epic builds on the Bank Badge epic (`bob-cli-lh`). It implements the consolidated
> research report `research:202611/bank_period_charts/bank_period_charts.md`. Read it with
> `sase artifact read file:explicit:920f6a67957826ec9a8ee48e "<why>"`. Bryan accepted
> every requirement in that report (A1–A10). This plan is the binding contract. Where it
> refines the research, see [Design refinements](#design-refinements-over-the-research).
> The panel is a third sibling host inside the existing `bob-stats-strip` fence, after the
> strip host and the badge host. It appears on week, quarter, ISO-year, and all-time
> notes, and contains:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to improve upon the "bank badge" work (see the bob-cli-lh epic
bead for context) by adding an excellent set of new bank transaction visualizations to
each period note (daily files don't need this). I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you help me implement this? Review the bank_period_charts.md file in the research sidecar
repo for context and inspiration before planning. I agree with all of the requirements
recommended in that research file (but keep in mind that you are responsible for
planning and splitting up this work appropriately).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %wait(bead=bob-cli-lh.4) %w:research.4m.linker

## Response

I'm collecting context first: the Bank Badge epic and the bank_period_charts research report in the research sidecar.

Reading the closeout tale and badge plan next, then the current bob-cli and plugin code.

Still reading code: now the periods report/strip column logic to see how the work charts define child buckets.

Reading the plugin's bank badge and period-strip fragments now.

Next: how the period-strip fence builds hosts and how its Both/Roots/Types switch works, so the new panel can match.

Checking the plugin's tests, styles source, and the bank data service's refresh rules.

Reading the CLI rules and docs-workflow memory notes that will govern the new `bob bank report` flag.

Checking whether bob-cli validates `stats.*` config keys (affects where `stats.bank_period` must be registered).

Now checking the plan schema (including whether an epic can wait on the in-flight badge closeout) via `--explain` on a stub.

The badge closeout coder (`bob-cli-lh.land--code`) is still running, so phases will need a start gate. Next I'm loading the memory-write rules, since the plan may propose a glossary term.

Design is taking shape. A few more facts to pin: an existing screen-reader-only CSS class, how mixins are wired, and the strip's caption/label helpers.

Since the plan will fix chart marks and colors, I'm loading the dataviz skill before committing to those choices.

I have what I need for the design. Two quick fact checks before writing: period-note path format and how the strip formats day captions.

I've finished the research and have a full design. Writing the epic plan now (5 phases: bob report aggregate, plugin decoder/model, painter/styles, hosts/lifecycle, docs).

Validation passed. Re-running without `--explain` as the skill requires.

The proposal is staged. Finishing the turn through `/sase_final`.

I've written and submitted an epic plan for Bank Period Charts. It passed validation and is waiting for your review; no code has changed yet.

**What you'll see:** on every week, quarter, year, and all-time note, one compact read-only panel sits right below the Bank Badge, inside the existing `bob-stats-strip` fence. Existing notes get it with no edits. Daily notes stay badge-only. The panel has:
- **In / Out:** when money moved, on the same child axis as the work charts above it.
- **Out by category:** ranked bars, top five plus `N more`. Unclassified and Cash out always show when nonzero.
- **Not counted:** one optional quiet line for transfers, uncategorized inflows, and cash traced.

**Phases** (the first two run in parallel):
1. **`report`** (bob-cli): adds `bob bank report -c/--charts`. Per-period money comes from the same accounting path as the existing totals, and tests check that the parts add up to the totals exactly. The child periods come from the same calendar code as `bob periods show`. Days not yet imported or not yet tracked are marked as such, never drawn as $0.
2. **`model`** (plugin): strict decoding plus a pure model of what to show. The plugin never adds up money.
3. **`paint`** (plugin): the panel's look, keyboard navigation, screen-reader tables, and light/dark × narrow/wide preview screenshots.
4. **`hosts`** (plugin): mounting, the `stats.bank_period` switch, and navigation that never creates or edits a note. It also checks the plugin against real JSON captured from the new bob, then deploys.
5. **`docs`**: contract and config docs, plus follow-up notes for re-scoping the `bob-cli-ku` bank-trial follow-up and a better coverage check.

**Where I changed the research, deliberately:**
- **One zero line on every grain.** Money in sits above the line in green and money out hangs below in neutral ink. Weeks show paydays as markers so they don't flatten the daily bars. This keeps money columns from looking like the work columns directly above.
- **bob totals the `N more` category row and the quarter columns** used on narrow year views. That keeps the "plugin never adds money" rule strict.
- **The panel never repeats the badge.** Waiting and coverage appear in it only if you turn the badge off.
- **No one-bar charts.** For example, the all-time note shows categories only during its first quarter.
- **The panel fetches separately from the badge.** An older bob or a bad payload can never take the badge down. The cost is one extra bob call per visible period note.

**Timing:**
- **Start gate:** the badge closeout is still running and touches the same files, so the first two phases wait until `bob-cli-lh` is closed.
- **Release lag:** the installed bob (0.5.0) doesn't have the new flag yet. Until the daily release ships it, the panel stays hidden and logs one console warning.
- **Previews:** apollo has no Chromium, so the preview screenshots only run on a machine that does.

**Your call at review:** two glossary edits are off by default because you didn't explicitly ask for memory changes. One adds a Bank Period Charts glossary term; the other adds one linking sentence to the Bank Badge term. Turn them on if you want them.
