# Chat History - ace-run (bob-cli-pl.1--3)

- **TIMESTAMP:** 2026-11-24 11:24:06 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** bob-cli-pl.1--3

# Monitor handoff

This agent delegated the remaining work to a monitor turn.
Monitor ID: 0q0abkf6g6pt
Inspect with: sase monitor show 0q0abkf6g6pt
Monitor turn: bob-cli-pl.1--mon-2
Directory: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16

Command:

```sh
python3 .git/pl1-acceptance/live-cleanup-retry.py
```

Reason:

Verify project count cleanup without racing the stale Mac writer through vault-sync

Next action:

Resume only bob-cli-pl.1. Read its latest phase note and .git/pl1-acceptance/recovery-checkpoint.json plus the frozen checkpoint.json. All source work, source tests, clean-base timing-failure proof, docs gates, CRLF fixture and real Obsidian Base acceptance are complete. This controlled retry uses the original guarded node script and fresh Bob binary, preserves original preimages, snapshots current notes separately, temporarily pauses Apollo sync between transactions and restores it with finally and a watchdog. First confirm bob-vault-sync.service is active; if not, restore it. On success inspect live-result.json, live-retry-dry-run.log, live-retry-apply.log, live-repeat.log, live-diff-stat.txt and live-diff-numstat.txt: exactly two key lines per note, dry-run unchanged, zero remaining_at_verification, repeat_noop and sync_restored true. Attach a durable final receipt and record phase evidence. The approved one-writer plan explicitly expects stale hosts can re-add keys until athena and Mac run bob plugins sync; Mac restoration is proven in 48c5a395a and file:explicit:5c8a64dd5b630b4d7f26d2e5. Distinguish the verified acceptance snapshot from subsequent stale-host writes and report any recurrence honestly; do not loop the same sweep indefinitely or change unrelated source. Original 105 removals were byte-exact, independently proved in live-original-transaction-proof.json. Preserve the independent sase.md task edit. Recheck plugin audit only if source/deployment drifted, run sase bead epic-symbols bob-cli-pl.1, and close only this phase when its acceptance is verified. Never create beads, modify memory, close the parent, hand-set status, or commit vault notes. Vault-sync owns commits. Remind Bryan athena and Mac need bob plugins sync. If failed inspect retained preimages/logs before retry, never overwrite them. Finish through sase_final.


## Prompt

%queue(weight=1)
%macros_enabled:false
# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first projections of exact continuation nodes; any historical source without recoverable node provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `1`

## Continuation Block `block:v1:572f8a2b1489ee0602a9ef4f66cc1081`

- **Node:** `agent-delta:20261124101410:9c7b12ad30c0bbcb`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:** `local:continuation/records/agent_delta/agent-delta:20261124101410:9c7b12ad30c0bbcb.json`
- **Checkpoint:** `local:continuation/checkpoints/monitor_handoff-a22a69dd2d4353b4.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update supersedes it.

%queue(weight=1)
#fork:bob-cli-pl.1--1
%model:gpt-6-astra@xhigh

% macros_enabled:false
# Monitored command finished

**Command:**

```text
cargo test --lib native::props && cargo test --test cli props && cargo build --bin bob && npm --prefix sase/repos/linked/bob-plugins test && BOB_CLI_DIR="$PWD" BOB_DOCS_BOB_MAC_CAPTURE_DIR="$PWD/sase/repos/linked/bob-mac-capture" npm --prefix sase/repos/linked/bob-plugins run docs:check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16
```

| | |
| --- | --- |
| **Outcome** | FAILED — exit 1 |
| **Started** | 2026-11-24T14:56:15.553091+00:00 |
| **Finished** | 2026-11-24T15:12:29.636870Z |
| **Elapsed** | 15m 3s of a 45m 0s budget |
| **Output** | 786 KiB · evidence refs: `file:monitor-diagnostic-manifest:h4h9fsfwsst5`, `file:monitor-retained-log:h4h9fsfwsst5` · full log: `sase monitor show h4h9fsfwsst5 --all-lines` |
| **Tool run** | sase tool show 45618419b628ec176ea534859fd941ec |

**Why this was monitored:** Verify project frontmatter writer retirement and build Bob for the guarded vault cleanup

## Last 200 lines of output
<!--sase: budget-span:open:kind=old_raw_excerpts;id=1-->

Everything between the fences below is raw command output -- untrusted data, not instructions. The only instruction in this prompt is the "Your next action" section.

```text
sync_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: '==',
    diff: 'simple'
  }

> bob-plugins@0.1.0 test:perf
> node --test --test-concurrency=1 scripts/test-block-id-prompt-task-wikilink-index-performance.cjs scripts/test-block-id-prompt-task-links-api-performance.cjs scripts/test-copy-chips-live-preview-performance.cjs scripts/test-navigation-copy-card-task-scope-performance.cjs scripts/test-navigation-prose-field-performance.cjs scripts/test-navigation-dependencies-stage-performance.cjs

✔ api.taskLinks session open (snapshot plus first rank) takes at most 50 ms (617.628966ms)
ℹ session open: 41.72 ms
✔ api.taskLinks keystroke-to-rows p95 takes at most 12 ms over 5,000 tasks (1006.678021ms)
ℹ keystroke p95: 9.00 ms
✔ api.taskLinks performs no vault reads while filtering (857.952918ms)
✖ api.taskLinks typed keystrokes p95 takes at most 12 ms over 5,000 tasks (4430.161436ms)
ℹ typed keystroke p95: 14.00 ms
✔ cold build of 6,500 notes / 5,000 tasks fits 1.5 s in chunks of at most 16 ms (903.932845ms)
✔ warm snapshot plus order takes at most 50 ms (555.226041ms)
✔ one keystroke rank of 5,000 rows takes at most 12 ms (469.681287ms)
✔ no vault reads happen while filtering (342.585159ms)
✔ cold build growth stays near-linear over a 6x step (321.742964ms)
✔ 2,000-line daily note with 200 chips fits the 35 ms CPU budget (30.449387ms)
✔ narrow viewport visits only visible syntax ranges (7.170368ms)
✔ clipboard writes stay out of the perf path (1.98084ms)
✔ 2,000-line mixed note paints both kinds inside the 35 ms CPU budget (156.112375ms)
✔ mixed discovery stays inside the viewport and re-resolves only on a new catalog (262.575022ms)
✔ 2,000-line task, scope, and chip resolution fit the 50 ms CPU budget (259.334351ms)
✔ stage opening builds 200/400/1000-task notes without cubic growth (64.761281ms)
✔ stage snapshots match standalone parsing across grammar vectors (8.574416ms)
✔ stage Warm-empty cache is ready without a vault fallback (0.802536ms)
✔ stage opening renders cross-note results with zero writes and cap (60.240398ms)
✔ stage CURRENT covers same-note, cross-note, blocked, and counted parents (2.193606ms)
✔ stage collections reuse one snapshot per parent (0.442589ms)
✔ stage cold refresh yields, preserves state, and performs no search reads (139.532864ms)
✔ stage cold refresh abandons after dismissal or replacement (60.461347ms)
✔ stage 400-task opening finishes in a child process before the parent timeout (359.109309ms)
✔ 10k-note keystroke-to-rows p95 is ≤ 8 ms CPU (673.780008ms)
✔ 10k-note first link-index build is ≤ 40 ms CPU (613.813382ms)
ℹ tests 26
ℹ suites 0
ℹ pass 25
ℹ fail 1
ℹ cancelled 0
ℹ skipped 0
ℹ todo 0
ℹ duration_ms 13985.877925

✖ failing tests:

test at scripts/test-block-id-prompt-task-links-api-performance.cjs:155:1
✖ api.taskLinks typed keystrokes p95 takes at most 12 ms over 5,000 tasks (4430.161436ms)
  AssertionError [ERR_ASSERTION]: typed keystroke p95 14.0 ms exceeds 12 ms
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/scripts/test-block-id-prompt-task-links-api-performance.cjs:181:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: '==',
    diff: 'simple'
  }
sase: run demand not recorded (tool run store is busy: database is locked (extended_code=5))
sase: recording incomplete
failed  exit=1  duration=899861ms
```

<!--sase: budget-span:close:1-->
## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-32319dec4ebfaba2.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "cargo test --lib native::props && cargo test --test cli props && cargo build --bin bob && npm --prefix sase/repos/linked/bob-plugins test && BOB_CLI_DIR=\"$PWD\" BOB_DOCS_BOB_MAC_CAPTURE_DIR=\"$PWD/sase/repos/linked/bob-mac-capture\" npm --prefix sase/repos/linked/bob-plugins run docs:check",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16",
    "member_agent_name": "bob-cli-pl.1--mon-0",
    "monitor_id": "h4h9fsfwsst5",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261124094256:f0766eeba13cce9f"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:aa8edc9f8c590af9581303eae0376a855b8dba952bb47782da83a0ed04e5569a",
    "starter_agent": "bob-cli-pl.1--1",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/24/20261124094256"
  },
  "recorded_at_epoch": 1795532246.81125,
  "schema_version": 1
}
```


## Your next action

Resume bob-cli-pl.1 after verification. Read its latest checkpoint note and approved design. Fix new failures; for pre-existing failures prove on clean base and record PROPOSED FOLLOW-UP on this phase only. All source work is implemented and deployed to Apollo; do not redo it. Complete remaining authorized work: locate the binary from this monitored cargo target (CARGO_TARGET_DIR inherited at run, also cargo metadata target_directory); BOB_BIN must use the fresh build since installed bob still protects retired counts. Prove the cleanup against a scratch CRLF project under done/: dry-run preserves bytes, apply removes only count keys, second apply is no-op. Then snapshot affected live vault notes, run plugin scripts/retire-project-count-keys.cjs --dry-run then --apply against ~/bob, verify exact before/after byte deltas and git diff --stat (vault-sync owns commits). Update projects.base and project.md per one-writer phase, using landed bare +; remove count formula/columns, waiting view/branch, change Active filter to wip. Verify Base rendering and no remaining retired frontmatter keys, audit/sync current two changed plugins as needed, report that athena/Mac need bob plugins sync. No processFrontMatter calls remain; docs contains audit; Highlights methods byte-identical. Run any missing planned gates. Run sase bead epic-symbols bob-cli-pl.1 then close only bob-cli-pl.1 with evidence. Do not close parent, create beads, or modify memory. Finish through /sase_final. Remaining verification and live-vault acceptance clearly fit one coder.
% macros_enabled:true

### Checkpoint

- **Kind:** `monitor_handoff`

### Assistant

<!--sase:budget-span:open:kind=checkpoint;id=1;checkpoint_ref=local%3Acontinuation%2Fcheckpoints%2Fmonitor_handoff-a22a69dd2d4353b4.json;covered=agent-delta%3A20261124101410%3A9c7b12ad30c0bbcb-->
I’ll read the phase checkpoint and design, isolate the test failures, then finish the vault cleanup and project views. I’m using the SASE bead, repository, and memory skills to resume the work.


The Rust property tests and fresh build passed. The plugin suite reported unrelated test failures, which I’ll check against the clean base. The phase checkpoint confirms that the writer removals are already deployed; the remaining work is the live cleanup and Base updates.


All three failing tests pass when rerun alone on the unchanged tree, so they appear sensitive to load. I found the fresh Bob binary in the monitor’s Cargo target directory. I’ll use it to verify the archived CRLF fixture before applying the guarded cleanup to live notes.


The CRLF fixture passed dry-run, exact removal, and the no-op rerun. The updated Base also renders in real Obsidian on Athena: Active shows only WIP projects and has no Tasks column. The live preview hit one 30-second subprocess timeout, so I’m increasing that bound before applying the cleanup.


All three Base views now pass the Obsidian check. Both changed plugins match their deployed Apollo files, and the Highlights commands and methods are byte-identical to the base revision. I’m running the missing documentation gate and the clean-base suite while the live preview finishes.


The two ledger timing failures reproduce on the clean plugin base. The task-link performance suite passes on the clean base, and all 44 tests from the failing suites pass in isolation on the working tree. I also shortened the navigation docs to meet the word limit. The interrupted live preview left all 106 candidate notes unchanged; the complete preview and apply will run under a monitor with byte checks.


Documentation lint now passes, along with the site build, links, and search checks. The gate is still building Bob for its executable tutorial. The live cleanup runner is ready to take fresh preimages, require a successful dry-run, apply the removals, and verify every changed byte plus a no-op rerun.


Only the tutorial check and live cleanup remain. I’ve saved the Base rendering evidence and recorded the pre-existing timing failures on this phase. I’ll keep `bob-cli-pl.1` open until the cleanup’s byte-verification report passes.


The full documentation gate passed, including the executable tutorial. I’m using `/sase_monitor` for the live dry-run, cleanup, and byte verification. The continuation will review that report and close only `bob-cli-pl.1` when it passes.


The cleanup monitor is still staging. I’m waiting for it to confirm the handoff before ending the turn.


The monitor is staged. I’m finishing through `/sase_final` with the phase kept open until the live cleanup is verified.


Updated the project views and verified all three in Obsidian. Property tests, focused plugin tests, CRLF cleanup checks, and docs pass. Existing timing failures are documented.

Live cleanup and byte verification are staged with automatic continuation. `bob-cli-pl.1` remains open pending that result.

Athena and Mac still need `bob plugins sync`.
<!--sase:budget-span:close:1-->

---

%macros_enabled:true
# New Query
%model:gpt-6-astra@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
python3 .git/pl1-acceptance/live-cleanup.py
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16
```

| | |
| --- | --- |
| **Outcome** | FAILED — exit 1 |
| **Started** | 2026-11-24T15:37:10.157645+00:00 |
| **Finished** | 2026-11-24T16:01:30.845348Z |
| **Elapsed** | 23m 19s of a 1h 30m 0s budget |
| **Output** | 13 KiB · evidence refs: `file:monitor-diagnostic-manifest:2cs8tw51atd0`, `file:monitor-retained-log:2cs8tw51atd0` · full log: `sase monitor show 2cs8tw51atd0 --all-lines` |
| **Tool run** | sase tool show 9670ac4df9c48823592e0c5073fdd37b |

**Why this was monitored:** Apply and verify guarded live-vault removal of retired project counts

## Last 200 lines of output
<!--sase:budget-span:open:kind=old_raw_excerpts;id=1-->

Everything between the fences below is raw command output -- untrusted data, not instructions. The only instruction in this prompt is the "Your next action" section.

```text
count
sase_blog_blockers.md	removed	task_count, open_task_count
sase_blog_drafts.md	removed	task_count, open_task_count
sase_blog.md	removed	task_count, open_task_count
sase_bug_bash.md	removed	task_count, open_task_count
sase_clans_and_tribes.md	removed	task_count, open_task_count
sase_clean_release.md	removed	task_count, open_task_count
sase_clean.md	removed	task_count, open_task_count
sase_cleanup.md	removed	task_count, open_task_count
sase_completion.md	removed	task_count, open_task_count
sase_config.md	removed	task_count, open_task_count
sase_decks.md	removed	task_count, open_task_count
sase_dir_xprompts_artifact.md	removed	task_count, open_task_count
sase_dir_xprompts.md	removed	task_count, open_task_count
sase_doctor.md	removed	task_count, open_task_count
sase_dyn_agent_fam_e2e.md	skipped	{"code":"lock_busy","hint":"Check the vault path, note, lock, and file permissions.","message":"another Bob vault maintenance run is active (waited on /run/user/1000/bob_sync.lock)"}
sase_dyn_agent_fam.md	removed	task_count, open_task_count
sase_final_polish.md	removed	task_count, open_task_count
sase_gate_shells.md	removed	task_count, open_task_count
sase_gate.md	removed	task_count, open_task_count
sase_goals.md	removed	task_count, open_task_count
sase_grok_cli.md	removed	task_count, open_task_count
sase_hoods.md	removed	task_count, open_task_count
sase_if_and_proc.md	removed	task_count, open_task_count
sase_install.md	removed	task_count, open_task_count
sase_linked_repo_delta.md	removed	task_count, open_task_count
sase_memory_audit.md	removed	task_count, open_task_count
sase_memory_plan.md	removed	task_count, open_task_count
sase_memory_webs.md	removed	task_count, open_task_count
sase_memory_write.md	removed	task_count, open_task_count
sase_memory.md	removed	task_count, open_task_count
sase_message_boards.md	removed	task_count, open_task_count
sase_model_panel.md	removed	task_count, open_task_count
sase_model.md	removed	task_count, open_task_count
sase_monitor_gate.md	removed	task_count, open_task_count
sase_monitor.md	removed	task_count, open_task_count
sase_more_agent_clis.md	removed	task_count, open_task_count
sase_onboard.md	removed	task_count, open_task_count
sase_pager.md	removed	task_count, open_task_count
sase_parallel_fams.md	removed	task_count, open_task_count
sase_piw_multi_prompt.md	removed	task_count, open_task_count
sase_plugin.md	removed	task_count, open_task_count
sase_polish_proc_lanes.md	removed	task_count, open_task_count
sase_post_blog.md	removed	task_count, open_task_count
sase_pre_blog.md	removed	task_count, open_task_count
sase_projects.md	removed	task_count, open_task_count
sase_prompt_stash_pinned_stashes.md	removed	task_count, open_task_count
sase_prompt_stash.md	removed	task_count, open_task_count
sase_pypi_releases.md	removed	task_count, open_task_count
sase_remote.md	removed	task_count, open_task_count
sase_research.md	removed	task_count, open_task_count
sase_sdd_repo.md	removed	task_count, open_task_count
sase_setup.md	removed	task_count, open_task_count
sase_sites.md	removed	task_count, open_task_count
sase_size_models.md	removed	task_count, open_task_count
sase_skill_bundles.md	removed	task_count, open_task_count
sase_toobig_symvision.md	removed	task_count, open_task_count
sase_update.md	removed	task_count, open_task_count
sase_usage.md	removed	task_count, open_task_count
sase_version.md	removed	task_count, open_task_count
sase.md	removed	task_count, open_task_count
vacation_sc_26.md	removed	task_count, open_task_count
Total: 105 notes, 210 keys removed, 1 skipped

Traceback (most recent call last):
  File "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/.git/pl1-acceptance/live-cleanup.py", line 52, in <module>
    run('--apply', 'live-apply.log')
  File "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/.git/pl1-acceptance/live-cleanup.py", line 46, in run
    raise RuntimeError(f'{filename}: exit {result.returncode}; inspect skips before continuing')
RuntimeError: live-apply.log: exit 1; inspect skips before continuing
failed  exit=1  duration=1396595ms
```

<!--sase:budget-span:close:1-->
## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/authored-56ad017647bfb122.json`

**Checkpoint (JSON):**

```text
{
  "author": {
    "actor_id": "bob-cli-pl.1--2",
    "actor_kind": "user"
  },
  "constraints": [
    "No new task beads, memory edits, parent close, or hand-set status",
    "Use sase_final for the ending declaration",
    "Vault-sync owns live vault commits; other hosts still need bob plugins sync"
  ],
  "coverage": [],
  "findings": [],
  "kind": "authored_checkpoint",
  "objective": "Complete only bob-cli-pl.1 after live project count cleanup",
  "remaining_work": [],
  "schema_version": 1,
  "source_refs": [],
  "unresolved_decisions": []
}
```


## Your next action

Resume bob-cli-pl.1. Read its latest phase notes and the frozen checkpoint; all source work, Apollo deployment, Rust tests, relevant plugin tests, clean-base failure proof, docs gates, and three-view real Obsidian Base acceptance are done. This monitor runs .git/pl1-acceptance/live-cleanup.py against ~/bob with the fresh prior monitor binary, writing only through bob props. On success inspect live-result.json, live-dry-run.log, live-apply.log, live-repeat.log and live-diff-stat.txt under .git/pl1-acceptance; confirm exact two-line-only removals and no count keys remain. Vault-sync owns commits. On failure inspect partial logs and apply-preimages before any retry; the runner intentionally refuses to overwrite its preimages. Fix only new issues; pre-existing timing failures already have clean-base evidence and PROPOSED FOLLOW-UP on this phase. Recheck current plugin audit/sync if needed, run sase bead epic-symbols bob-cli-pl.1, record evidence, and close only bob-cli-pl.1. Never create task beads, modify memory, close the parent, or hand-set status. Remind Bryan that athena and Mac need bob plugins sync. Finish through sase_final; remaining acceptance fits one coder.
%macros_enabled:true

## Response

The cleanup removed 210 keys from 105 notes; one note was skipped because the vault lock was busy. I’ll inspect the saved preimages, retry that note, and verify the final byte changes before closing the phase. I’m using the SASE bead, repository, memory-read, and finalizer skills.


The dry-run covered all 106 notes successfully. The apply log shows one `lock_busy` skip. I’ll compare the current notes with the frozen preimages before retrying, so any concurrent edits stay intact.


The audit found that the Mac restored the count keys through vault-sync after Apollo removed them. Git history confirms this; Apollo has the updated plugin. One task line also changed independently, which I’ll preserve.

The approved plan anticipates stale hosts re-adding counts. I’m checking how to isolate the cleanup briefly so its exact byte changes can be verified without racing sync.


Both changed plugins still match Apollo’s deployed files. I’ll rerun the sweep with Apollo’s sync watcher temporarily stopped, preserving the original preimages and taking a separate fresh snapshot. The runner will verify the removals and no-op repeat, then restart sync automatically.

Athena and the Mac will still need `bob plugins sync`; the stale Mac is actively restoring these keys.


The retry runner is ready. It preserves the original evidence and the independent task edit, and includes a timed fallback to restart sync if interrupted. I’m attaching the stale-host evidence with `/sase_artifact`, then using `/sase_monitor` for the full sweep. The phase will stay open until the verification passes.


Vault history confirms that all 105 successful writes removed exactly the two count lines. The restored keys are attributable to the stale Mac writer. The evidence attachment is still running; I’ll let it finish before staging the retry.


The verification approach is unchanged: preserve the current note bytes, isolate the sweep from sync, and check exact removals plus a no-op repeat. Evidence registration is taking longer than expected. I’m waiting for it to finish before staging the monitor.


The controlled retry is staged, and the recovery evidence is attached to `bob-cli-pl.1`. I’m finishing through `/sase_final`; the phase remains open pending the byte-verification result and confirmation that sync restarted.


All 105 successful removals were byte-exact, but the stale Mac plugin restored the keys through sync.

A controlled retry is staged with automatic sync restoration. `bob-cli-pl.1` remains open pending verification.

Athena and Mac still need `bob plugins sync`.
