# Chat History - ace-run (18z--plan)

- **TIMESTAMP:** 2026-11-05 17:55:54 EST
- **MODEL:** claude/opus
- **AGENT:** 18z--plan

**Plan:** /home/bryan/.sase/plans/202611/doctl_login_script.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/doctl_login_script.md`

> # Add a guided doctl_login script to chezmoi for athena's Apollo recovery token
> ## Goal
> Add a chezmoi-managed bash script, `doctl_login`, that is deployed only to athena. It
> makes the one-time `doctl` authentication dead simple, the same way `bob gcal login`
> makes Google Calendar setup simple:
> - numbered steps;
> - a short checklist with the exact URL;
> - a hidden token prompt;
> - validation before anything is saved;
> - an idempotent rerun that only re-checks.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli If I'm going to set up `doctl` on this machine, I want a script that makes this
dead simple. This probably shouldn't be a part of `bob` so I was thinking we could write
a script to my chezmoi repo? See the `bob gcal login` command for an idea of what I am
looking for and see the `18w.f0` sase agent for context behind the recent `doctl`
install. Can you help me implement this?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the prior doctl plan and now looking at `bob gcal login` as the UX model.

Opened the chezmoi repo; checking how the doctl installer landed and where helper scripts live.

Confirmed doctl v2.3.0 is installed on athena but not logged in; checking whether the 18w.f0 installer commit has landed in chezmoi.

Reading the pending Apollo recovery runbook from the 18w.f0 diff so the new script matches its token scopes and agent policy.

Studying the chezmoi script/test conventions; now checking doctl v2's auth CLI surface (read-only `--help`).

Key finding: doctl v2 also has an OAuth `doctl auth login --no-browser --scopes` flow. Checking doctl's source for how token validation and the no-browser callback work before choosing the auth path.

Settled the design: a guided, idempotent bash `doctl_login` in chezmoi, built on the approved token decisions. Recording the prior plan as linked context, then writing the plan.

Writing the plan file now.

Plan validates cleanly. Submitting it.

Staged. Finishing through `/sase_final`.

I wrote the plan and it's now waiting for your approval. Nothing has been built yet and no files were changed in bob-cli or chezmoi. The plan is a single-agent, medium-size job (`sase_plan_doctl_login_script.md`).

**What it adds:** a bash script in chezmoi at `home/bin/executable_doctl_login`, deployed only to athena via `.chezmoiignore`. It's modeled on `bob gcal login`:

- **Three numbered steps.** It checks the doctl binary, then the token, then confirms it can see apollo. The look matches `bob gcal login`: same columns, colored ✓/!/✗, the URL on its own line.
- **Token setup.**
  - It shows a short checklist: the token page URL, **No expiry**, and the 8 custom scopes you already approved.
  - It reads the token from a hidden prompt.
  - Before saving anything, it asks DigitalOcean which scopes the token has. If any are missing, it says which and asks again.
  - It saves through `doctl auth init`. The token never appears on the command line, in output, or in logs.
- **Rerunning is a read-only check.** When a token is already saved, it re-checks the scopes and shows apollo's ID, status, region and IP. It also warns if the token has an expiry date, since DigitalOcean's token form defaults to 90 days.
- **No terminal, no prompts.** Without a terminal it never asks for input, so agents can run a bare `doctl_login` as a safe status check.
- **Flags:** `-r` swaps in a new token, `-l` removes the saved one (then reminds you to revoke it), `-y` skips the remove confirmation.
- **Tests:** about 16 bashunit cases using fake versions of doctl, curl and ssh, including a check that a token never leaks into output.

**Why not doctl's browser sign-in?** doctl v2 has one (`doctl auth login`), but its no-browser mode still waits for a reply on athena's own localhost. Approving from your Mac over SSH would need port forwarding. Its sign-in also depends on a refresh token that could expire between outages, which goes against your No-expiry choice.

**Coordination with 18w.f0:** that agent's installer, its tests, the runbook (`apollo/recovery.md`) and the tailnet memory section aren't committed yet. They're held until you answer its question ("done" or "later"). This plan doesn't touch any of them. If the runbook hasn't landed when this runs, the agent files a follow-up task for the edits instead.

**Decisions for you at review:**
1. **`extra_scopes`** (default **refuse**): refuse to save a token with extra scopes that can change things (like `droplet:delete`), or just warn and save it anyway.
2. **`runbook_pointer`** (default **yes**): point the runbook's setup section at `doctl_login`, keeping the manual steps as a fallback.
3. **`memory_tailnet`** (default **no**): add one sentence about `doctl_login` to the tailnet memory note.

After it lands:
1. Run `chezmoi update -a --force` on athena.
2. Run `doctl_login`.
3. Answer 18w.f0's pending question with "done" so it can check the setup and commit the installer and runbook.
