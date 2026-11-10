# Chat History - ace-run (research.41.gem)

- **TIMESTAMP:** 2026-11-10 10:15:56 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.41.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261110_095915.md`

## Prompt

%id(gem, clan=research.41)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.41.cdx`, `research.41.cld`, `research.41.grk`, `research.41.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to make the stats strips shown in period notes look much nicer.

- For one, we should only use task types in the current charts to reduce clutter.
- We should show root parents in a separate chart.
- We should only show the top N root parents (where N is configurable--set this field to
  5 in my chezmoi repo) in this new chart.
- We should be able to toggle between showing root parents only, task types only, and
  both (like we can in the day strip).
- See the ~/tmp/screenshots/20261110_095225.png screenshot for an example of what a
  weekly period note looks like now (you should also improve the other period note
  types).
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

# Research Report: Period Stats Strip Redesign (`research.41.gem`)

The research investigation into redesigning the period note statistics strips across Bob has completed. The full research report has been written to [period_stats_strip_redesign__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/period_stats_strip_redesign__gem.md) and registered as durable artifact `explicit:ad3d6899f513ce24d18cfc6a` (`research:202611/period_stats_strip_redesign__gem.md`).

---

### Key Findings & Plan Critique

1. **Current Failure Modes Identified:**
   - **Legend/Chart Disconnect:** The legend row (`.bob-period-strip-lanes-row`) displays both Root Parents (`●`) and Task Types (`▰`), but the column bars below exclusively stack Root Parents. A user seeing `▰ PLAN 27h 21m` in the legend expects to see `PLAN` in the column bars, but it is entirely absent.
   - **Color Collision:** Roots and Task Types share the same 8-slot palette (`yellow`, `red`, `blue`, etc.). A yellow segment in the column currently represents `bob.md`, not `BUILD`.
   - **Long-Tail Root Clutter ("Rainbow Lasagna"):** In multi-week or quarterly views, tracking 10–20 root notes fractures bars into 1–2px slivers of visual noise.
   - **Defective Toggle:** The period strip's cycle switch currently only toggles the legend text and does not repaint the column bars or affect their rendering.

2. **Critique of the Proposed Plan:**
   - **Switching to Task Types:** **Strongly endorsed.** Task types form a stable, high-signal 7-category taxonomy (`BUILD`, `PLAN`, `FIX`, `CHORE`, `READ`, `WRITE`, `MEET`) that reflects cognitive mode during GTD reviews.
   - **Showing Root Parents in a Separate Chart:** **Endorsed with layout refinement.** Placing two full-height, separate charts stacked vertically would double the height (~280px+) and duplicate X-axis labels (days/weeks, total hours, closeout marks).
   - **Recommended Layout — The "Synchronized Twin-Track":** In `both` mode, render two synchronized tracks (Track 1: Task Types; Track 2: Top-5 Roots) sharing a **single bottom X-axis**. This maintains a compact ~190px vertical footprint and allows effortless vertical correlation between *activity mode* and *project allocation*.
   - **Top N Roots & the "Other" Invariant:** Truncating to Top 5 roots is essential, but ranks 6+ **must be summed into an `Other` bucket** (rendered in neutral grey `--text-faint` at the top of the stack). Discarding them would cause bar heights to disagree with total worked hours.

3. **Backend Contract Delta:**
   - `bob-ledger-tools` currently receives **no task type breakdown per column** from `bob periods show -f json`.
   - [`src/native/periods/report.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/periods/report.rs) must be updated to emit both `stacks.themes` and `stacks.roots` (with top-N folding) per column.

---

### Configuration Contract

Add the following to Bryan's [`chezmoi` config.yml](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/chezmoi/home/dot_config/bob/config.yml):

```yaml
periods:
  top_roots: 5
  default_view: both # both | themes | roots
```

---

### Artifact Registration Details

- **Report Path:** [period_stats_strip_redesign__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/period_stats_strip_redesign__gem.md)
- **Artifact ID:** `explicit:ad3d6899f513ce24d18cfc6a`
- **Artifact Label:** `research:202611/period_stats_strip_redesign__gem.md`
- **Snapshot Path:** [period_stats_strip_redesign__gem-1777beca34dc.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261110095922/period_stats_strip_redesign__gem-1777beca34dc.md)
