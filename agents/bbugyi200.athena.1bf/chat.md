# Chat History - ace-run (1bf)

- **TIMESTAMP:** 2026-11-11 11:06:23 EST
- **MODEL:** claude/claude-fable-5
- **AGENT:** 1bf

## Prompt

#gh:gh_bobs-org__bob-cli Can you review all open task beads in this project with the goal of surfacing
the 5 most impactful beads I could work right now? End your analysis with the ranked
list of 5 beads (with good justifications). 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete. %m:claude-fable-5

## Response

I'll review the open task beads and produce a ranked impact report. First, let me load the required reference memory on beads and artifacts.

Memory loaded. Now let me list the open task beads in this project.

The output was saved to a file. Let me read it.

Prior top-10 audit exists from 2026-11-04 (`task_bead_top10_with_two_host_agent_audit`) — I'll cite it and note what changed since. Now writing the report.

Report written. Now registering it as a durable artifact snapshot.

Registration succeeded (`file:explicit:87d0a0f58b941344704eccc9`), with the source left in the research repo as requested. Now finalizing the turn so the research-repo write is committed.

Done. I reviewed all **218 open task beads** (210 workable right now), read the 14 strongest candidates in full with audited reads, wrote the research report to `sase/repos/research/202611/open_task_bead_impact_ranking.md`, and registered it as a durable snapshot: **`file:explicit:87d0a0f58b941344704eccc9`**, labeled `research:202611/open_task_bead_impact_ranking.md` (source left in the research repo; the commit is declared and will land when the turn ends).

## The 5 most impactful beads to work right now

1. **bob-cli-jx — Mac tip-anchoring tests fail on every macOS CI run** (ci, L). Three `CaptureAliasTipPanelTests` time out deterministically on every run since aafed83, keeping bob-mac-capture's Test step red — so Bundle, Launch smoke, and Install are skipped and **every Mac change ships unverified** through the repo's only gate. Fixing it unblocks the whole Mac pipeline and ends the daily landing-triage churn. Do small companion **jy** (red `just typecheck-tests` on clean master) in the same session.

2. **bob-cli-h9 (+ sibling jz) — docs word-budget failures redden `just docs-check` on clean master** (ci, S/M). h9 has the highest corroboration in the store (**+14 in 7 days**, re-confirmed today on your exact HEAD 7eb82440) — every landing agent keeps re-triaging it. One coordinated trim of five mounted pages (4 Mac + 1 plugins) clears the whole class. (Note: this doesn't block the release train — ci.yml deliberately excludes docs-check — the cost is agent churn and gated docs publishing.)

3. **bob-cli-f8 — task-wikilink CPU budgets fail repeatedly on athena** (ci, L, +12). Blocks a clean full bob-plugins `npm test`; reproduces *in isolation*, so it's a real perf/measurement regression on the capture typing-latency path, not a load flake — and it may be masking real regressions. The most-paid-for unresolved question in the plugins repo.

4. **bob-cli-jr — `bob stats show worked` panics "RefCell already borrowed"** (bug, S). Live-vault crash: any single-metric stats request over a range including today exits 101, so clients get no data. Root cause is already traced to `homes.rs:412` with a fix sketch — the best impact-per-hour fix available.

5. **bob-cli-k8 — `created:` stamps are 5h wrong on UTC-clock hosts** (bug, S). Every notebook/project note/ref created from apollo gets a permanently wrong `created:` instant (chrono::Local offset on configured-timezone wall time). It's silent corruption that **compounds daily**; the fix is small and already shaped on the `records/plan.rs` pattern.

**Free win:** bob-cli-hp (+7) no longer reproduces — fixed in passing by commit 2a37f8ce, with two landings confirming green; just verify and close it. The report also covers near-misses (dq/ht, jh, 9x, the e0/gy SASE-stranding class, the flake family) and why each ranked below the cut.
