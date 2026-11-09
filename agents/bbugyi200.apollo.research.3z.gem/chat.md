# Chat History - ace-run (research.3z.gem)

- **TIMESTAMP:** 2026-11-09 17:48:47 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3z.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_173943.md`

## Prompt

%id(gem, clan=research.3z)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3z.cdx`, `research.3z.cld`, `research.3z.grk`, `research.3z.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I need a way to give event tasks associated with Google Calendar events that I don't own
metadata like `@body` or `-30 I need to walk home from the park`.

- The problem is that I can't change the description or title of these events in Google
  Calendar.
- I also need to be able to set this metadata ahead of time (I would normally do this
  when I RSVP to the event--not on the day of).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
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

### Independent Research Report: Ahead-of-Time Metadata for Unowned Google Calendar Event Tasks

**Researcher:** `gem` (5-Researcher Swarm)  
**Report Path:** [`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/gcal_unowned_event_metadata__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/gcal_unowned_event_metadata__gem.md)  
**Snapshot Artifact:** `research:202611/gcal_unowned_event_metadata__gem.md` (`file:explicit:d77bcee1e3ec81cdabc5faa3`)

---

### Key Findings & Executive Summary

1. **Critique of the Need & Core Invariant:**
   - **Verdict:** Storing metadata ahead of time for unowned events is an essential missing link in Bob's time-allocation model. Without it, Bryan cannot reserve travel buffers (`-30m` walk/commute), route personal appointments to appropriate areas (`@body`), or exclude personal meals from worked Pomodoro tracking (`#off`). Waiting until day-of sync violates GTD principles by deferring known logistics to the morning of execution.
   - **Constraint:** As an attendee, Bryan cannot modify event titles or descriptions in Google Calendar (`403 Forbidden`). Moreover, Bob's grant is strictly read-only (`decisions:bob-gcal-is-read-only-and-proposes-once`). The metadata **must live locally in the Bob vault**.
   - **Requirement Adjustment:** Metadata annotation must be **decoupled from the network RSVP act**. Bryan frequently RSVPs on mobile or in Gmail where Bob CLI cannot intercept the click. The annotation engine must support annotating any upcoming event (whether already accepted, tentative, or unreplied), with an optional `--rsvp yes|maybe|no` convenience flag.

2. **Storage Architecture: Per-Host Git-Synced Preference Journal (`.bob/gcal/<host>.jsonl`)**
   - We evaluated four storage models (JSONL journals, sidecar notes, future daily note staging, and local config).
   - **Recommended:** Extend Bob’s existing `.bob/gcal/<host>.jsonl` journal with a new record kind: `gcal.override`.
   - **Why:** Fits Bob’s established multi-host architecture (`decisions:relation-label-prefs-live-in-per-host-journal`, `decisions:theme-prefs-live-in-per-host-journal`). Each host (Mac, Athena, Apollo) writes to its own JSONL file, guaranteeing immunity from Git merge conflicts across machines while synchronizing cleanly through `vault_sync`.

3. **Data Model & Scoping:**
   - **Dual-Scope Targeting:** Supports single-instance overrides (`(calendar_id, event_id)` or `ical_uid`) for one-off appointments, as well as series-wide overrides (`(calendar_id, series_id)`) for recurring invitations from colleagues.
   - **Payload:** Route (`@body`), buffer and labelled reason (`-30 I need to walk home from the park`), clock tag (`#off` / `#on`), and custom prep notes (child checklist bullets).
   - **Precedence Ladder:**
     `Instance Override` > `Series Override` > `Series Memory` > `Google Tokens` > `Colors` > `Calendar Root` > `Default (meet)`.
   - **Resilience:** Overrides are keyed by stable Google event identities (`event_id` and `ical_uid`), so if an organizer moves the event time, reschedules to a new day, or renames the meeting, the metadata remains attached and automatically applies when the target day syncs.

4. **User Experience & Interaction Design:**
   - **Interactive TUI (`bob gcal annotate`):** A bordered fuzzy finder of upcoming unowned events with an interactive form for route, buffer, clock tag, and prep notes, showing a live daily-note Markdown preview before saving.
   - **Express CLI One-Liner:** Reuses Bob's existing `DescriptionDirectives` parser:
     ```bash
     bob gcal annotate "Dentist" "@body #off -30 I need to walk home from the park"
     ```
     This allows Bryan to use the exact same directive grammar he already uses in Google Calendar descriptions with zero new syntax to learn.
   - **Inspection & Management:** `bob gcal overrides` lists active ahead-of-time overrides, and `bob gcal list` displays `✦ annotated` badges alongside planned buffer wings.
