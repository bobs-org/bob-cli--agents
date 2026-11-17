# Chat History - ace-run (ep--plan)

- **TIMESTAMP:** 2026-11-17 17:18:59 EST
- **MODEL:** claude/opus
- **AGENT:** ep--plan

**Plan:** /home/bryan/.sase/plans/202611/item_start_dot_route_alias.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/item_start_dot_route_alias.md`

> # `.` at an item start types `@`
> ## Goal
> In Bob Mac Capture, typing `.` as the first character of a capture item should do what
> typing `@` there does: become `@` and open the route completion list. Today a leading
> `.` stays a literal dot. The screenshot shows the draft `.` previewing as
> `- [ ] #task . [created::…]` in `mac_inbox.md`. A fast `..` must still type one literal
> `.`, so a leading `.bashrc` or `.5` stays typeable.
> "Item start" means the same position where the whole-item `;` → `:` alias already fires:
> - the start of the draft;
> - the start of every later blank-line item in a bulk capture;

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me fix the `.` alias so it works at the start of a capture (it
should trigger `@` completion)? See the ~/tmp/screenshots/20261117_154622.png screenshot
for context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the `.` sigil-alias rule in bob-cli's capture rewriter to see why a leading `.` stays literal.

Still exploring: finding where the docs explain why a line-initial `.` stays literal, then I'll check the Mac app side.

Reading the original `.`→`@` plan to see why a leading `.` was deliberately left literal.

The Mac side forwards every unmodified `.` to bob, so a leading `.` does reach `capture-rewrite`. Next I'm checking the Mac fast `..` escape probe, which may skip a `.` at a line start.

Mac docs currently promise "item-start `.bashrc`/`.5` stay literal", so the Mac phase will update them too. Reading those doc passages and the typing-tips table.

I have what I need. Writing the plan now: a single medium tale covering the bob rule plus the small Mac escape and tip changes, with one memory decision for the glossary entry.

The plan passes validation with 0 warnings. Submitting it with `sase plan propose`.

I've written the plan and submitted it for your approval; nothing has been changed in either repo yet. It's a single medium tale called **"`.` at an item start types `@` in capture"**.

**Why the leading `.` stays a dot:** bob's rule that turns `.` into `@` only fires after body text plus a space or tab. Its position check rejects a `.` at position 0 or at a line start, so `bob capture-rewrite --cursor 1 -- '.'` leaves the dot alone. A bare `@` already opens route completion there, and `;` already turns into `:` at the same "item start" positions, so `.` is the odd one out.

**Part 1, bob-cli:**
- Let the `.` → `@` rule also fire when the `.` starts an item: the start of the draft, any later blank-line item, or after leading spaces on an item's first line. It still needs `@` to open route completion there.
- Add a new typing-tip lesson, `route_item_start` ("at an item start"), so typing `@` there teaches `.`.
- Update the unit, tip and CLI tests, the help text and the docs. There's no grammar bump.

**Part 2, Bob Mac Capture:** with only the bob change, a fast `..` at the very start of the draft would give `@.` instead of a literal `.`. The Mac code that undoes the alias on a second dot is never set up at position 0, and its fast-typing check only looks for a space before the caret. The plan:
- lets that undo, and the Space/Escape restores, work at position 0;
- extends the fast-typing check to item starts, for `.` only;
- registers the new tip lesson;
- adds tests and updates the four docs pages that currently say "item-start `.bashrc`/`.5` stay literal", without pushing any page past its word cap.

**Scope I chose myself:** bullet and checkbox starts (`- .`, `- [ ] .`) keep their current behavior, matching how `;` already works. A literal leading dot (`.bashrc`, `.5`) is typed with a fast `..`.

**Decision for you:** one memory toggle, defaulting to yes. It rewrites one bullet in the Capture Alias glossary entry, which would otherwise wrongly say `.` → `@` only works after body text.
