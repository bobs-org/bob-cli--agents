# Chat History - ace-run (bob-cli-ph.2--1)

- **TIMESTAMP:** 2026-11-23 18:32:27 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-ph.2--1

## Prompt

%macros_enabled:false
# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first projections of exact continuation nodes; any historical source without recoverable node provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `4`
- **Shared ancestry reused:** `1` attributed node(s)

## Continuation Block `block:v1:5e32fe933998373d0c68151b5e875da2`

- **Node:** `legacy-boundary:20261123160331:60a774161f8eb84c`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:60a774161f8eb84c`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess transcript turns from Markdown headings.

- **Source:** agent session `bob-cli-ph.2` member `bob-cli-ph.2--plan`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:** `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_ph_2__plan-261123_160331.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed into guessed local turns.

```text
# Chat History - ace-run (bob-cli-ph.2--plan)

- **TIMESTAMP:** 2026-11-23 16:11:32 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** bob-cli-ph.2--plan

**Plan:** /home/bryan/.sase/plans/202611/plugin_drawer_completion.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/plugin_drawer_completion.md`

> - **BEAD:** bob-cli-ph.2
> # Finish bob-cli-ph.2 from the landed plugin readers
> ## Outcome and scope
> Complete only assigned phase `bob-cli-ph.2`: preserve the landed dual-read plugin
> readers, repair their standalone fixture test, finish verification and deployment,
> record usable rollout evidence, and close the phase. Do not redo the recognizer or
> advance the writer, rendering, migration, or memory phases.
> This remainder fits one coding agent. The implementation and documentation already
> landed; the prior continuations stopped on unrelated timing assertions rather than an
> unfinished reader implementation. The only newly confirmed implementation gap is a

*See full plan file for details.*

## Prompt

%id(2, clan=bob-cli-ph, bead=bob-cli-ph.2)
%auto
#gh:gh_bobs-org__bob-cli
%m:gpt-6-astra 
%w(bob-cli-ph.1, for_epic=false)
%w(bead=bob-cli-ph.1)
Can you complete the work for bead bob-cli-ph.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-ph.2` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-ph.2` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-ph.2 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-ph.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-ph.2 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-ph.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-ph.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.
Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.


## Response

I’ll read the phase scope, decisions, and prior notes, then check what has already landed. I’ll use the SASE bead and planning skills to submit a validated plan before changing files.


The phase has had several earlier runs, so I’m checking their recorded work and closeout evidence before proposing anything further.


The core plugin changes have landed in commit `19ac4a3e`, and this phase has no remaining `--epic-symbol` entries. I’ll use the repository-access and prior-chat skills to check what remains—particularly verification and deployment—so the plan builds on that work.


The last run stopped on two ledger timing failures; its log reported no drawer failures. The current focused drawer, requirement-copy, and split checks are passing so far. The remaining work appears to fit one coding agent: verify the landed implementation, document any unchanged-base failures, deploy the four bundles, and record evidence before closing the phase.


I found one in-scope gap: the new drawer test suite requires bob-cli fixtures at a fixed relative path, so it fails to load in a standalone bob-plugins checkout. The approved plan required that case to work. I’ll include a small fixture-loading fix in the completion plan. All 22 focused tests pass in the linked checkout.


The plan covers the fixture test fix, independent verification gates, and deployment evidence for all four plugins. It also explicitly allows closure after documenting failures reproduced on the clean base, as you requested. I’m validating it before submitting the handoff.


The plan passed validation and is staged for review. I’m using `/sase_final` to complete the handoff; implementation and phase closure remain pending under the requested planning workflow.


Validated and staged the completion plan. Existing reader changes have landed, and 22 focused tests pass. Remaining work covers the standalone-fixture test fix, verification, deployment, and closure.

`bob-cli-ph.2` remains in progress. The requested [sase_plan workflow](/home/bryan/.codex/skills/sase_plan/SKILL.md) requires “finish through `/sase_final`” after staging; that handoff is complete.

```

## Continuation Block `block:v1:44bddf2fd0a7a346117924f5d89ce321`

- **Node:** `legacy-boundary:20261123161121:cbd4e24a310ea7e0`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:cbd4e24a310ea7e0`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess transcript turns from Markdown headings.

- **Source:** agent session `bob-cli-ph.2` member `bob-cli-ph.2--gate`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:** `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_ph_2__gate-20261123161121.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed into guessed local turns.

````text
# Chat History - ace-run (bob-cli-ph.2--gate)

- **TIMESTAMP:** 2026-11-23 16:11:31 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** bob-cli-ph.2--gate

## Prompt

sase gate answer --id ea0983ff-d07f-4a24-911c-92d1a9824054 --kind plan

## Response

# Tale ready for review: plugin_drawer_completion.md

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

## Continuation Block `block:v1:f32f5df89fc9014d98a7b7ded7d3fed2`

- **Node:** `agent-delta:20261123160331:ffeaa46c8e758acb`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:** `local:continuation/records/agent_delta/agent-delta:20261123160331:ffeaa46c8e758acb.json`
- **Checkpoint:** `local:continuation/checkpoints/gate_handoff-dc85fb65803f951d.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update supersedes it.

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202611/plugin_drawer_completion.md

The above plan has been reviewed and approved. Implement it now.

### Checkpoint

- **Kind:** `gate_handoff`

### Assistant

<!--sase:budget-span:open:kind=checkpoint;id=1;checkpoint_ref=local%3Acontinuation%2Fcheckpoints%2Fgate_handoff-dc85fb65803f951d.json;covered=agent-delta%3A20261123160331%3Affeaa46c8e758acb-->
I'll start by reading the SASE repo, artifact, and plan skills, then load the approved plan from the sidecar.

I'll record skill use, read the artifacts memory, and open the plans sidecar so I can load the approved plan.

Next I’ll audit-read the approved plan and inspect the workspace so I can implement it.

The approved phase is a test-fixture repair plus deployment closeout. I’ll load the bead, related plans, and plugin checkout next.

The phase is still in progress with no notes. I’ll open the plugin repo and load the related plans next.

While the plan artifacts finish loading, I’ll read the plugin repo’s agent rules and the current drawer test.

I’ll inspect the current drawer tests, the reqs twin-copy pattern, and the repo state so the fixture fix matches the established approach.

I have the fixture-loading defect. Next I’ll patch the test to use the plugin-local canonical copy, then confirm standalone and linked runs.

I'll update the drawer twin-copy test so vectors load from the plugin-local fixture and bob-cli comparison is optional.

I’ll write a disposable shim that proves standalone DV/DH still run, a mismatched plugin copy fails, and linked bob-cli drift is still caught.

The first shim would double-run the tests. I’ll patch `fs` only, then execute the real test file.

Standalone and linked fixture checks passed. Next I’ll run the focused plugin suites from the plan.

Focused suites passed 107/107. I’ll run the plugin build next, then the independent longer gates.

Build is clean. I’ll run validate and docs:check now, then start the longer independent test gates with logs.

docs:check is still compiling. I’ll start `npm test` and `just check` independently so a slow gate does not block the others.

docs:check passed; `npm test` failed. I’ll inspect the full log and keep waiting on `just check`.

Isolation passed. I’ll reproduce the timing failures on the clean pre-fix tree, then wait for `just check`.

The restore `cp` was blocked by an overwrite prompt. I’ll put the repaired test file back and inspect the clean-tree results.

Clean-tree `npm test` failed the same two 25 ms flakes; `just check` passed. I’ll record those follow-ups, then deploy the four dual-read plugins.

Sync is blocking two plugins deployed from other checkouts. I’ll fetch, inspect those plugin paths, and see whether those agents are still running.

Nav’s vault copy is an abandoned pre-dual-read deploy, and workspace 15 is idle. I’ll fast-forward onto origin, then ask before using `-F`.

The drawer twin suite now runs standalone, and the test repair is committed. Deployment is waiting on one overwrite question.

**Fixture repair.** `scripts/test-task-drawers-twin-copies.cjs` loads DV/DH vectors from task-status-cycler's plugin-local fixture, always compares all four plugin copies to that canonical copy, and only compares to bob-cli when that directory exists. A missing bob-cli tree emits a diagnostic; missing or malformed plugin-local fixtures still fail.

**Verification.** A filesystem shim (real bob-cli fixtures left in place) passed linked and standalone runs, still executed all four DV/DH tests, caught a mismatched plugin copy in isolation, and caught bob-cli drift when linked. Focused suites passed 107/107. `npm run build`, `npm run validate`, and `npm run docs:check` exited 0. `just check` on bob-cli 588c6210 exited 0.

**Unrelated `npm test` red.** Full `npm test` failed only the two tracked 25 ms ledger nodes: `test-ledger-tools-event-link-times.cjs:1069` (82.4 ms) and `test-ledger-tools-frees-marks.cjs:481` (201 ms). Isolation passed 40/40. The same two failed on clean `a73f70bf` (68.6 ms and 183 ms). Tracked by `bob-cli-km` and `bob-cli-io`; recorded as a `PROPOSED FOLLOW-UP` on `bob-cli-ph.2`.

**Deploy.** After fast-forward to `d3a17f0c`:
- `task-status-cycler` and `block-id-prompt` are `synced`, vault `main.js` matches source, and `bob-task-drawer-dual-read-v1` is present.
- `bob-ledger-tools` is blocked: uncommitted deploy from workspace 10, and `bob-cli-pf.5.1.7` is still running. No `-F`.
- `bob-navigation-hotkeys` is an abandoned pre-dual-read vault copy (no marker). Sync refuses without `-F`. That overwrite question is staged.

The follow-up should wait for `bob-cli-pf.5.1.7`, honor the nav answer, deploy the four plugins from the committed tree, run smoke, then close `bob-cli-ph.2`.
<!--sase:budget-span:close:1-->

## Continuation Block `block:v1:c4398c2ce6c3a8551d8a57cff1759866`

- **Node:** `legacy-boundary:20261123165246:1383bd2cf60f6ada`
- **Kind:** `legacy_boundary`
- **Parents:** `agent-delta:20261123160331:ffeaa46c8e758acb`
- **Content:** `compat:legacy-boundary:1383bd2cf60f6ada`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess transcript turns from Markdown headings.

- **Source:** agent session `bob-cli-ph.2` member `bob-cli-ph.2--gate-0`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:** `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_ph_2__gate_0-20261123165246.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed into guessed local turns.

````text
# Chat History - ace-run (bob-cli-ph.2--gate-0)

- **TIMESTAMP:** 2026-11-23 18:15:20 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-ph.2--gate-0

## Prompt

sase gate answer --id 5c356a70-205d-4b85-ba76-6938a5aef1e5 --kind question

## Response

# bob plugins sync refuses to overwrite bob-navigation-hotkeys without -F. The vau

Gate state: answered
Reason: gate answered
Selected options: submit

Branches:

- [x] Submit answers (submit)

Option results:

[
  {
    "id": "submit",
    "result": {
      "answers": [
        {
          "custom_feedback": null,
          "question": "bob plugins sync refuses to overwrite bob-navigation-hotkeys without -F. The vault copy is version 2.107.0 from an uncommitted bob-cli_15 deploy at 8efc5a6d (2026-11-23T18:13:26Z, apollo). No agent is still running in that checkout, and git log HEAD..@{upstream} -- plugins/bob-navigation-hotkeys is empty, so those vault bytes never landed. -F would discard vault main.js sha256 d2b3bdd19c3bd292205b7a603906b37a2e081b35aa953c3e0caa2d41da76b5de (4,760,186 bytes, no bob-task-drawer-dual-read-v1 marker) and styles.css sha256 e9b654f7687861ffbfa13193aac84748a0b096233170071b4f05686aca10374a, replacing them with this checkout's dual-read bundle (main.js c3c4bbdf4dbd4a076f9c3ae0eecd5bc66caa4b39f8292420ab3ce9f1c7c3d5c7, marker present). That vault copy predates landed 19ac4a3e (dual-read drawer readers) and 6d98af17 (diamond ink staged requirement cues). Overwrite the abandoned vault nav deploy?",
          "selected": [
            "Yes, overwrite with -F"
          ]
        }
      ],
      "global_note": ""
    }
  }
]

Output tail:

```text
$ commands/submit
{"answers": [{"custom_feedback": null, "question": "bob plugins sync refuses to overwrite bob-navigation-hotkeys without -F. The vault copy is version 2.107.0 from an uncommitted bob-cli_15 deploy at 8efc5a6d (2026-11-23T18:13:26Z, apollo). No agent is still running in that checkout, and git log HEAD..@{upstream} -- plugins/bob-navigation-hotkeys is empty, so those vault bytes never landed. -F would discard vault main.js sha256 d2b3bdd19c3bd292205b7a603906b37a2e081b35aa953c3e0caa2d41da76b5de (4,760,186 bytes, no bob-task-drawer-dual-read-v1 marker) and styles.css sha256 e9b654f7687861ffbfa13193aac84748a0b096233170071b4f05686aca10374a, replacing them with this checkout's dual-read bundle (main.js c3c4bbdf4dbd4a076f9c3ae0eecd5bc66caa4b39f8292420ab3ce9f1c7c3d5c7, marker present). That vault copy predates landed 19ac4a3e (dual-read drawer readers) and 6d98af17 (diamond ink staged requirement cues). Overwrite the abandoned vault nav deploy?", "selected": ["Yes, overwrite with -F"]}], "global_note": ""}
```


````

---

%macros_enabled:true
# New Query
%model:grok-4.6
%effort:high

%macros_enabled:false
# Gate answered

**Decision:** bob plugins sync refuses to overwrite bob-navigation-hotkeys without -F. The vau

| | |
| --- | --- |
| **Outcome** | ANSWERED — Submit answers |
| **Answered via** | tui |
| **Opened** | 2026-11-23T21:52:47Z |
| **Answered** | 2026-11-23T23:15:20Z |
| **Commands** | 1 of 1 completed |
| **Gate** | question/5c356a70-205d-4b85-ba76-6938a5aef1e5 |

## Results

### submit — `commands/submit`

```json
{
  "answers": [
    {
      "custom_feedback": null,
      "question": "bob plugins sync refuses to overwrite bob-navigation-hotkeys without -F. The vault copy is version 2.107.0 from an uncommitted bob-cli_15 deploy at 8efc5a6d (2026-11-23T18:13:26Z, apollo). No agent is still running in that checkout, and git log HEAD..@{upstream} -- plugins/bob-navigation-hotkeys is empty, so those vault bytes never landed. -F would discard vault main.js sha256 d2b3bdd19c3bd292205b7a603906b37a2e081b35aa953c3e0caa2d41da76b5de (4,760,186 bytes, no bob-task-drawer-dual-read-v1 marker) and styles.css sha256 e9b654f7687861ffbfa13193aac84748a0b096233170071b4f05686aca10374a, replacing them with this checkout's dual-read bundle (main.js c3c4bbdf4dbd4a076f9c3ae0eecd5bc66caa4b39f8292420ab3ce9f1c7c3d5c7, marker present). That vault copy predates landed 19ac4a3e (dual-read drawer readers) and 6d98af17 (diamond ink staged requirement cues). Overwrite the abandoned vault nav deploy?",
      "selected": [
        "Yes, overwrite with -F"
      ]
    }
  ],
  "global_note": ""
}
```

## Your next action

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202611/plugin_drawer_completion.md

The above plan has been reviewed and approved. Implement it now.


### Questions and Answers

#### Q1: Overwrite nav plugin

> bob plugins sync refuses to overwrite bob-navigation-hotkeys without -F. The vault copy is version 2.107.0 from an uncommitted bob-cli_15 deploy at 8efc5a6d (2026-11-23T18:13:26Z, apollo). No agent is still running in that checkout, and git log HEAD..@{upstream} -- plugins/bob-navigation-hotkeys is empty, so those vault bytes never landed. -F would discard vault main.js sha256 d2b3bdd19c3bd292205b7a603906b37a2e081b35aa953c3e0caa2d41da76b5de (4,760,186 bytes, no bob-task-drawer-dual-read-v1 marker) and styles.css sha256 e9b654f7687861ffbfa13193aac84748a0b096233170071b4f05686aca10374a, replacing them with this checkout's dual-read bundle (main.js c3c4bbdf4dbd4a076f9c3ae0eecd5bc66caa4b39f8292420ab3ce9f1c7c3d5c7, marker present). That vault copy predates landed 19ac4a3e (dual-read drawer readers) and 6d98af17 (diamond ink staged requirement cues). Overwrite the abandoned vault nav deploy?

- [x] **Yes, overwrite with -F** — Replace the abandoned pre-dual-read vault nav 2.107.0 bundle with the dual-read source so this phase can finish that deploy.
- [ ] **No, keep the vault copy** — Leave bob-navigation-hotkeys protected. This phase cannot record a synced dual-read nav deploy until that build lands or you later authorize -F.

%macros_enabled:true

## Response

I'll pick up from the approved overwrite: read the plan and skills, then deploy nav with `-F` and finish the remaining dual-read plugin closeout.

Skills are loaded. Next I’ll record skill use, read the artifacts memory, and open the plan sidecar.

I’ll load the approved plan, open the plugin and plans repos, and check whether `bob-cli-pf.5.1.7` still blocks ledger deploy.

The plan read is still running. I’ll wait for it and pull the bead plus `bob-cli-pf.5.1.7` status from the truncated output.

Nav overwrite is approved; ledger is still held by `bob-cli-pf.5.1.7`. I’ll read plugin deploy rules and inspect current source and vault state.

Plugin tree is clean at the fixture-repair commit. I’ll inspect current vault sync state, then overwrite nav with `-F` and reassess ledger.

List now reports all 12 plugins synced. I’ll extract the four dual-read rows, hashes, and dry-run sync so we know whether `-F` is still required.

Vault bytes already match the dual-read source, so `-F` is unnecessary. I’ll restamp the four plugins from this clean commit, then run smoke as far as this host allows.

Athena has Obsidian; apollo does not. I’ll restamp the four plugins here, then run isolated smoke on athena.

All four plugins restamped clean at `63e9e760`. Next I’ll run local self-test and isolated Obsidian smoke on athena.

I’ll set up a throwaway worktree on athena and run isolated Obsidian smoke plus the deployed-vault check.

Athena smoke passed, including the deployed-vault check. I’ll save the report, record deploy evidence, and close the phase.

Artifacts are stored. I’ll record the per-plugin deploy evidence and close `bob-cli-ph.2`.

Closed `bob-cli-ph.2`. Dual-read readers are deployed from clean bob-plugins `63e9e760` and Obsidian smoke passed.

**Deploy (apollo vault, restamped 2026-11-23T23:21:06Z).** All four plugins are `synced` from this SHA, with `bob-task-drawer-dual-read-v1` in source and vault `main.js`, hashes equal:

| Plugin | Version | `main.js` SHA-256 |
| --- | --- | --- |
| task-status-cycler | 1.58.3 | `451084581ab2305af4301315b9d47ca5ff7eda96b503e64fb3a72d647fe14fa3` |
| block-id-prompt | 1.45.0 | `87fece9b22afd6d0a3fb1b5a2bf122c493369bad7b48abc5ac32a520e146dadd` |
| bob-ledger-tools | 1.157.1 | `b6580dde7e5c60044e19af2d7470b980e896692f0bb90e1a2495c49774aab556` |
| bob-navigation-hotkeys | 2.107.0 | `c3c4bbdf4dbd4a076f9c3ae0eecd5bc66caa4b39f8292420ab3ce9f1c7c3d5c7` |

The approved nav `-F` was not needed: vault bytes already matched the dual-read bundle, so the sync rewrote the stamp without force.

**Smoke.** Apollo has no Obsidian/xvfb. Athena ran the isolated startup plus deployed-vault check against a worktree at `63e9e760` and the rsynced apollo plugins: **PASS**. Layout-ready 436 ms, heap 59.7 MiB, four editors ok, 0 exceptions/crashes, 12 synced / 0 drift. Report: `file:explicit:ea63e67c4a620dbad55354a6`.

**Readers.** Drawer twin suite 13/13 on this SHA, including standalone fixture load and legacy Notes writers (`- NOTES`). Offline self-test 17/17 (not an Obsidian pass). `build:check` exited 0.

The two 25 ms ledger timing flakes stay recorded as `PROPOSED FOLLOW-UP` (`bob-cli-km`, `bob-cli-io`) and did not keep this phase open. Parent epic `bob-cli-ph` is still open; `bob-cli-ph.3` can proceed.
