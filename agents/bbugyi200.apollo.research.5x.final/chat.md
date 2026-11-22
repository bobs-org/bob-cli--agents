# Chat History - ace-run (research.5x.final)

- **TIMESTAMP:** 2026-11-22 16:45:16 EST
- **MODEL:** claude/claude-fable-5
- **AGENT:** research.5x.final
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261122_160554.md`

## Prompt

%clan(research.5x, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to make it so drawers no longer need to be capitalized.

- You should make sure that this work does not conflict with the (wip) bob-cli-on epic
  bead.
- We will need some other way to mark these sub-bullets as special without marking the
  task in the same way (I think this rules out `#foo` tags, right?).
  - Think hard about the best way to do this.
  - Regardless of what we store on disk, we should make sure to render these drawer
    sub-bullets in a distinct (and easily recognizable) way.
- I think we will need to fix the capture syntax we use for drawers to support this
  change. We already support targeting generic H2 sections when capturing to notebooks,
  so that logic should be re-used if possible/desirable.
- Goals of this Change
  - This change will allow us to represent the true/intended capitalization of the
    section name in drawers.
  - This task is a stepping stone towards the larger goal of giving every project note a
    distinct, lossless task representation (i.e. a way to convert it to/from a task
    without any data loss).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.5x.final %m:claude-fable-5
%wait:research.5x.cdx %wait:research.5x.cld %wait:research.5x.grk %wait:research.5x.mus %wait:research.5x.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to make it so drawers no longer need to be capitalized.

- You should make sure that this work does not conflict with the (wip) bob-cli-on epic
  bead.
- We will need some other way to mark these sub-bullets as special without marking the
  task in the same way (I think this rules out `#foo` tags, right?).
  - Think hard about the best way to do this.
  - Regardless of what we store on disk, we should make sure to render these drawer
    sub-bullets in a distinct (and easily recognizable) way.
- I think we will need to fix the capture syntax we use for drawers to support this
  change. We already support targeting generic H2 sections when capturing to notebooks,
  so that logic should be re-used if possible/desirable.
- Goals of this Change
  - This change will allow us to represent the true/intended capitalization of the
    section name in drawers.
  - This task is a stepping stone towards the larger goal of giving every project note a
    distinct, lossless task representation (i.e. a way to convert it to/from a task
    without any data loss).
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

First run `sase repo open research -r "Write the swarm research reports"` and use
the path it prints as `<research checkout>`. The month directory is
`<research checkout>/202611`; create it if missing.

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.5x.cdx`, `research.5x.cld`, `research.5x.grk`, `research.5x.mus`, `research.5x.gem` dependencies, matching by `wait_name` and the canonical research
   label's existing `__<suffix>.md` suffix. Never reassign suffixes from list order.
   Read each report through its canonical research reference (or the `ref` field's
   `file:<id>` reference if the original has
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
   agent `research.5x.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.5x.linker`, can find it:

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

I'll start by opening the research checkout and reading the five registered reports, then do my own research in the bob-cli codebase.

Now let me read all five reports in full.

Two reports read. Now reading the remaining three.

Epic status, decisions, and the lossy-casing test are all confirmed. One more memory read, then I'll set up the report directory.

All files are in place. Now I'll write the consolidated report.

Now registering the consolidated report as a durable artifact.

All steps are complete. Now submitting the final declaration as required.

Consolidation complete. The five reports and my consolidated report are now at `sase/repos/research/202611/true_case_drawers/` (reports renamed to `true_case_drawers__{cdx,cld,grk,mus,gem}.md` with their asset directories moved alongside so figure links keep working), the consolidated report is registered as artifact `file:explicit:5cdddef6e7bbddc2181d65bd` with label `research:202611/true_case_drawers/true_case_drawers__final.md`, and the commit declaration was accepted.

**The recommendation:** this is a good idea, and all five researchers plus my own verification agree. Store a drawer as a bullet whose entire body is one bold span — `- **API Design**` — which is exactly what your own roadmap note (`bob.md:120`) asks for. Highlights of the consolidated design:

- **Marker decision.** Two researchers independently chose bold; I rejected the three alternatives on verified grounds: `- § Title` (cdx) is painful to type and degrades to an unfamiliar glyph; `- ## Title` (grk) puts real ATX-heading semantics inside list items (CM6 styling bugs, giant GitHub `<h2>`, visual clash with the requirement `⌗⌗`); and mus's persisted bullet-start `#` has a fatal flaw mus missed — stored `- #Design Notes` would be indexed by Obsidian as the tag `#Design`, recreating exactly the tag pollution it rules out. Your instinct on `#foo` tags is confirmed on four independent grounds.
- **Recognizer.** Exact whole-bold-span rule, no trailing text, no `*` inside, **no trailing colon** (gem's rule — it automatically keeps the gcal-imported `**Note:**` a note and gives you `- **TL;DR:** …` bold labels for free). Empty drawers are recognized (53 of 109 project sections are empty, so lossless reversal needs them) but capture never creates one. `drawer_key` stays case-folded, so `NOTES` keeps working.
- **Critical hazard found:** `gcal/description/bullets.rs` today *defuses* imported ALL-CAPS lines by wrapping them in `**…**` — under bold markers that branch would manufacture drawers from calendar descriptions. It must flip (write `__…__`, identical bold rendering) before the marker lands.
- **Capture.** One shared place resolver extracted from the notebook machinery (exact → slug → ambiguous → near-miss → create; quoted verbatim, catalog spelling for slugs), `- #slug` stays the shortcut whose menu acceptance writes `- **Title**`, grammar bump 29 → 30, catalog v3 that stops uppercasing project H2s. Your scoped `*` → `**|**` expansion survives gem's italics/auto-pair objections by firing only in drawer positions on empty bodies, plus Smart Enter and atomic Backspace.
- **bob-cli-on:** zero semantic conflict, but real file/vector contention — ship after phases `.11`/`.12`/`.15`/`.17`, with one cheap instruction to `.12` now (keep section casing behind two named functions so this becomes a two-function swap later). The `^prj` `## NOTES` duplication bug stays the epic's fix.
- **Rollout:** dual-read release → gated migration of the only **7** ALL-CAPS drawers in the vault (each rename is your explicit casing decision — no automated recasing ever) → cutover removing legacy recognition. Doing this now, before the epic's NOTES filing multiplies drawers, is the cheapest moment it will ever be.
- **Honest scoping:** this delivers byte-identical drawer ⇄ `## H2` titles — a real stepping stone — but the full lossless project⇄task goal still has five audited gaps (notably the generated `### Done & Canceled` groups that block reversal on 62 of 102 projects) and needs its own spec.

Open questions left for you in the report: glyph/hue taste pass, the seven migration spellings (especially whether `DONE` is really a drawer), confirming the trailing-colon exclusion, and whether an explicit childless `- **Title**` draft may create an empty drawer (I recommend keeping the refusal).
