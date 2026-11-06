# Chat History - ace-run (bn--code)

- **TIMESTAMP:** 2026-10-31 10:43:46 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bn--code

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/alt_n_inbox_route_and_walk_advance.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- advance_scope = due_row (planner default: due_row). Implement the "advance_scope = due_row" branch; ignore "advance_scope = landing". Context: "Should Alt+N advance the walk from any due walk row, not only the exact `]s` landing?".
- memory_walk_record = yes 🧠. Memory edits are authorized for decisions:answering-advances-the-walk, decisions:alt-n-answers-from-due-rows only. Context: "Record Alt+N's due-row advance as a decision and mark answering-advances-the-walk superseded in part?".
- memory_inbox_glossary = yes 🧠. Memory edits are authorized for glossary:inbox-file only. Context: "Update the Inbox File glossary strand so Alt+N is among the keys that route inbox tasks?".
- memory_inbox_record = no. Do not edit decisions:inbox-answers-route-first. Context: "Also write the pending inbox-routing decision record (bead bob-cli-4t), including Alt+N, and close that bead?".
No other memory note may be edited.
Implement only the branches selected above.


## Response

Implemented the approved plan: Alt+N now routes inbox tasks and advances from any due walk row.

**What changed**

- bob-plugins `bob-navigation-hotkeys` 2.62.2 → 2.63.0:
  - New `511-plugin-lane-inbox-route.js`: on an inbox task, Alt+N asks where the task goes after the probe refusals and the Pending Work Log prompt. `↵` acts then moves (never follows/parks), `⇧↵` stays, Esc cancels with nothing written. Move failure settles today's `lane` outcome plus a separate `Not moved: … · still in <inbox>` notice.
  - Fixed the swapped Task Card lane labels (`[ ]` → commit, `[*]`/`[/]` → release, counted sessions probe the batch) via new `formatLaneRouteActionLabel` in `255-inbox-route.js`, exported for tests.
  - New `536a-plugin-review-due-row.js` + shared origin builder in `536-plugin-review-advance.js`: Alt+N captures a due-row origin (same note + line text in the pre-write queue) and `continueReviewWalkAfter` advances it exactly once. Landing anchors' unanswered rows stay walkable; PRE/POST/RECURRING stay; other keys and `api.reviewWalk.capture` stay landing-gated.
- bob-cli docs: `docs/projects.md` (Alt+N gesture order, notice, Task Link exclusion), `docs/freshness.md` (§6 outcome + landing-paragraph sentence + dated §13 entry naming nav 2.63.0). Generated glossary/decisions pages refreshed.
- Memory (all authorized): new `decisions:alt-n-answers-from-due-rows`, `answering-advances-the-walk` marked superseded-in-part with back-link, `glossary:inbox-file` routing sentence updated. Added a scope note to bead `bob-cli-4t` (record stays open there, per the `no` branch).

**Verification (all observed)**

- New suites: `test-navigation-lane-inbox-route.cjs` (17 tests) and `test-navigation-review-due-row.cjs` (12 tests) — 29/29 pass.
- Related suites (gestures, lane-toggle, inbox-route, inbox-route-card, review-advance, task-link-lane): 154/154 pass. `npm run build`, `build:check`, `validate` pass; `just docs-check` passes in both repos.
- Full plugin `npm test`: 4605/4610 pass; the 5 failures (sheet DOM, freshness-namespace, gcal, note-ready, relation-index) reproduce identically on the untouched base tree, so they are pre-existing and unrelated.

**One open item:** `bob plugins sync` refused to deploy nav to the vault because the deployed build comes from another workspace's uncommitted changes (bob-cli_15). I did not force-overwrite; the vault copy predates this change, and deployment rides with the normal land/sync flow.
