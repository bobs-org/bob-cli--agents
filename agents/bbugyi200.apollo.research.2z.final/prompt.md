%clan(research.2z, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] We recently / are in the middle of adding support for the `#untracked` tag to Google
Calendar events. The plan (see the bob-cli-f6 epic bead for context) was to not track
the pomodoros corresponding to untracked event tasks at all, but I'm not sure this is
the best approach. I'd like to start tracking these pomodoros as a part of a separate,
"untracked" group of stats instead somehow.

- I think we can probably implment this by using the `u::` task property for untracked
  pomodoro (this way we still track the duration of each pomodoro somehow).
- The stats dash and the `bob stats` command would then need some way to toggle over to
  showing untracked time (preferably with an option to show just untracked time and all
  time, including untracked).
- As a part of this change, we should generalize this concept of an "untracked pomodoro"
  a bit (which should maybe be named something else, since the time will techinically
  still be tracked after this change?).
  - Add an excellent new glossary term for "untracked pomodoro" (or whatever we decide
    to call these).
  - A pomodoro should be untracked iff all of its task links correspond with tasks that
    have the `#untracked` tag.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.2z.final %m:@xlarge
%wait:research.2z.cdx %wait:research.2z.cld %wait:research.2z.grk %wait:research.2z.mus %wait:research.2z.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

We recently / are in the middle of adding support for the `#untracked` tag to Google
Calendar events. The plan (see the bob-cli-f6 epic bead for context) was to not track
the pomodoros corresponding to untracked event tasks at all, but I'm not sure this is
the best approach. I'd like to start tracking these pomodoros as a part of a separate,
"untracked" group of stats instead somehow.

- I think we can probably implment this by using the `u::` task property for untracked
  pomodoro (this way we still track the duration of each pomodoro somehow).
- The stats dash and the `bob stats` command would then need some way to toggle over to
  showing untracked time (preferably with an option to show just untracked time and all
  time, including untracked).
- As a part of this change, we should generalize this concept of an "untracked pomodoro"
  a bit (which should maybe be named something else, since the time will techinically
  still be tracked after this change?).
  - Add an excellent new glossary term for "untracked pomodoro" (or whatever we decide
    to call these).
  - A pomodoro should be untracked iff all of its task links correspond with tasks that
    have the `#untracked` tag.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

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
   dispatch's `research.2z.cdx`, `research.2z.cld`, `research.2z.grk`, `research.2z.mus`, `research.2z.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.2z.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.2z.linker`, can find it:

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