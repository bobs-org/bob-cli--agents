# Chat History - ace-run (bob-cli-ph.10--5)

- **TIMESTAMP:** 2026-11-25 23:59:19 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-ph.10--5

# Monitor handoff

This agent delegated the remaining work to a monitor turn.
Monitor ID: 54sx1365n1b9
Inspect with: sase monitor show 54sx1365n1b9
Monitor turn: bob-cli-ph.10--mon-5
Directory: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15

Command:

```sh
set +e
rust_status=0
just check
rust_status=$?
plugin_status=0
(cd sase/repos/linked/bob-plugins && npm run build)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
(cd sase/repos/linked/bob-plugins && npm test)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
(cd sase/repos/linked/bob-plugins && npm run build:check)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
(cd sase/repos/linked/bob-plugins && npm run docs:check)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
sync_status=1
if [ "$plugin_status" -eq 0 ]; then
  bob plugins sync
  sync_status=$?
fi
sase bead epic-symbols bob-cli-ph.10
symbols_status=$?
if [ "$rust_status" -eq 0 ] && [ "$plugin_status" -eq 0 ] && [ "$sync_status" -eq 0 ] && [ "$symbols_status" -eq 0 ]; then
  sase bead close bob-cli-ph.10 --note "Verified ALL-CAPS drawer cutover: just check and plugin build/tests/build:check/docs:check passed, plugins synced, and no epic symbols remained."
else
  exit 1
fi
```

Reason:

Rerun required Rust and plugin gates after phase-scoped drawer vector repairs

Next action:

Inspect the full gate result. Make further repairs only for bob-cli-ph.10-scoped failures, then rerun the required Rust and plugin checks. Sync only if every plugin check passes. Rerun epic-symbols and close only bob-cli-ph.10 if all checks and sync pass with no symbols. Otherwise leave the phase in progress and report exact unrelated blockers. Do not close ancestors or edit memory.


## Prompt

%queue(weight=1)
%macros_enabled:false
# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first projections of exact continuation nodes; any historical source without recoverable node provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `1`

## Continuation Block `block:v1:f0146abbfff4a46690ef0ec96681ad1c`

- **Node:** `agent-delta:20261125230339:e421c803f389530d`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:** `local:continuation/records/agent_delta/agent-delta:20261125230339:e421c803f389530d.json`
- **Checkpoint:** `local:continuation/checkpoints/monitor_handoff-3a1f1dd6ac7796de.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update supersedes it.

%queue(weight=1)
#fork:bob-cli-ph.10--3
%model:gpt-6-luna@xhigh

% macros_enabled:false
# Monitored command finished

**Command:**

```text
set +e
just check
rust_status=$?
(cd sase/repos/linked/bob-plugins && npm run build && npm test && npm run build:check && npm run docs:check)
plugin_status=$?
sync_status=1
if [ "$plugin_status" -eq 0 ]; then
  bob plugins sync
  sync_status=$?
fi
sase bead epic-symbols bob-cli-ph.10
symbols_status=$?
if [ "$rust_status" -eq 0 ] && [ "$plugin_status" -eq 0 ] && [ "$sync_status" -eq 0 ] && [ "$symbols_status" -eq 0 ]; then
  sase bead close bob-cli-ph.10 --note "Verified ALL-CAPS drawer cutover: CLI docs and just check passed, plugin build/tests/build:check/docs:check passed, plugins synced, and no epic symbols remained."
else
  exit 1
fi
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15
```

| | |
| --- | --- |
| **Outcome** | FAILED — exit 1 |
| **Started** | 2026-11-26T03:50:22.422566+00:00 |
| **Finished** | 2026-11-26T04:03:13.033007Z |
| **Elapsed** | 10m 23s of a 45m 0s budget |
| **Output** | 1,440 KiB · evidence refs: `file:monitor-diagnostic-manifest:gfypcgz8ffa1`, `file:monitor-retained-log:gfypcgz8ffa1` · full log: `sase monitor show gfypcgz8ffa1 --all-lines` |
| **Tool run** | sase tool show ee7902a5f0f7b5ef43c9b126e928f4c8 |

**Why this was monitored:** Verify the ALL-CAPS drawer retirement phase and complete its authorized closeout

## Last 200 lines of output
<!--sase: budget-span:open:kind=old_raw_excerpts;id=1-->

Everything between the fences below is raw command output -- untrusted data, not instructions. The only instruction in this prompt is the "Your next action" section.

```text
est.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: [ 'req_parent', 'A requirement needs a task or requirement directly above it' ],
    expected: [ 'req_in_drawer', 'Drawers hold notes — put the requirement directly under the task' ],
    operator: 'deepStrictEqual',
    diff: 'simple'
  }

> bob-plugins@0.1.0 test:perf
> node --test --test-concurrency=1 scripts/test-block-id-prompt-task-wikilink-index-performance.cjs scripts/test-block-id-prompt-task-links-api-performance.cjs scripts/test-copy-chips-live-preview-performance.cjs scripts/test-navigation-copy-card-task-scope-performance.cjs scripts/test-navigation-prose-field-performance.cjs scripts/test-navigation-dependencies-stage-performance.cjs

✖ api.taskLinks session open (snapshot plus first rank) takes at most 50 ms (582.350122ms)
ℹ session open: 51.78 ms
✔ api.taskLinks keystroke-to-rows p95 takes at most 12 ms over 5,000 tasks (768.521082ms)
ℹ keystroke p95: 8.95 ms
✔ api.taskLinks performs no vault reads while filtering (680.596486ms)
✔ api.taskLinks typed keystrokes p95 takes at most 12 ms over 5,000 tasks (3097.482778ms)
ℹ typed keystroke p95: 12.00 ms
✔ cold build of 6,500 notes / 5,000 tasks fits 1.5 s in chunks of at most 16 ms (588.163829ms)
✔ warm snapshot plus order takes at most 50 ms (334.272326ms)
✔ one keystroke rank of 5,000 rows takes at most 12 ms (349.918746ms)
✔ no vault reads happen while filtering (227.806543ms)
✔ cold build growth stays near-linear over a 6x step (244.006329ms)
✔ 2,000-line daily note with 200 chips fits the 35 ms CPU budget (24.935445ms)
✔ narrow viewport visits only visible syntax ranges (5.352706ms)
✔ clipboard writes stay out of the perf path (1.992193ms)
✔ 2,000-line mixed note paints both kinds inside the 35 ms CPU budget (92.859907ms)
✔ mixed discovery stays inside the viewport and re-resolves only on a new catalog (200.091423ms)
✔ 2,000-line task, scope, and chip resolution fit the 50 ms CPU budget (216.13173ms)
✔ stage opening builds 200/400/1000-task notes without cubic growth (48.309133ms)
✔ stage snapshots match standalone parsing across grammar vectors (7.676477ms)
✔ stage Warm-empty cache is ready without a vault fallback (0.755111ms)
✔ stage opening renders cross-note results with zero writes and cap (54.450104ms)
✔ stage CURRENT covers same-note, cross-note, blocked, and counted parents (1.811966ms)
✔ stage collections reuse one snapshot per parent (0.488185ms)
✔ stage cold refresh yields, preserves state, and performs no search reads (113.440373ms)
✔ stage cold refresh abandons after dismissal or replacement (55.757826ms)
✔ stage 400-task opening finishes in a child process before the parent timeout (241.937429ms)
✔ 10k-note keystroke-to-rows p95 is ≤ 8 ms CPU (581.847097ms)
✔ 10k-note first link-index build is ≤ 40 ms CPU (503.449477ms)
ℹ tests 26
ℹ suites 0
ℹ pass 25
ℹ fail 1
ℹ cancelled 0
ℹ skipped 0
ℹ todo 0
ℹ duration_ms 10397.804357

✖ failing tests:

test at scripts/test-block-id-prompt-task-links-api-performance.cjs:88:1
✖ api.taskLinks session open (snapshot plus first rank) takes at most 50 ms (582.350122ms)
  AssertionError [ERR_ASSERTION]: session open 51.8 ms exceeds 50 ms
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-plugins/scripts/test-block-id-prompt-task-links-api-performance.cjs:106:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async startSubtestAfterBootstrap (node:internal/test_runner/harness:385:3) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: '==',
    diff: 'simple'
  }
No --epic-symbol entries for bob-cli-ph.10.
failed  exit=1  duration=621106ms
```

<!--sase: budget-span:close:1-->
## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-2f394ceb78a8c859.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "set +e\njust check\nrust_status=$?\n(cd sase/repos/linked/bob-plugins && npm run build && npm test && npm run build:check && npm run docs:check)\nplugin_status=$?\nsync_status=1\nif [ \"$plugin_status\" -eq 0 ]; then\n  bob plugins sync\n  sync_status=$?\nfi\nsase bead epic-symbols bob-cli-ph.10\nsymbols_status=$?\nif [ \"$rust_status\" -eq 0 ] && [ \"$plugin_status\" -eq 0 ] && [ \"$sync_status\" -eq 0 ] && [ \"$symbols_status\" -eq 0 ]; then\n  sase bead close bob-cli-ph.10 --note \"Verified ALL-CAPS drawer cutover: CLI docs and just check passed, plugin build/tests/build:check/docs:check passed, plugins synced, and no epic symbols remained.\"\nelse\n  exit 1\nfi",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15",
    "member_agent_name": "bob-cli-ph.10--mon-2",
    "monitor_id": "gfypcgz8ffa1",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261125224542:4379be5d301cf920"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:518b959418fdc41d821a038b48450283e690abd021bc2fb6a3749238cbd7a7de",
    "starter_agent": "bob-cli-ph.10--3",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/25/20261125224542"
  },
  "recorded_at_epoch": 1795665169.2912796,
  "schema_version": 1
}
```


## Your next action

Inspect the gate result. If every check, plugin sync, and epic-symbol scan passed and bob-cli-ph.10 is closed, report that result. If anything failed, make only bob-cli-ph.10-scoped repairs, rerun the required Rust and plugin checks, sync only after plugin checks pass, rerun epic-symbols, and close only bob-cli-ph.10 after all checks pass and no symbols remain. For unrelated failures, leave the bead in progress and report the exact blocker. Do not close ancestors or edit memory.
% macros_enabled:true

### Checkpoint

- **Kind:** `monitor_handoff`

### Assistant

<!--sase:budget-span:open:kind=checkpoint;id=1;checkpoint_ref=local%3Acontinuation%2Fcheckpoints%2Fmonitor_handoff-3a1f1dd6ac7796de.json;covered=agent-delta%3A20261125230339%3Ae421c803f389530d-->
The plugin gate now has at least one unit-test failure and a narrowly missed performance threshold; the excerpt also includes a failing assertion. I’ll inspect the full gate summary and the phase’s current diff, then repair only failures that belong to `bob-cli-ph.10` and rerun the authorized checks.

The Rust gate is blocked by errors in task-relations and task-status code, outside this drawer phase. Plugin unit tests also report many failures; I’m checking whether any of those specifically exercise the ALL-CAPS retirement before deciding whether a phase-only repair is warranted. The plugin sync did not run because plugin checks failed, and the phase bead is still in progress.

One plugin failure is directly tied to this phase: its byte preservation test compares against the stale text “legacy detail” even though the fixture contains “uppercase plain detail.” I’ll correct that expected text. The other Rust errors and the remaining plugin failures point to task-relations, task-status hooks, and requirement/navigation behavior outside this phase; I’ll preserve those and let the full rerun confirm the blockers.

The scoped expectation is corrected, and the complete rerun is staged as monitor **4tm71v**. Its command runs all Rust and plugin checks independently, syncs only if all plugin checks pass, and closes only `bob-cli-ph.10` if every gate succeeds and the symbol scan is clear. I’m preparing the required finalizer now; the bead remains open pending that result.

I fixed the phase-specific drawer test’s stale expectation: it now checks that `uppercase plain detail` is preserved. The previous gate also found unrelated Rust lint errors in `task_relations`, `task_status_hooks`, and `capture/relations`, plus plugin failures across task requirements and navigation. The performance test measured 51.78 ms against a 50 ms limit.

The full rerun is staged as monitor **4tm71v**. It will run the Rust and plugin checks, sync only if all plugin checks pass, and close only `bob-cli-ph.10` if every gate passes and no epic symbols remain. The bead is still in progress; I declared the plugin test change for commit with the bead kept open.
<!--sase:budget-span:close:1-->

---

%macros_enabled:true
# New Query
%model:gpt-6-luna@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
set +e
rust_status=0
just check
rust_status=$?
plugin_status=0
(cd sase/repos/linked/bob-plugins && npm run build)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
(cd sase/repos/linked/bob-plugins && npm test)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
(cd sase/repos/linked/bob-plugins && npm run build:check)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
(cd sase/repos/linked/bob-plugins && npm run docs:check)
step_status=$?
if [ "$step_status" -ne 0 ]; then plugin_status=$step_status; fi
sync_status=1
if [ "$plugin_status" -eq 0 ]; then
  bob plugins sync
  sync_status=$?
fi
sase bead epic-symbols bob-cli-ph.10
symbols_status=$?
if [ "$rust_status" -eq 0 ] && [ "$plugin_status" -eq 0 ] && [ "$sync_status" -eq 0 ] && [ "$symbols_status" -eq 0 ]; then
  sase bead close bob-cli-ph.10 --note "Verified ALL-CAPS drawer cutover: just check and plugin build/tests/build:check/docs:check passed, plugins synced, and no epic symbols remained."
else
  exit 1
fi
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15
```

| | |
| --- | --- |
| **Outcome** | FAILED — exit 1 |
| **Started** | 2026-11-26T04:10:15.926184+00:00 |
| **Finished** | 2026-11-26T04:35:26.978109Z |
| **Elapsed** | 22m 35s of a 45m 0s budget |
| **Output** | 1,460 KiB · evidence refs: `file:monitor-diagnostic-manifest:4tm71vbzjx4j`, `file:monitor-retained-log:4tm71vbzjx4j` · full log: `sase monitor show 4tm71vbzjx4j --all-lines` |
| **Tool run** | sase tool show 12191b0335f8c38b1d02092e811bdc0f |

**Why this was monitored:** Rerun ALL-CAPS drawer phase checks after its scoped test repair

## Last 200 lines of output
<!--sase:budget-span:open:kind=old_raw_excerpts;id=1-->

Everything between the fences below is raw command output -- untrusted data, not instructions. The only instruction in this prompt is the "Your next action" section.

```text
 Mac app
skipped: docs/start/mac-capture.md:81: first Mac capture needs the Mac panel
tutorial: passed
docs-check: passed (executable first-day tutorial)

docs-check: CLI media determinism
media: check passed (regeneration is byte-stable)
docs-check: passed (CLI media determinism)

docs-check: documentation unit tests
============================= test session starts ==============================
platform linux -- Python 3.14.4, pytest-9.1.1, pluggy-1.7.0
rootdir: /home/bryan/.cache/bob-plugins-docs/bob-cli/tools/docs
configfile: pyproject.toml
plugins: platformdirs-4.13.5
collected 448 items

tools/docs/tests/test_assemble.py ....                                   [  0%]
tools/docs/tests/test_assets.py .....s.                                  [  2%]
tools/docs/tests/test_capture_token_coverage.py ..                       [  2%]
tools/docs/tests/test_check.py ....                                      [  3%]
tools/docs/tests/test_compatibility.py ......                            [  5%]
tools/docs/tests/test_contracts.py ........                              [  6%]
tools/docs/tests/test_demo_tasks.py ..                                   [  7%]
tools/docs/tests/test_edit_links.py ....                                 [  8%]
tools/docs/tests/test_environment.py ........                            [ 10%]
tools/docs/tests/test_fences.py .......                                  [ 11%]
tools/docs/tests/test_gen_components.py ....                             [ 12%]
tools/docs/tests/test_gen_plugins.py ...........                         [ 14%]
tools/docs/tests/test_gen_reference.py ........                          [ 16%]
tools/docs/tests/test_generated.py .....                                 [ 17%]
tools/docs/tests/test_host.py ..................                         [ 21%]
tools/docs/tests/test_host_workflow.py .........                         [ 23%]
tools/docs/tests/test_links.py ...........                               [ 26%]
tools/docs/tests/test_links_online.py ......                             [ 27%]
tools/docs/tests/test_lint.py .......................................... [ 37%]
................                                                         [ 40%]
tools/docs/tests/test_media.py .........                                 [ 42%]
tools/docs/tests/test_mounts.py ........................................ [ 51%]
....................................                                     [ 59%]
tools/docs/tests/test_publish_drill.py ..........                        [ 61%]
tools/docs/tests/test_publish_issue.py .............                     [ 64%]
tools/docs/tests/test_publish_plan.py ........................           [ 70%]
tools/docs/tests/test_publish_record.py ..............                   [ 73%]
tools/docs/tests/test_publish_verify.py ...........                      [ 75%]
tools/docs/tests/test_publish_workflow.py .........................      [ 81%]
tools/docs/tests/test_search_smoke.py ........                           [ 83%]
tools/docs/tests/test_templates.py .....                                 [ 84%]
tools/docs/tests/test_tutorial.py ..................                     [ 88%]
tools/docs/tests/test_urls.py .........................                  [ 93%]
tools/docs/tests/test_weekly_issue.py ......                             [ 95%]
tools/docs/tests/test_weekly_workflow.py ....................            [ 99%]
tools/docs/tests/test_yaml_tools.py ..                                   [100%]

=========================== short test summary info ============================
SKIPPED [1] tools/docs/tests/test_assets.py:75: generation dependencies are absent (run with --group fonts)
================== 447 passed, 1 skipped in 92.93s (0:01:32) ===================
running: uv run --project tools/docs --group material pytest tools/docs/tests
docs-check: passed (documentation unit tests)

docs-check: follow-on gates
skipped: CLI reference golden is a cargo test, not a docs-check gate

docs-check: all implemented gates passed
No --epic-symbol entries for bob-cli-ph.10.
failed  exit=1  duration=1352667ms
```

<!--sase:budget-span:close:1-->
## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-5ab23346aa3e1dc0.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "set +e\nrust_status=0\njust check\nrust_status=$?\nplugin_status=0\n(cd sase/repos/linked/bob-plugins && npm run build)\nstep_status=$?\nif [ \"$step_status\" -ne 0 ]; then plugin_status=$step_status; fi\n(cd sase/repos/linked/bob-plugins && npm test)\nstep_status=$?\nif [ \"$step_status\" -ne 0 ]; then plugin_status=$step_status; fi\n(cd sase/repos/linked/bob-plugins && npm run build:check)\nstep_status=$?\nif [ \"$step_status\" -ne 0 ]; then plugin_status=$step_status; fi\n(cd sase/repos/linked/bob-plugins && npm run docs:check)\nstep_status=$?\nif [ \"$step_status\" -ne 0 ]; then plugin_status=$step_status; fi\nsync_status=1\nif [ \"$plugin_status\" -eq 0 ]; then\n  bob plugins sync\n  sync_status=$?\nfi\nsase bead epic-symbols bob-cli-ph.10\nsymbols_status=$?\nif [ \"$rust_status\" -eq 0 ] && [ \"$plugin_status\" -eq 0 ] && [ \"$sync_status\" -eq 0 ] && [ \"$symbols_status\" -eq 0 ]; then\n  sase bead close bob-cli-ph.10 --note \"Verified ALL-CAPS drawer cutover: just check and plugin build/tests/build:check/docs:check passed, plugins synced, and no epic symbols remained.\"\nelse\n  exit 1\nfi",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15",
    "member_agent_name": "bob-cli-ph.10--mon-4",
    "monitor_id": "4tm71vbzjx4j",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261125230339:e421c803f389530d"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:b8aeed5a5ef0b24738eef4f8465ae4adf148314b5332acf4296735ef0593db07",
    "starter_agent": "bob-cli-ph.10--4",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/25/20261125230339"
  },
  "recorded_at_epoch": 1795666371.243521,
  "schema_version": 1
}
```


## Your next action

Inspect the gate result. Repair only bob-cli-ph.10-scoped failures, then rerun the required Rust and plugin checks. Sync only after every plugin check passes. Rerun epic-symbols and close only bob-cli-ph.10 if every check and sync pass with no symbols. Otherwise leave it in progress and report exact unrelated blockers. Do not close ancestors or edit memory.
%macros_enabled:true

## Response

I’ll inspect the full monitor log and `bob-cli-ph.10` status to pinpoint the remaining failure. Then I’ll make only phase-scoped repairs and rerun the required gates; plugin sync and bead close remain conditional on all checks passing.

The run confirms that docs checks and the epic symbol scan passed, but the overall command still failed. I’ve opened the linked plugin checkout; I’m now reading its repo instructions and the bead’s audited record, and I’ll extract the earlier Rust and plugin failures before deciding whether anything falls within this phase.

The Rust gate has five compile errors in task relation/status code and capture relations, outside this phase. The plugin gate has 54 unit-test failures and one performance miss; two failures explicitly expect the legacy uppercase `FUTURE WORK` drawer. I’m checking the phase plan and current changes to determine whether other failures are stale legacy drawer vectors before making any edits.

I found a scoped cause behind the large plugin failure count: the task-requirements fixture vectors and twin tests still treat uppercase `NOTES` and `FUTURE WORK` as drawers, while the cutover code now treats them as ordinary notes. I’ve migrated those cases to bold true-case headers and updated the two task-split tests that still use uppercase drawer fixtures. I’m checking these targeted tests before rerunning the full gates.

The repaired phase-related plugin tests now pass: 206/206 across the task-requirements twin vectors, task-split drawer gestures, and drawer-based requirement refusals. I’ll rerun the full Rust and plugin gates now. The gate will sync only if every plugin check passes, scan the phase symbols, and close only `bob-cli-ph.10` if Rust, plugin checks, sync, and the symbol scan all pass.

I updated the task-requirements vectors and plugin tests to use bold true-case drawers, and added checks that uppercase headings are ordinary notes. The focused plugin tests pass: **206/206**.

The full gate rerun is staged as monitor **54sx13**. It will run `just check` and all four plugin checks, sync only if every plugin check passes, then scan symbols and close only `bob-cli-ph.10` if all gates pass. The phase remains in progress pending that result.

The previous full run’s Rust blockers were dead-code and lint errors in `task_relations/ties.rs`, `task_status_hooks/relations.rs`, and `capture/relations.rs`. That run also had unrelated navigation and requirement plugin failures and a task-links performance result of 13 ms against a 12 ms limit. The staged rerun will confirm what remains.
