# Chat History - ace-run (research.3z.linker.w0--plan)

- **TIMESTAMP:** 2026-11-09 19:02:45 EST
- **MODEL:** claude/opus
- **AGENT:** research.3z.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/private_gcal_event_notes.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/private_gcal_event_notes.md`

> # Plan: Private event notes for Google Calendar events
> ## Why this design
> Bryan wants metadata such as `@body` or `-30 I need to walk home from the park` on the
> Event Tasks of Google Calendar events he does not own. He can't edit those events'
> titles or descriptions. He also has to set the metadata when he RSVPs, which is weeks
> before the daily note (and so the Event Task) exists.
> The design follows the research report he approved:
> `research:202611/private_notes_for_unowned_gcal_events/private_notes_for_unowned_gcal_events.md`.
> Every phase agent should read it first with
> `sase artifact read research:202611/private_notes_for_unowned_gcal_events/private_notes_for_unowned_gcal_events.md "<reason>"`.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I need a way to give event tasks associated with Google Calendar events that I
don't own metadata like `@body` or `-30 I need to walk home from the park`. Can you help
me implement this?

- The problem is that I can't change the description or title of these events in Google
  Calendar.
- I also need to be able to set this metadata ahead of time (I would normally do this
  when I RSVP to the event--not on the day of).
- Review the private_notes_for_unowned_gcal_events.md file in the research sidecar repo
  for context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.3z.linker

## Response

Reading the research report on private notes for unowned Google Calendar events.

Read the research and the relevant decision records; now exploring the gcal code in bob-cli.

Still mapping the gcal internals (description parsing, journal, root selection) to ground the design.

Still reading: how sync builds each planned row, the gog field mask, and the CLI layout.

Checking what gog offers for event search, then looking at the Mac capture app.

Now checking the memory-write rules, since the plan will add a decision record and glossary term.

I have enough context; checking the epic plan schema before writing the plan.

Writing the epic plan now.

Validation passes but warns that the new memory strands look uncovered; checking how the validator matches selectors.

Restoring the keyword selectors and rewording the body so the new strands are named by web and slug, not by file path.

Validation is clean. Since the file was reformatted on disk, I'll skim it once for coherence before proposing.

The plan reads coherently. Proposing it.

I've written a seven-phase epic plan for **private event notes** and submitted it for your review; nothing starts until you approve it. It passed validation with no warnings and builds on the research report you approved.

**The idea:** a private event note is a description of a Google event that only Bob reads. Bob stores it in the vault's gcal journal, keyed by the event's Google ID, so you can write it the moment you RSVP, weeks before the daily note exists. Sync then applies it over Google's description field by field. Google keeps the time, title and links, and Bob never writes to Google.

```console
$ bob gcal note deerwood @family -30 Drive to Deerwood +15 Drive home
```

That one-liner gets split into the lines you'd write in a Google description. Bob echoes them back with a small time bar (`09:30 ╱╱╱ 10:00 ━━━━ 12:00 ╱ 12:15`) so a `-30` that should have been `+30` stands out. It also shows exactly how the Event Task will look in your daily note, and says whether the note is saved for later or already applied. A typo like `@bdy` is rejected right away with "did you mean" suggestions.

**Choices I made:**
- **Command and term:** `bob gcal note`, and the term "private event note".
- **Which events:** any event, owned or not, including invitations you haven't answered or answered Maybe. A note waits until the event becomes an Event Task.
- **Recurring events:** a This event / All events choice, like Google's own dialog.
- **Kill switch:** `gcal.description: off` hides note bullets too, but the note's `@route`, `#off` and buffers still apply.
- **Durability:** `sync -F` keeps notes, and notes are never deleted silently. If a note can no longer be read because of a corrupted journal line, Bob holds that row and warns instead of quietly reverting it to Google's values.

**Phases:**

| Phase | Size | What it does |
| --- | --- | --- |
| engine | medium | Stores notes in the journal; note fields win over Google's description, per field |
| select | medium | Finds the event (title search over the next 90 days, a pasted Google Calendar link, or an exact ID), picker, list and show |
| hardening | small | Records which row fields came from a note; holds rows when a note can't be read |
| write | medium | Tidies input into note lines, validates, previews, saves, applies; the JSON the Mac app uses |
| extras | small | Edit in `$EDITOR`, `-A` copies Bob lines from an organizer's description, a doctor check, a warning for Bob lines in someone else's description |
| records | small | Decision record, glossary term, and a guide, "Plan an event you don't own" |
| mac | large | An Event note mode in Bob Mac Capture: event picker, highlighted editor, live time bar with hatched buffer wings, save and undo |

The engine runs first; after that, select and hardening can run in parallel, and extras and records in parallel after write. The Mac phase plans itself before coding.

**Decisions waiting for you at review:**
1. **auto_sync** (default yes): on the Mac that runs sync, saving a note immediately updates any affected daily note that already exists.
2. **mac_chord** (default ⌘E from any draft): the alternatives are ⌘E only in an empty draft, or Ctrl-G e.
3. **memory_record** (default yes): a new decision record, "Private Event Notes Beat Google Per Field", which partly supersedes the buffer and gcal-root records.
4. **memory_glossary** (default no): a "Private Event Note" glossary term.

**Left out, recorded as follow-ups:**
- A phone path through Google Keep.
- RSVPing from Bob.
- Letting a note reach a row whose title or time you've already edited.
- "This and following" for recurring events.
- A Ledger Tools tooltip saying a value came from your note.

Until a phone path exists, you can route events from your phone today by setting `gcal.colors` in your config (it's currently commented out) and changing the event's colour when you RSVP. Colour only sets the root, not buffers or reasons.
