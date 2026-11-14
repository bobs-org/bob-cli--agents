# Chat History - ace-run (research.4m.gem)

- **TIMESTAMP:** 2026-11-14 08:17:51 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.4m.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261114_080152.md`

## Prompt

%id(gem, clan=research.4m)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4m.cdx`, `research.4m.cld`, `research.4m.grk`, `research.4m.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to improve upon the "bank badge" work (see the bob-cli-lh epic bead for
context) by adding an excellent set of new bank transaction visualizations to each
period note (daily files don't need this). I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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

Completed independent design and architecture research for period-note bank transaction visualizations and registered the report as a durable SASE artifact.

### Deliverable & Registration

- **Report:** [period_note_bank_visualizations__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/period_note_bank_visualizations__gem.md)
- **Registered artifact:** `research:202611/period_note_bank_visualizations__gem.md` (`id: explicit:ac801a0e1027e80e4b20f0f6`, stored snapshot `/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261114080202/period_note_bank_visualizations__gem-2a4f259e6f8d.md`)
- **Final declaration:** Submitted and accepted for `sdd:research` (`commit` via `sase final submit`).

### Key Conclusions in the Report

1. **Critique & Core Hazards:** Adding bank visualizations to period notes (`Week`, `Quarter`, `Year`, `All time`) pairs naturally with `bob-stats-strip` and the weekly Monday QFX review loop, but naive chart stacks risk crowding `## Intentions` / `## Outcomes` above the fold, missing existing notes due to create-only scaffolds ([docs/periods.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/docs/periods.md#L6)), crushing daily spending bars under payday inflows, clashing with red/magenta limit reservations ([styles.css](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/styles.css#L114)), and sending bloated `days[].rows[]` payloads over IPC.
2. **Called-Out Adjustments (`A1`–`A8`):**
   - Attach a **2-column collapsible `.bob-bank-panel`** (~155–185 px desktop height, 1-click collapsible per device, gated by `stats.bank_visuals`) inside `.bob-bank-badge-host` beneath `bob-stats-strip` so every existing period note gets coverage immediately, plus an optional explicit `bob-bank` (`view: period`) fence that suppresses the top panel if placed manually.
   - Coverage-gate completely (`0 px` on untracked/`0/0/0`/future periods; single collapsed leading ghost before `tracked_since`), keep `bob-period-parts` time-only by default, omit typical baselines until ≥4 closed periods exist, avoid pie charts and an 8-hue category rainbow, keep strip actions strictly read-only (`span[role=link]`, zero `<button>` elements), and compute viz aggregates in Rust rather than folding raw `BankRow` arrays in JS.
3. **Recommended Visualization Suite (`-p PERIOD -s -v`):**
   - **Flow Proportion Tape & Kept-Apart Strip:** Proportional In vs Out meter, signed Net pill (`--bob-bank-in-ink` green for surplus, calm neutral ink for drawdowns — never red or magenta), and non-zero footnotes (`transfers`, `refunds`, `cash_out`, `cash_traced`, `unclassified_in_cents`).
   - **Child-Period Cashflow Rhythm Chart:** Plotted along the exact `bob-period-strip` CSS-grid spine (`Mon..Sun` Out bars + floating payday stems on `Week`; diverging `+In` / `Out` butterfly with month ticks, outlier cap glyphs, quarter/year groupings, `@container (max-width: 420px)` quarter fallback on `Year`, and roving arrow-key navigation on `Quarter`/`Year`/`All time`).
   - **Ranked Category Mix:** Top 5–6 Out categories + pinned `Cash out` / `Unclassified` horizontal bars in a muted neutral/slate tonal ramp with emojis and hover brushing into the rhythm chart.
   - **Period Highlights & Waiting Nudge:** Capped top outflows/inflows plus oldest period waiting link jumping directly to `bank/YYYY-MM.md:line`.
4. **Data Contract (`bob-cli` + `bob-plugins`):** Add `-v, --viz` on `bob bank report` ([cli.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/bank/cli.rs#L100-L119), [report.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/bank/report.rs#L325-L416)) emitting schema-1 `viz.{granularity, group_kind, groups, buckets, inflow_breakdown, highlights}` through `compute_totals`, decoded strictly in [241h-plugin-bank-decode.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/241h-plugin-bank-decode.js#L131-L153) with `BANK_CACHE_SIZE` bumped to `32` in [241j-plugin-bank-data.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/241j-plugin-bank-data.js).
