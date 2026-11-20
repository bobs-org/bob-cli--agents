# Chat History - ace-run (1el--code)

- **TIMESTAMP:** 2026-11-20 10:43:02 EST
- **MODEL:** claude/opus
- **AGENT:** 1el--code

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/picker_score_beats_status.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- empty_query_sections = keep (planner default: keep). Implement the "empty_query_sections = keep" branch; ignore "empty_query_sections = drop". Context: "Keep the trailing BLOCKED / CLOSED section headers when the stage filter is empty?".
- decision_record = no. Do not edit decisions. Context: "Add a decisions-web strand recording that task pickers rank by match score and use status only to break ties?".
No other memory note may be edited.
Implement only the branches selected above.
%macros_enabled:true


## Response

Reading the approved plan; next I'll open bob-plugins and start the bob-cli `order_for_picker` change.

bob-cli `order_for_picker` now ranks by score first; running its unit tests.

Now the bob-cli integration tests and vectors.

Adding bob-cli integration tests next; first checking whether the existing `kept` tests actually tie under the new order.

Now updating the shared vectors (fixing `rank-kept-open-first` into a real tie and adding `rank-history-best-match-first`).

Now the two integration test files.

bob-cli code and tests pass. Next: bob-cli docs.

Applying the bob-cli doc edits.

bob-cli side done. Now the bob-plugins nav stages — reading the ranker helpers and the Depends-on planner.

Reworking the nav-stage planners now; reading the Blocks and Links/Linked-from planners.

Now writing the shared helpers in `290-local-task-items.js`.

Now the Depends-on planner (300).

Now the Blocks stage (302).

Now the Links-to / Linked-from planners (304).

Now the renderer header (410).

Building and running the nav plugin tests to see which assertions pinned the old split.

All 642 existing nav stage tests still pass. Now writing the new plugin tests; reading the existing test patterns.

Writing the Depends-on stage tests now (screenshot repro, ties, cap, empty query).

Depends-on tests pass. Now the Blocks stage tests.

Adding the render test and the Links-to cases.

Nav stage tests pass. Updating the stale planner comment, then verifying the new tests fail against the old build.

New tests fail on the old build and pass on the new one. Now the `((` wikilink picker in block-id-prompt.

Replacing the picker-view divider test with the flat, score-first contract.

Now syncing the shared vectors fixture into bob-plugins and updating its pinned SHA.

All 530 block-id-prompt tests pass, including the shared vectors and the perf suite. Now the bob-plugins docs.

The nav reference doc hit its 6000-word budget from my extra sentence; reverting that optional tweak.

The plugin docs check uses a cached bob-cli master checkout; the glossary drift looks pre-existing there. Checking with bob-cli's own `just docs-check` in my workspace.

The glossary drift exists on clean master too (from the previous commit's glossary memory change). Checking whether upstream already fixed it.

No upstream fix yet. Regenerating the generated glossary page so the docs gate can pass.

Glossary is fixed; a second, unrelated gate failure surfaced (a broken `/develop/validation/` URL). Checking whether it's pre-existing.

Pre-existing in bob-plugins (commit 2f1e016): a code-span path the URL checker resolves as a bob-cli page. One-line fix to a relative link, matching the sibling docs.

bob-cli docs gate passes. Now the full gates: bob-cli fmt/lint first.

Lint finished; now running the full bob-cli test suite and the full bob-plugins `npm test` in parallel.

Three bob-cli failures in unrelated modules and two plugin perf-budget failures (run concurrently with cargo, so likely load). Checking each against clean master / in isolation.

The cli integration binary passed (3862/3862); only 3 lib tests in `periods update` failed. Confirming they fail on clean master.

Confirmed pre-existing on master (from `a0b91a8d feat(periods)`), unrelated to this change. Now rerunning the two plugin perf tests in isolation.

The ledger-tools perf tests pass 3/3 in isolation (they tripped only while cargo was running). Next, the live read-only check against `~/bob`.

Sync is clean now with no refusals; it also deployed the landed upstream `bob-chips` update. Rerunning the full plugin suite on the fast-forwarded base, without cargo running alongside.

Bead bookkeeping done. Doing a last review of the source diffs before finalizing.

Diffs look right. Finalizing the turn.

I implemented the plan in both repos (keep branch, no decision record). Task pickers now put the best match first, and task status only breaks ties between equal scores. Commits for bob-cli and bob-plugins are declared and land when this turn ends.

**Live check on `~/bob`:** with the query `spike`, the Blocked task `Spike S0: write the promise sentence…` moved from row 11 (in the trailing BLOCKED section) to row 0. The check only read the vault.

**What changed**
- **Depends on, Blocks and Links-to stages:** each is now one list ordered by match score. At equal score, open tasks come before Blocked ones, and closed tasks and `done/` archives sink. The ~60-row cap counts this merged list, so a strong Blocked match is never folded into "type to search N more". Blocked rows keep their muted title, 🔒 badge and "Also waits on this" text.
- **Section headers:** a typed query shows one RESULTS header. An empty filter still shows the trailing BLOCKED / CLOSED header.
- **Linked from stage:** equal-score matches now use the stage's canonical order instead of whatever order the pool happened to be in.
- **`((` picker and bob-cli `order_for_picker`:** completed tasks rank by score too, ahead of open ones when they match better and after them only at equal score. The "Completed history" divider is gone from filtered lists. This also applies to the capture `&` and `((` completions.
- **Docs:** I updated the bob-cli and bob-plugins docs, and added a new LG24 row to the Links-stage table.

**Where I departed from the plan**
- The plan said the existing `kept` pair in the bob-cli tests ties on score. It doesn't: `^kept` is a field-prefix match and `locked-kept` only a word prefix, so the completed "Old kept" now comes first.
  - I rewrote that test and renamed it `query_ranks_history_by_score_and_open_first_on_ties`.
  - I changed the closed row in the `rank-kept-open-first` vector to `^old-kept` so the pair really ties.
  - The plugin copy of the vectors file and its pinned hash are updated to match. The commit messages explain both.
- To get `just docs-check` passing, I fixed two problems that were already on master:
  - I regenerated `docs/reference/glossary.md`, which went stale after commit `b7007011`.
  - I fixed a broken link in bob-plugins `docs/develop/architecture.md`. Task bead `bob-cli-nv` tracks that bug, and I noted the fix there.

**Test results**
- **Passed:** bob-cli `just fmt`, `just lint` and `just docs-check`, and the full bob-cli integration suite (3862 tests). In bob-plugins, the build check, all 33 nav stage test files and all block-id-prompt tests passed, including the performance tests.
- **Fails on unchanged master:** three bob-cli lib tests for `periods update`, from commit `a0b91a8d`. The in-progress Intentions epic `bob-cli-nh` already records them.
- **Fail only under load:** two timing tests in bob-ledger-tools, which this change doesn't touch. The machine's load average was about 180; both pass 3/3 on their own. I added my reproductions to the existing flaky-test beads.
- **Will pass once bob-cli lands:** bob-plugins `npm run docs:check` checks against bob-cli master, which still has the stale glossary.

**Deploy:** `bob plugins sync` first refused to overwrite `bob-ledger-tools`, because another workspace's build was deployed and it had already landed upstream. I followed the repo's runbook without `-F`: fast-forwarded, synced clean, then redeployed. Every plugin is now deployed, including the landed upstream `bob-chips` update.

**Possible follow-up:** Bob Mac Capture's `/` Go To picker still lists closed tasks after open ones whatever the score. The plan left it out of scope, so it's unchanged.
