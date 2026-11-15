# Chat History - ace-run (research.4q.gem)

- **TIMESTAMP:** 2026-11-15 11:18:48 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.4q.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261115_110057.md`

## Prompt

%id(gem, clan=research.4q)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4q.cdx`, `research.4q.cld`, `research.4q.grk`, `research.4q.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I use a different Google Calendar (under the same bryanbugyi34@gmail.com account) to
track birthdays. See the ~/tmp/screenshots/20261115_105604.png screenshot for context. I
would like the `bob gcal sync` command to support syncing multiple calendars from the
same account starting with this "Birthdays" calendar.

- It should always be clear which event task came from which Google Calendar.
- Once you're confident in the implementation, you should run the
  `bob gcal sync -D yesterday` command with the updated `bob` binary to ensure that this
  worked (Ava's birthday should be added as an all-day bullet).
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

I completed the independent research and design report on multi-calendar `bob gcal sync` and the `"Birthdays"` starter use case.

### Deliverable & Artifact Registration

- **Report:** [multi_calendar_gcal_sync_and_birthdays__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/multi_calendar_gcal_sync_and_birthdays__gem.md)
- **Artifact registration:** Registered without `--move` under label `research:202611/multi_calendar_gcal_sync_and_birthdays__gem.md`
  - **ID:** `explicit:7e02a5a1edaeeab9c5379c55` (`file:explicit:7e02a5a1edaeeab9c5379c55`)
  - **Snapshot path:** [multi_calendar_gcal_sync_and_birthdays__gem-f56a8b1088f1.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261115110108/multi_calendar_gcal_sync_and_birthdays__gem-f56a8b1088f1.md)
- **Finalizer declaration:** Accepted for `commit` on `repo-d6ea06103505` (`sdd:research`). No code or vault files were modified.

---

### Key Findings

1. **Multi-calendar plumbing mostly exists already:** `bob-cli` already has `gcal.calendars` (`{ id, root? }`), `FetchContext::fetch_days`, `OccurrenceKey { calendar_id, event_id }`, per-calendar journal records, `bob gcal calendars`, and `-C/--calendar` support in `note` and `ack` — while [~/.config/bob/config.yml](file:///home/bryan/.config/bob/config.yml#L92-L103) currently leaves `calendars:` commented out.
2. **Immediate blocker for `Ava's Birthday`:** [classify.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/gcal/classify.rs#L134-L136) rejects every Google event whose `eventType` is outside `"default" | "fromGmail"`. In [20261115_105604.png](file:///home/bryan/tmp/screenshots/20261115_105604.png), `Ava's Birthday` displays Google Calendar's birthday banner (`eventType: "birthday"`), so enabling the `"Birthdays"` calendar alone would silently omit `Ava's Birthday`.
3. **Zero user-facing provenance today:** `SnapshotEvent.calendar_name` is `#[allow(dead_code)]` in [snapshot.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/gcal/snapshot.rs#L37-L38); daily-note bullets (`[📅](...)`), `bob gcal sync` reports (`ReportRow`), `bob gcal list` tables, `doctor` output, Pomodoro hover tooltips, and Mac Capture Agenda rows do not surface which calendar an event came from.
4. **Duplicate `"Birthdays"` name in Bryan's account:** [20261115_105604.png](file:///home/bryan/tmp/screenshots/20261115_105604.png) shows **two** checked calendars named `Birthdays` (a teal Contacts layer and an olive custom calendar containing `Ava's Birthday` and `Dad's Birt...`), so matching or labeling purely by Google `summary` is ambiguous.

---

### Critique & Justified Requirement Adjustments

- **Hybrid recommendation instead of pure calendar-only birthday tracking:** Syncing curated `"Birthdays"` into `## Events` as `- **all day**` context bullets cleanly avoids task/ROTTEN/MEET inflation while keeping Google Calendar as the date source of truth — **but** day-of all-day bullets provide zero advance lead time for gifts, cards, or cakes. Keep a **hybrid** workflow: Google Calendar `"Birthdays"` (`mode: context`) for ambient awareness across everyone, plus recurring `[repeat:: every year]` tasks in notes like [family.md](file:///home/bryan/bob/family.md#L1-L7) only for VIP birthdays needing prep.
- **Selective secondary modes instead of symmetric sync across all 9 calendars:** Syncing Google `Tasks`, `Time Blocks`, or Contacts `Birthdays` symmetrically would duplicate entries or collide with Bob tasks and `MEET` Pomodoros.
- **Explicit adjustments called out in the report:**
  1. **Provenance on both Event Tasks and context rows** (since `Ava's Birthday` is an all-day context bullet, not an Event Task, per [vault-format.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/reference/vault-format.md#L594-L595)).
  2. **Implicit primary, explicit secondary (with opt-in primary `label:`):** Non-primary calendars always show their label in Markdown (`[📅 Birthdays](...)`), while `primary` keeps compact `[📅](...)` by default unless configured with `label:`; CLI/JSON/`list`/tooltips still include all calendars explicitly.
  3. **Allow `eventType == "birthday"` as `Inclusion::Context`** in [classify.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/gcal/classify.rs#L134-L158).
  4. **Config keyed by stable `id` with optional `label`, `mode`, `color`, and `ack`**, duplicate-`primary` deduplication, duplicate-name disambiguation, and config-order tie-breaking in `compare_events` ([snapshot.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/gcal/snapshot.rs#L379-L393)).
  5. **Host/date reality for live sync proof:** `athena` reports `no_client` (the `bob-gcal` grant lives on the `writer` Mac), so live testing after implementation should target the Mac with explicit `-D 2026-11-14` rather than relative `-D yesterday`, alongside offline fake-`gog` tests in `bob-cli`.

---

### Recommended Solution Summary

- **Markdown format (`[📅 <label>](<url>)`):** Embed the non-primary calendar label inside the existing link badge (e.g., `- **all day** Ava's Birthday [📅 Birthdays](...)`), keeping it inside Google-owned `spans.badges` in `lifecycle.rs` (`apply_span_updates` can update renamed labels automatically), compatible with `clean_event_title` in [event_task.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/event_task.rs#L1063-L1087) and Obsidian's Jump-to-link, and free of Dataview/Tasks right-to-left inline field parsing hazards ([config.yml](file:///home/bryan/.config/bob/config.yml#L17-L22)) — with a `\u{200b}` guard if a label begins with `YYYY-MM-DD`.
- **Visual & cross-client polish:** Tint `[📅 <label>]` links in Obsidian `bob-ledger-tools` using Bob's 8-hue palette (leaving the time pill's `MEET`/`root`/off-clock colors untouched), append `· <label>` to Pomodoro Task Link hover tooltips, update `markdown_link_target` in [capture_pomodoros_agenda.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/capture_pomodoros_agenda.rs#L1077-L1083) and `iconLinkEnd` in [CaptureAgendaInlineText.swift](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/CaptureAgendaInlineText.swift#L338-L346) so labeled links parse cleanly, add additive `calendar` JSON metadata for Mac Capture Agenda chips, and upgrade `bob gcal calendars` (`--yaml`, colored dots), `list`, `sync`, `doctor`, and `-C` label matching.
