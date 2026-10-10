- **PLAN:**
  [202610/keep_capture_controls_visible_with_idle_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/keep_capture_controls_visible_with_idle_agenda.md)
- **AGENTS:**
  - [bbugyi200.apollo.6g.w1.w0.f0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.6g.w1.w0.f0.md)

%macros_enabled:false

# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first
projections of exact continuation nodes; any historical source without recoverable node
provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `3`

## Continuation Block `block:v1:78323f72ae0a80e67548028bff45f80a`

- **Node:** `legacy-boundary:20261010125719:fa190a5455b5f0a7`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:fa190a5455b5f0a7`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess
transcript turns from Markdown headings.

- **Source:** agent session `6g.w1.w0` member `6g.w1.w0--plan`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:**
  `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-6g_w1_w0__plan-261010_125719.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed
into guessed local turns.

```text
# Chat History - ace-run (6g.w1.w0--plan)

- **TIMESTAMP:** 2026-10-10 13:40:21 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** 6g.w1.w0--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-6g_w1_w0__plan-261010_125719.md`
- 2. --code — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-6g_w1_w0__code-261010_125719.md`

**Plan:** /home/bryan/.sase/plans/202610/restore_idle_agenda_after_clear.md


## Prompt

#gh:gh_bobs-org__bob-cli %w:6g.w1 The new idle display that shows the current and all future pomodoros
for the bob-mac-capture app does not come back if the user clears the input bar like it
should. See the ~/tmp/screenshots/20261010_125548.png screenshot for an example of what
this looks like. Can you help me fix this?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:gpt-6-astra %auto

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/restore_idle_agenda_after_clear.md`

> # Restore the idle Pomodoro agenda when capture input is cleared
> ## Outcome and scope
> When the user deletes the capture draft, including leaving only whitespace or newlines,
> Bob Mac Capture must immediately show its cached idle agenda again: the current Pomodoro
> and all future Pomodoros. No previous preview summary, action label, pending-list
> notice, or draft error may keep the agenda hidden or return after an asynchronous
> operation finishes. Background agenda revalidation continues through the existing store.
> This is one bounded Mac-app state-lifecycle fix and its regression coverage, implemented
> by one coding agent. Medium size accounts for the two asynchronous preview paths and the
> macOS model tests. No CLI, JSON schema, capture grammar, agenda layout, or memory

*See full plan file for details.*


```

## Continuation Block `block:v1:aea3731f6e8863e71516e08b60d2c2b2`

- **Node:** `legacy-boundary:20261010134004:eadf326e758e97b5`
- **Kind:** `legacy_boundary`
- **Parents:** (none)
- **Content:** `compat:legacy-boundary:eadf326e758e97b5`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess
transcript turns from Markdown headings.

- **Source:** agent session `6g.w1.w0` member `6g.w1.w0--gate`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:**
  `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-6g_w1_w0__gate-20261010134004.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed
into guessed local turns.

````text
# Chat History - ace-run (6g.w1.w0--gate)

- **TIMESTAMP:** 2026-10-10 13:40:20 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** 6g.w1.w0--gate

## Prompt

sase gate answer --id b5467183-1201-48fc-a9e8-d19636df3281 --kind plan

## Response

# Tale ready for review: restore_idle_agenda_after_clear.md

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

## Continuation Block `block:v1:ddf403fcd69b944352a3ea4074b2824f`

- **Node:** `agent-delta:20261010125719:be08e306bec88806`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:**
  `local:continuation/records/agent_delta/agent-delta:20261010125719:be08e306bec88806.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update
supersedes it.

%model:@medium @plan:202610/restore_idle_agenda_after_clear.md

The above plan has been reviewed and approved. Implement it now.

### Assistant

I'll start by reading the execute-plan skill and opening the plans sidecar so I can load
the approved plan.

I'll load the SASE plan and artifact skills next so I can open the sidecar plan the
right way.

I'll record the skill uses, read artifact memory, and open the plans sidecar so I can
load the approved plan.

The artifact identity is `plan:202610/restore_idle_agenda_after_clear.md`. I'll read
that plan and open the plans sidecar.

This is a tale plan for Bob Mac Capture, not a PR DAG. I’ll open that repo and load the
governing decisions next.

The linked checkout is missing, so I’ll open the GitHub fallback the plan names.

The checkout is at the planned revision. I’ll read the model, visibility, store, and
tests next.

I have the diagnosis: blank edits leave preview state around, so the agenda stays
hidden. I'll reuse the full analysis reset and add the regressions next.

Source reset is in. Next I’ll extend the agenda model tests around the blank-edit path.

Blank capture edits now restore the idle Pomodoro agenda immediately.

Bob Mac Capture’s blank-edit path reused only part of draft cleanup, so leftover preview
cards, errors, pending-list notices, and picker chips kept `agendaVisible` false after
the editor was empty. Clearing the draft now runs the same full `resetAnalysisState`
used by Discard and empty-panel presentation, including pending-list state. An in-flight
explicit Preview is retired so a late success or failure cannot refill a blank editor;
an in-flight capture keeps its request identity.

Changes are in `bob-mac-capture` (`README.md`, `CapturePanelModel.swift`,
`CaptureAgendaModelTests.swift`).

This Linux host has no Swift/AppKit toolchain, so the new regressions were not run here.
On a Mac:

```sh
./Scripts/xcode-swift.sh test --filter CaptureAgendaModelTests
./Scripts/xcode-swift.sh test --filter CapturePanelModelTests
just format-lint
just build
just test
```

---

%macros_enabled:true

# New Query

I think this broke something (see the ~/tmp/screenshots/20261010_142424.png screenshot
for context). Can you help me diagnose the root cause of this issue and fix it? Think
this through thoroughly and create a plan using your `/sase_plan` skill. Choose and
author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
