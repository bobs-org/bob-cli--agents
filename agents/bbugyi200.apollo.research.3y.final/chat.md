# Chat History - ace-run (research.3y.final)

- **TIMESTAMP:** 2026-11-09 11:41:35 EST
- **MODEL:** claude/opus
- **AGENT:** research.3y.final
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_110046.md`

## Prompt

%clan(research.3y, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to display a little hint to the user in the bob-mac-capture app when they
type a character that they could have used a capture alias for.

- For example, if they press `@` to select an area/project note, we should show a hint
  teaching them about the `.` alias.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.3y.final %m:@xlarge
%wait:research.3y.cdx %wait:research.3y.cld %wait:research.3y.grk %wait:research.3y.mus %wait:research.3y.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to display a little hint to the user in the bob-mac-capture app when they
type a character that they could have used a capture alias for.

- For example, if they press `@` to select an area/project note, we should show a hint
  teaching them about the `.` alias.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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
   dispatch's `research.3y.cdx`, `research.3y.cld`, `research.3y.grk`, `research.3y.mus`, `research.3y.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.3y.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.3y.linker`, can find it:

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

Bob probes confirm the alias boundaries (a lone `.` stays literal, `Buy milk @.` stays literal). Now checking the completion-list footer and keycap styles to settle where the hint should sit.

Code checks are done. Moving the five reports (and grk's figure files, so its image links keep working) into the new folder.

Now rendering the two figures with the PDF-matching config.

Figure 2 reads cleanly. In figure 1 the last note's text spills out of its box, so I'm widening that note and re-rendering both.

Both figures fit the PDF page (78.3% and 100%) and answer their questions on their own. Writing the consolidated report.

Report written. Checking one styling claim I took from grk (the Increase Contrast stroke values) before registering.

The code doesn't show a 12%→28% Increase Contrast switch on the picker keycaps, so I'm rewording that line rather than asserting it.

Registering the consolidated report as a durable artifact for the linker.

Registered (`file:explicit:7d645c9c107d3389e2802068`). Finishing the turn through the SASE final declaration.

I wrote the consolidated report at `202611/capture_alias_typing_tips/capture_alias_typing_tips__final.md` and registered it as `file:explicit:7d645c9c107d3389e2802068`. The five reports are in the same folder, renamed `capture_alias_typing_tips__{cdx,cld,grk,mus,gem}.md`. grk's four figure files moved with them under their original names, so its image links still work. The host commits the research repo after this turn.

## Should you build it?

Yes, as a small lesson inside the list the sigil opens, and only after narrowing the requirements:

- **The `@` example is only half true.** `.` becomes `@` only after body text and a space or tab. It stays literal:
  - for a leading `@`
  - after a leading `@route` that is already in the draft (found while checking; none of the five reports had it)
  - glued to a word
  - inside code or a wikilink

  So bob has to prove each tip. It swaps the alias key in for the typed sigil and runs its real rewrite. The tip shows only if that rebuilds the exact same draft and caret. The Mac never keeps its own alias table.
- **This is a habit problem, not a discovery problem.** Every alias landed between Nov 4 and Nov 9, and `.`→`@` landed yesterday; you wrote them. Retiring the tip after the first use, or after three views, would end it before the habit forms. Tips should start frequent, space out while ignored, and go silent once you use the alias at least 75% of the time.

## What I found beyond the five reports

- **Three reports put the tip on a bob call that never happens.** For a bare `@`, the Mac builds the route list from its local target cache and never calls `bob capture-complete`. `capture-parse` takes no cursor. The workable route is cld's: add a field to `bob capture-rewrite --cursor` and call it from a separate app lane that blocks nothing.
- **The route list has no stable footer.** Its footer only appears when no row is selected, but the route list opens with row 0 selected. The footer also scrolls away. The tip needs its own 24 pt row pinned below the list.
- **The main study supports placement, not loudness.** I read Grossman et al. (CHI 2007) directly. Their strongest visual hint did slightly worse than no hint (50% vs 57.1% shortcut use, not significant) because people had already looked away. So the tip must sit in the list you're reading while you choose, never in a toast or the status bar. If you type `@er⇥` faster than you read, it may not help at all.
- **Naming:** "alias" already means four things in the codebase, including the Settings "Capture alias" hotkey. So the JSON field is `sigil_alias_tip` and the setting is "Show typing tips".

## Recommended solution

1. **bob:** add the proven tip to `bob capture-rewrite --cursor`, with a test that pairs every alias with its reverse check.
2. **Mac, route list first:** a typed `@ # ^ : + ~` (with Shift or Option) starts a separate bob call that blocks nothing. The tip is one line pinned to the bottom of the card the sigil opened:

   `Next time  [.] → @  after a word`

   - The keycap is neutral and the `@` uses its editor colour.
   - There is no icon, button, or animation.
   - It shows at most once per capture.
   - If it misses the list's first frame, it is dropped.

   Ship `.`→`@` and `/`→`#` first (both use the route-list card), then the picker ones (`.`→`^`, `;`→`:`, `,`→`+`, `=`→`~`). Tips for `x`/`s` in pomodoro closes come later.
3. **Stop rule:** after three weeks, check the local usage counts and delete the feature if you aren't using the aliases more.

## Requirement changes I made

- **Scope:** I widened it from `@` alone to six aliases, deferred the `x`/`s` close tips, and dropped tips for the fast double-tap flips (`~`→`~~` and the `- ^^` move choice).
- **Trigger:** only a typed key counts, never paste or Undo.
- **Additions:** a Settings toggle and reset, plus the three-week stop rule.

The report also lists factual errors in the individual reports for anyone reading them.

## Open questions for you

1. **Do you usually route with a leading `@`?** If so, the flagship tip will rarely fire, because no `.` alias exists there. The usage counts will show it either way.
2. **Fade by fluency, or retire after first use?** I recommend fading by fluency.
3. **Should the `#` tip teach only `/`, or `/` or `\`?** I recommend `/` only.
4. **Is about 5 ms of extra bob call per sigil acceptable?** It's off the critical path and only fires on sigil keys.
