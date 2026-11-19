# Chat History - ace-run (research.5f.gem)

- **TIMESTAMP:** 2026-11-19 07:57:40 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.5f.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261119_074240.md`

## Prompt

%id(gem, clan=research.5f)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5f.cdx`, `research.5f.cld`, `research.5f.grk`, `research.5f.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We already support a headline in daily files, intentions in weekly period notes,
outcomes in quarterly period notes, and themes in yearly period notes. I would like to
unify this concept into a single term, "intentions", that describes the same structure,
which should have a period associated with it, including daily (e.g. "daily intentions",
"weekly intentions", etc...).

- Instead of H2 sections or the **Headline** bullet used in daily files, we should start
  supporting new `intentions` (user-set list of strings), `summary` (agent-set string),
  and `reflection` (user-set string) frontmatter fields to daily files and period notes.
- We should hide these frontmatter properties in Obsidian. Instead, we should generalize
  the code (if possible--at least the UX should be shared) used for the
  album/record/bank cards that are rendered at the top of album notes, record notes, and
  the ~/bob/bank.md file.
  - This new "intentions card" (this and "album/record/bank cards" should be considered
    types of "property cards") will only be shown when the `intentions` frontmatter
    property is set.
  - It should be very easy for the user to modify the current intentions and/or
    reflection using a property card editor that is triggered by the `==` keymap.
- As a part of this change, you should add two new `#periods` daily GTD tasks to the
  ~/bob/gtd_daily.md file that (1: a `#pre` task) ask me to launch an agent to review
  all of the work that I did the previous day and add a `summary` field to that day's
  daily file and (2: a `#post` task) ask me to manually (by typing something like
  `[n==r` from today's current daily file, for example) set the `reflection` field on
  yesterday's daily file.
  - We should add excellent agent instructions to a file somewhere that describes how
    this summary should be generated and point to that file using some kind of sentinal
    value for the `summary` field maybe? This is just my first thought on
    implementation. The goal is to make sure that agents always find these instructions
    when asked to summarize a daily file without ever having to show these instructions
    to the user when they have daily files open in Obsidian (think hard about the best
    way to implement this).
- We should add excellent new glossary terms for "intention", "property card",
  "intention card", "album card". "record card", and "bank card".
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

Completed the independent research and design analysis for unifying intentions, generalized Property Cards, daily GTD tasks/agent summary discovery, and the new glossary terms.

### Report & Registration
- **Report:** [unifying_intentions_and_property_cards__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/unifying_intentions_and_property_cards__gem.md)
- **Registered Artifact Ref:** `file:explicit:7791a07df04a2c38ea32f52a` (label `research:202611/unifying_intentions_and_property_cards__gem.md`)
- **Final Declaration:** Submitted and accepted via `sase final submit` for repository `sdd:research`.

### Summary of Critique & Recommended Design

1. **Data Model & Justified Adjustments**
   - Unify daily `**Headline:**`, weekly `## Intentions`, quarterly `## Outcomes`, and yearly `## Theme` + `## Outcomes` into frontmatter `intentions` (`list[str]`), `summary` (`str`), and `reflection` (`str`) across Daily, Week, Quarter, and Year notes (keeping `all_time.md` excluded).
   - **Adjustment 1 — Keep period `## Review` out of YAML `summary`:** Week/Quarter/Year `## Review` sections are 250–600 words of structured Markdown protected by `review_digest` in [note.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/periods/note.rs) and [draft.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/periods/draft.rs). Keep `## Review` in the period body and scope `summary` uniformly to a 1–3 sentence executive summary (the agent day summary on daily notes; the former Review `**Headline:**` on period notes).
   - **Adjustment 2 — Fix frontmatter parsing & YAML quoting:** `parse_frontmatter()` in [note.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/periods/note.rs) currently skips all indented YAML lines (`starts_with(' ')` / `'\t'`), which drops block lists (`intentions:`) and block scalars (`reflection: |-`). Replace that parser with `serde_yaml` for reads and extend [yaml_spans.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/yaml_spans.rs) for span-preserving guarded writes (`bob intentions update -i -`, modeled on [cli.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/records/cli.rs) and [protocol.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/records/protocol.rs)), quoting values containing `[[...]]`.
   - **Adjustment 3 — Card visibility & property hiding:** Render the **Intention Card** whenever *any* of `{intentions, summary, reflection}` is non-empty (rather than gating strictly on `intentions`, which would strand `summary` or `reflection` invisible in hidden frontmatter). Generalize the selective property hider in [242ka-plugin-record-sheet-properties.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/242ka-plugin-record-sheet-properties.js) and [styles.css](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/styles.css#L11051-L11140) so owned keys (`intentions`, `summary`, `reflection`, `summary_digest`) hide only when the card mounts cleanly outside Source mode and embeds, while `==` still opens the editor on empty notes.

2. **Generalized Property Card UX (`bob-plugins`)**
   - Share the **platform** across Album (`241v` / `241y`), Record (`242k` / `242p` / `242s`), Bank (`248c` / `248k`), and Intention cards—shared `.bob-property-card` chrome CSS, selective property hiding (`242ka`), mounting host, capture-phase `==` router ([248m-plugin-schema-double-equals.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/248m-plugin-schema-double-equals.js), plus Reading-mode `==` chord fallback), close-key ladder ([241xc-plugin-card-close-keys.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/241xc-plugin-card-close-keys.js)), `GuardedUpdateSession` ([242aa-plugin-guarded-update-session.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/242aa-plugin-guarded-update-session.js)), and `y` YAML excursion (`242e`)—while keeping domain modals cleanly separated.
   - Mount the Intention Card directly below the `prev · parent · next` navigation line on both daily and period notes (leaving `openLabeledBodyLink("prev")` in [670-plugin-project-files.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/670-plugin-project-files.js#L151-L169) unaffected so `[n==r` works directly). Design `IntentionCardModal` around direct jumps (`i` ordered sentence-list editor with parent-period peek, `s` summary inspect/edit/prompt copy, `r` reflection textarea displaying yesterday's `summary` directly above, `y` YAML).

3. **Daily GTD Tasks & Agent Instruction Discovery**
   - **Recommend against a `summary:` sentinel value** because it corrupts truthiness/presence checks across downstream tools (`bob-period-parts`, Dataview, `capture-pomodoros --tasks`), bloats daily notes/templates, drifts across versions, and cannot provide cross-vault work evidence.
   - Instead, pair **`bob daily brief <date>` + `bob daily draft <date> -i -`** (embedding canonical versioned summary rules alongside deterministic Pomodoro logs, completed vault tasks, off-clock minutes, events, and `summary_digest` protection) with a rule in `/home/bryan/bob/AGENTS.md` and the copyable launch prompt inside the new `#pre #periods` task in `/home/bryan/bob/gtd_daily.md`. Pair with the `#post #periods` `[n==r` reflection task and migrate `#post #headline` -> `#post #intentions` (`post_stages: [periods, intentions]`).

4. **Glossary & Ecosystem**
   - The report includes full draft glossary entries formatted for [glossary.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/docs/reference/glossary.md) for **Intention**, **Property Card**, **Intention Card**, **Album Card**, **Record Card**, and **Bank Card**, plus coordinated migration notes for `bob capture-pomodoros --tasks` ([capture_pomodoros_agenda.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/capture_pomodoros_agenda.rs)) and `bob-mac-capture`.
