# Chat History - ace-run (1b3--plan)

- **TIMESTAMP:** 2026-11-11 05:40:22 EST
- **MODEL:** claude/opus
- **AGENT:** 1b3--plan

**Plan:** /home/bryan/.sase/plans/202611/record_route_span_overlap.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/record_route_span_overlap.md`

> # Fix invisible `@dir/stem` drafts and missing record-update previews
> Typing `@eat/burger_bistro` in Bob Mac Capture (or accepting Burger Bistro from the
> `@eat/` list) washes the draft blue but shows no text. The footer says
> `Ignored malformed parse spans`, and no preview of the planned edit appears. Two repos
> change: **bob-cli** (this repo) and the linked **bob-mac-capture** repo. Open
> bob-mac-capture with `/sase_repo` and read its `AGENTS.md` before editing it.
> ## Diagnosis (verified)
> 1. **bob emits overlapping spans.** Commit `12641768`
>    (`feat(capture): parse existing record updates`) added an exception to `merge_spans`
>    in `src/native/capture_parse.rs`. The exception keeps the `record_stem` span nested

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I can't see the text when using the `@eat/burger_bistro` syntax in the
bob-mac-capture app. I'm also not seeing any preview of the changes that would be made.
See the ~/tmp/screenshots/20261111_052730.png screenshot for context. Can you help me
diagnose the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm tracing the "Ignored malformed parse spans" status in the Mac app back to the parse spans bob returns for `@eat/burger_bistro`.

Found the note in the vault; now reproducing bob's parse output for `@eat/burger_bistro` to see which spans the Mac app is rejecting.

Now checking what bob's dry-run preview returns for this draft, and how the Mac gates the live preview.

Bob's dry-run preview for the record update works fine from the CLI, so the missing preview is on the Mac side. Checking how the panel decides between the record card and the preview card.

I have the full diagnosis. Writing the plan now.

The plan passes validation. Submitting it.

I found the cause of both problems. The plan to fix them is submitted for your approval, and no code has changed yet.

## Root cause

**1. bob sends the Mac app overlapping highlight ranges.** For each draft, bob reports byte ranges (spans) that tell the app what to color. The help for `bob capture-parse` says these never overlap. But commit `12641768` (`feat(capture): parse existing record updates`, Nov 9) changed `merge_spans` in `src/native/capture_parse.rs` so the stem's span stays nested inside the route's span:

```
bob capture-parse -f json -- '@eat/burger_bistro'
  record_route 0–18
  record_stem  5–18   ← nested inside the route
```

Any `@dir/` route with a stem does this, including `@eat/^custom-stem`.

**2. The Mac app rejects every span and skips the repaint.** It requires spans that don't overlap. When it gets these, it shows "Ignored malformed parse spans" and returns without clearing the previous coloring.

**3. That's why the text is invisible rather than just uncolored.** While the draft is `@eat/`, the app hides the `@` (clear text color) so the 🍽️ emoji can sit in its place, and adds the blue background. Picking Burger Bistro from the list replaces bytes 0–9, so the new text copies the `@`'s clear color and blue background. Lines you type after it copy it too. Every later parse is rejected, so nothing ever repaints. That gives the blue, empty draft in your screenshot.

**4. Why there's no preview.** bob's dry run is fine: it reports `kind: record_update`, with your note marked as an added line. The Mac side has two gaps:
- The Record Card takes the preview's spot, so the preview is hidden until you press Escape.
- After Escape, the app only uses the record preview for *new* records. Updates fall back to a generic view showing just the title and path. A "phase 12" comment in the code marks this as never finished: the before→after rows were built but never connected for updates.

## The plan (one agent, medium size)

- **bob-cli:** a route with a stem reports one span covering the whole token again. Tests will check that record spans never overlap.
- **Mac, safety net:** when the app rejects spans, it clears the old coloring, so text stays readable even if bob breaks this again.
- **Mac, update preview:** updates use the record preview, showing only the fields that changed (before → after) and the lines being added. The "View Markdown" section stays.
- **Mac, tests and docs:** new test data for record updates, generated from the fixed bob; a test that every record test file passes the overlap check; and updated Mac docs.

**One decision for you, `card_changes` (default: on):** should the Record Card itself list the planned changes, so you see them without pressing Escape? I set it on because Return can capture straight from the card without you ever seeing the preview.

The bob fix lands first, since the Mac test data comes from it. Until bob's next daily release, the Mac fix alone gives readable but uncolored text for these drafts.

Not covered: records inside `%t` templates have a similar overlap of their own. The plan has the agent check it after the fix and file a task if it's still broken.
