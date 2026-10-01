- **PLAN:**
  [202610/dashboard_lane_cap_and_next_query.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/dashboard_lane_cap_and_next_query.md)
- **AGENTS:**
  - [bbugyi200.apollo.40.f0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.40.f0.md)

%xprompts_enabled:false

# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first
projections of exact continuation nodes; any historical source without recoverable node
provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `3`

## Continuation Block `block:v1:22f424ef4e9aeba4bda5fae2e6b1a5e1`

- **Node:** `legacy-boundary:20261001152428:6765bdfdcfee3af0`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:6765bdfdcfee3af0`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess
transcript turns from Markdown headings.

- **Source:** agent session `40` member `40--plan`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:**
  `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-40__plan-261001_152428.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed
into guessed local turns.

```text
# Chat History - ace-run (40--plan)

- **TIMESTAMP:** 2026-10-01 15:38:50 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** 40--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-40__plan-261001_152428.md`
- 2. --code — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-40__code-261001_152428.md`

**Plan:** /home/bryan/.sase/plans/202610/dashboard_badge_parity.md


## Prompt

#gh:gh_bobs-org__bob-cli The `PENDING` and `READY` badges in the ~/bob/dash.md file show incorrect
counts that differ from the task counts shown for the queries in the corresponding
sections in that file. Can you help me diagnose the root cause of this issue and fix it?
Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:gpt-6-astra %auto

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/dashboard_badge_parity.md`

> # Make dashboard badge counts agree with their task sections
> ## Outcome and scope
> The number displayed by each dashboard lane badge must equal the number of tasks in its
> corresponding Tasks section after the caches settle. Fix PENDING and the same defect in
> NEXT, close a confirmed READY filter-parity gap, and add regression coverage that
> compares badges with the actual dashboard query contract. Preserve sticky task lanes,
> ledger-derived TODAY, freshness-gated READY, and the existing whole-lane budgets used
> outside the dashboard.
> This is a medium tale: one coding agent can implement and validate the bounded change
> across bob-plugins, the Bob vault, and bob-cli documentation. An epic and parallel

*See full plan file for details.*


```

## Continuation Block `block:v1:558fe1f5f78cd06554325730d42f5aeb`

- **Node:** `legacy-boundary:20261001153840:55f9bc5e72a9693d`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:55f9bc5e72a9693d`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess
transcript turns from Markdown headings.

- **Source:** agent session `40` member `40--gate`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:**
  `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-40__gate-20261001153840.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed
into guessed local turns.

````text
# Chat History - ace-run (40--gate)

- **TIMESTAMP:** 2026-10-01 15:38:50 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** 40--gate

## Prompt

sase gate answer --id 2fa151a1-b69f-4fe2-a83e-86660cfe8340 --kind plan

## Response

# Tale ready for review: dashboard_badge_parity.md

Gate state: answered
Reason: gate resolved automatically

Output tail:

```text
$ commands/approve
{"action": "approve", "commit_plan": false, "run_coder": true}
$ commands/commit
{"action": "approve", "commit_plan": true, "run_coder": false}
```


````

## Continuation Block `block:v1:38180ba8e8c85ecb31be73e7efe3a141`

- **Node:** `agent-delta:20261001152428:de29893d23626c7c`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:**
  `local:continuation/records/agent_delta/agent-delta:20261001152428:de29893d23626c7c.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update
supersedes it.

%model:@medium @plan:202610/dashboard_badge_parity.md

The above plan has been reviewed and approved. Implement it now.

### Assistant

Implemented the approved `202610/dashboard_badge_parity` plan.

**What changed**

- `bob-plugins` (`plugins/bob-ledger-tools/main.js`, bumped to 1.14.0): new additive
  `dashboardLaneBudget("pending"|"next")` API returning
  `{section, lane, cap, over, today}` — the section count excludes TODAY (and
  `dash.md`), while `pendingBudget()`/`nextBudget()` keep whole-lane semantics for all
  non-dashboard callers. New `renderDashboardLaneBadge` with lifecycle-owned refresh
  (Tasks-cache, TODAY, rollover, caps) reusing the existing debounce/disposal pattern.
  Fixed `readyTaskVisible` to match Tasks semantics: `#hide` is a case-insensitive
  substring match (`#hide/x`, `#Hide` now excluded) and
  `_templates`/`_conflicts`/`dash.md` checks are case-insensitive, all shared through
  one `dashboardSectionBaseVisible` predicate.
- `dash.md` (live vault): badges show the section count (e.g. PENDING 49) with
  `49 in this section; whole lane 50/10; 1 in TODAY` in tooltip/aria; NEXT section now
  uses `status.symbol is *`; fallback visibility matches the same base rules;
  unavailable stays `–`, never zero.
- New regression suite `scripts/test-ledger-tools-dashboard-parity.cjs` (wired into
  `npm test`) comparing badge models against an independent query simulation by
  identities and counts; corrected the two READY fixtures that pinned the old hide
  behavior.
- `docs/plan.md` and plugin README document the section-vs-lane split, visibility rules,
  and fallback behavior. No Rust changes.

**Verification (observed)**

- `npm test`: 1099 pass, 0 fail. `npm run validate`: 6/6 plugins valid.
- Deployed via `bob plugins sync` — vault has 1.14.0. Vault `dash.md` change auto-synced
  (`2357e5eb`, working tree clean, local/remote SHAs match).

**Limitation**: the live Obsidian UI comparison (settled badge vs. actual Tasks results
on the Mac runtime) could not be performed from this Linux workspace, so per the plan I
report that rather than claiming UI parity — headless suites are green but are not proof
of rendered parity.

---

%xprompts_enabled:true

# New Query

Now we are not showing the configured limit for these badges (e.g. we are showing `24`
instead of `24/15`) and we seem to have broken the query used in the "NEXT tasks"
section (see the ~/tmp/screenshots/20261001_160031.png screenshot for context). Can you
help me diagnose the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
