# Chat History - ace-run (research.5i.gem)

- **TIMESTAMP:** 2026-11-19 12:04:58 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.5i.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261119_114242.md`

## Prompt

%id(gem, clan=research.5i)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5i.cdx`, `research.5i.cld`, `research.5i.grk`, `research.5i.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Once property cards are fully implemented, I would like to improve and unify the way
they look a bit more.

- We should stop rendering the H1 section in album notes and in daily files in favor of
  rendering it in that note's schema card like we should already do for record notes.
- Make sure you make it very clear from the title whether the user is looking at an
  album note, a record note, or a daily file (they look too similar currently since they
  both render a schema card at the top--maybe use a nice unique icon and/or card color
  for this?).
- See the bob-cli-ms and bob-cli-nh epic beads for context.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Completed independent research and registered the design report in the `research` repository.

### Report & Snapshot
- **Report file:** [property_card_title_and_visual_unification__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/property_card_title_and_visual_unification__gem.md)
- **Registered artifact:** `research:202611/property_card_title_and_visual_unification__gem.md` (`id: explicit:8ba2492c0beeda88671d7c70`, `ref: file:explicit:8ba2492c0beeda88671d7c70`)
- **Finalizer declaration:** Accepted for `commit` on `sdd:research` (`repo-6764d4771d1a`)

---

### Summary of Critique & Key Findings

Moving page titles into top-of-note `.bob-property-card` headers and retiring body `# H1` sections on albums and daily files is the right direction—it removes stacked `.inline-title` + Properties + `# H1` + Card clutter and promotes `##` sections to top level in Obsidian's Outline pane. However, applying the proposal literally on top of **bob-cli-ms** / **bob-cli-ms.8** and **bob-cli-nh** hits five gaps:

1. **Empty-daily blackout (`309 / 311` 2026 dailies + every fresh morning note):** Under `plan:202611/period_intentions.md`, the Intention Card does not mount when `intentions`, `summary`, and `reflection` are all empty. Removing `# YYYY-MM-DD ddd` without an always-mounted Daily Header leaves empty dailies either title-less (if `.inline-title` hides) or showing raw stem `20261119` (and `135 / 311` pre-June Zorg dailies like [20260101.md](file:///home/bryan/bob/2026/20260101.md) lack both `# ` H1 and `aliases:`).
2. **Albums lack a persisted YAML `title:` field:** `src/native/albums/create.rs` writes no `title:` key, `derive_title` ([mod.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/src/native/albums/mod.rs#L122-L123), [scan.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/src/native/notebooks/scan.rs#L789-L836)) resolves `H1 → aliases[0] → humanize_stem`, and `notebookHeaderNoteTitle` ([241e-plugin-notebook-header-model.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/241e-plugin-notebook-header-model.js#L164-L198)) only checks `frontmatter.title` for `record`. Five of six live albums (`eat.md` → `# Restaurants`, `tv.md` → `# TV`, `sase_blog_zettel.md` → `# SASE Blog Zettel`, etc.) would lose their real titles if `# H1` is dropped first.
3. **Nav-line inversion (`prev · W47 · next`):** Daily files carry `[[...|prev]] · [[...|Www]] · [[...|next]]` directly under H1 ([daily.md](file:///home/bryan/bob/_templates/daily.md#L15-L17)), and `bob-navigation-hotkeys` (`[n`/`]n` via [680-plugin-link-parse.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/680-plugin-link-parse.js#L17-L47) and [670-plugin-project-files.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/670-plugin-project-files.js#L829)) scans body lines directly. Dropping H1 orphans `prev · W47 · next` unless docked and mirrored inside the card like `.bob-record-walk-rail`.
4. **Same-hue album/record collision & uncolored daily accents:** Records and their parent albums share the same `data-root-hue` (e.g., `green` for both [eat.md](file:///home/bryan/bob/eat.md) and [ani_ramen_house.md](file:///home/bryan/bob/eat/ani_ramen_house.md)), while daily/period notes get `null` from `pomodoroHomeResolve` and fall back to `--interactive-accent` violet. Relying on color alone also fails `forced-colors: active` accessibility.
5. **Sibling inconsistency (`W`/`Q`/`Y` periods & `bank.md`):** Period notes share the Intention Card with dailies ([2026-W47.md](file:///home/bryan/bob/2026/2026-W47.md)), and `bank.md` shares `.bob-property-card`; leaving them out splits one card family across mismatched layouts.

---

### Justified Requirement Adjustments

1. **Always mount Daily/Period cards on desktop Reading & Live Preview** (decoupled from empty intention/summary/reflection fields), collapsing empty states to a slim header + docked nav rail (+ quiet `＋ Set daily intentions` prompt on open today notes).
2. **Extend header/H1 unification to eligible Period notes (`W`/`Q`/`Y`, excluding `all_time`) and harmonize `bank.md`'s eyebrow header** so all 4 `.bob-property-card` species follow one design system.
3. **Add `title:` YAML support to albums first** (`bob albums create`, `derive_title`, `notebookHeaderNoteTitle`, guarded `bob albums update` / `bob albums tidy`), while deriving daily/period card titles deterministically from canonical paths/IDs (`YYYYMMDD`, `YYYY-Www`) so all `135` historical Zorg dailies work without edits.
4. **Dock and fold `prev · W47 · next` inside the Daily/Period card** (same selection-reveal pattern as `.bob-record-walk-rail`), keeping canonical Markdown nav lines intact for `[n`/`]n`, mobile, and Source mode.
5. **Use a multi-channel identity system** (border silhouette + surface weight + bespoke vector SVG icon + eyebrow badge + title ornament) alongside dedicated temporal colors (`--bob-day-accent`), paired with generalized fail-open `bob-property-card-owns-title` hiding on desktop.

---

### Recommended Design Summary

- **Shared 4-zone `.bob-property-card` anatomy:** `(1) Eyebrow ([SVG + BADGE] · Crumb · Actions)` → `(2) Hero Title ([Emblem/Leaf] + --inline-title)` → `(3) Managed Card Body` → `(4) Optional Docked Nav Rail`.
- **Distinct visual silhouettes across species:**
  - **Album ("Collection Cover"):** **3px left accent border** (`border-inline-start`), richer header tint (`12%` / `7%` body), `[library SVG] ALBUM · Body · N items` badge, and rounded **`frontmatter.emoji` medallion** beside the title.
  - **Record ("Dossier Sheet"):** Calm **`1px` hairline neutral-frosted sheet** (`2.5%–3%` tint) contrasting cleanly against albums of the same root hue, `[album.emoji/tag] <NOUN>` pill (`RESTAURANT`), clean hero typography, field chips, and docked `.bob-record-walk-rail` + progress thumb (fixing `data-root-hue="purple"` → `"violet"` in [styles.css](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/styles.css#L11500)).
  - **Daily ("Calendar Leaf"):** **3px TOP accent rule** (`border-top`) in a non-area slate-teal temporal color (`--bob-day-accent`), `[calendar SVG] DAILY / TODAY · W47` badge, mini **`NOV / 19` calendar leaf emblem**, docked `‹ Wed 18 · ↑ W47 · Fri 20 ›` rail, and compact empty state.
  - **Period & Bank:** Horizon banner (`[calendar-range] WEEKLY · W47`) and Ledger hub (`[landmark] BANK`) following the exact same header grammar.
