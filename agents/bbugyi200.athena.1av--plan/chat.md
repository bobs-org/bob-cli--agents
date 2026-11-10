# Chat History - ace-run (1av--plan)

- **TIMESTAMP:** 2026-11-10 08:04:30 EST
- **MODEL:** claude/opus
- **AGENT:** 1av--plan

**Plan:** /home/bryan/.sase/plans/202611/dot_alias_prefers_dependency_once_routed.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/dot_alias_prefers_dependency_once_routed.md`

> # Spaced `.` prefers `&` once the item is routed
> ## Goal
> In Bob Mac Capture, typing `.` after a space or tab should give `&` (Depends On), not
> `@`, when the capture item already has a route marker such as `@foo:bar`, `@foo^bar`, or
> `@foo+bar`. Bryan rarely uses multi-target bulk capture (`@a:x @b:y`), so after a route,
> `&` is the character he actually wants. bob makes this choice and the Mac app only
> applies bob's edit ([[decisions:mac-capture-is-a-thin-client]]), so this is a bob-cli
> change. The Mac app's Swift code does not change; only its docs do.
> ## Root cause (confirmed with `bob capture-rewrite` / `capture-complete`)
> `expand_sigil_alias` in `src/native/capture_language/rewrite.rs` tries `.` aliases in

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli The `.` to `&` capture alias isn't working as expected in the bob-mac-capture
app. Namely, when typing `.` after a space in the app and a `@foo[:^+]bar` reference
already exists, the `.` alias should expand to `&` instead of `@`. Even though another
`@baz[:^+]buz` reference is supported it is not common for me to use this type of bulk
capture and the `.` alias is meant to always expand to the most intuitive/desirable
character based on the context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the capture alias rewrite code (`src/native/capture_language/rewrite.rs`) to see why a spaced `.` turns into `@` instead of `&` when the item already has a `@route:id` marker.

Still exploring: the fix is a precedence change in the spaced-`.` alias lane. I'm now checking which parse API can tell whether the current line already carries a route marker.

I've located the rule and every doc/help/memory surface that describes it. Now checking the docs conventions and the Mac Capture side so the plan covers both repos correctly.

I'm checking the Bob Mac Capture repo for docs or tests that describe the old `.`→`@` precedence, so the plan covers both repos.

Nearly done exploring — confirming the tip-test layout, then I'll write the plan.

Now writing the plan file.

The plan validates; I'm clearing one remaining coverage warning by naming the memory strand by its selector instead of its file path.

Validation passes with no warnings. Submitting the plan.

I wrote and validated a plan for the fix and submitted it with `sase plan propose`. It is staged for your review; no code has changed yet.

**Why it happens:** I reproduced the bug with the installed `bob`. In `src/native/capture_language/rewrite.rs`, a spaced `.` always tries `@` before `&`. After a route at the end of a line, typing another `@` would open route completion, either to add a second target (`@a:x @b:y`) or to replace a bare `@foo`. So `@` wins and the `&` option is never reached:

| Draft | Today | Expected |
| --- | --- | --- |
| `Buy milk @foo:bar .` (also `^bar`, `+bar`) | `@` | `&` |
| `Buy milk @foo:bar` + child line `- detail .` | `@`, which is then a duplicate-marker error | `&` |
| `@foo:bar Buy milk .` (route at the start) | `&` | already correct |

**The plan (small, size `medium`):**
- **The rule:** if the capture item already has a complete route marker, `.` tries `&` first and falls back to `@` only where `&` can't open.
- **When `@` still wins:**
  - an unrouted item: `Buy milk .`
  - `>` transfer lines and `<` merge slots
  - a draft-wide `@@route` declaration
  - a separate blank-line item
  - a `@foo:bar` in the middle of a line, which bob already treats as plain text
- **To add a second target on purpose,** type `@` directly.
- **Typing tips** come out right on their own, because bob works them out by running the same rewrite.
- **Tests:**
  - unit tests for both outcomes
  - tip tests
  - a CLI test for `capture-rewrite`
- **Docs:** the `capture-rewrite` help text and `docs/capture.md`, plus the generated reference pages.
- **Bob Mac Capture:** no Swift changes. Three doc passages that describe the old order get corrected: `relationship-pickers.md`, `keyboard.md` and `capture-panel.md`.

**Two decisions for you at approval:**
1. **`routed_scope`** (default `any_route`): should a bare `@foo` or `@foo#section` also switch `.` to `&`, not just `@foo:bar`, `@foo^bar` and `@foo+bar`? Today `Buy milk @foo .` gives `@`, and picking a route then quietly turns `@foo` into plain text. The cost is that a name like `Ping @alice .` would also give `&`.
2. **`memory_glossary_capture_alias`** (default yes): update the glossary's capture-alias entry, which currently says `.` gives `&` only when no `@` alias applies. That will be false once this ships.
