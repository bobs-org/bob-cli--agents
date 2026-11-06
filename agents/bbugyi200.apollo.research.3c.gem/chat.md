# Chat History - ace-run (research.3c.gem)

- **TIMESTAMP:** 2026-11-05 08:58:35 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3c.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_084433.md`

## Prompt

%id(gem, clan=research.3c)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3c.cdx`, `research.3c.cld`, `research.3c.grk`, `research.3c.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We already support the `offclock` boolean area note / project note file frontmatter
field to specify that all tasks in an area/project, recursively, should be treated as
offclock. I would now like to add support for a new `offclock_types` property that takes
a list of task type names as values.

- This field should work just like `offclock`, but only tasks which have one of the
  types listed by this field should be treated as offclock.
- As our first use-case I would like to migrate the area notes in my Obsidian vault that
  currently use `offclock` to start using `offclock_types` instead, with MEET being the
  only task type that they filter for.

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

# Research Report: Introducing `offclock_types` Area/Project Property

The independent research report has been completed, written to disk, and registered as a durable artifact snapshot.

- **Report Path:** [`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_35/sase/repos/research/202611/offclock_types_property_design__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_35/sase/repos/research/202611/offclock_types_property_design__gem.md)
- **Artifact Snapshot ID:** `explicit:c8d2e10bca6c9a46aaba00e6`  
- **Artifact Label:** `research:202611/offclock_types_property_design__gem.md`

---

### Key Findings & Executive Summary

#### 1. Critique: Is this a good idea?
**Yes, build it.**
- **Solves real operational friction:** Today's boolean `offclock: true` is an all-or-nothing hammer. Bryan introduced `offclock: true` on `love.md` and `body.md` primarily to prevent Google Calendar events (`[type:: MEET]`) from cluttering work time. However, this had the adverse side effect of treating *all* focused personal tasks (e.g., workouts, tax prep, household projects) as off-clock unless decorated with `#on`. `offclock_types: [MEET]` cleanly separates personal calendar appointments from focused personal work.
- **Superior to alternatives:** Evaluated alternatives (global type rules in `config.yml`, Gcal route-level flags, inverted `onclock_types`, or pure `#off` tagging) either broke area contextualization, violated the rule that the vault is the source of truth, inverted Bob's on-clock baseline, or caused calendar sync churn.

#### 2. Critical Architectural Challenges & Adjustments

1. **Decoupling Clock Resolution from Type Catalog:**
   - In `bob-cli` (`pomodoro_homes::clock::effective_clock`) and `bob-plugins` (`plugins/task-status-cycler/src/062-pomodoro-clock.js`), clock evaluation is on the hot synchronous path and must not depend on loading the full theme catalog (`Catalog`) or plan config.
   - **Resolution:** A task's type for clock matching is determined structurally: explicit inline field `[type::]` on the task line first; falling back to inherited `task_type:` on the root walk. Both are already available in `NoteFacts` and frontmatter caches without external catalog dependencies.
2. **Inheritance & Root Walk Termination:**
   - Following Bob's established PT13 inheritance model, the nearest area/project note specifying a clock policy wins and **terminates the walk**. If a child note specifies `offclock_types: [MEET]`, tasks that are not `MEET` are on-clock; they do *not* fall through to an ancestor's `offclock: true`.
3. **Mutual Exclusivity & Linting:**
   - A note must not specify both `offclock` and `offclock_types`. Doing so emits a `note_offclock_conflict` lint and defaults safely to on-clock.
   - Frontmatter parsing should be lenient: accepting either YAML sequence (`[MEET]`) or scalar (`MEET`), normalizing names to uppercase component keys.
4. **Vault Migration & Historical Clock Drift:**
   - Under Decision `off-clock-follows-tag-then-note-default`, closed Pomodoro rows freeze their recorded key (`[off::]` / `[t::]`). Migrating `body.md` and `love.md` from `offclock: true` to `offclock_types: [MEET]` will cause past closed sessions linking non-`MEET` tasks to recompute as on-clock, generating `clock_drift` warnings in `bob stats`. A pre-migration audit is provided to measure and manage this transition.
5. **UI Transparency:**
   - Update `bob-ledger-tools` link chip tooltips to display `Off-clock · MEET from love` rather than generic `Off-clock · from love`, explaining why sibling links under the same area differ in clock state.

---

### Implementation Phases

1. **`bob-cli` Core & Test Vectors:**
   - Extend `NoteFacts` in `src/native/pomodoro_homes/facts.rs` with `offclock_types: Option<NoteOffClockTypes>`.
   - Update `effective_clock` and `resolve_note_default` in `src/native/pomodoro_homes/clock.rs`.
   - Add new test vectors to `tests/fixtures/pomodoro_clock/vectors.json`.
2. **`bob-plugins` Synchronization:**
   - Update `taskEffectiveClockResolution` in `plugins/bob-ledger-tools/src/036-pomodoro-clock.js`.
   - Update `taskEffectiveOffClock` in `plugins/task-status-cycler/src/062-pomodoro-clock.js`.
   - Sync test fixtures and run `npm test`.
3. **Vault Migration & Documentation:**
   - Audit `~/bob/body.md` and `~/bob/love.md` and update frontmatter to `offclock_types: [MEET]`.
   - Deploy plugins with `bob plugins sync`.
