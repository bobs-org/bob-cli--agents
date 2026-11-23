# Chat History - ace-run (1f8--plan)

- **TIMESTAMP:** 2026-11-23 03:54:13 EST
- **MODEL:** claude/opus
- **AGENT:** 1f8--plan

**Plan:** /home/bryan/.sase/plans/202611/task_reqs_criterion_diamond.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/task_reqs_criterion_diamond.md`

> # Plan: Task requirements wear the criterion diamond
> ## Context
> Bryan likes task requirements (epic `bob-cli-on`, now closed) but not how they look. A
> requirement is drawn as a depth-counted hash run (`⌗⌗`, `⌗⌗⌗`, `⌗⌗⌗⌗`). In Obsidian it
> reads as Markdown `##` / `###` headings. In the Mac capture panel it is grey monospace
> text that looks like broken, typed Markdown. He asked to change how requirements are
> displayed without changing how they behave, once `bob-cli-on` was complete, and asked
> the planner to lead the design: intuitive, reliable, and beautiful.
> Before starting any phase, read
> `research:202611/task_reqs_display_redesign/task_reqs_display_redesign.md` with

*See full plan file for details.*

## Prompt

%auto
#gh:gh_bobs-org__bob-cli I think I like the general direction of the task reqs feature, but the way that
we present them in Obsidian and in the capture panel (using `##`, `###`, etc...) is
pretty bad.

- Once the work associated with the bob-cli-on epic bead is complete, I would like to
  change the way that we display task reqs without changing the behavior of this
  functionality.
- Review the task_reqs_display_redesign.md file in the research sidecar repo for context
  and inspiration before planning. I agree with all of the requirements recommended in
  that research file (except for any sase memory file changes, which should only be
  implemented if I approve them or explicitly asked for them in this prompt), but keep
  in mind that you are responsible for planning and splitting up this work
  appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you help me implement this? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %wait(bead=bob-cli-on)

## Response

The bob-cli-on epic is already closed. Next I'll read the research report and the drawer-casing epic (bob-cli-ph) that's now in progress, then look at the current req rendering code.

Reading the detailed design spec sections (geometry, state styling, Mac, cards, wire values) from the companion reports.

Next I'll open the linked bob-plugins and bob-mac-capture repos and map every place reqs are drawn today across all three repos.

Inventory is complete across all three repos. Now checking a few specifics (copy strings, guard notices, key bindings) and the memory notes this work would make stale.

Memory check done: only the `glossary:task-requirement` strand describes the hash run. Now reading the drawer epic's Obsidian/Mac rendering design so the diamond composes with its drawer glyph.

Checking the existing refusal copy for tick attempts so the new click guard can reuse it rather than invent new wording.

Design is converging. Checking whether the real-Obsidian e2e harness can take screenshots (for a light/dark taste pass), then I'll write the plan.

The harness supports screenshot "look" tests, so I'll require a light/dark taste pass. One last check on the Rust requirement-state type name, then I'll write the plan.

Writing the plan now.

Validation passed on the first run. Tightening a few phrases (one stale internal reference, an empty "Cost" bullet, an out-of-scope memory clause), then revalidating.

Revalidated cleanly. Submitting the plan.

I've written a seven-phase epic plan for redrawing task requirements, and it's waiting for your review. Nothing in it changes how requirements behave, how they're stored, or how you type them.

**The look.** The research report's direction stands, with your answers to its open questions:
- A requirement gets one small diamond in place of its checkbox, the same size at every depth. Indentation alone shows nesting.
- The fill shows state: ◇ pending, ◆ met with its task, faded when moot or excluded, slashed when dropped, → when carried into its own task.
- In Obsidian the diamond takes its owner task's colour. On the Mac it's the standard task teal.
- In the Mac capture draft, the real `[ ]` stays visible as a teal chip, like the existing route and theme chips. The live preview, the Pull-In card and both successor cards draw the diamond from state that `bob` reports.
- Plain-text CLI output prints `◇`. The "met" line uses `✓` instead of a filled diamond, because `◆` already marks the default Pomodoro in the CLI.
- All seven display defects the research verified and left for this redesign are fixed (the eighth, the Mac caret reveal, is already gone).

**Design calls I added beyond the research:**
1. **Wait for the drawer epic's rendering phases (bob-cli-ph.7 and .8).** That epic is in progress and edits the same CSS, plugin code, preview data and Mac painting code. Its design already reserves the diamond for requirements next to its tray glyph for drawers, so the two should be tuned side by side. Please approve with `--wait 'bead=bob-cli-ph.7,bead=bob-cli-ph.8'`. The first phases also check this and stop if either is still open.
2. **The Mac draft never hides bytes.** Besides deleting the overlay, this removes the concealment code and the caret-reveal workaround the requirements epic added in its last commit, so there's less to break.
3. **The idle agenda gets the diamond too.** The research missed it: requirement rows there currently show as `[ ] text` bullets.
4. **Cards preview what you've staged.** Staging Drop slashes the row's diamond and staging Own task turns it to →, so the card shows what will land.
5. **Clicking a diamond in Obsidian never ticks it.** It shows a short notice explaining why (for example, that it's met when the task closes). Hovering shows a real tooltip.
6. **The diamond's colour always matches its owner's task mark.** Today's requirement colour misses two of the owner's type states.

**Phases** (the first three can start in parallel):
1. `glyph-contract`: the CLI strings, card JSON values and docs, with the plugin copies updated in the same phase so no test goes red.
2. `line-annotations`: `bob` marks which preview and agenda lines are requirements, so the Mac doesn't have to guess.
3. `obsidian-marks`: the diamond in notes, the display fixes, and light/dark screenshots for a look check.
4. `obsidian-cards`: the diamond on the Obsidian successor card.
5. `mac-editor`: the teal chip in the draft.
6. `mac-diamonds`: the diamond in the Mac preview, agenda and Pull-In card.
7. `memory`.

**Memory decisions for you:** rewriting the hash-run sentence in the Task Requirement glossary entry is on by default, because this work makes that sentence false. Adding a new decision record is off unless you opt in.
