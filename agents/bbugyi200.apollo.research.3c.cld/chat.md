# Chat History - ace-run (research.3c.cld)

- **TIMESTAMP:** 2026-11-05 08:57:35 EST
- **MODEL:** claude/opus
- **AGENT:** research.3c.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_084433.md`

## Prompt

%id(cld, clan=research.3c)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.3c.cdx`, `research.3c.grk`, `research.3c.mus`, `research.3c.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
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

I'm reading the existing `offclock` resolver code and its callers so I can map out where `offclock_types` would go.

Still mapping the code: I've found the clock resolver and am now tracing how a task's effective type is computed, since `offclock_types` will need both.

Reading the task-type suggestion code now, because the clock resolver will need a task's effective type.

Now checking the Obsidian plugin side: there are JavaScript copies of the clock resolver that would need the same change.

Gathering vault evidence: so far, all 10 off-clock sessions recorded since the feature shipped are MEET sessions. Next I'll check which non-MEET love/body tasks this change would put on the clock.

Checking two odd ledger rows, then I'll look at how capture computes the clock relative to retyping in the same transaction.

Tracing the Google Calendar preview path now. It builds a fake task line with no type, so `offclock_types` would misreport there unless that line is fixed.

Confirmed Bob Mac Capture doesn't read `clock_source`, so the JSON change is low-risk there. Checking how it shows "via" labels, then I'll check the existing test vectors.

I have what I need from the code and vault. One last check on how type names are normalized, then I'll write the report.

Writing the report now.

I recommend building `offclock_types` much as you described, with six adjustments. Moving love and body to `offclock_types: [MEET]` shouldn't change any recorded history. The report is written and registered as an artifact, and the host will commit it to the research repo after this turn.

**Why it's a good idea.** The thing you're describing depends on both the area and the task type: meetings under love/body are off the clock, meetings under job are not. Only a key on the area/project note can express that. It also fits the existing rules: `#on`/`#off` tags still win, closed rows stay frozen, nothing gets written onto task lines, and mixed sessions still count as Worked. Your `bob#^off-meets` task, typed FIX, confirms the narrower behavior is what you want.

**What the vault shows (read-only scan):**
- Only `love.md` and `body.md` set `offclock`.
- There are 10 closed off-clock rows so far. All are MEET sessions linking `[type:: MEET]` calendar Event Tasks, so the switch causes no drift in recorded rows.
- What does change is future work. For example, the open `() — CHORE` placeholder linking `body#^jenika-note` would now record as Worked.

**Requirement adjustments:**
1. **Match the task's effective type**, not just an explicit `[type::]` field. Calendar rows rooted at `meet` get MEET without a field. Closed tasks must resolve too: their field if set, otherwise the inherited type.
2. **Nearest declaration wins.** On a note with `offclock_types`, a task whose type isn't listed is on the clock. It does not fall through to a parent's `offclock: true`, so a sub-area can narrow its parent.
3. **If one note has both keys, `offclock_types` wins**, with a lint in stats only. This also lets you migrate safely while hosts run different versions.
4. **Value rules:** accept a list or a single name; any invalid item puts the note's tasks on the clock with the existing invalid-value lint; a blank value or `[]` inherits from the parent.
5. **Retyping a linked task during a running session should restamp that session's `[t::]`/`[off::]`.** Now that type decides the clock, retyping, renaming a running Pomodoro, or landing a task on MEET can flip it. Today that would only be corrected at close.
6. **Fix the `bob gcal list` preview.** It builds a fake task line without a type, so it would show love events as on the clock even though sync records them off. The fake line needs `[type:: MEET]`.

**Alternatives I rejected:**
- Reusing `offclock:` with a list value: Obsidian Properties would flag a type mismatch, since it has one type per property name.
- A type-side setting in `config.yml`.
- `offclock: events` (calendar rows only): the runner-up, but it misses hand-captured MEET tasks.
- Having gcal write `#off` onto events.
- An inverse `onclock_types` list.

**Recommended rollout:**
1. Implement it once in the Rust clock resolver (`pomodoro_homes/clock.rs`), reusing the existing type-resolution logic, and mirror it in the bob-ledger-tools JavaScript.
2. Add new cases to the shared `pomodoro_clock` test vectors.
3. Keep `clock_source: "note"` in JSON output and add an optional `clock_type` field. Bob Mac Capture doesn't read `clock_source`, so this is safe there.
4. Migrate in two steps: first add `offclock_types: [MEET]` alongside `offclock: true`. Remove `offclock: true` only after the new bob and plugins are on athena, apollo, and the Mac. Otherwise a Mac-side `bob gcal sync` on an old version could permanently record family meetings as Worked.
5. Write a new decision record that partly supersedes `off-clock-follows-tag-then-note-default`, and update the glossary through `/sase_memory_write`. I didn't edit any memory.

One thing to coordinate: the in-progress `^no-off-task-limit` work must use this same resolver, or the two features will disagree about which tasks are off the clock.

Report: `sase/repos/research/202611/offclock_types_note_defaults__cld.md` (artifact label `research:202611/offclock_types_note_defaults__cld.md`)
