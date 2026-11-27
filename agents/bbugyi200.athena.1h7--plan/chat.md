# Chat History - ace-run (1h7--plan)

- **TIMESTAMP:** 2026-11-27 10:58:30 EST
- **MODEL:** claude/opus
- **AGENT:** 1h7--plan

**Plan:** /home/bryan/.sase/plans/202611/snooze_early_wake_test_leak.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/snooze_early_wake_test_leak.md`

> # Stop plugin tests from waking real snoozed tasks early
> ## Diagnosis
> Bryan's suspicion is half right. The early wake _is_ a timezone error, but `bob tick`
> did not cause it. The Mac's `bob-tick` job runs in America/New_York, and `bob tick` has
> never run on apollo (apollo has no tick state). The real cause is a bob-plugins **unit
> test** that ran the installed `bob snooze wake` against the real vault on apollo, a UTC
> host, with Bob's config hidden.
> Evidence, in order:
> 1. `- **1301** [[bob#^how-to-extract-inline-prose]]` was written to `2026/20261127.md`
>    at about 09:01 ET from the Mac.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Snoozed tasks seem to be waking up early. I think that the `bob tick` command
is maybe using the wrong timezone? See the snoozed task that was just awoken in the
~/bob/2026/20261127.md file and the bob-cli-q5 epic bead for context Can you help me
confirm/deny my suspicion, diagnose the true root cause, and fix the issue?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
  %m:@xlarge

## Response

I'll start by gathering context: the vault note, the epic bead, and the tick/snooze code.

Key clue: the wake commit `dc06affb1` came from **apollo** at `14:33:31 +0000` — i.e. 09:33 New York time, and "woke 14:33" is a UTC wall clock. Let me look at that commit and apollo's setup.

No snooze decision record exists (the epic chose `decision_record = no`). Now the code: how `bob tick` / `snooze wake` compute "now".

`bob` resolves its day zone from config `timezone:` first, then the host zone. Let me check apollo's actual zone, Bob config, and what runs `bob tick` there.

Apollo's config already has `timezone: America/New_York`, and apollo has no cron jobs — so something else on apollo woke the row using a UTC wall clock. Let me find what process did it.

Apollo runs SASE agents in bob-cli workspaces. Let me find which code paths can wake a snooze (any could have been triggered on apollo), then look for logs around 14:33 UTC.

An apollo agent (`bob-cli-qq.10.3`) was running the bob-plugins test suite right before the wake. Let me check what tool runs were active on apollo at 14:33:02 UTC.

Agent processes on apollo carry `DATE=date` (the dotfiles export) — `current_datetime()` has a special path for that. Let me read it and how the receipt's `woken_at` is derived.

Still tracing which apollo process triggered the 14:33 UTC wake — checking the apollo agent's chat transcript now.

The apollo agent re-ran `test-snooze-model-vectors.cjs` alone right in the wake window. Let me read that test.

The fork was a Codex agent; its rollout log will have exact commands with timestamps.

Something finished at exactly the wake moment: ace-run `20261127092530` (monitor `7089wtnnseny`). Let me see what that was.

The wake began the same second this SASE monitor agent finalized (`done.json` 14:33:01.955, wake 14:33:02). Let me check whether a SASE finalizer/hook for this project or vault runs `bob`.

The wake receipt's `wake_id` embeds the waking PID (311720). Searching apollo's logs for that PID to name the caller.

Journal shows a burst of **"SASE checks runner"** scopes (parent PID 303818) starting 14:32:56–14:33:12, and the waking PID 311720 falls right in that range. Let me see what those checks run.

No Rust test build ran near 14:33 on apollo. Let me check whether any other bob subcommand (e.g. capture, which file hooks like `bob_research_capture` call) can trigger a wake internally.

Only a direct `bob snooze wake` could have done it. Let me find what the "SASE checks runner" scopes executed at 14:32:56–14:33:12.

Those checks are PR-status polls, not `bob`. Let me list every agent running on apollo at 14:33 UTC using a login shell (sase isn't on the non-login PATH).

Let me check whether apollo's installed `bob` binary changed around the wake (an install/upgrade could run a different build or post-install steps).

SASE's "snooze" is its own notification feature, unrelated. No agent typed `snooze wake`, so a script spawned it. Let me check bob-plugins test scripts that execute the **real** `bob` binary.

Tick pins `BOB_DIR` for its children, so that path is safe. Let me read the snooze CLI unit tests that call `wake()` in-process.

That's a structural test only. Let me pull every Codex command on apollo between 14:24 and 14:36 UTC to see what the qj.5.1.3 agent actually ran around the test build.

`tests/tasks_real_vault_parity.rs` — a test that deliberately runs against the **real** vault. Let me read what it executes.

That one is opt-in and copies the vault. Let me check the integration tests that actually run `snooze wake`/`tick` and how they set env.

All snooze/tick integration tests are isolated. Let me confirm what the qj.5.1.3 finalizer actually ran between 14:30:35 and 14:35:24 UTC.

The commit finalizer's "stitch main" op ran 14:31:29 → 14:35:00 (211 s), bracketing the wake. Let me see its steps.

The 3-minute gap was bead-page publication, not tests. Let me see what the long-running session 81217 and the 14:27 `cargo test` calls in qj.5.1.3 actually were and when they finished.

Let me pin the timing of the Grok agent's full `npm test` run against the 14:33:02 wake.

Only one `bobSpawnJson` caller lacks a vault path, so a fail-closed rule in the shared helper is cheap. Let me check other plugins' spawn helpers too.

I have the full causal chain. Let me load the planning skill.

Let me check what `docs/snooze.md` promises about the wake zone, and which bob-cli tests run automatic sweeps without a `timezone:` (to scope a possible bob-cli guard).

I have enough to write the plan. Before authoring, let me read the two decisions I'll cite, plus the `snoozed-task` glossary strand to confirm no memory note becomes false.

Let me check the existing skip-report plumbing and where the wake report fields are documented, so the plan names the right files.

I have everything needed. Writing the plan now.

Now fixing the frontmatter: add `title`/`goal`, quote values, and keep labels ≤100 chars and the ask ≤120.

Validation passed. Submitting the plan.

Your suspicion is half right. It was a timezone bug, but `bob tick` wasn't involved: a bob-plugins unit test woke the task. I've written a fix plan and submitted it for your review; no code has changed yet.

## What happened

1. **The wake ran on apollo, which is on UTC.** Vault commit `dc06affb1` (`vault(apollo)`, 14:33:31 UTC) is the one that struck `**1301** [[bob#^how-to-extract-inline-prose]]`. Apollo's wake receipt (`~/.local/state/bob-cli/snooze/last-wake.json`) records the wake at `14:33:02+00:00` against `/home/bryan/bob`. 13:01 counted as already passed at 14:33 UTC, so the task woke at 09:33 your time. "woke 14:33" is a UTC clock reading.
2. **`bob tick` is ruled out.** It has never run on apollo (there's no tick state there), and the Mac's `bob-tick` job uses New York time. Apollo's config does set `timezone: America/New_York`, and a normal `bob` there reports New York time correctly. So whatever woke the task couldn't see your config.
3. **The culprit was a test run.** From about 14:30 to 14:34:53 UTC, the agent `bob-cli-qq.10.2` ran the full bob-plugins `npm test` on apollo. One test in it, `test-ledger-tools-planned-today.cjs`, does this:
   - It hides your config on purpose (`XDG_CONFIG_HOME=/definitely/missing/…`) but keeps the real `HOME`.
   - It starts the real bob-ledger-tools plugin through a test harness that claims to be desktop Obsidian and has no vault path.
   - It loads a sample snoozed row that is due. That fires the plugin's every-minute waker, which runs the real installed `bob snooze wake`.
   - With no vault path, the plugin doesn't set `BOB_DIR`, so `bob` uses your real vault (`~/bob`).
   - With the config hidden, `bob` falls back to apollo's UTC clock. It woke your real 13:01 row, wrote the receipt and sent a notification. The test ignored the result because the dates didn't match its sample data.

The same leak happens on athena and the Mac too. There it wakes real rows at the correct time, so nobody noticed.

## The plan

The plan is `sase_plan_snooze_early_wake_test_leak.md`, sized for one agent:

1. **bob-plugins waker:** it refuses to run `bob snooze wake` unless it can pass the open vault's path as `BOB_DIR`. Two regression tests cover both cases.
2. **bob-plugins tests can't touch your real data:** a shared setup file points `BOB_DIR` at a path that doesn't exist and gives each test a throwaway state directory. It's loaded for the whole `npm test` run and by the test harnesses, so re-running one test file on its own is covered too. A guard test fails if that setup is ever removed.
3. **bob-cli (one decision for you):**
   - **Default:** a scheduled sweep skips and writes nothing when `timezone` isn't configured, and reports `skip_reason: zone_unconfigured`.
   - **Cost:** a machine with no `timezone` setting stops auto-waking snoozes until one is added. All three of your machines already set it.
   - **Unaffected:** waking a specific task by name still works anywhere.
   - **Alternative:** leave bob-cli as is and rely on the bob-plugins fixes alone.

## For you to decide

- **The task that woke early** is now linked under your 10:25–10:50 BUILD Pomodoro. I left it alone. To put it back to sleep until 1:01 PM: `bob snooze add bob:how-to-extract-inline-prose 13:01`.
- **One loose end** I've left out of scope: one other plugin feature (period notes, `292b-plugin-period-notes.js`) also runs `bob` without passing a vault path. It could be tracked as a follow-up task.
