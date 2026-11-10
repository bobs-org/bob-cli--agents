# Chat History - ace-run (1am--plan)

- **TIMESTAMP:** 2026-11-09 17:45:26 EST
- **MODEL:** claude/opus
- **AGENT:** 1am--plan

**Plan:** /home/bryan/.sase/plans/202611/dot_block_id_separator_toggle.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/dot_block_id_separator_toggle.md`

> # Glued `.` toggles the block-ID separator (`@route:id.` ↔ `@route^id`)
> ## Goal
> Make `.`, the easy-to-reach alias key for `^`, toggle a complete block-ID marker's
> separator between `:` and `^` when it is typed right against the ID:
> - `Create sase-gallery … @sase:sase-gallery.` →
>   `Create sase-gallery … @sase^sase-gallery`
> - `@sase^sase-gallery.` → `@sase:sase-gallery`
> - sealed project-note forms: `@route:id@.` → `@route^id@`, `@route^id@.` → `@route:id@`
> Today the `.` stays literal (`bob capture-rewrite` answers `changed: false`). It ends up
> inside the ID, and the preview fails with "Pomodoro capture block ID must be non-empty

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make it so the `.` capture alias can be used instead of `^`/`:`
at the end of a `@foo[:^]bar` token to toggle the `^` to/from `:`? For example, in the
~/tmp/screenshots/20261109_154240.png screenshot, `@sase:sase-gallary` should have been
transformed to `@sase^sase-gallary` when the `.` was typed.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Exploring the capture rewrite code: the existing `^`/`:` separator toggle is in `src/native/capture_language/rewrite.rs`. Next I'm checking how a `.` could reuse it.

Checking the Mac capture app's handling of `capture-rewrite` results, to see whether the change can stay in bob-cli only.

Still checking which keys make the Mac app call `capture-rewrite`. After that I'll write the plan.

Confirmed the Mac app already sends `.` through the rewrite lane and applies `switch_block_id_separator` replies for any key. Checking a few edge cases before writing the plan.

Mac docs are mounted from the bob-mac-capture repo, so any Mac doc edits belong there. Now looking at the existing separator-toggle tests so the plan can point at them.

I have what I need for both repos. Writing the plan now.

Validation wants `title`/`goal`, and yes/no decisions written as toggles (boolean defaults, no `choices:`), with the memory decision using a `memory:` selector. Fixing those.

Plan validates, with one remaining warning about the memory-decision selector. Tracking that down before proposing.

Plan validates with no warnings. Proposing it.

I've written the plan and submitted it for your approval. Nothing has been changed in either repo yet.

**The fix needs both repos.** In bob-cli, typing `^` right after `@route:id` already switches it to `@route^id`, but a `.` there stays literal and lands inside the ID. In your screenshot, though, the `.` never reached bob at all. Typing `@sase:` after task text opens the Block ID picker's New ID composer, and a non-ID character like `.` saves the typed ID and inserts the `.` straight into the editor ("type-through"). That path never calls `bob capture-rewrite`. So a bob-only change would fix typing straight into the editor, but not your exact case.

**The plan** (one coding agent, medium size):
- **bob-cli:** make a `.` typed against a complete marker flip the separator: `@sase:sase-gallery.` → `@sase^sase-gallery`, and `@sase^sase-gallery.` → `@sase:sase-gallery`. Sealed project-note markers (`@route:id@.` ↔ `@route^id@`) flip too. It goes into the existing separator-switch rule, the way `=` was added to the relation-direction flip. A glued `.` is never valid in an ID, so nothing is lost, and Undo in the Mac app still gives you back the literal `.`.
- **Mac app:** when the New ID composer types through a single `.`, `^`, `:`, `+` or `;`, send it through `capture-rewrite` like an editor keystroke, and bob decides what it does. With an older bob the key just stays literal.
- **Unchanged:** the other `.` shortcuts (`@errands.` → `@errands^`, `Buy milk .` → `@`, `@home .` → `&`, `- ^.` → `- ^^`) keep working. A `.` after `@route+id` stays literal; I decided that myself, since flipping an existing-task `+id` to `^id` would almost always mean a duplicate ID.
- **Tests, help text and docs:** unit and CLI tests in bob-cli, Swift tests in the Mac app, updated `capture-rewrite` help, and both repos' docs. Checks are bob's `just check` plus the Mac repo's usual compile checks and macOS CI run.

**Decisions for you when you review:**
- **`.` on bullet task IDs too** (`- Task :id.` → `- Task ^id`): on by default. It's the same switch, so it would be odd for `.` to work in one place but not the other.
- **`;` also switching `@route^id;` → `@route:id`:** off by default. You only asked for `.`, and `.` already flips both ways.
- **Updating the Capture Alias glossary note** to mention the `.` toggle: off by default. The note isn't wrong as it stands, so this needs your opt-in.

Not included: a typing tip that teaches `.` for the toggle, and sending other type-through characters (`/`, `\`, `,`…) through bob.
