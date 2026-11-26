# Chat History - ace-run (research.6h.gem)

- **TIMESTAMP:** 2026-11-26 09:04:58 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6h.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_084124.md`

## Prompt

%id(gem, clan=research.6h)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6h.cdx`, `research.6h.cld`, `research.6h.grk`, `research.6h.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I just canceled the bob-cli-pl and bob-cli-q6 epic beads because I realized I'd made a
mistake that might cause some confusion and an inconsistent conceptual model for
property cards. Namely, the ~/bob/bank.md file should have never been an area note. It
should be a child of the ~/bob/cash.md file (as it is), but is only used for bank row
tracking purposes (it never contains tasks). I would like to complete the work for these
two epics, but only after the bank.md file is no longer an area note and any logic that
was added to support this strange state (which would produce two cards I think, right?:
one bank card and one area card) is removed.

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

Research complete. The full analysis has been written to [bank_non_area_and_card_epics_completion__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/bank_non_area_and_card_epics_completion__gem.md) and registered as a durable artifact:

- **Artifact ref:** `file:explicit:d518501ea2dc315d4b2712ca`
- **Label:** `research:202611/bank_non_area_and_card_epics_completion__gem.md`
- **Stored path:** [bank_non_area_and_card_epics_completion__gem-6b3b5a0db163.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261126084130/bank_non_area_and_card_epics_completion__gem-6b3b5a0db163.md)

### Key Findings & Critique

- **Yes — this is strongly the right correction.** Inspecting [20261126_070316.mp4](file:///home/bryan/tmp/screencasts/20261126_070316.mp4) confirms `bank.md` flipped between **BANK** and **AREA** cards on cursor moves and stacked **both** cards with duplicate `Properties · 5` feet on `_`. Even after 10 arbitration commits (`06c87a06`..`831ac794`), keeping two title/foot/frontmatter owners on one note remained broken. Removing `type: "[[area]]"` fixes the root cause across `bob-plugins`, `bob areas`, `bob capture-targets`, `bob props`, and `//` Go To Notes, matching `decisions:notebook-routes-write-notes`.
- **Most of `bob-cli-pl` and `bob-cli-q6` is already done on `master`:** `pl.1–pl.8`, `pl.9.1.1`, `q6.1–q6.3`, `q6.5`, and core `q6.4` code/glossary (`1ca74ece`) already landed. Only the Bank–Area arbitration fallout, real-Obsidian acceptance for Home + Bank takeover, `q6.6`'s passive-fold proof & screenshots, retired-count verification, docs, 3 approved glossary strands, and clean plugin deployment remain.

### Five Justified Requirement Adjustments (Called Out in the Report)

1. **Critical Blocker — Re-parent [subscriptions.md](file:///home/bryan/bob/subscriptions.md) from `[[bank]]` to `[[cash]]`:** `src/native/albums/registry.rs` enforces a hard `album_parent_kind` error requiring every album's parent to be an Area or Project. Removing `type: "[[area]]"` from `bank.md` without re-parenting `subscriptions.md` breaks `bob albums check` **and disables all subscription attribution** in `bob bank`. `bob bank` binds subscriptions strictly by noun `subscription`, `cash.md` already claims subscriptions in its summary, and running `bob albums sync` right after re-parenting (before removing `type: "[[area]]"` from `bank.md`) automatically cleans `bank.md`'s `## Albums` section and populates `cash.md`'s.
2. **Make `bank.md` an untyped singleton hub (omit `type:`):** Matches `dash.md`/`rotten.md`/`crowded.md`, avoids a broken self-linking `type: "[[bank]]"`, and works out of the box with `bob bank`, `bob props`, `note_catalog`, `pomodoroHomeResolve` (`cash`'s magenta hue), and `albumHeaderOwnerChain` (`BANK · Cash`).
3. **Remove `NoteKind::Bank` from `bob props`'s Area settings contract (`props_contract_v1`):** On a non-area `bank.md`, 6/8 `AREA SETTINGS` are inert (even `color:` is ignored by `pomodoro_homes::chain_hue` on non-area/project notes). Dropping `NoteKind::Bank` from `src/native/props/contract/settings.rs` returns `bank.md` to plain `props_v1` (matching Album/Record/Day/Period), with `bank:` still card-owned by `==` and `parent`/`summary`/`created` editable in `+`. Because `bob props` has not shipped in a release tag yet (latest tag is `v0.6.0`), removing it now avoids any published crates.io break.
4. **Add three lightweight guardrails:** keep `"bank.md"` defensively excluded in `249b-plugin-home-card-model.js` (prevents two-card collision during multi-host rollout), move `is_bank_note` before `facts.is_area` in `src/native/note_catalog/mod.rs`, and add non-blocking `bank_hub_area_type` and `bank_hub_task` warnings in `bob bank check`.
5. **Drop `q6.6`'s "area strip on bank card" and finish everything in one 5-phase epic:** Phase 1 (`bob-cli` contract removal + guards) and Phase 2 (`bob-plugins` delete `249db` + arbitration hooks, restore `bank` to `props_v1`, fix the deterministic `obsidian-frontmatter-takeover-e2e-lib.cjs:1063` self-test failure, add passive-fold proof) in parallel → Phase 3 (`~/bob/` vault migration in exact sync order) → Phase 4 (real-Obsidian takeover acceptance + family screenshots) → Phase 5 (retired-count sweep, docs, approved glossary strands `area-card`/`project-card`/`property-card`, clean `bob plugins sync` clearing the current `bob-ledger-tools 1.166.5` uncommitted drift).
