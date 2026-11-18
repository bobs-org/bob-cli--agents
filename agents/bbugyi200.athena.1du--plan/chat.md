# Chat History - ace-run (1du--plan)

- **TIMESTAMP:** 2026-11-18 07:33:47 EST
- **MODEL:** claude/opus
- **AGENT:** 1du--plan

**Plan:** /home/bryan/.sase/plans/202611/sdd_clone_recovery_spares_live_work.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/sdd_clone_recovery_spares_live_work.md`

> # Plan: Stop SDD clone self-heal from stashing live agent work
> ## Where this lands
> All code changes land in the **`sase` project** (`sase-org/sase`). The restore in step 4
> also edits that project's `plans` sidecar. If this coder is not running in a `sase`
> workspace, open the repo with `sase repo open sase` and do all edits, checks, and
> commits in the path it prints. Read `sase/memory/lint_and_test.md` there before
> finishing. That checkout's `AGENTS.md` lists the memory notes to read first, including
> `ace.md` if you touch anything under `src/sase/ace/`.
> ## What happened (evidence)
> `sase-1tb.land--2` (the monitor follow-up that closed epic `sase-1tb`) ended FAILED in

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli The `sase-1tb.land` sase agent just failed. Is there something that we can/should fix here? If so, use your /sase_plan skill to plan the appropriate changes. Think hard about this. %m:@xlarge

## Response

Looking through the `sase-1tb.land` transcripts to find where it failed. It belongs to the `sase` project, not bob-cli.

Found the land agent's chain. The final check went green. Now working out why the agent still ended as failed.

The member artifact dirs were cleaned up when the agent was dismissed. Checking the session root's workflow log and finalizer records for the failure reason.

The failing member is `sase-1tb.land--2`, the follow-up after the green check. Reading its run log.

Reading the finalizer's "dirty work vanished" check in the sase source to see why it fired on the plans sidecar.

Confirmed `pull_sdd_clone` escalates to a destructive stash-and-reset whenever the clone has local tracked edits. Checking the git-operation telemetry log for the exact caller that fired at 01:57:32.

Narrowing down which process ran that cross-workspace sweep.

Identifying the periodic caller. The likely chain is `get_workspace_directory` → `ensure_workspace_checkout` → `ensure_workspace_sdd_clone` → `pull_sdd_clone`.

The `sidecar_sync` lumberjack (axe `sidecar_auto_sync`, 27 targets) is the likely sweeper. Checking its log around 01:57.

The sweep is still running every couple of minutes, so I'll catch it live with `ps` to get the exact parent process.

I'll grab a live Python stack of the cleanup chop with `py-spy` (read-only) to get the exact call path into `pull_sdd_clone`.

I have the full causal chain. Loading the plan skill to write it up.

Drafting the plan now. I'm confirming one routing detail first: the coder must land in the `sase` project, but this session is a bob-cli agent.

No memory note or doc describes the dirty-clone stash behavior, so no memory correction is needed. Checking the finalizer test location, then writing the plan.

The references in the plan check out. Running a final validation without `--explain`, then submitting.

Staged. Finishing through `/sase_final`.

Yes, this needs a fix, and it's a bug in sase rather than anything the agent did wrong. I've staged a plan for it.

**What failed.** `sase-1tb.land--2` was the last turn of the land session, the one that closed epic `sase-1tb`. The green check, the epic close, the main fix commit `c5f4964` and the beads commit all landed. The run was then marked FAILED by the commit finalizer: "dirty work vanished without an attributable commit" for the `plans` sidecar. The only thing actually lost is a one-line plan change: `202611/fast_video_artifact_pane.md` going from `status: wip` to `status: done`.

**Root cause.** The finalizer's guard was right; the edit really was destroyed while the finalizer was still running. I caught the responsible process live with `py-spy`:

- **Trigger:** the axe `hooks` routine runs a `stale_running_cleanup` job about every 2 minutes. One of its steps repairs leaked monitor claims.
- **Why it reached sase_30:** a monitor's follow-up agent reuses the monitor's workspace. So the dead monitor's held claim and the live `land--2` agent were both on sase_30, and the repair inspected a workspace someone was actively using.
- **How a lookup became destructive:** to find the workspace's directory, the repair calls a lookup that also syncs the workspace's plans clone. That sync saw uncommitted edits, treated the clone as stuck, stashed the edit and ran `git reset --hard origin/main`. There was nothing new upstream to pull, so the reset only threw work away.
- **Wider exposure:** the same sweep also syncs your primary checkout's plans clone, so your own uncommitted plan edits there are at risk too. The sweep is still running.

The lost edit is still recoverable from sase_30's plans clone, in `stash@{0}` and `refs/sase/recovery/20261118T065732Z-main-ae5be8e005`.

**Plan staged** (single-agent, medium; nothing starts until you approve it):
1. A clone whose only problem is uncommitted edits is left alone, never stashed or reset. Only genuinely stuck states (for example a half-finished rebase) still self-heal. Fresh workspaces don't need the old behaviour, because launch already wipes and re-clones the sidecars.
2. The leaked-monitor repair skips any workspace that has a live agent on it. It also switches to a plain path lookup that never touches the clone.
3. When dirty work vanishes, the finalizer's error will name the recovery ref and the command to restore it.
4. It flips `fast_video_artifact_pane.md` to `status: done` to restore the lost edit.

There are two decisions for you at review:
- **How to treat uncommitted edits:** the default is to always leave them alone. The alternative still cleans them up in workspaces with no claim on them.
- **Finalizer error message:** whether to add the recovery-ref hint from step 3. It defaults to on.

**Routing caveat:** I proposed this from a bob-cli session, but every change is in the `sase` project. The plan tells the coder to use `sase repo open sase` if it isn't already in a sase workspace. If the approval screen lets you edit the coder prompt, adding `#gh:gh_sase-org__sase` there is cleaner.

No declaration was needed for this turn because nothing in this workspace was changed.
