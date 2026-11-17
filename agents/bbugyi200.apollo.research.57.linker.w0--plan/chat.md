# Chat History - ace-run (research.57.linker.w0--plan)

- **TIMESTAMP:** 2026-11-17 15:32:13 EST
- **MODEL:** claude/opus
- **AGENT:** research.57.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/schema_card_field_jumps.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/schema_card_field_jumps.md`

> # Plan: Schema card field jumps, numbered fields, and grouped rhythm
> ## Context
> Bryan asked for `J`/`K` (next/previous field) and `1`–`9` (jump to field N) keymaps on
> the schema editing cards, with each field's number shown near its name and more vertical
> space before each field's choices. He agreed with **every requirement** in the
> consolidated research report. Read it first:
> ```bash
> sase artifact read research:202611/schema_card_field_jump_design/schema_card_field_jump_design.md "Field jump design requirements"
> ```
> The screenshot that motivated this is `~/tmp/screenshots/20261117_110414.png` (Zettel

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to add new `J`/`K` and `1-9` keymaps to Obsidian when the schema
editing cards (supported by album notes, record notes, and the ~/bob/bank.md file) are
open in Obsidian.

- The `J` and `K` keymaps should trigger a jump from the current selection to the
  next/previous selection, respectively, that represents a field.
- For example, consider the ~/tmp/screenshots/20261117_110414.png screenshot. In this
  case, if I used the `J` keymap, I would expect my current selection to jump down to
  the "Claim" field.
- The `1-9` keymaps should jump directly to the field associated with that number. To
  support these keymaps, we should start indexing each field selection (starting at 1)
  and showing that index in the schema editing panel somewhere close to its
  corresponding field name.
- Also, as a part of this change, we should add some vertical space before field
  selections (so it is clearer which choices are associated with which fields).
- Review the schema_card_field_jump_design.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.57.linker

## Response

Reading the research report on schema card field jumps before exploring the plugin code.

Research read. Now exploring the bob-plugins schema card code to ground the plan.

Still mapping the schema card code (paint, body, arrange, bank Setup card) so the plan names exact seams.

Reading the bank Setup card's keyboard and group model now; then tests and docs, then I'll write the plan.

Checking the docs and test harnesses the plan must name; nearly ready to write it.

Pulling the concrete CSS sketches from two researcher reports, then writing the plan.

Design settled. Writing the epic plan file now, then validating it.

Validation passed. One wording fix ("Nothing is selected" could read as clearing selection), then revalidate.

I've written the plan as a three-phase epic and submitted it for your review. It passed validation and is waiting for your approval; no code has changed yet.

**How the keys work (album and record notes share one card):**
- **The rule:** `⇧J`/`⇧K` move to the next/previous field in the order shown on screen. `1`–`9` jump straight to field N.
- **From a choice, `⇧K` goes to that choice's own field first.** So from "Draft", `⇧K` lands on Status, and from Status, `⇧J` lands on Claim (your screenshot case).
- **Lowercase `j`/`k` don't change:** they still step through every choice and still wrap around.
- **Field jumps stop at the ends instead of wrapping.** Hitting an end, or pressing a digit with no field (e.g. `7` on a 3-field album), leaves the selection where it is and gives the row a small 3px bump. Holding the key bumps only once, and reduced-motion turns the bump off.
- **Jumps scroll the field and its choices into view.** Today nothing scrolls, so field 9 could land off-screen.
- **Jumps never write anything.**
- **Digits lose one current meaning.** Today they're silently stored as a repeat count for `⌥J/K` moves (e.g. `4⌥K` moves an item four slots); that goes away.
- **Bug fix along the way:** while a reorder is pending, the card draws the new order but `j`/`k` follow the saved one, so they can jump backwards on screen. Navigation, field numbers and the drawn rows will now all use the same order, so numbers always match what you see.

**How it looks:**
- Each field gets a small square number badge just left of its name. It turns accent-colored when that field is selected, or when one of its choices is, which shows where `⇧K` will land.
- Field rows lose their gray fill so they read as headings. They currently look identical to the choice chips because Obsidian's button styling overrides the intended transparent style.
- Each field group gets about 0.8em of space above it, including between Claim and Section, which today sit closer together than chips do.
- Field names, choices and `+ field` line up on one left edge, with the number badges in a column to their left.
- The hint row at the bottom gains `⇧J/K 1–3 field`.

**Bank setup card (`bank.md`):** it only gets `⇧J`/`⇧K` to jump between category groups, because digits are already your category shortcuts there and `1`–`8` keep working. This also fixes a side effect: `⇧K` currently picks 🚗 Car because shortcut matching ignores case. After the change, only lowercase `k` picks Car.

**Phases:**
1. **`field-nav`:** the album keys and navigation, tests, a real-keypress test in Obsidian, and docs.
2. **`field-visuals`:** badges, styling and spacing. It is checked in real Obsidian by measuring alignment and by looking at light, dark and narrow-window screenshots.
3. **`bank-groups`:** the bank group jumps.

Phases 2 and 3 both build on phase 1 and can run in parallel. All code goes in bob-plugins; bob-cli doesn't change.

**Decision for you:** I left one item off by default: adding a short decision record to memory saying schema-card digits mean "field numbers as shown on screen", so the future Record Card follows the same rule. Turn it on when you approve if you want it.

**What I left out on purpose:** `0` stays unbound, and fields 10 and up get no number. The read-only fallback card that appears while bob is unavailable gets no new keys. Spacing is done with styling only, without restructuring the card, because drag-to-reorder depends on the current layout.
