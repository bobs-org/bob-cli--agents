# Chat History - ace-run (1ek--plan)

- **TIMESTAMP:** 2026-11-20 09:15:18 EST
- **MODEL:** claude/opus
- **AGENT:** 1ek--plan

**Plan:** /home/bryan/.sase/plans/202611/install_all_mac_capture_skip_unchanged.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/install_all_mac_capture_skip_unchanged.md`

> # install-all: rebuild and restart Bob Mac Capture only when its app changed
> ## Goal
> Today every `just install-all` on macOS rebuilds, re-signs, swaps in, and **restarts**
> Bob Mac Capture, even when nothing in `../bob-mac-capture` changed since the last
> install. The restart quits the running app and stashes any open draft. On SSH sessions
> it can also stop at the signing keychain preflight. After this change, `install-all`
> runs the Mac Capture install (build, swap, and restart) only when the installed app no
> longer matches what the checkout would build. Otherwise the step prints a skip row and
> does not touch the app. The change is entirely in bob-cli. bob-mac-capture's
> `Scripts/install.sh` stays the single install path whenever a rebuild is needed.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me have the `just install-all` command start only restart the
bob-mac-capture app when necessary (when new changes were pushed to that repo that
require a re-build, for example)? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading `scripts/install_all` to see how the bob-mac-capture step builds and restarts the app today.

I've read the mac app's `install.sh`: every run rebuilds, swaps, and restarts the app. Next I'm checking the existing "installed" watermark that install-all writes.

I've mapped the install-all script, the existing install watermark, and its tests. Now I'm reading the docs and CLI-rules memory notes, since the plan will change user-visible docs and add an option.

Next I'm checking which docs, in both repos, describe install-all's Mac Capture behavior and would become wrong.

I have the full picture. Now writing the plan: a single-repo `tale` (bob-cli only) that adds an "is the installed app current?" check before the Mac Capture step.

Validation passes. Submitting the plan:

I wrote the plan and submitted it for your approval with `sase plan propose`. I haven't changed any project files; the work starts once you approve.

**What happens today:** every `just install-all` on the Mac runs the full Mac Capture install. That means a Swift build, re-signing, swapping the app into `~/Applications`, and restarting it if it's running, which stashes any open draft. It does this even when nothing in `bob-mac-capture` changed. From SSH it can also stop at the keychain unlock prompt for signing.

**The plan (one agent, bob-cli only):**
- **A new "is the app current?" check.** It's a new `install_ui app-current` command. It compares three things: the commit recorded at the last successful install (install-all already saves this in `installed.json`), the checkout as it is now, and the app in `~/Applications`. It asks for a rebuild if:
  - the app is missing,
  - there's no install record, or it came from a different checkout,
  - the last install was built from uncommitted changes,
  - the app is newer than the record (someone ran `just install` directly), or
  - any app file differs from the recorded commit.

  It compares file contents, not commit history, so rolling the checkout back still triggers a rebuild if app files differ.
- **When the app is current**, the Mac Capture step prints a skip row like `up to date · 11dcba7 · app current @11dcba7 · not rebuilt`. It skips the signing check, so there's no keychain prompt, and the app keeps running untouched. The time estimate stops counting the Mac Capture build.
- **When the app isn't current**, it prints the reason (for example `rebuild  3 app files changed since @a2aab30`) and runs today's install unchanged.
- **Cases that still always rebuild:**
  - **App is signed ad-hoc (no stable signing identity).** A reinstall is the only way to switch it to the stable identity, which is the fix install-all currently suggests.
  - **New `-f/--force-mac-capture` flag.** Today, flags are lost when install-all restarts itself after pulling a newer bob-cli; the plan passes this one through an environment variable so it survives.
  - **The Python helper is unavailable** (`BOB_INSTALL_UI=0`, or no Python 3.9+). The check can't run, so it falls back to today's always-rebuild behaviour.
- **bob-cli updates alone won't restart the app.** I checked that the app re-detects a replaced `bob` binary on its own.
- **Tests and docs.** New unit tests for the check, Darwin scenarios added to `test_install_all.py`, and a "Restart Mac Capture" section in `docs/guides/install-everything.md`. No bob-mac-capture changes are needed.

**One choice for you at approval (`rebuild_trigger`):**
- **`app_inputs`** (default): also skip when only docs, tests, CI config, or test/doc helper scripts changed. Any other path, including ones the list doesn't cover, still rebuilds.
- **`any_change`**: skip only when the checkout is exactly the commit that was last installed.

The default saves less than you might expect. 479 of 575 bob-mac-capture commits in the last 60 days touched app files, so the main win is skipping when nothing at all has changed.
