# Chat History - ace-run (research.37.linker.w0--plan)

- **TIMESTAMP:** 2026-11-04 08:42:37 EST
- **MODEL:** claude/opus
- **AGENT:** research.37.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/move_choice.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/move_choice.md`

> # Plan: Choose parent tasks to move in with a `- ^^` capture bullet
> Research: `research:202611/parent_task_move_choice/parent_task_move_choice.md`. Bryan
> accepted every requirement it recommends (A1–A12). This plan turns that report into a
> contract and splits it into phases. §2.2 lists where this plan goes beyond the report.
> It extends the shipped move-bullet work of epic `bob-cli-gl`
> (`plan:202611/capture_move_bullets.md`); every rule of that contract still holds unless
> this plan says otherwise.
> ## 1. The experience
> You are carving a project for leaving Google out of `cash`, a 25-task area. You know one
> task by name and want to see the rest:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to add support for a new `^^` capture syntax that can be used with
the `@foo[^:]bar@` syntax. Can you help me implement this?

- See the bob-cli-gl epic bead for context on the recent support we added for pulling in
  child tasks from the parent project when using the `@foo[^:]bar@` syntax.
- When `^^` is found as the only contents of a capture bullet using this syntax, we
  should prompt the user to select one or more tasks from the parent project after they
  submit the capture.
- The selected tasks will be added as `^foo` / `:foo` bullets as if the syntax
  introduced by the bob-cli-gl epic bead was used directly.
- This task prompt should take inspiration from the successor prompt I'm thinking, but
  keep in mind that we need a way to support `:` as well as `^` (and not selected, which
  should be the default).
- Review the parent_task_move_choice.md file in the research sidecar repo for context
  and inspiration before planning. I agree with all of the requirements recommended in
  that research file (but keep in mind that you are responsible for planning and
  splitting up this work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.37.linker

## Response

I'm collecting context: I've read the bob-cli-gl epic, and next I'll read the research report and the move-bullet code it builds on.

I'm reading the `bob capture` planner next: where pull-in answers are resolved and where project-note moves run. That's where the `^^` choice will plug in.

Still mapping the code. Now reading how the two parsers claim move bullets, so the `^^` arm fits into the same path.

I have the bob-cli picture. Now opening the Mac app repo, since the Move card lives there.

The Mac side is mapped: no generic choice card exists, and the Move picker currently drops `action_continuation_keys`. Next I'm checking the docs layout and the plan schema.

I'll author one decisions-web record under a memory decision, defaulted on with your quote. Next I'm checking the successor-offer key scheme and the ID-minting helper the plan will reuse.

I'm settling the design details now: the per-row consequence rule, mark persistence, and the phase split. Next I'm checking how the renderer numbers move slots, so `^^` picks can share one slot.

I have everything I need. Writing the epic plan now: 8 phases, 5 for bob-cli and 3 for Bob Mac Capture, plus one memory decision.

Validation passed on the first try. I'm making three small fixes: correcting the `^` heads in the consequence table, tightening the predict/describe equality rule, and adding the decision callout.

The plan validates. Submitting it for review now.

I've proposed an epic plan for `- ^^` and it's staged for your review. Nothing starts until you approve it, and no code has been written yet. It validated cleanly and follows the research report's twelve requirements, with a few design calls of my own, listed below.

**How it works for you**
- Typing `^` again in the `- ^` picker closes it and leaves `- ^^`. Today the second `^` is swallowed by the picker's filter.
- When you press Return, a Move card opens before anything is written, built from the live preview.
  - Each row shows the sigil it would get if you had typed it: `·` leave (the default), `^` move, `:` move & link.
  - Pressing `^` or `:` sets the highlighted row and moves down a row; Space toggles leave/`^`; ⌘A marks the visible rows.
  - Return with nothing marked does nothing; ⇧↩ means "move none"; ⎋ returns to the draft and keeps your marks.
- Your picks land where the `^^` line sits, in the parent note's order. They produce exactly what typed `- ^id` / `- :id` bullets would. Tasks without a block ID get one in the same write. Everything goes through one `bob capture --move-in` call.
- From a terminal, a dry run lists numbered rows. A real run with an unanswered `- ^^` always refuses until you pass `-m 1,:3` or `-m none`.

**Design calls beyond the research**
1. **Both `^` and `:` on every movable row.** Choosing `:` always does exactly what a typed `- :id` would, and its text says what will happen, e.g. "stays unlinked until the project starts Nov 6". The research instead dropped `:` for projects with a future start date. The "links today" counter counts only picks that really add a link.
2. **One shared builder for the consequence text.** The new card, the existing `- ^` picker, and the dry-run report all use it. This also fixes two bugs in today's picker: it says "becomes Next" for In Progress tasks, and it promises a link to Blocked tasks.
3. **Marks are remembered per parent note,** so you can press ⎋, fix a typo, and press Return without losing your choices. Rows already moving through an explicit `- ^id` show that sigil dimmed and can't be changed.
4. **The work is split finer than the research suggested.**

| Phase | Repo | Size | Depends on |
| --- | --- | --- | --- |
| `contract` (docs, conformance cases, decision record) | bob-cli | medium | — |
| `cli-grammar` (parsing `^^`, picker key, grammar bump) | bob-cli | medium | `contract` |
| `cli-consequence` (shared consequence text) | bob-cli | medium | `contract` |
| `cli-report` (the report, `-m`, refusals) | bob-cli | medium | `cli-grammar`, `cli-consequence` |
| `cli-execute` (ID minting, placement, output) | bob-cli | medium | `cli-report` |
| `mac-draft` (typing `^^`) | Bob Mac Capture | small | `cli-grammar` |
| `mac-card` (the Move card itself) | Bob Mac Capture | medium | `cli-report` |
| `mac-flow` (wiring into submit, Pull-In, refusals, docs) | Bob Mac Capture | medium | `cli-execute`, `mac-draft`, `mac-card` |

**Things to know when you review**
- **One decision for you:** whether `contract` adds a new record to the `decisions` memory web, as the research recommends. It defaults to yes, quoting your "I agree with all of the requirements…" line, so turn it off if you didn't mean that to cover memory.
- **Overlap with bob-cli-go:** that transfer epic (phases go.10–12) is still in progress and touches the same parser, editor spans and grammar version. Phase dependencies can't reach outside this epic, so the plan tells each phase to rebase onto bob-cli-go and compute the grammar bump from the current value.
- **Temporary refusals:** until `cli-execute` lands, `bob capture` refuses `^^` drafts at the in-between stages without writing anything.
- **Walkthroughs you'll likely do:** `mac-flow` should finish with three real-card walkthroughs. I expect no agent can drive the Mac UI, so you'll probably do those yourself.
