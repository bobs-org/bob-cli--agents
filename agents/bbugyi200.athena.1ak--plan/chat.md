# Chat History - ace-run (1ak--plan)

- **TIMESTAMP:** 2026-11-09 11:52:36 EST
- **MODEL:** claude/opus
- **AGENT:** 1ak--plan

**Plan:** /home/bryan/.sase/plans/202611/hourly_gmail_sync_cron.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/hourly_gmail_sync_cron.md`

> # Enable the hourly bob-gmail-sync cron job on the Mac
> ## Goal
> Turn on the Mac's `bob-gmail-sync` cron job and run it **hourly**, at minute `:07`. It
> runs `bob gmail sync -q`, which files `bob`-labelled Gmail threads as tasks and watches
> them for replies. Then update the bob-cli docs that still describe the job's old
> 15-minute slot.
> ## Background (verified 2026-11-09 during planning)
> - Epic `bob-cli-ii` (plan `plan:202611/gmail_sync_reply_watch.md`) built
>   `bob gmail sync`. Its `cron` phase (bead `bob-cli-ii.8`, reviewer decision
>   `cron_enabled = no`) added the job to the chezmoi cron data on purpose as

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me enable the hourly gmail sync that we were supposed to add to my
crontab? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Found it: a `bob-gmail-sync` job exists on the mac but is `enabled: false` and set to every 15 minutes, not hourly. I'm now checking why it was disabled and whether the mac can actually run it.

The job was deliberately added disabled by bead `bob-cli-ii.8`. I'm reading that bead and the related writer-pin bead (`bob-cli-ew`) to see what was supposed to happen before enabling.

The cronrun environment resolves `bob` correctly. My SSH doctor run passed, but that shell may carry env that cron lacks, so I'm re-running doctor (read-only) under a stripped cron-like environment.

The docs fix is clear. Last check is whether `cronctl apply mac` can install over SSH now, or whether the TCC block (bead `bob-cli-if`) still applies.

Validation flagged missing `title`/`goal` and choice/why labels over 100 chars. Fixing those.

Validation passes. Submitting the plan.

I've written and submitted the plan for the hourly Gmail sync. Nothing is changed yet: the plan is waiting for your approval, and an implementing agent starts once you approve it.

**What happened:** an earlier phase of the Gmail-sync work added the `bob-gmail-sync` job to the Mac's crontab data turned off on purpose, every 15 minutes at `7,22,37,52`. Its rollout checklist ended with "ask an agent to set it to enabled", which is this step.

**What I checked on the Mac (read-only):**
- The installed `bob` has `bob gmail sync`, and `bob gmail doctor` passes.
- Doctor also passes in a stripped-down environment like cron's. `gog` (the Gmail client `bob` uses) stores its login in a file, so it doesn't need your logged-in session.
- A manual sync succeeded at 06:25 today, and a dry-run sync found nothing new.
- The only doctor warning is that 13 of your 17 Gmail routing labels don't match a note. That's yours to fix in Gmail and is outside this plan.

**What the plan does:**
1. **Crontab data (chezmoi):** turns `bob-gmail-sync` on and changes its schedule to `7 * * * *`. Minute `:07` keeps the existing spacing: two minutes after projects sync, three before task reconcile, clear of highlights at `:00`. The writer setting stays commented out because the Mac's hostname keeps changing (bead `bob-cli-ew`).
2. **Docs (bob-cli):** `docs/vault-git-sync.md` still describes four 15-minute jobs; the plan corrects that and adds a one-line link from `docs/gmail.md`.
3. **Install on the Mac:** after the commit is pushed, the change is applied to the Mac remotely. Then the job runs once for real and its log is checked.

**Possible results of the install step:**
- If the Mac is asleep, it picks up the change the next time it updates.
- If the Mac reports "Operation not permitted", it is refusing remote crontab changes; you'd need to run `chezmoi update -a` in a Terminal on the Mac.

**Decision for you:** whether to also delete the leftover `cron.retire` migration list in the same change, which finishes and closes bead `bob-cli-if`. I defaulted to yes: `cronctl status` already says it can go, no live crontab line changes, and the crontab instructions say to delete it at this point.

Hourly runs won't trigger false alarms. Bob only warns, or emails a failure, after more than two hours without a successful sync, so one missed run is quiet.
