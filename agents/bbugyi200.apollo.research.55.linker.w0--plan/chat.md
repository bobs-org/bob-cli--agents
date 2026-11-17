# Chat History - ace-run (research.55.linker.w0--plan)

- **TIMESTAMP:** 2026-11-17 11:28:38 EST
- **MODEL:** claude/opus
- **AGENT:** research.55.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/record_card.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/record_card.md`

> # Record Card: an editable value sheet under the H1 of every record note
> ## Scope and completion owner
> Record notes are the last Bob surface that shows record data in the wrong vocabulary.
> The album index, the Mac Record Card, `bob records show`, and the `[!records]` callout
> say `✍️ Draft` and `🔮 Future Work`. The note itself shows Obsidian's raw Properties
> rows instead: `status: draft`, `section: future`, a linked `type: record`, and an ISO
> `created` (see Bryan's screenshot `~/tmp/screenshots/20261117_101208.png`, the
> `sase_blog_zettel/bead_lifecycle.md` record). Properties edits have no schema: no choice
> picker, required marks, bounds, or URL checks. `+ Add property` invites
> `record_unknown_field`, and every Properties save re-serializes the whole frontmatter.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to start rendering a schema card in record notes for the fields
corresponding to the parent album notes fields. Can you help me implement this?

- See the ~/tmp/screenshots/20261117_101208.png screenshot for an example of what record
  notes look like now.
- This new schema card should be rendered underneith the H1 title section in the record
  note but above the H2 "Notes" section.
- The frontmatter fields in record notes should be hidden in favor of this new schema
  card.
- This new schema card should take heavy inspiration from the existing schema cards
  rendered in album notes and in the ~/bob/bank.md file. Namely, the new record note
  schema card should have as close to full parity with these other schema cards as is
  possible/desirable. For example, this schema card should support the ability to edit
  field values, the `==` keymap which is being implemented right now (see the
  202611/double_equals_schema_keymap.md file in the plans sidecar repo), excellent
  keyboard navigation, etc...
- Review the record_card.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.55.linker

## Response

Now reading the record_card research report and the `==` keymap plan, then I'll look at the existing album and bank schema cards in bob-plugins.

I've read the research report and the `==` plan. Next I'm going through the bob-plugins album and bank card code and the bob-cli `records` writer, so the plan builds on what's already there.

Still mapping the bob-cli side: reading how `records update` and `records show` work today, so the plan can extend them additively.

Tracing how the album, bank, and subscription headers mount after the H1, since the record sheet will use that same slot.

Checking how the album card's end-to-end tests run, and reading the shared guarded-update session the card will build on.

I've got the album session wrapper. Now checking whether the shared session can apply without a preview first, since that decides how a choice pick saves in one keystroke.

Looking at a real album and record in your vault, plus the JSON `bob records` returns for them, so the sheet's field shapes come from real data.

Checking the other entry points (the Ctrl+Shift+P fallback in navigation-hotkeys and Command Mode's album row) so the Record Card can sit next to them.

Now the bob-cli update planner and its JSON output, to pin down exactly what the new per-record read and guarded envelope need to add.

Almost done exploring. Last checks: how the album card saves open panes before writing and how its YAML excursion works, since the Record Card will reuse both.

Exploration is done. I'm checking one last detail (whether the album report is ever available on mobile) and then writing the plan.

Validation passes. One wording fix: the CSS selectors can only be checked against real Obsidian in the land agent's CDP walkthrough, not in unit tests.

Still valid. Submitting the plan.

I wrote the plan as a 7-phase epic and submitted it for your review. It passed validation and is waiting for your approval; nothing is built until you approve it.

**What you'll get:**
- **Record sheet.** A quiet card under the H1, above `## Notes`, styled like the album header but lighter. It shows the album's fields in the album's own wording (`✍️ Draft`, `🔮 Future Work`).
  - Choice values render as chips; dates read like `Aug 8, 2025 · 1y ago`; links and URLs are clickable.
  - Empty optional fields collapse into one row of `＋ Year ＋ Service` buttons.
  - A missing required field gets an amber `missing` mark; a value that breaks the album's rules gets an amber tag.
  - `parent`, `type`, `title` and `created` become the breadcrumb, the H1 and a small "added today, 7:55 AM" footer.
  - Old keys like `lid` and `source_*` sit in a read-only "N other properties ▸" fold. Every frontmatter key is shown somewhere exactly once.
- **Record Card.** A keyboard-first editor modeled on the album Schema Card:
  - `j`/`k` move between fields and `Enter` edits one.
  - Digits pick a choice, `t` sets today, `Ctrl+D` clears a field and `u` undoes.
  - `Tab` saves and moves to the next field, for filling a record out quickly.
  - `y` jumps to the field's YAML line; a single `=` opens the parent album's Schema Card.
- **Entry points.** `==` now opens the Record Card on record notes, changing what was shipped this morning (records currently keep Vim's reindent). The card also opens from Ctrl+Shift+P, a new **Edit record** palette command, Command Mode, the sheet's `⊞ Edit` button, and clicks on rows or chips.
- **Writes.** Every edit goes through `bob records update`, so the album's records index stays current. I'm adding two things to bob-cli: `bob records show TYPE STEM`, which reads one record, and `-i FILE` on `bob records update`, which refuses to write if the record changed since the card read it and returns what Undo needs.

**Changes from the research report:**
- **Properties stay visible until the last phase.** They are hidden only once every kind of field can be edited from the card, so there's never a stretch where you can't edit a record.
- **Records stay editable even if the Mac's bob is out of date.** The plugin syncs to the Mac through the vault before the Mac's `bob` gets reinstalled. `bob albums list` will report whether bob supports the new commands; until it does, the sheet is read-only and Properties stay visible.
- **Old-style record types get no sheet.** Records still typed as their noun (for example `type: "[[restaurant]]"`) keep plain Properties. All 186 of your records already use `type: "[[record]]"`.

**Phases:** the two bob-cli phases run alongside the first plugin phase. The plugin phases (sheet → saving → card → typed fields → entry points and hiding Properties) run one after another, so their deploys never collide. The final check runs real Obsidian on athena, since apollo has no Obsidian. You'll still need to run `just install-all` on the Mac before editing turns on there.

**Two choices for you when you approve:**
- **`inline_title` (default: hide).** Hide the `bead_lifecycle` filename title on record notes so the page opens on the H1 and the sheet. You can still rename from the tab header or file explorer.
- **`decision_record` (default: off).** Have the last agent write a decision record saying record values are edited only through bob.

Settled without asking, following the report's recommendations:
- **No commit per edit.** Record edits work like capture and let vault-sync commit later, unlike album schema edits, which commit each change.
- **Mobile keeps plain Properties.** There's no bob on mobile, so the sheet can't load there.
