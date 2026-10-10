- **PLAN:**
  [202610/daily_dashboard_badge_parity.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_dashboard_badge_parity.md)
- **AGENTS:**
  - [bbugyi200.apollo.68.f0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.68.f0.md)

%macros_enabled:false

# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first
projections of exact continuation nodes; any historical source without recoverable node
provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `3`

## Continuation Block `block:v1:a0be844c1785cdd286c88f1ef78a38b3`

- **Node:** `legacy-boundary:20261010090011:afd7a910bdf5e8d1`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:afd7a910bdf5e8d1`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess
transcript turns from Markdown headings.

- **Source:** agent session `68` member `68--plan`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:**
  `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-68__plan-261010_090011.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed
into guessed local turns.

```text
# Chat History - ace-run (68--plan)

- **TIMESTAMP:** 2026-10-10 09:06:32 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** 68--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-68__plan-261010_090011.md`
- 2. --code — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-68__code-261010_090011.md`

**Plan:** /home/bryan/.sase/plans/202610/dashboard_badge_warnings.md


## Prompt

#gh:gh_bobs-org__bob-cli I would like to be able to finish my GTD morning review by confirming that none
of the badges shown at the top of the ~/bob/dash.md file are red, but I can't currently
do that because some of them seem to be red for no reason.

- See the ~/tmp/screenshots/20261010_085532.png screenshot for context.
- The `BLOCKED` badge is showing as red when that badge should never be red (there is no
  limit on how many blocked tasks there can be).
- The `NEXT` badge is showing as red even though there are only 10 next tasks and the
  limit is 15.

Can you help me fix these issues? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:gpt-6-astra %auto

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/dashboard_badge_warnings.md`

> # Make dashboard badge warnings trustworthy
> ## Outcome and scope
> Bryan wants the badges at the top of `dash.md` to provide a useful final morning-review
> check. BLOCKED has no cap and must always be informational. For capped dashboard lane
> badges, the count being colored must be the count shown next to the cap. A count exactly
> at the cap is acceptable; only a strict excess is red. Unknown data remains visibly
> unavailable, not a healthy zero.
> This is one medium tale: bounded changes to the Bob vault dashboard, the shared
> bob-ledger-tools dashboard renderer, regression coverage, and contract documentation.
> One coding agent can implement and validate it together. No new commands, configuration

*See full plan file for details.*


```

## Continuation Block `block:v1:853772598b20d6fe4159ce2b3d9806a2`

- **Node:** `legacy-boundary:20261010090621:494f0d2e4e7d127c`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:494f0d2e4e7d127c`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess
transcript turns from Markdown headings.

- **Source:** agent session `68` member `68--gate`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:**
  `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-68__gate-20261010090621.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed
into guessed local turns.

````text
# Chat History - ace-run (68--gate)

- **TIMESTAMP:** 2026-10-10 09:06:32 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** 68--gate

## Prompt

sase gate answer --id 85eff6fe-e105-41d3-b80a-139488648057 --kind plan

## Response

# Tale ready for review: dashboard_badge_warnings.md

Gate state: answered
Reason: gate resolved automatically

Output tail:

```text
$ commands/approve
{"action": "approve", "commit_plan": false, "decisions": {"lane_warning_scope": "section"}, "run_coder": true}
$ commands/commit
{"action": "approve", "commit_plan": true, "decisions": {"lane_warning_scope": "section"}, "run_coder": false}
```


````

## Continuation Block `block:v1:9e526e04487308cee41e83af67017e83`

- **Node:** `agent-delta:20261010090011:1cc68dd96e4bde91`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:**
  `local:continuation/records/agent_delta/agent-delta:20261010090011:1cc68dd96e4bde91.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update
supersedes it.

%model:@medium @plan:202610/dashboard_badge_warnings.md

The above plan has been reviewed and approved. Implement it now.

Auto decisions for this plan (final · no human reviewed this plan):

- lane_warning_scope = section (planner default: section). Implement the
  "lane_warning_scope = section" branch; ignore "lane_warning_scope = whole_lane".
  Context: "Should dashboard NEXT and PENDING turn red only when their displayed section
  count exceeds the cap?". Implement only the branches selected above.

### Assistant

I’ll open the plans sidecar through the SASE repo workflow, read the approved plan, then
implement its selected `section` scope in this checkout.

The plan requires coordinated changes in bob-cli, bob-plugins, and the vault checkout,
followed by plugin sync. I’m opening those repositories and loading the vault sync
guidance before touching files.

I’m applying the `sase_memory_read` workflow for the vault-specific sync instructions,
since this change includes `dash.md` and live deployment.

The three checkouts are clean. The current renderer uses the whole-lane `over` flag for
red while displaying the section count; `dash.md` repeats that mismatch, and BLOCKED is
styled red unconditionally. I’m tracing the existing model and UI tests now so the fix
covers both initial badges and live refresh.

The selected policy is now in the shared model and the inline fallback: badge color
derives from the displayed section count, with whole-lane excess called out separately.
The tooltip and accessibility copy distinguish those two caps; I’ve also made BLOCKED
informational and neutral and updated the contract docs. Next I’m rebuilding the
generated plugin entrypoint before running the focused checks.

The first focused run passed the model boundary cases, API checks, and the other
dashboard suites. One new UI assertion had the wrong expected amount: `17/15` means two
over the whole-lane cap, not seven; I corrected that expectation and am now exercising
the actual `dash.md` Dataview block through its normal, failing, legacy, and unavailable
API paths.

The focused plugin checks now pass, including both lane boundaries and the live widget
crossing above and back to the cap. The Dataview harness exercised throw/no-node
fallback and legacy boundaries; I separately corrected its high-count fixture and
confirmed BLOCKED stays neutral at 0, 378, and 5,000. I’m running the required full
plugin suite next.

The required full `npm test` completed in 16 seconds but failed in task-status-cycler
successor tests: assertions expected completion dates of 2026-10-09, while the code used
today’s date, 2026-10-10. The dashboard-focused suites still pass. I’m checking those
tests’ date setup and will leave unrelated task-cycler behavior untouched unless the
failure traces back to this change.

The full suite failures are confined to existing successor tests with hard-coded
2026-10-09 fixtures and date writers reading the actual 2026-10-10 system date. The
plan’s focused suites and repository validation pass. I’m checking the plugin sync dry
run now, then I’ll deploy only `bob-ledger-tools` from this opened source checkout.

Plugin sync completed from the opened source checkout: `manifest.json` and `main.js`
copied, `styles.css` unchanged, none skipped. The plan also calls for publishing the
vault dashboard change through the vault’s Git sync, so I’m following the repository’s
required commit workflow before syncing it.

The vault checkout commit succeeded and is clean against `origin/master`. Before running
the live vault sync, I’m checking whether the live vault has its own registered checkout
so I can verify local changes without risking unrelated edits being swept into the sync.

The vault sync brought the live checkout to the exact Bob commit (`2725e01`) with no
conflicts and no local changes staged. There’s no Obsidian GUI process available here,
so visual verification in Live Preview/Reading view is unavailable; I’m doing a final
Dataview-block smoke check against the current file before finalizing the repositories.

The final Dataview smoke check passes on the current `dash.md`: throw-after-append
cleanup leaves one lane badge, the selected fractions stay non-red for whole-lane-only
excess, unavailable values remain `–`, and BLOCKED is neutral. I’m checking the three
repository states now, then I’ll submit the required SASE final declaration for the
remaining workspace changes.

Implemented the approved `lane_warning_scope = section` behavior. NEXT and PENDING show
`section/cap` and turn red only when that displayed section exceeds its cap. Tooltips
and accessibility labels still identify whole-lane excess separately. BLOCKED is
informational, has no cap, and uses a neutral accent.

The screenshot case is now `NEXT 10/15` in normal color: 17 tasks total minus 7 in TODAY
leaves 10 in the section; the whole lane’s 2-task excess remains in the details. Daily
and CLI warnings retain whole-lane checks.

**Validation:** `npm run build`, `npm run build:check`, `npm run validate`, and the
focused dashboard suites passed. The Dataview harness exercised fallback, unavailable
data, badge grouping, navigation, and BLOCKED counts. The full `npm test` had failures
in existing task-status-cycler successor tests: fixtures expect 2026-10-09, while the
completion writer used 2026-10-10.

**Deployment:** Plugin sync copied `manifest.json` and `main.js` with no skips;
`styles.css` was unchanged. `bob plugins list` showed the plugin enabled but marked it
as drift against its default source checkout, which still reported 1.40.0. The opened
source checkout’s changes are included in the accepted SASE final declaration. The vault
change is committed as `2725e01` and synced with matching local and remote SHAs and no
conflicts.

There was no Obsidian GUI process available, so Live Preview and Reading view checks in
light and dark appearance remain unverified. The final declaration was accepted; the
host will commit the bob-cli docs and bob-plugins changes after this turn.

Changed files:
[dashboard renderer](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/070-ready-and-review.js),
[dashboard parity tests](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-dashboard-parity.cjs),
[dash.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/bobs-org/bob/dash.md),
[dashboard docs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/docs/dashboard.md),
and
[plan docs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/docs/plan.md).

---

%macros_enabled:true

# New Query

It also looks like the `NEXT` and `PENDING` badges shown in the daily file do not use
the same counts as the dash.md file. See the ~/tmp/screenshots/20261010_093245.png
screenshot for context. Can you help me fix this so daily files use the same badge
counts as the dash.md file? Think this through thoroughly and create a plan using your
`/sase_plan` skill. Choose and author the appropriate tier, validate and revalidate
until it passes, then submit it with `sase plan propose` (as the skill instructs) before
making any file changes.
