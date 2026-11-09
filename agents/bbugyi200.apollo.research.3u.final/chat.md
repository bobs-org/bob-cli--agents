# Chat History - ace-run (research.3u.final)

- **TIMESTAMP:** 2026-11-09 07:46:20 EST
- **MODEL:** claude/opus
- **AGENT:** research.3u.final
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_070553.md`

## Prompt

%clan(research.3u, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I like the set up we have now where I ask agents to add useful context to period note
files at the end of that period (an agent just updated the ~/bob/2026/2026-W45.md file
today, for example). I want to improve the agent instructions contained in these files
to try to make the summaries/context produced by agents even more useful, but I'm not
sure what changes to make.

Can you do some research with the goal of helping me decide if this is a good iea and
(if so) what changes to these period note agent instructions would be most useful?]]) %id:research.3u.final %m:@xlarge
%wait:research.3u.cdx %wait:research.3u.cld %wait:research.3u.grk %wait:research.3u.mus %wait:research.3u.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I like the set up we have now where I ask agents to add useful context to period note
files at the end of that period (an agent just updated the ~/bob/2026/2026-W45.md file
today, for example). I want to improve the agent instructions contained in these files
to try to make the summaries/context produced by agents even more useful, but I'm not
sure what changes to make.

Can you do some research with the goal of helping me decide if this is a good iea and
(if so) what changes to these period note agent instructions would be most useful?

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
   dispatch's `research.3u.cdx`, `research.3u.cld`, `research.3u.grk`, `research.3u.mus`, `research.3u.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.3u.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.3u.linker`, can find it:

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

Reading the five researcher reports now; cdx done, cld in progress.

All five reports read; now verifying their key claims against the code and vault.

Verified the headline-wrap claim (11 of 20 wrapped). Now checking the W45 brief itself.

Checking the related open beads, then doing a quick source check on the outside citations.

Example W45 draft validated (114 words, no write). Now finalizing it, then moving the reports and writing the consolidated report.

Rendering the one figure for the report; fixing a copy prompt that stalled the last step.

Figure rendered; checking its fit and layout.

Figure fits at 100% and reads cleanly. Now writing the consolidated report.

Report drafted; tightening the proposed callout, which came out longer than I'd claimed.

Report registered and the snapshot matches the file. Finishing the turn through the SASE finalizer.

Yes, it's a good idea, and the instructions are worth a v2. But editing the prompt alone won't fix the biggest problems; two of them are in bob-cli code. The consolidated report is written and registered at `202611/period_review_instructions_v2/period_review_instructions_v2__final.md`.

**What's wrong now.** The setup itself is sound: numbers come only from the brief, `bob periods draft` writes only `## Review`, and you own Intentions and Reflection. Every number in the W45 draft matches its brief. The weak part is the content: the Reviews describe minutes logged, not what the week produced. I re-checked these against the vault and code:
- **Headlines lead with hours.** 18 of 19 weekly Headlines open with "A 24h 45m week, 5h 28m below typical…", repeating the stats strip right above them. Only W44 names the work first.
- **Headlines get cut off.** 11 of 20 are wrapped onto a second line, but both the parser and the draft check read only the first line. So the parent notes and the Q4 brief show half a sentence, and W45 shows as "…led by WIP/Next". The v1 instructions are themselves wrapped mid-sentence, and agents copy that.
- **Finished is ranked by minutes.** Five of W45's seven Finished slots are daily `gtd_daily` rows. "Complete first weekly and quarterly review!" (done Nov 5) never made it into the Review.
- **The questions are templated.** 18 of the 59 questions so far rest only on a number being above or below typical.
- **Nothing on the human side has started yet.** No Intentions or Reflections exist anywhere. Your new task to write intentions and outcomes depends on this work, so v2 has to work both with and without Intentions.

**What to change, in order:**
1. **Two bob-cli bug fixes, before the first quarterly review on 2027-01-04:**
   - Read the Headline as its whole first paragraph. This repairs all 11 cut-off Headlines without redrafting anything.
   - Stop `bob task archive` from marking W41 and W44 as `edited`. Today their review state wrongly says you edited them.
2. **A v2 weekly instruction block** (full text in §7 of the report):
   - a one-line Headline that names the work, with one good and one bad example;
   - a hand-picked **Shipped** list that never includes daily review rows;
   - **Carried forward** limited to 3 items, marking ones last week also carried;
   - 0–2 numbered questions about a choice, each resting on a fact the agent checked;
   - the 250-word cap treated as a ceiling, not a target;
   - explicit rules that unknown isn't zero and a task's title isn't its status.
3. **A v2 brief:** group all completions and leave out routine rows, include last week's Review, and drop bare host labels like "apollo agent" from "Bryan's words". Today 27 of 40 entries are those labels.

I wrote a sample W45 Review under v2 and checked it with `bob periods draft -n`, which writes nothing. It came out at 116 words versus the live 239. The proposed instruction block is about 50% longer than v1, more than two researchers advised; the report says what to cut first.

**Where the researchers disagreed,** the report settles each point: for example, questions are capped at 0–2 rather than a fixed 3, and an empty Intentions section is mentioned in the agent's reply rather than with a placeholder line in the note. It also corrects errors in individual reports. One sample rewrite listed a task as done in W45 that was completed today (in W46), and included a count the agent had computed rather than taken from the brief. One report didn't look at the actual notes. One cited paper (AuthScribe) couldn't be found, so nothing relies on it.

**Decisions for you:**
- Should the Review end with a short menu of candidate Intentions? It would help with your intentions task but loosens the "no advice" rule.
- Should W40–W45 be redrafted under v2 before the Q4 review?
- Should the brief start listing releases and decision records? That has the most value for a later reader, at the cost of tying the vault to other repos.

The five reports and grk's figures are now under `202611/period_review_instructions_v2/`, alongside the final report and its new before/after figure. The research repo commit is declared and lands after this turn. I didn't file task beads; the bug fixes and brief changes are listed as candidate phases of your "Improve period agent instructions!" task. While rendering the figure I accidentally overwrote a leftover scratch file, `/tmp/mmdwork/figure.mmd`, from a Nov 8 session.
