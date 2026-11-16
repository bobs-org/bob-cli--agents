# Chat History - ace-run (bob-cli-ly.4--1)

- **TIMESTAMP:** 2026-11-16 06:16:15 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** bob-cli-ly.4--1

# Monitor handoff

This agent delegated the remaining work to a monitor turn.
Monitor ID: m59y80ee7mcg
Inspect with: sase monitor show m59y80ee7mcg
Monitor turn: bob-cli-ly.4--mon-0
Directory: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-mac-capture

Command:

```sh
python3 - <<'PY_VERIFY'
import shlex
import subprocess

def run(argv, **kwargs):
    print('+ ' + shlex.join(argv), flush=True)
    return subprocess.run(argv, check=True, text=True, **kwargs)

run(['just', 'portable-check'])
ssh = ['ssh', '-o', 'BatchMode=yes', '-o', 'ConnectTimeout=8', 'mac']
probe = subprocess.run(ssh + ['mktemp -d /tmp/bob-note-goto-verify.XXXXXX'], capture_output=True, text=True)
if probe.returncode:
    print('SCRATCH MAC UNAVAILABLE: ' + probe.stderr.strip(), flush=True)
else:
    scratch = probe.stdout.strip()
    if not scratch.startswith('/tmp/bob-note-goto-verify.') or len(scratch.splitlines()) != 1:
        raise RuntimeError('Unexpected scratch directory')
    try:
        run(['rsync', '-az', '--exclude=.git', '--exclude=.build', '--exclude=.sase',
             '-e', 'ssh -o BatchMode=yes -o ConnectTimeout=8', './', 'mac:' + scratch + '/'])
        run(ssh + ['cd ' + shlex.quote(scratch) + ' && Scripts/bundle.sh --identity - && just typecheck-tests'])
    finally:
        run(ssh + ['rm -rf -- ' + shlex.quote(scratch)])
run(['Scripts/macos-ci-check'])
print('PREFLIGHT PASSED. Read current tree status; commit dirty tests through sase_final before exact-HEAD CI.', flush=True)
run(['git', 'status', '--short'])
run(['git', 'rev-parse', 'HEAD'])
PY_VERIFY
```

Reason:

Compile deterministic alias-tip setup and verify Notes picker completion

Next action:

Finish bob-cli-ly.4. All phase production work is landed through f24475e5; the carried tree fixes four separator-test fixed sleeps and the unrelated alias-tip session test ordering. Read phase note 13 and this monitor result. On green preflight, DO NOT rerun preflight and DO NOT watch the old f24475e5 SHA while the tree is dirty. Stage a PURE exact-HEAD master/push CI watcher resolving HEAD only after host finalization; explicitly submit sase_final with commit decision for linked bob-mac-capture, message test(capture): synchronize separator replies and alias tip setup, bead_action keep. A handoff alone may carry the dirty tree, so explicit commit declaration is essential at that step. On verified exact-HEAD success, record run URL/SHA, check epic-symbols, and close only bob-cli-ly.4. If preflight fails, diagnose; failures reproduced identically on clean base are PROPOSED FOLLOW-UP notes and do not keep this phase open. Never close parent bob-cli-ly, create beads, or edit memory. Live Mac .base opening and docs-cap/clean-base DotRouteAlias evidence are already on the bead. Current changes were not yet Mac-compiled when this monitor was staged; they must remain carried until verification finishes.


## Prompt

%queue(weight=1)
%macros_enabled:false
# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first projections of exact continuation nodes; any historical source without recoverable node provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `1`

## Continuation Block `block:v1:f0627f4c2f17a9184677f31e4159880f`

- **Node:** `agent-delta:20261116052813:d8d38f0d18f2324c`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:** `local:continuation/records/agent_delta/agent-delta:20261116052813:d8d38f0d18f2324c.json`
- **Checkpoint:** `local:continuation/checkpoints/monitor_handoff-c9a16fe1c5e5dce5.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update supersedes it.

%id(4, clan=bob-cli-ly, bead=bob-cli-ly.4)
%auto
#gh:gh_bobs-org__bob-cli
%m:gpt-6-astra 
%w(bob-cli-ly.2,bob-cli-ly.3, for_epic=false)
%w(bead=bob-cli-ly.2)
%w(bead=bob-cli-ly.3)
Can you complete the work for bead bob-cli-ly.4? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-ly.4` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-ly.4` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-ly.4 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-ly.4 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-ly.4 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-ly.4`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-ly.4 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

### Checkpoint

- **Kind:** `monitor_handoff`

### Assistant

<!--sase:budget-span:open:kind=checkpoint;id=1;checkpoint_ref=local%3Acontinuation%2Fcheckpoints%2Fmonitor_handoff-c9a16fe1c5e5dce5.json;covered=agent-delta%3A20261116052813%3Ad8d38f0d18f2324c-->
I’ll read the bead’s scope, decisions, and prior notes, then check what has already landed before implementing the remaining work. I’m using the SASE memory and finalization skills for this run.


The phase notes show the implementation is already complete. The remaining issue is macOS CI: previous runs passed the Notes picker tests but failed intermittently in existing separator tests. I’m opening the linked Mac repository to verify the landed code and inspect those failures.


The latest failures come from tests that assume a subprocess finishes within 200 ms. I’ll replace those sleeps with bounded waits for the rewrite to finish, preserving the assertions. That is a small enough remainder to handle here. The GitHub connector only lists pull-request runs, so I’m using `gh` to inspect this master-branch CI run.


Four affected tests now wait for rewrite completion and deliberately delay the fake reply beyond the old 200 ms limit. The Mac is reachable, so I’m also checking the required `.base` opening behavior and arranging a scratch compile before macOS CI.


The Mac check passed: an existing `.base` opened through `bob-open-notes` as a Bases view, its contents stayed unchanged, and I restored the previous active tab. I’m staging scratch compilation and CI verification through SASE. The verifier will only watch a committed SHA, avoiding the earlier loop that kept checking the old commit.


The implementation was already landed. I fixed four timing-sensitive tests and verified `.base` navigation on the Mac.

Verification is staged in SASE monitor `ggvpm8`, with automatic continuation through commit, exact-SHA CI, and closure. `bob-cli-ly.4` remains open pending verification.
<!--sase:budget-span:close:1-->

---

%macros_enabled:true
# New Query
%model:gpt-6-astra@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
python3 - <<'PY_VERIFY'
import json
import pathlib
import shlex
import subprocess
import time

def run(argv, **kwargs):
    print("+ " + shlex.join(argv), flush=True)
    return subprocess.run(argv, check=True, text=True, **kwargs)

run(["just", "portable-check"])
ssh = ["ssh", "-o", "BatchMode=yes", "-o", "ConnectTimeout=8", "mac"]
probe = subprocess.run(ssh + ["mktemp -d /tmp/bob-note-goto-verify.XXXXXX"], capture_output=True, text=True)
if probe.returncode:
    print("SCRATCH MAC UNAVAILABLE: " + probe.stderr.strip(), flush=True)
else:
    scratch = probe.stdout.strip()
    if not scratch.startswith("/tmp/bob-note-goto-verify.") or len(scratch.splitlines()) != 1:
        raise RuntimeError("Unexpected scratch directory")
    try:
        run(["rsync", "-az", "--exclude=.git", "--exclude=.build", "--exclude=.sase",
             "-e", "ssh -o BatchMode=yes -o ConnectTimeout=8", "./", "mac:" + scratch + "/"])
        run(ssh + ["cd " + shlex.quote(scratch) + " && Scripts/bundle.sh --identity - && just typecheck-tests"])
    finally:
        run(ssh + ["rm -rf -- " + shlex.quote(scratch)])

run(["Scripts/macos-ci-check"])
dirty = run(["git", "status", "--porcelain"], capture_output=True).stdout.strip()
if dirty:
    print("PREFLIGHT PASSED; COMMIT REQUIRED BEFORE EXACT-SHA WATCH. The checked working tree is still dirty.", flush=True)
    print(dirty, flush=True)
else:
    sha = run(["git", "rev-parse", "HEAD"], capture_output=True).stdout.strip()
    deadline = time.monotonic() + 300
    workflow_run = None
    while time.monotonic() < deadline:
        runs = json.loads(run(["gh", "run", "list", "-R", "bobs-org/bob-mac-capture",
            "--workflow", "CI", "--commit", sha, "--limit", "100",
            "--json", "databaseId,headSha,headBranch,event,status,conclusion,url"],
            capture_output=True).stdout)
        workflow_run = next((r for r in runs if r["headSha"] == sha and r["headBranch"] == "master" and r["event"] == "push"), None)
        if workflow_run:
            break
        time.sleep(10)
    if workflow_run is None:
        raise RuntimeError("No master CI run found for exact committed SHA " + sha)
    print("EXACT-SHA RUN " + json.dumps(workflow_run), flush=True)
    run(["gh", "run", "watch", str(workflow_run["databaseId"]), "-R",
         "bobs-org/bob-mac-capture", "--exit-status", "--interval", "20"])
    current_sha = run(["git", "rev-parse", "HEAD"], capture_output=True).stdout.strip()
    if current_sha != sha:
        raise RuntimeError("HEAD changed while watching CI")
    print("VERIFIED EXACT SHA " + sha + " " + workflow_run["url"], flush=True)

PY_VERIFY
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | FAILED — exit 1 |
| **Started** | 2026-11-16T10:38:53.245275+00:00 |
| **Finished** | 2026-11-16T11:07:41.129525Z |
| **Elapsed** | 28m 11s of a 1h 40m 0s budget |
| **Output** | 2,446 KiB · evidence refs: `file:monitor-diagnostic-manifest:ggvpm81v09dc`, `file:monitor-retained-log:ggvpm81v09dc` · full log: `sase monitor show ggvpm81v09dc --all-lines` |
| **Tool run** | sase tool show 281a8948c1970c8bbf1aac279a157c0c |

**Why this was monitored:** Compile delayed separator regression cases and finish Notes picker macOS verification

## Last 200 lines of output
<!--sase:budget-span:open:kind=old_raw_excerpts;id=1-->

Everything between the fences below is raw command output -- untrusted data, not instructions. The only instruction in this prompt is the "Your next action" section.

```text
43852193445 is in_progress (712s elapsed, 4686s left)
macos-ci-check: run 43852193445 is in_progress (722s elapsed, 4676s left)
macos-ci-check: run 43852193445 is in_progress (733s elapsed, 4665s left)
macos-ci-check: run 43852193445 is in_progress (744s elapsed, 4654s left)
macos-ci-check: run 43852193445 is in_progress (755s elapsed, 4644s left)
macos-ci-check: run 43852193445 is in_progress (765s elapsed, 4633s left)
macos-ci-check: run 43852193445 is in_progress (776s elapsed, 4622s left)
macos-ci-check: run 43852193445 is in_progress (787s elapsed, 4611s left)
macos-ci-check: run 43852193445 is in_progress (797s elapsed, 4601s left)
macos-ci-check: run 43852193445 is in_progress (808s elapsed, 4590s left)
macos-ci-check: run 43852193445 is in_progress (819s elapsed, 4579s left)
macos-ci-check: run 43852193445 is in_progress (830s elapsed, 4568s left)
macos-ci-check: run 43852193445 is in_progress (840s elapsed, 4558s left)
macos-ci-check: run 43852193445 is in_progress (851s elapsed, 4547s left)
macos-ci-check: run 43852193445 is in_progress (862s elapsed, 4536s left)
macos-ci-check: run 43852193445 is in_progress (873s elapsed, 4525s left)
macos-ci-check: run 43852193445 is in_progress (883s elapsed, 4515s left)
macos-ci-check: run 43852193445 is in_progress (894s elapsed, 4504s left)
macos-ci-check: run 43852193445 is in_progress (905s elapsed, 4493s left)
macos-ci-check: run 43852193445 is in_progress (916s elapsed, 4482s left)
macos-ci-check: run 43852193445 is in_progress (926s elapsed, 4472s left)
macos-ci-check: run 43852193445 is in_progress (937s elapsed, 4461s left)
macos-ci-check: run 43852193445 is in_progress (948s elapsed, 4450s left)
macos-ci-check: run 43852193445 is in_progress (959s elapsed, 4439s left)
macos-ci-check: run 43852193445 is in_progress (969s elapsed, 4429s left)
macos-ci-check: run 43852193445 is in_progress (980s elapsed, 4418s left)
macos-ci-check: run 43852193445 is in_progress (991s elapsed, 4407s left)
macos-ci-check: run 43852193445 is in_progress (1002s elapsed, 4396s left)
macos-ci-check: run 43852193445 is in_progress (1012s elapsed, 4386s left)
macos-ci-check: run 43852193445 is in_progress (1023s elapsed, 4375s left)
macos-ci-check: run 43852193445 is in_progress (1034s elapsed, 4364s left)
macos-ci-check: run 43852193445 is in_progress (1044s elapsed, 4354s left)
macos-ci-check: run 43852193445 is in_progress (1055s elapsed, 4343s left)
macos-ci-check: run 43852193445 is in_progress (1066s elapsed, 4332s left)
macos-ci-check: run 43852193445 is in_progress (1077s elapsed, 4321s left)
macos-ci-check: run 43852193445 is in_progress (1087s elapsed, 4311s left)
macos-ci-check: run 43852193445 is in_progress (1098s elapsed, 4300s left)
macos-ci-check: run 43852193445 is in_progress (1109s elapsed, 4289s left)
macos-ci-check: run https://github.com/bobs-org/bob-mac-capture/actions/runs/43852193445
macos-ci-check: snapshot SHA f5f21a13c6662bc05c18d54a51f8e954e71ef7b6
macos-ci-check: macOS job macOS 26 SwiftPM
  [ok] Set up job
  [ok] Check out repository
  [ok] Check scripts
  [ok] Show toolchain
  [ok] Lint Swift formatting
  [ok] Build
  [failure] Test
  [ok] Upload render fixtures
  [ok] Upload test hang samples
  [skipped] Bundle
  [skipped] Verify plist and signature
  [skipped] Launch smoke test
  [skipped] Upload launch smoke test diagnostics
  [skipped] Install and reinstall
  [ok] Post Check out repository
  [ok] Complete job
macos-ci-check: required macOS steps failed: Test (failure)
macos-ci-check: failed Swift tests
  BobMacCaptureTests.CaptureAliasTipPanelTests testListThenPickerSequenceShowsAtMostOneTip
macos-ci-check: deleted remote branch ci/precommit/016c2a4501fea68f61fa03ffef621940
Traceback (most recent call last):
  File "<stdin>", line 27, in <module>
  File "<stdin>", line 9, in run
  File "/home/bryan/.pyenv/versions/3.11.13/lib/python3.11/subprocess.py", line 571, in run
    raise CalledProcessError(retcode, process.args,
subprocess.CalledProcessError: Command '['Scripts/macos-ci-check']' returned non-zero exit status 1.
failed  exit=1  duration=1690772ms
```

<!--sase:budget-span:close:1-->
## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-0daf396a8470e603.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "python3 - <<'PY_VERIFY'\nimport json\nimport pathlib\nimport shlex\nimport subprocess\nimport time\n\ndef run(argv, **kwargs):\n    print(\"+ \" + shlex.join(argv), flush=True)\n    return subprocess.run(argv, check=True, text=True, **kwargs)\n\nrun([\"just\", \"portable-check\"])\nssh = [\"ssh\", \"-o\", \"BatchMode=yes\", \"-o\", \"ConnectTimeout=8\", \"mac\"]\nprobe = subprocess.run(ssh + [\"mktemp -d /tmp/bob-note-goto-verify.XXXXXX\"], capture_output=True, text=True)\nif probe.returncode:\n    print(\"SCRATCH MAC UNAVAILABLE: \" + probe.stderr.strip(), flush=True)\nelse:\n    scratch = probe.stdout.strip()\n    if not scratch.startswith(\"/tmp/bob-note-goto-verify.\") or len(scratch.splitlines()) != 1:\n        raise RuntimeError(\"Unexpected scratch directory\")\n    try:\n        run([\"rsync\", \"-az\", \"--exclude=.git\", \"--exclude=.build\", \"--exclude=.sase\",\n             \"-e\", \"ssh -o BatchMode=yes -o ConnectTimeout=8\", \"./\", \"mac:\" + scratch + \"/\"])\n        run(ssh + [\"cd \" + shlex.quote(scratch) + \" && Scripts/bundle.sh --identity - && just typecheck-tests\"])\n    finally:\n        run(ssh + [\"rm -rf -- \" + shlex.quote(scratch)])\n\nrun([\"Scripts/macos-ci-check\"])\ndirty = run([\"git\", \"status\", \"--porcelain\"], capture_output=True).stdout.strip()\nif dirty:\n    print(\"PREFLIGHT PASSED; COMMIT REQUIRED BEFORE EXACT-SHA WATCH. The checked working tree is still dirty.\", flush=True)\n    print(dirty, flush=True)\nelse:\n    sha = run([\"git\", \"rev-parse\", \"HEAD\"], capture_output=True).stdout.strip()\n    deadline = time.monotonic() + 300\n    workflow_run = None\n    while time.monotonic() < deadline:\n        runs = json.loads(run([\"gh\", \"run\", \"list\", \"-R\", \"bobs-org/bob-mac-capture\",\n            \"--workflow\", \"CI\", \"--commit\", sha, \"--limit\", \"100\",\n            \"--json\", \"databaseId,headSha,headBranch,event,status,conclusion,url\"],\n            capture_output=True).stdout)\n        workflow_run = next((r for r in runs if r[\"headSha\"] == sha and r[\"headBranch\"] == \"master\" and r[\"event\"] == \"push\"), None)\n        if workflow_run:\n            break\n        time.sleep(10)\n    if workflow_run is None:\n        raise RuntimeError(\"No master CI run found for exact committed SHA \" + sha)\n    print(\"EXACT-SHA RUN \" + json.dumps(workflow_run), flush=True)\n    run([\"gh\", \"run\", \"watch\", str(workflow_run[\"databaseId\"]), \"-R\",\n         \"bobs-org/bob-mac-capture\", \"--exit-status\", \"--interval\", \"20\"])\n    current_sha = run([\"git\", \"rev-parse\", \"HEAD\"], capture_output=True).stdout.strip()\n    if current_sha != sha:\n        raise RuntimeError(\"HEAD changed while watching CI\")\n    print(\"VERIFIED EXACT SHA \" + sha + \" \" + workflow_run[\"url\"], flush=True)\n\nPY_VERIFY",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-ly.4--mon",
    "monitor_id": "ggvpm81v09dc",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261116052813:d8d38f0d18f2324c"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:e138f29a8d8cd07a63e460c7146b33d5bfb1f999dabed96cb49ce51e3f3e1846",
    "starter_agent": "bob-cli-ly.4--plan",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/16/20261116052813"
  },
  "recorded_at_epoch": 1794825569.3372085,
  "schema_version": 1
}
```


## Your next action

Finish bob-cli-ly.4 after this verification. All phase implementation is already landed through f24475e5; this turn changes only four CaptureSeparatorToggleTests fixed waits into bounded rewrite completion waits, with 300 ms fake replies. Mac .base URI acceptance was confirmed live and recorded on the bead. Read the monitor result. If the checked working tree remains dirty after a green preflight, use sase_final with a commit decision for the linked bob-mac-capture repository (test(capture): await unchanged separator rewrite replies), bead_action keep, and stage a pure exact-HEAD CI watcher that resolves HEAD only after host finalization. Do NOT rerun preflight or watch the old f24475e5 SHA when the corrected tree is still dirty. If this monitor already reports VERIFIED EXACT SHA, record its run URL/SHA, check epic-symbols, and close only bob-cli-ly.4. On a new failure, diagnose and fix it; unchanged clean-base failures do not keep this phase open per the user's instruction, record PROPOSED FOLLOW-UP evidence and close once scope is verified. Do not close bob-cli-ly or edit memory. Existing docs cap failure and clean-base DotRouteAlias flake are recorded in phase notes.
%macros_enabled:true

## Response

The verification failed in a different test, `CaptureAliasTipPanelTests`. I’ll inspect the failure and bead notes, then determine whether it needs a fix or is an unrelated failure covered by your closure instructions. I’m using the SASE memory, repository, and finalization skills.


All Notes picker tests and the four corrected separator tests passed. The remaining failure is in an alias-tip test; I’m checking its request sequence to find out why the expected tip never appeared.


The test assumes the tip reply arrives before a 200 ms completion debounce. If the list opens first, the app correctly drops the late tip, and the test’s setup fails. I’ll make that ordering explicit while preserving its assertion that a session shows at most one tip.


The alias-tip test now delivers the first reply before opening the list, then checks that the second tip is rejected by the session limit. The previous run passed 2,512 portable tests, scratch Mac compilation, and all Notes picker tests. I’ll use SASE monitoring to compile this additional test change and rerun macOS CI.


The failure and fix are recorded on `bob-cli-ly.4`, which has no remaining epic-symbol entries. The verification handoff is still being staged; it will check the edited tree before committing, then continue to exact-SHA CI and bead closure.


Notes picker and separator tests passed; I fixed the new alias-tip test race.

Mac compilation and CI verification are staged in monitor `m59y80`, with automatic continuation through commit and exact-SHA verification. `bob-cli-ly.4` remains open pending those checks.
