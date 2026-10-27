# Chat History - ace-run (research.1p.final)

- **TIMESTAMP:** 2026-10-16 20:36:34 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1p.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261016_133648.md`

## Prompt

%clan(research.1p, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I'm thinking about integrating qmd (see https://github.com/tobi/qmd) into bob or my
Obsidian vault somehow (agent instructions to use it when searching my Obsidian vault,
for example). Can you do some research with the goal of helping me decide the best way
to implement this? Also, critique this plan in general. Is this a good idea? Would you
take a different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.1p.final %m:@xlarge
%wait:research.1p.cdx %wait:research.1p.cld %wait:research.1p.grk %wait:research.1p.mus %wait:research.1p.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I'm thinking about integrating qmd (see https://github.com/tobi/qmd) into bob or my
Obsidian vault somehow (agent instructions to use it when searching my Obsidian vault,
for example). Can you do some research with the goal of helping me decide the best way
to implement this? Also, critique this plan in general. Is this a good idea? Would you
take a different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.1p.cdx`, `research.1p.cld`, `research.1p.grk`, `research.1p.mus`, `research.1p.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.1p.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.1p.linker`, can find it:

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

Now let me read each report through `sase artifact read`.

Five reports read. Now my own research, prioritizing disagreements (BM25-first vs. hybrid; npm vs. git pin; daemon; nightly wiring; corpus scope) and gem's unmeasured claims.

Both throwaway installs are removed; `~/bob`, `~/.config/qmd`, and `~/.cache/qmd` were never touched. Now verifying where SASE skills live, which determines where a vault-search skill would go.

Reports moved. One last check before writing: two reports cite a `qmd bench` fixture format.

`qmd bench` exists in 2.8.3. Writing the consolidated report now.

Report written. Registering it as a durable artifact for the linker.

Registration succeeded. Now the final declaration.

I've written the consolidated report at `202610/qmd_agent_vault_search/qmd_agent_vault_search__final.md` and registered it as `research:202610/qmd_agent_vault_search/qmd_agent_vault_search__final.md` (`file:explicit:d0e68829443eb4086264a409`). The five reports are now `qmd_agent_vault_search__{cdx,cld,grk,mus,gem}.md` in the same directory. The research repo commit is declared and lands when this turn ends.

**Verdict:** qmd is a good idea in a narrow form, but "tell agents to use qmd when searching the vault" is the wrong shape. Most agent questions about the vault are about tasks, statuses, and references, and `bob query`, `bob plan` and `bob ref` already answer those correctly.

**What I added on top of the five reports:**
- **Search quality, retested on the same 10 questions** (cld's set, with known target notes):
  - Searching with two or three short alternative terms, using no models (`rg` or qmd's lexical mode, under 0.4 s), found a correct note for 9 of 10 questions.
  - qmd's hybrid search (keywords plus embeddings, no reranking) also found 9 of 10, with better ranking.
  - Reranking added almost nothing, and qmd's default `qmd query` did worse.
  - Every method missed the question that needed Bob's own terms (ROTTEN, freshness), so a vault map and vocabulary in the skill matter more than embeddings.
- **athena has an RTX 3080 Ti.** cld had assumed it was CPU-only. On it, embedding the whole vault took 4m47s, against about 3h50m on apollo's CPU, and reranked queries took 15–18 s instead of 2.5–8 min. That makes running qmd cheap on athena, but it doesn't change the quality result and doesn't help agents on apollo.
- **Five disagreements between the reports, resolved:**
  - Which search mode agents use by default.
  - npm release vs. a git commit for the install.
  - Whether to run a background qmd server.
  - Whether index refresh hooks into `bob nightly`.
  - What goes into the index.
- **gem's numbers and config are wrong.** It proposes folders the vault doesn't have and timings nobody measured. I set its three-part design aside.

**Recommendation:**
1. **Now, with no new infrastructure:** a `bob_search` skill in chezmoi `home/sase/skills/`. It covers which tool answers which kind of question, a map of the vault, Bob's vocabulary, multi-term `rg` recipes, and rules for reading and citing the source note. Add a one-line pointer in `~/bob/AGENTS.md`.
2. **Pilot, starting on athena:** qmd as an optional "concept search" tier, pinned to 2.8.3. Agents reach it only through a small wrapper that always uses hybrid search with no reranking and no query expansion. It indexes a curated set of notes and keeps daily notes keyword-only. Each host keeps its own index, refreshed by a timer outside `vault-sync` and `nightly`.
3. **After 2–3 weeks:** you write 30–50 test questions from memory. If qmd finds notes the skill-plus-`rg` approach misses and agents actually use it, turn the wrapper into `bob search`. Otherwise drop qmd and keep the skill.

**Housekeeping:**
- My 10-question test is small, and the search terms were written by people who had seen the answers. That's why the pilot test should use your own questions.
- The test installs on apollo and athena were throwaway copies and are deleted. `~/bob` and your qmd config and cache folders were never touched.
- `~/bob/AGENTS.md` still says the vault "is actively synced by Obsidian Sync", which is out of date. The report suggests fixing it when you add the skill pointer.
- The report ends with three questions for you:
  - Do you also want search inside the Obsidian app? That's a separate decision.
  - Should agent-written research reports (`ref/chat`) count as default evidence?
  - Is athena's GPU free for this?
