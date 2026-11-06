# Chat History - ace-run (research.3c.linker.w0--plan)

- **TIMESTAMP:** 2026-11-05 10:01:45 EST
- **MODEL:** claude/opus
- **AGENT:** research.3c.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/offclock_types.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/offclock_types.md`

> # Plan: `offclock_types`, off-clock by area and task type
> Research:
> `research:202611/offclock_types_area_type_clock/offclock_types_area_type_clock.md` (read
> it with `sase artifact read`). Bryan accepted all of its requirement adjustments (A1–A6)
> and answered its open questions as follows: MEET is the only listed type, re-stamps use
> the narrow scope, and hand-written untyped events stay on-clock until they are typed
> MEET. The sibling link-budget work (`1a5c9b00`, `plan_budget/off_clock.rs`) already
> resolves links through `effective_clock`, so it picks up this feature with no further
> change.
> ## Contract (every phase implements or documents this)

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli We already support the `offclock` boolean area note / project note file
frontmatter field to specify that all tasks in an area/project, recursively, should be
treated as offclock. I would now like to add support for a new `offclock_types` property
that takes a list of task type names as values. Can you help me implement this?

- This field should work just like `offclock`, but only tasks which have one of the
  types listed by this field should be treated as offclock.
- As our first use-case I would like to migrate the area notes in my Obsidian vault that
  currently use `offclock` to start using `offclock_types` instead, with MEET being the
  only task type that they filter for.
- Review the offclock_types_area_type_clock.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.3c.linker

## Response

Reading the `offclock_types_area_type_clock.md` research report first, then I'll look at the current `offclock` code.

Still mapping the clock callers. Next I'm checking whether the link-budget commit that just landed uses `effective_clock` or only the tag check.

Rust side is mapped; the link-budget commit already uses `effective_clock`, so research item 10 is done. Now I'm checking the Obsidian plugin's copy of the clock logic in bob-plugins.

Both plugin copies of the shared clock vectors match bob-cli. Now I'm checking how the plugin works out a task's effective type, since the clock will now depend on it.

Mapping the naming/retype paths now; these need a clock re-stamp once type affects the clock.

Next I'll read the memory records that govern the release train, the off-clock decision, and vault editing, since they decide how the migration can be staged.

Next I'll load the memory-write skill, because the plan adds a decision record and updates glossary terms.

Last checks before writing: which repo owns the off-clock chip docs, and whether `bob --version` reports a commit SHA (useful for confirming host upgrades before the cutover).

Starting the plan now. First I'll get the expected epic schema from the validator.

I can fold memory changes into two decisions, since one memory decision may cover several notes, which stays under the five-decision cap. Next I'm checking the repo's own verification commands.

I have what I need. Writing the epic plan now: six phases, one cutover decision, and two memory decisions.

The `ask` contains a colon, so I'll quote it.

Validation passes with no warnings. Submitting the plan.

I've written and submitted an epic plan for `offclock_types`. It passed validation with no warnings and is staged for your approval. I haven't changed any code, memory, or vault files yet.

**How it behaves**
- `offclock_types` goes on area and project notes and is read on the same walk up the note tree as `offclock`.
- `#on` and `#off` on a task still win.
- Otherwise the nearest note on the walk that sets either key decides:
  - With a valid list, a task is off-clock only if its type is listed. Any other type is on-clock, and the walk stops there; a parent's `offclock: true` is not consulted.
  - "Type" means the full inherited chain, including closed tasks: the task's own field, then the reading rule, then the nearest note's `task_type:`, then `plan.default_type`.
- If a note has both keys, the list wins. A stats-only `note_offclock_shadowed` warning reports it, which makes the two-step vault migration safe.
- `[]`, a blank value, `null`, or a lone `-` count as no setting. Any bad item makes the whole key invalid, which means on-clock plus a warning that names the key.

**Phases**
1. **`clock-type-filter`** (bob-cli, medium): parse the key, give the type pill and the clock one shared type lookup, apply the new rule in the clock lookup, add the new warnings, and update the docs. The shared clock test cases gain a `config` field, so cases can set `plan.default_type`, plus about 16 new cases.
2. **`clock-surfaces`** (medium): `bob gcal list` currently checks the clock with a made-up task line that has no type, so after migration it would show love events as on-clock while sync writes them off-clock. This phase fixes that. It also makes naming a running Pomodoro, or a `#type` that renames it, recompute its on/off-clock stamp in the same write.
3. **`type-rename-coverage`** (medium): `bob types rename` also rewrites the lists and removes duplicates when two types merge; `split` reports lists it leaves behind.
4. **`plugin-mirror`** (bob-plugins, medium): the Obsidian copy of the clock logic gets the same rules, and both plugins' test-case copies are updated byte for byte. Obsidian's own Pomodoro naming has no clock logic today, so that phase records re-stamping there as a follow-up rather than building it.
5. **`memory-records`** (small): a new decision record that partly supersedes `off-clock-follows-tag-then-note-default`, plus updates to four glossary terms.
6. **`vault-migration`** (small): record the current clock-drift count, then add `offclock_types: [MEET]` to `love.md` and `body.md` alongside `offclock: true`. It also makes the property a list in Obsidian and checks the result with a bob built from the workspace.

The commit that just landed for the link budget already uses the full clock lookup, so it needs no change.

**Decisions for you at approval**
- **`cutover`**, meaning when `offclock: true` is removed from the two notes. The default is **gate**: a confirmable command waits until you've run `just install-all` on athena, apollo, and the Mac, so a host still on old code doesn't record love and body meetings as Worked. The alternatives are a follow-up for later, or removing it immediately.
- **Two memory decisions**, both defaulting to yes, because the planned work would make the current memory text inaccurate.
