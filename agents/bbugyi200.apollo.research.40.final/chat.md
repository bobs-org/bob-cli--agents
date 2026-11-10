# Chat History - ace-run (research.40.final)

- **TIMESTAMP:** 2026-11-10 07:50:29 EST
- **MODEL:** claude/opus
- **AGENT:** research.40.final
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261110_071827.md`

## Prompt

%clan(research.40, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] Can you help me write a small, accurate, useful, and visually appealing guide that walks
users through how to add metadata to private event tasks? See the bob-cli-ji epic bead
for context.]]) %id:research.40.final %m:@xlarge
%wait:research.40.cdx %wait:research.40.cld %wait:research.40.grk %wait:research.40.mus %wait:research.40.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

Can you help me write a small, accurate, useful, and visually appealing guide that walks
users through how to add metadata to private event tasks? See the bob-cli-ji epic bead
for context.

When you author or carry over Mermaid diagrams, load `/mermaid_diagrams` before
drafting, even when no image or diagrams companion runs. The skill has the shared
figure-selection, styling, and PDF-render review rules. If the provider skill is not
deployed, verify the edited plugin's guide with `sase macro show skill/mermaid_diagrams --format raw` (or
`sase macro show /mermaid_diagrams --format raw`) and use the form this host supports.
This guidance does not enable a companion diagrams agent.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.40.cdx`, `research.40.cld`, `research.40.grk`, `research.40.mus`, `research.40.gem` dependencies, matching by `wait_name` and the canonical research
   label's existing `__<suffix>.md` suffix. Never reassign suffixes from list order.
   Open the research repo with `/sase_repo`, then read each report through its canonical
   research reference (or the `ref` field's `file:<id>` reference if the original has
   moved) using `sase artifact read`. Do not read predecessor chat transcripts. If the
   records above do not identify exactly one report per expected suffix, stop and report
   the missing or ambiguous input instead of guessing.
2. Research the request yourself, prioritizing gaps, weak evidence, and disagreements
   between the reports.
3. Pick a descriptive stem `<name>` that collides with nothing in the month directory
   (do NOT end the name with `_consolidated` or `_<YYYYmmdd>` or anything similar unless
   it relates to the research topic), create `<month-dir>/<name>/`, and move each report
   inside it as `<name>__<suffix>.md`, preserving its existing suffix. Each report's
   `source_path` is provenance for where it lives in your own opened research checkout;
   resolve its canonical repo-relative path there before moving it. Never modify the
   other agents' checkouts or the stored snapshot recorded at `ref` — only the copy in
   your own checkout moves. Preserve every file and never overwrite: on any collision,
   pick a different stem first.
4. Write the consolidated report to `<name>/<name>__final.md`: merge the strongest findings
   from every report above and your own research, resolve conflicts, cut duplication,
   and add missing critical context without unnecessary length.

   Do not create `<name>/<name>.md`, not even as a placeholder, because the linker
   agent `research.40.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.40.linker`, can find it:

   sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

   Use the consolidated report's actual absolute path and its path relative to the
   research repo root, for example `research:202609/<name>/<name>__final.md`. Register
   only the consolidated report, and do not pass `--move`. If registration fails,
   report that failure; do not report the task as fully complete.

Final layout:

```text
<month-dir>/<name>/
├── <name>__cdx.md
├── <name>__cld.md
├── <name>__grk.md
├── <name>__mus.md
├── <name>__gem.md
└── <name>__final.md
```

## Response

I'm reading the five researcher reports; cdx is done, the other four are next.

Four of five reports read (gem too). Now checking the epic, the approved plan, and the current code to settle where the reports disagree.

Status: confirmed that sync writes a not-yet-started meeting as `[*]`, not `[ ]`. Now testing how shells handle `#off`, `;`, and apostrophes, and checking the Mac guide's key markup.

Mac Capture HEAD (28aa5b3) still has no Event note mode, so every report's status claims hold. Next I'll draft and render the merged "when does it land" figure.

Figure is final: 681×1048 px, 85.2% fit, readable. Next I'm moving the five reports into the new report directory, then writing the consolidated guide.

Writing the consolidated report now.

Report written. Now checking the guide draft against the docs lint rules: word count, description length, and banned phrases.

The repo's own counter puts the guide at 1,470 words. That's just under the 1,500 target, not the "about 1,000" I wrote, and too long for a "small" guide. Trimming it to about 1,100.

Guide is trimmed to 1,167 words. Checking that the Mermaid block in the report matches the rendered figure, then registering the report.

Registered. Now finishing the turn with `/sase_final`.

I wrote a combined report with a ready-to-paste guide, **"Plan an event you don't own"**, meant for `docs/guides/plan-events-you-dont-own.md`. Don't publish it yet: the `bob gcal note` command and the Mac Event note mode haven't shipped. The installed `bob` still answers `error: unrecognized subcommand 'note'`, and Mac Capture has no Event note mode. Only the engine that applies notes is on master. So the draft follows the approved plan, and the report ends with a checklist to run once the command lands.

**The guide:**
- **Name:** it calls the feature a "private event note", not a "private event task". The note is the private part; the Event Task it produces is an ordinary row that doesn't exist yet when you RSVP.
- **Length:** 1,167 words by the docs site's own word counter, under the 1,500-word target. It doesn't use any markup the docs lint rejects.
- **Example:** one neutral event (a "Holiday brunch" from "Sam", with `@family`, `-30 Drive to the restaurant`, `+15 Drive home`) runs through every step: the command output, the time bar showing reserved time, the resulting task row, the list view and the Mac section.
- **Visuals:** the time bar from the command output, a styled task row, two tables, two callouts, and one flowchart answering "when will my note show up?". The flowchart renders at 681 × 1048 px (85% of the page width) and I checked the image. No other guide has a diagram yet, so it's easy to drop; a table below it carries the same facts.

**The trap the plan's own examples fall into:** four of the five drafts typed the note without quotes, as the plan's examples do. I tested bash and zsh with your settings:
- An unquoted `#off` is read as a comment, so it and everything after it on the line are silently dropped.
- An unquoted `;` ends the command, so `+15 Drive home` runs as a separate command (`+15: command not found`) after Bob has already saved the first half.

The guide therefore teaches one form only: `bob gcal note brunch -- '<note>'`.

**Where the five drafts disagreed:**
- **Task row:** for a meeting that hasn't started, sync writes `[*]`. The plan's preview shows `[ ]`, so the preview example needs to be regenerated from real output before publishing.
- **Scope flag:** `-s` takes only `event` or `series`. One draft's `-s all` and "event is the default" are wrong; a recurring event run from a script without `-s` exits with an error.
- **`#off` and `#on` together:** the note is rejected when saved, not resolved with `#on` winning.
- **Clearing a note:** the event falls back to the all-events note first, then to Google's description.
- **Where the guide goes:** put it under **Plan the day** in both the guides index and the site navigation. Separately, Connect Google Calendar and Connect Google Mail are in the site navigation but missing from `docs/guides/index.md`.

Before publishing, `docs/gcal.md` § Known limits needs fixing too: it still says an event description you can't edit can't hold a buffer, which contradicts the guide.

The five original reports and grk's figure files are in `202611/private_event_notes_how_to/` in the research repo, with the combined report as `private_event_notes_how_to__final.md` (registered as `file:explicit:abe57e976ceb87998b6fdc0a`). The research-repo changes are declared for the automatic commit when this turn ends.
