# Chat History - ace-run (1fg--plan)

- **TIMESTAMP:** 2026-11-23 07:57:40 EST
- **MODEL:** claude/opus
- **AGENT:** 1fg--plan

**Plan:** /home/bryan/.sase/plans/202611/tick_network_blips.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/tick_network_blips.md`

> # Stop `bob tick` from mailing on self-healing network blips
> ## Problem
> Epic `bob-cli-pj` (plan `202611/tick_contention_noise.md`) fixed the vault-contention
> noise from the Mac's `*/5` `bob tick` cron. Those failures made up 13 of the 19 failed
> steps from 2026-11-18 to 2026-11-23: `refs scan_failed` while the daily note changed,
> and `projects lock_busy`. That plan explicitly left network failures as a non-goal. They
> "cannot yet be told apart from real sync problems such as a git conflict".
> Every one of the other 6 failed steps was a network outage, and each one healed itself
> on the next tick:
> | When (UTC)       | Step       | Tick line                                                | Real cause                                            |

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me verify that this issue is fixed? If not, use your /sase_plan skill to plan the appropriate changes.
 See the
^cron-lt-bbugyi-kellys task in the ~/bob/dev.md file for context. %m:@xlarge

## Response

Checking the Mac's bob-tick log now to see whether the failures from Nov 22 are still happening after the recent fixes.

The Mac has run cleanly since the last failure. Now I'm checking whether the code fixes actually cover each failure class.

Still checking the code. The failures are fixed, but I want to know why the receipt said "refs due" without refs running.

Confirmed that the Mac is running the build with the fix. Now I'm checking when it was installed so I can count how many clean hours it has had.

I've confirmed the vault-contention fixes. Now I'm looking at the two failure types the fix deliberately left out: the bare `gmail exit 1` and `projects sync_failed`.

Checking the Mac's Gmail sync health file to find out what caused the `gmail exit 1` on Nov 22.

Still reading: vault-sync reports failures only as untyped strings, so tick can't tell a network blip from a git conflict. Checking the gcal adapter next, then I'll write the plan.

I have the verdict. The contention fixes are deployed and working, but the network-blip class is still unfixed (it was deliberately left out). Starting the plan for that remaining part.

Still gathering facts for the plan: Gmail and Google already tag errors as `network`/`timeout`. Checking how gcal reports them in JSON.

I have enough to write the plan. Writing it now.

The plan validates. Submitting it.

It's mostly fixed. Five of the six emails in the task's thread came from vault contention, and that's fixed and running on the Mac. The sixth (the 13:15 one on Nov 22: `gmail exit 1` plus `projects sync_failed`) was a network outage. The earlier fix deliberately left network failures out, so that kind of failure will still send an email. I've submitted a plan to cover it.

**What's fixed:**
- **The fix is on the Mac.** It runs bob-cli at `2652b794`, which includes the contention epic `bob-cli-pj`. That build was installed Nov 23 at 05:32 EST, after a partial build the night before.
- **No failures since.** The last failed run was 2026-11-22 23:14Z. Every run since then has exited 0.
- **Tests pass at that commit.** All 156 `tick::` and `highlights::scan_interleave::` tests pass in CI at exactly the commit the Mac runs.
- **Thin real-world proof.** Only two refs scans have run on the full build, and no edit has collided with a scan since. So the "edit during scan" path is proven by tests, not yet by a real event on the Mac.

**What's still open:** since Nov 18 there have been 19 failed steps. Thirteen were contention, now fixed. The other six were network blips that fixed themselves on the next run: two gcal ("check your network connection"), two gmail (bare `exit 1` after 2+ minutes of retries), and two `projects sync_failed`.

Tick can't tell these apart from real problems, for three reasons:
- **vault-sync errors are plain text.** An unreachable remote looks the same as a merge conflict.
- **Gmail's failure reason never reaches tick.** That's why the email just says `exit 1`.
- **Tick ignores the network flag gcal and gmail already send.** It only checks for the contention error codes.

**The plan:** I submitted one plan (single agent, medium size), now waiting for your approval. It would:
- Mark vault-sync's unreachable-remote failures as network errors, and carry that flag through `projects` and `refs`.
- Add a list of failure causes to gmail's JSON output.
- Have tick report network-only failures as an `offline` wait that exits 0.
- Still send one email if a step stays offline for 2 hours, using the existing contention timer.
- Keep real problems (conflicts, auth, setup) failing on the first run, and include the actual error message in every remaining failure email.

**Decision for you:**
- **When to retry after an offline wait:** I defaulted to retrying on the next 5-minute run. The cost is that Gmail may burn about 2 minutes of retries on each run while the Mac is offline. The alternative waits out each step's normal interval, which is fewer retries but up to an hour before mail and calendar catch up.

Two other things I noticed, neither of which fails a run:
- **Refs scans are slower.** No-change scans took 361–454s on the new build, against about 110–130s before. The Mac was on battery and under heavy load, so I can't pin it on the code yet.
- **Misleading "refs due".** The tick footer kept saying "refs due" for about 2 hours this morning, while the refs step skipped itself because nothing in `lib/` had changed. That's cosmetic.

Separately, CI on master is red from 4 `props::` tests on macOS and a lint failure, none related to tick or refs.
