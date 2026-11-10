# Chat History - ace-run (research.40.gem)

- **TIMESTAMP:** 2026-11-10 07:27:35 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.40.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261110_071827.md`

## Prompt

%id(gem, clan=research.40)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.40.cdx`, `research.40.cld`, `research.40.grk`, `research.40.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Can you help me write a small, accurate, useful, and visually appealing guide that walks
users through how to add metadata to private event tasks? See the bob-cli-ji epic bead
for context. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Guide: Adding Metadata to Private Event Tasks (`bob-cli-ji`)

A comprehensive, accurate, and visually structured user guide has been authored and registered in the research repository.

- **Report Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202611/private_event_task_metadata_user_guide__gem.md`
- **Repo-Relative Path:** `202611/private_event_task_metadata_user_guide__gem.md`
- **Artifact Label:** `research:202611/private_event_task_metadata_user_guide__gem.md`
- **Artifact ID:** `explicit:8da53b7e5aa88adbf56da895`
- **Artifact Ref:** `file:explicit:8da53b7e5aa88adbf56da895`

---

## Executive Summary of the Guide

### 1. The Core Concept
A **Private Event Note** allows you to attach Bob-only directives and metadata to Google Calendar events you do not own (or shared events where notes must remain private), weeks before the daily note exists.
- **Read-Only Google:** Bob never modifies Google Calendar or exposes notes to organizers/attendees.
- **Keyed to Event ID:** Notes are stored in your vault journal (`.bob/gcal/<host>.jsonl`) and keyed to `{calendar_id, event_id}` or `{calendar_id, series}`.
- **Applied at Sync:** When that day's daily note is created, Bob layers your private note over Google's description field-by-field to produce an enriched **Event Task**.

### 2. Supported Directives & Grammar

| Syntax | Target Field | Effect |
| :--- | :--- | :--- |
| `@<route>` | Area / Project | Sets `[root:: <route>]` (e.g. `@family`, `@body`, `@job`) |
| `#off` / `#on` | Clock Tag | Sets `#off` (excluded from worked metrics) or `#on` |
| `-N` / `-Nm` | Before Buffer | Reserves $N$ minutes before meeting in `[buffer:: -Nm ...]` |
| `+M` / `+Mm` | After Buffer | Reserves $M$ minutes after meeting in `[buffer:: ... +Mm]` |
| `-0` / `+0` | Clear Buffer | Explicitly zeroes out a buffer inherited from Google |
| `-N <reason>` | Reason Bullet | Sets buffer and generates `↤ *Nm before* · <reason>` |
| `+M <reason>` | Reason Bullet | Sets buffer and generates `↦ *Mm after* · <reason>` |
| `<prose>` | Task Bullet | Appends bullet points directly under the Event Task row |

### 3. Command Line Interface (`bob gcal note`)

```bash
# 1. Inspect existing notes (next 90 days)
bob gcal note

# 2. Add routing, buffers, reasons, and checklist items in one line
bob gcal note deerwood @family -30 Drive to Deerwood +15 Drive home Bring camera

# 3. Handle recurring series (-s series vs -s event)
bob gcal note "Little Gym" -s series @abby -30 Drive to gym

# 4. Open interactive editor with git-style scissors line
bob gcal note -e deerwood

# 5. Adopt fragile external organizer directives into Bob
bob gcal note -A "PermitFlow"

# 6. Dry run preview without saving
bob gcal note deerwood @family -30 Drive there -d

# 7. Clear private note (reverting to Google's description)
bob gcal note -c deerwood
```

#### Terminal Preview Visual
When writing a note, Bob prints a visual time-rail alongside the "Lands as" task block:
```text
✎ Deerwood. Christmas breakfast
  Sun Dec 13 · 10:00–12:00 · from Kelly · Yes

  ● family  09:30 ╱╱╱╱╱╱ 10:00 ━━━━━━━━━━━━━━━━━━━━━━━━ 12:00 ╱╱╱ 12:15

  lands as
  - [ ] #task **1000-1200** Deerwood. Christmas breakfast [📅](https://www.google.com/calendar/event?eid=...)
    [buffer:: -30m +15m] [root:: family] [type:: MEET] ^deerwood-christmas-breakfast
    - ↤ *30m before* · Drive to Deerwood
    - ↦ *15m after* · Drive home
    - Bring camera

✓ Noted · only in Bob · lands in 2026/20261213.md when that day syncs
```

### 4. macOS Menu-Bar Interface (`bob-mac-capture`)
- **Shortcut:** Press `⌘E` from anywhere in Mac Capture to open **Event Note Mode**.
- **Interactive Picker:** Filter upcoming events, inspect RSVP badges, and see existing note chips.
- **Rich Editor:** Real-time syntax coloring for routes, buffers, and reasons, with red squiggles on validation errors.
- **Live Preview:** Renders the dynamic time capsule with diagonal hatched wings for buffers.
- **Shortcuts:** `⏎` Save, `⇧⏎` New line, `⌘⌫` Clear note, `⎋` Back, `⌘Z` Undo.
