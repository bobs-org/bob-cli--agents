# Chat History - ace-run (research.3u.gem)

- **TIMESTAMP:** 2026-11-09 07:17:16 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3u.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_070553.md`

## Prompt

%id(gem, clan=research.3u)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3u.cdx`, `research.3u.cld`, `research.3u.grk`, `research.3u.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I like the set up we have now where I ask agents to add useful context to period note
files at the end of that period (an agent just updated the ~/bob/2026/2026-W45.md file
today, for example). I want to improve the agent instructions contained in these files
to try to make the summaries/context produced by agents even more useful, but I'm not
sure what changes to make.

Can you do some research with the goal of helping me decide if this is a good iea and
(if so) what changes to these period note agent instructions would be most useful? 
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

# Research Report: Period Note Agent Instructions

**Researcher:** `research.3u.gem`  
**Report File:** [`period_note_agent_instructions__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/period_note_agent_instructions__gem.md)  
**Relative Repo Path:** `202611/period_note_agent_instructions__gem.md`  
**Artifact ID:** `explicit:9cad60d3ea970bd0b2aa7bf9`  
**Artifact Label:** `research:202611/period_note_agent_instructions__gem.md`  
**Snapshot Path:** `/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261109070558/period_note_agent_instructions__gem-21f13adb6a3e.md`

---

### Executive Summary

#### 1. Is this a good idea?
**Yes, upgrading the period note agent instructions is a high-leverage improvement, provided it preserves hard word caps and non-judgmental boundaries.**

The underlying `bob-cli` architecture (`bob periods ensure`, `bob periods brief`, `bob periods draft`, and dynamic `bob-stats-strip` widgets) functions reliably. However, an analysis of the production draft created today in [`2026-W45.md`](file:///home/bryan/bob/2026/2026-W45.md#L33-L78) reveals that the `v1` prompt contract produces low-signal, mechanical output:
- **Redundancy:** Top tasks are duplicated between "Where the time went" and "Finished", burning ~25% of the 250-word cap.
- **Routine Chore Spam:** 5 of the 7 slots in "Finished" were consumed by routine daily review rows (`[[gtd_daily]]`), obscuring actual project deliverables.
- **Number Regurgitation:** The `**Headline:**` repeats total hours and percentage deltas already shown in the stats strip above `## Review` and in parent tables.
- **Ignored Qualitative Context:** `bob periods brief` already extracts Bryan's manual log entries ("Bryan's words"), work-type distribution (BUILD vs. PLAN vs. FIX), and off-clock personal areas (Abby, Kelly, Body), but `v1` instructions never tell agents to use them.
- **Nagging Auditing Questions:** Questions focus on checklist compliance (e.g. asking why Wednesday missed closeout) rather than strategic GTD reflection.

---

### 2. Recommended Changes: The `weekly v2` Prompt Contract

Updating `src/native/periods/instructions.rs` to **`weekly v2`** (and rolling it out across the vault via `bob periods ensure -R`) introduces five high-impact refinements:

1. **Narrative Headline without Metric Repetition:**  
   Summarize the week's defining accomplishment or strategic focus without reciting total hours or deltas already rendered in the stats strip.
2. **Deduplicated & Filtered "Finished" Section:**  
   Exclude tasks already highlighted in "Where the time went"; filter out recurring checklist chores (`[[gtd_daily]]`, routines, pills); and compact routine completions into a single phrase (e.g. *"Daily review closed 6/7 days"*), freeing up slots for actual shipped deliverables.
3. **Incorporate Work Types & Off-Clock Balance:**  
   Synthesize the balance of work types (e.g. BUILD 43%, PLAN 30%, FIX 17%) and off-clock personal areas (e.g. 11h 30m across Abby, Kelly, Body) to give visibility into cognitive labor and life balance.
4. **Leverage "Bryan's Words":**  
   Instruct agents to consult the `## Bryan's words` section of `bob periods brief` to ground the narrative in Bryan's stated intentions, epic launches, and context.
5. **Re-orient "Questions" Toward Strategic GTD Decisions:**  
   Frame questions around trade-offs, next steps on shipped work, and pruning vs. scheduling decisions for chronic rotten keeps (3+ keeps), rather than administrative compliance audits.

---

### 3. Concrete Before vs. After (2026-W45)

| Metric / Section | `weekly v1` (Actual Draft) | `weekly v2` (Proposed Redraft) |
| :--- | :--- | :--- |
| **Headline** | `A 24h 45m week, 5h 28m below typical, put 45% into bob, led by WIP/Next auto-decay and weekly/quarterly/yearly note templates.` (22w) | `Shipped WIP auto-decay and period note scaffolding in bob, while advancing SASE sidecar publishing and triage.` (16w) |
| **Where the time went** | Standard time bullets (88w) | Adds: `Work types: BUILD 43%, PLAN 30%, FIX 17%. Off-clock: 11h 30m across [[abby]], [[kelly]], [[body]].` (102w) |
| **Finished** | Repeats auto-decay and templates; lists 5 daily review rows (48w) | Lists non-routine closes: `doctl` auth, sidecar publishing, anacron error fixes, plus `+242 more` (36w) |
| **Questions** | - What kinds of tasks made up those closes?<br>- Wed 4 missed closeout — what happened?<br>- Three keeps carry no reason — what keeps them on the list? (36w) | - *Bob took 45% of worked time on core tooling; does the completion of auto-decay and period scaffolding unblock your primary Q4 deliverables?*<br>- *Four tasks have reached 3+ keeps without progress; which of these should be scheduled with hard prerequisites vs. pruned to Someday?* (44w) |
| **Word Budget** | **236 / 250 words** (~26% repetitive noise) | **217 / 250 words** (100% signal density) |

---

### 4. Implementation Steps in `bob-cli`

1. **Bump Version:** Set `INSTRUCTIONS_VERSION = 2` in [`src/native/periods/instructions.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/periods/instructions.rs).
2. **Update Templates:** Update `render_weekly()`, `render_quarterly()`, and `render_yearly()` with the refined v2 contracts.
3. **Update Docs & Tests:** Update [`docs/periods.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/docs/periods.md) and CLI period tests.
4. **Deploy Across Vault:** Run `bob periods ensure -R` to rewrite callouts across all period notes in the vault in one atomic transaction.

For full details, rationale, and text templates, see the complete report in [`period_note_agent_instructions__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/period_note_agent_instructions__gem.md).
