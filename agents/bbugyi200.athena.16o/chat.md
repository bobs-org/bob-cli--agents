# Chat History - ace-run (16o)

- **TIMESTAMP:** 2026-10-31 11:54:40 EDT
- **MODEL:** claude/opus
- **AGENT:** 16o

## Prompt

#gh:gh_bobs-org__bob-cli How do I specify that a specific project should be used for a given Google
Calendar event that the `bob gcal sync` command will use to create an event task?

Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete. %m:@xlarge

## Response

Researching how `bob gcal sync` picks a project/root per event — read the root-selection code; now checking how `@route` hints are parsed from titles and descriptions.

Code is fully traced. Grabbing a quick read-only look at the live config and routable targets for concrete examples, then writing the report.

Report drafted; verifying one claim (where the stripped title is applied) before registering it.

Now registering the report as a durable artifact.

To pick the project for one event, end the event's title in Google Calendar with `@<project>`, such as `Planning sync @bob`. On the next `bob gcal sync`, the Event Task gets `[root:: bob]` and the `@bob` is removed from the title shown in the note. You can also put `@bob` alone on one line of the event description. If the title also ends in an `@word`, the title wins.

Event Tasks always stay in the daily note's `## Events` section. The "project" is the task's `[root::]` field, which decides which area or project the meeting's time counts toward.

**Things to know:**
- **Only some projects are accepted.** The project must be its own root: either a top-level project or one with `root: true`. `@bob`, `@sase`, `@job_2026` and `@sase_blog` work. Sub-projects like `@sase_art` (under `sase`) and `@job_2026_apply_29` are rejected. Bob warns and falls back to the default, `meet`. Use the parent project instead, or add `root: true` to the sub-project.
- **Set it before the first sync.** Sync writes `[root::]` once and never changes it. If the task already exists, edit `[root:: …]` on the line in the daily note.
- **Recurring events:** editing `[root::]` on one occurrence sets the root for future occurrences, and that beats a later `@` in the title.
- **A wrong `@` word in the title blocks the description.** For example, `Coffee with @alice` makes Bob look only for `alice`, so a description line `@job` is never checked.
- **The description form may not always work.** Google's web editor may save line breaks as HTML, so Bob might not see `@bob` as its own line. I haven't tested this. The title form avoids the problem.
- **Checking first:** `bob gcal list` shows the chosen root and where it came from, and `bob gcal sync -d` shows the exact change without writing.

To set a root for many events at once, map an event colour (`gcal.colors`) or a whole calendar (`gcal.calendars[].root`) to it in config. Your `gcal:` config block is currently commented out, so right now only the `@` word and recurring-event edits work.

The report is at `sase/repos/research/202610/bob_gcal_event_project_route.md`, with line references into the source. It's registered as artifact `explicit:6f00b80ea7f54c251cf607ea` (label `research:202610/bob_gcal_event_project_route.md`), and the research repo commit has been declared for the host to make.
