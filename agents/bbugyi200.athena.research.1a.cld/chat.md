# Chat History - ace-run (research.1a.cld)

- **TIMESTAMP:** 2026-08-27 09:59:45 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1a.cld
- **PROMPT:** `~/.sase/multi_prompts/202608/gh_bobs_org__bob_cli-multiprompt-260827_094431.md`

## Prompt

%id(cld, clan=research.1a) %m:@research_b  #gh:gh_bobs-org__bob-cli I would like to stop using obsidian sync and start using
my obsidian vault's GitHub repo as the primary and only way that I sync my obsidian
vault between my MacBook and this machine. I frequently use Obsidian on both machines at
once so it's important that the sync process be as frictionless as possible for me
(without eating up resources on either machine).

Can you do some research with the goal of helping me understand the best way to
implement this? End your analysis with a recommended solution. Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.


## Response

I'll start by getting the lay of the land — the vault, its repo, and existing docs about Obsidian sync here.

Report written. Now the required final declaration.

Research written to `sase/repos/research/202608/obsidian_git_only_sync.md` (643 lines).

## What I found

**The resource objection is empirically false.** Measured on your actual vault: `git status` = 10 ms warm, `git add -A --dry-run` = 20 ms, remote poll = 490 ms — or **220 ms with SSH `ControlMaster`**. A 15-second loop is ~1.5% of one core. Your notes are under 25 MB; it's `old_lib/` (1.7 GB of the 1.8 GB tree) that makes the repo look heavy.

**The real problem isn't conflict frequency, it's conflict *handling*.** Git's default — write `<<<<<<<` markers into the file and halt — is unacceptable when Obsidian is live-reconciling on-disk changes into an open note, and when `bob move-done-tasks` parses that note's task syntax at 03:30. That one design decision is the whole project.

**The Obsidian Git plugin is the wrong engine here**, for reasons specific to your setup: it only runs while Obsidian is open (athena is a server whose vault is edited by cron and agents), its finest interval is minutes, it would race `bob bulk-git-commit`, and it has no unattended conflict policy. Upstream's docs don't cover multi-desktop use at all.

Two things I dug up that you'd otherwise hit cold:

- **A silent regression.** Obsidian Sync currently carries your six custom `bob-*` plugins to the MacBook via its `community-plugin` config type. Git can't — they're explicitly `.gitignore`d. Report recommends tracking the built artifacts in the vault repo, since that's the only genuinely frictionless option.
- **`bob bulk-git-commit` never fetches** (`src/native/sync.rs:48`). That's only safe today because Obsidian Sync guarantees convergence before cron runs. Remove Sync and the 03:30 commit diverges from whatever the Mac pushed. Must ship with the switch, not after.

Also: the plugin docs' "Snap not supported" warning doesn't apply — `snap info` shows obsidianmd ships it under **classic** confinement, so there's no sandbox blocking git.

## Recommendation

Build `bob vault-sync` (a new subcommand — `bob-cli` is already cross-platform and installed on both machines), driven by `inotifywait -t 15` under systemd on athena and `fswatch` under `launchd` on the Mac. **Merge, never rebase** — a failed rebase leaves a half-replayed worktree for Obsidian to find. Resolve every conflict as a **Syncthing-style conflict copy**: remote wins in place, local preserved as `<stem>.conflict-<host>-<timestamp>.md`. That's Obsidian Sync's own "create conflict file" strategy, so you're re-implementing supported behavior. Never `merge=union` — it would silently duplicate task lines in the Pomodoro ledger.

Latency lands at ~5–10 s out, ≤15 s in. That's 10–20× worse than Sync and still fine for one person with two keyboards.

Four open questions are flagged in §9. **The first one could invalidate the plan**: if you use Obsidian on a phone, git-only doesn't work — upstream calls the mobile git implementation "very unstable." I found no `workspace-mobile.json` in the vault, but your `.gitignore` lists it, so I couldn't rule it out from here.
