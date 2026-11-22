# Chat History - ace-run (1fa.1--plan)

- **TIMESTAMP:** 2026-11-22 17:55:54 EST
- **MODEL:** claude/opus
- **AGENT:** 1fa.1--plan

**Plan:** /home/bryan/.sase/plans/202611/tick_contention_noise.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/tick_contention_noise.md`

> # Stop `bob tick` from mailing on self-healing vault contention
> ## Problem
> The Mac's `*/5` `bob tick` cron mails whenever a run exits 1. From 2026-11-18 to
> 2026-11-22, 16 of 929 runs failed. Every failure either healed itself on a later tick or
> was a network blip:
> |     Count | Step                        | Code                   | Cause                                                                                                                                  |
> | --------: | --------------------------- | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
> |         8 | `refs`                      | `scan_failed`          | "scan inputs changed during planning (input changed: `2026/2026112x.md`, `bob.md`, library membership)"                                |
> |         4 | `projects`                  | `lock_busy`            | `bob projects sync` waits only 3 s for `bob_sync.lock`; in the same run `tasks` waited about 116 s on the same lock and then succeeded |
> | 2 + 2 + 2 | `gcal`, `gmail`, `projects` | network, `sync_failed` | Network or vault-sync outages; out of scope (see Non-goals)                                                                            |

*See full plan file for details.*

## Prompt

%id:@.1
#gh:gh_bobs-org__bob-cli Is this something we can/should fix? If so, use your /sase_plan skill to plan the appropriate changes. See the
^cron-lt-bbugyi-kellys task in the ~/bob/dev.md file for context. %m:@xlarge

## Response

I'm reading the refs scan planner to see why tonight's `bob tick` runs failed, then I'll check the projects/gmail failures.

I'm now tracing the tick runner and the docs, to decide whether these failures are real bugs or noise.

I've got the Mac's tick history: failures are intermittent, mostly the refs scan. Next I'm checking how often each failure kind happens and what the refs step is spending its time on.

I'm reading the tick run loop to see how "waiting" vs "failed" outcomes are recorded. Then I'll look at why a no-change refs scan takes about 2 minutes.

Working out what the per-PDF planner actually reads from the vault. That decides whether a daily-note edit really needs a full re-plan.

The Mac app doesn't read tick receipts. I'm checking the Obsidian plugins for any consumers next, then I'll read the plan skill and write the plan.

The plan validates. I'm submitting it for your review now.

Yes, we can and should fix this. I've submitted a two-phase plan for your review.

**Why the runs failed.** From Nov 18 to Nov 22, 16 of 929 Mac `bob tick` runs failed. All of them either fixed themselves on a later tick or were network outages:

- **refs, 8 failures (1 in 8 refs runs):** this is the main source of the emails. Before planning, `bob ref scan` takes a snapshot of every vault note (7,451 files). Planning then takes about 110 s even when nothing changed, because it parses all 743 PDFs. If any note changes in that window, the scan fails; it was usually today's daily note while you were editing it. Each retry re-plans the whole library, so one tick can re-plan it up to 6 times before giving up. That's why failed runs took 4 to 12 minutes.
- **projects, 4 failures (`lock_busy`):** `bob projects sync` waits only 3 s for the vault lock. In the same run, `tasks` waited about 2 minutes on that lock and succeeded.
- **gcal, gmail and projects, 6 failures:** network or vault-sync outages.

On top of that, tick reports any nonzero exit from a step as "failed". That includes cases its own docs say should count as "waiting", such as a busy vault.

**The plan:**
1. **Contention counts as waiting** (medium):
   - When a step gives up on the vault lock, tick records it as waiting and exits 0.
   - `bob ref scan` gets a new `inputs_changed` error code for "notes changed during the scan", which tick also treats as waiting.
   - If a step is still waiting after 2 hours, it's reported as failed (`stalled`), so a real stuck lock still emails you. The plan has a decision for you here: 2h is the default, with 6h or 1h as alternatives.
   - A change to a destination asset still fails and emails, because that path refuses to write for safety.
   - The new error code changes the JSON contract, so the commit gets a `!`. Nothing in Bob Mac Capture or the plugins reads that code.
2. **The refs scan only re-plans what an edit affects** (large; the worker will plan it first):
   - An edit to a note no PDF's plan depends on, like the daily note, no longer forces a full re-plan.
   - Changes to one PDF's own files re-plan just that PDF.
   - Library membership or config changes still rebuild everything.
   - This applies at all three places the scan currently starts over.

**Left out on purpose:**
- **Network failures keep emailing.** They can't yet be told apart from real sync problems like a git conflict.
- **No speed-up of the 110 s planning pass.** That's separate performance work; making it faster would also narrow the window for this race.
