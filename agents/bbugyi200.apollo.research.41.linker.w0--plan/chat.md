# Chat History - ace-run (research.41.linker.w0--plan)

- **TIMESTAMP:** 2026-11-10 11:23:46 EST
- **MODEL:** claude/opus
- **AGENT:** research.41.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/period_strip_two_charts.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/period_strip_two_charts.md`

> # Period stats strips: a Roots chart, a Types chart, and a switch that works
> ## Why and what
> The period stats strip (`bob-stats-strip` on week, quarter, year, and all-time notes) is
> cluttered. Today it mixes roots and types in one legend line, stacks only roots in the
> columns, and has a switch that never repaints the strip. Bryan's screenshot
> `~/tmp/screenshots/20261110_095225.png` shows the **2026-Q3 quarterly note**, so the
> design must work for 7 to 53 columns, not just a week.
> Bryan accepted every requirement in the research report
> `research:202611/period_strip_two_chart_redesign/period_strip_two_chart_redesign.md`.
> This plan turns it into one design, a contract shared by bob-cli and bob-plugins, and

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I want to make the stats strips shown in period notes look much nicer. Can you
help me implement this?

- For one, we should only use task types in the current charts to reduce clutter.
- We should show root parents in a separate chart.
- We should only show the top N root parents (where N is configurable--set this field to
  5 in my chezmoi repo) in this new chart.
- We should be able to toggle between showing root parents only, task types only, and
  both (like we can in the day strip).
- See the ~/tmp/screenshots/20261110_095225.png screenshot for an example of what a
  weekly period note looks like now (you should also improve the other period note
  types).
- Review the period_strip_two_chart_redesign.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.41.linker

## Response

I'm opening the research sidecar so I can read the redesign report.

The research report is detailed. Next I'll look at the mockups and then check the current code in bob-cli and bob-plugins.

The mockup images aren't indexed as artifacts, so I'll view them from the checkout that `sase repo open` gave me.

The mockups give a clear visual target. Now I'll check the bob-cli code and open the linked plugin and chezmoi repos.

I've traced the bob-cli report builder; next I'm checking how stats split minutes across types and roots.

Still mapping the code. I've covered bob's config and stats internals; now I'm checking the docs and the plugin side.

Now the plugin side.

I'm reading the plugin's fence and switch code to see how repaint and caching work.

I'm checking live `bob periods show` output to confirm how root hues come through today.

I've decided where root colors get assigned. Next I'm reading the memory notes the plan touches: vault conventions, docs rules, and the glossary and decision entries.

Next, the chezmoi config's `stats:` block.

I'm looking at a recent epic plan to match how phases target linked repos.

I'll load the dataviz guidance so the chart spec in the plan follows sound mark, legend, and color rules.

Next I'm checking the existing test harnesses on both sides so the plan's verification steps are concrete.

Still verifying how the stats pass and terminal output handle part dimensions, which decides where the new type split lives.

I'll run the dataviz palette validator on candidate root colors before recommending any vault color change.

Before designing the config phase, I'll check how earlier plans handled chezmoi edits and the apply step.

I've settled the phase graph. One more check: whether bob caches stats on disk in a way a `types:` config change wouldn't invalidate.

I have what I need for the design. I'll check the epic plan schema with a stub before writing the full plan.

The `ask` with a colon inside needs quoting.

Validation passes. Submitting the plan.

I've written the plan and it passes validation. It's staged for your review, and no code changes start until you approve it.

It's an epic with five phases, each sized medium:

| Phase | Repo | Depends on | What it does |
| --- | --- | --- | --- |
| `strip_polish` | bob-plugins | — | Quick fixes to today's strip: colored legend dots, bars on one baseline with honest heights, no year values, no truncated "so far", labels instead of raw keys in tooltips. Period strips stop flipping your Day strips. Colors follow identity. |
| `type_split` | bob-cli | — | A new type split in Stats that counts only your configured types. Labels like SASE get no share; unnamed and label-only sessions go to their own buckets. |
| `period_charts` | bob-cli + chezmoi | `type_split` | `bob periods show` gains new JSON fields with the folded series and per-column stacks. Adds the `stats.period_strip.top_roots` setting (1–8, default 5; a bad value warns instead of failing), fixes the "so far" wording for quarters and years, and sets `top_roots: 5` in chezmoi. |
| `chart_painter` | bob-plugins | `strip_polish`, `period_charts` | Roots chart above Types chart on one shared axis. Each legend is the chart's title and names every color. A ●/■ switch cycles Both → Roots → Types, remembered separately from the Day strip, with a "Cycle period stats charts" command. Shows a Roots-only fallback while the installed bob is older. |
| `long_periods` | bob-plugins | `chart_painter` | Year view: no per-column labels, and four quarter columns when the note is narrow. All time: leading untracked years collapse into one ghost. Also the parts table, legend-hover dimming, the full preview matrix, docs, and memory updates. |

`strip_polish` and `type_split` can run at the same time.

**Where I departed from the research:**
- **Colors stay put.** A root's color no longer depends on how many minutes it has; ties go alphabetically, which keeps bob on blue. This rule is shared by the Day strip, the Stats panel, and the period charts, so a root looks the same everywhere.
- **No `+N` in chart legends.** Charting only the top 5 roots plus "N more" keeps every color named.
- **Thinner bars.** Bars are at most 24 px wide with air between them, instead of filling each slot.
- **Less chrome.** Untracked periods are short dotted ghosts, and today's column gets a stronger caption instead of a dashed outline.
- **A leaner first fix.** The quick-fix phase hides the broken period switch instead of wiring one that could only swap legends over the root-stacked columns. The real switch comes with the two charts.

**Four decisions for you at approval:**
- **PLAN color (default: keep gray).** Changing `PLAN: auto` to `aqua` is optional; gray already reads as "a type you chose to mute."
- **Pin sase to orange (default: yes).** Without the pin, sase lands on orange or aqua depending on whether dev is also in the chart. Orange is the one color no top-level area uses. This edits the frontmatter of `~/bob/sase.md`.
- **Glossary update (default: yes).** The Stats Strip entry still describes a parts row stacked by root parent, which the new charts make wrong.
- **New decision record (default: yes).** It records the two-chart rules. I based this on your agreement with the whole research report.

Your top 5 roots will still sometimes sit next to each other in look-alike colors: orange/red and, in dark mode, magenta/aqua. Changing Bob's shared palette is out of scope. Names in the legend, the ●/■ shapes, the hatching for unattributed time, and the tooltips give a second way to tell series apart.
