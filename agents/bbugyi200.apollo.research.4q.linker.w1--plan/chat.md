# Chat History - ace-run (research.4q.linker.w1--plan)

- **TIMESTAMP:** 2026-11-15 12:22:55 EST
- **MODEL:** claude/opus
- **AGENT:** research.4q.linker.w1--plan

**Plan:** /home/bryan/.sase/plans/202611/gcal_calendar_marks.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/gcal_calendar_marks.md`

> # Plan: Multi-calendar gcal sync with calendar marks, starting with Birthdays
> ## Context
> Bryan keeps birthdays in a separate Google Calendar named **Birthdays** under the same
> account as his primary calendar. He wants `bob gcal sync` to sync it too, and he wants
> it to always be clear which calendar a row came from. The consolidated research report
> `research:202611/gcal_multi_calendar_sync/gcal_multi_calendar_sync.md` (read it with
> `sase artifact read`) recommends a design that Bryan accepted in full. This plan
> implements it.
> Facts verified while planning:
> - **Multi-calendar fetch already exists.** `gcal.calendars` accepts several entries

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I use a different Google Calendar (under the same bryanbugyi34@gmail.com
account) to track birthdays. See the ~/tmp/screenshots/20261115_105604.png screenshot
for context. I would like the `bob gcal sync` command to support syncing multiple
calendars from the same account starting with this "Birthdays" calendar. Can you help me
implement this?

- It should always be clear which event task came from which Google Calendar.
- Once you're confident in the implementation, you should run the
  `bob gcal sync -D yesterday` command with the updated `bob` binary to ensure that this
  worked (Ava's birthday should be added as an all-day bullet).
- Review the gcal_multi_calendar_sync.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.4q.linker

## Response

Reading the research report (`gcal_multi_calendar_sync.md`) before I explore the gcal code.

Research is thorough. Now exploring the gcal code to confirm its claims and size the work.

Still exploring: now tracing how the planner builds title spans and journal hashes, which is where the calendar mark has to go.

Doctor already has a calendars check to enrich. Next: sync's human/JSON row output and the fake gog test harness.

Reading host and install facts so the plan's live-verification step works (research says apollo has no gcal OAuth client).

Hosts have a checkout plus `just install`; athena holds the OAuth grant and the Mac is reachable. Next I'll check the chezmoi-managed bob config, since the rollout phase has to edit it.

Code exploration is done; the research's claims check out. Next I'm loading the memory-write rules, since the plan adds a decision record.

I have what I need. Design is settled: an epic of six phases, with live acceptance on athena or the Mac since apollo has no grant. Checking the epic plan schema next.

Writing the epic plan now. Six phases: config, marked rows, CLI surfaces, de-configured freeze, decision record plus chezmoi, and live acceptance.

Plan validates cleanly. Submitting it.

I've written a six-phase epic plan and submitted it for your approval. Nothing is built yet, so `bob gcal sync -D yesterday` hasn't run; that happens in the last phase.

**Most of this already exists.** `gcal.calendars` already accepts several calendars, sync already fetches each one, and the sync history already keys rows by calendar and event. Adding the Birthdays calendar to config would already put Ava's birthday in the note. The missing piece is showing which calendar each row came from.

**Design: calendar marks.** Each calendar other than your primary one gets a short emoji in config, chosen by calendar id (never by name; your sidebar has two "Birthdays"). Rows from that calendar start with the emoji:

```markdown
- **all day** 🎂 Ava's Birthday [📅](…)
```

- **Unmarked means your own calendar.** Your primary rows stay as they are, so existing notes don't change.
- **No plugin changes.** The emoji is part of the title Bob takes from Google, so Ledger Tools and Bob Mac Capture show it without any edits.
- **Edits are handled the usual way.** If you change a mark, rows you haven't edited update on the next sync. Rows you have edited keep your text and you get one notice.
- **Config is strict.** A mark is required for every non-primary calendar, must be unique, and can't reuse an emoji that Tasks or Bob already gives a meaning to (like 📅 or 🍅).

**Phases** (2 and 3 can run in parallel):
1. **calendar-config** (medium): the `mark` setting and its checks; an upfront check that each configured calendar exists and isn't listed twice; and a test fake that can serve different events per calendar.
2. **marked-rows** (medium): put the mark on rows in the daily note.
3. **deconfigured-freeze** (small): if you remove a calendar from config, its old rows stay put with one notice. Today they can be wrongly removed as "moved" or "deleted".
4. **calendar-surfaces** (medium): marks in `bob gcal calendars`, `list`, `sync`, `doctor`, `ack` and `note`, plus new fields in the JSON output (`schema_version` stays at 1).
5. **enable-birthdays** (small): a decision record, an "add another calendar" step in the setup guide, and the Birthdays entry with 🎂 in your chezmoi `config.yml`.
6. **live-acceptance** (small): apollo has no Google Calendar login, so this runs over SSH on the Mac, or athena if the Mac is unreachable. It installs the new `bob`, applies the config, does a dry run first, then the real sync, then a rerun to check nothing is duplicated.
   - If it runs after today (2026-11-15), "yesterday" won't be Ava's day, so it will use `-D 2026-11-14` instead and say so.

**One breaking change:** a plain list like `calendars: [primary, work]` will now fail, because `work` needs a mark. So the first commit is marked `feat(gcal)!`. Nobody has a multi-calendar config today.

**Two choices for you when you approve:**
- **Which emoji Birthdays gets:** 🎂 (default), 🎁 or 🥳.
- **Whether to add the decision record:** defaults to yes, since you accepted the research's recommendations.
