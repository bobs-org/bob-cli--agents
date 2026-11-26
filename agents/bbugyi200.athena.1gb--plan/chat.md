# Chat History - ace-run (1gb--plan)

- **TIMESTAMP:** 2026-11-26 04:59:37 EST
- **MODEL:** claude/opus
- **AGENT:** 1gb--plan

**Plan:** /home/bryan/.sase/plans/202611/home_card_kind_scoped_frontmatter_release.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/home_card_kind_scoped_frontmatter_release.md`

> # Keep property cards' native-Properties takeover when the home card refreshes
> ## Problem
> Obsidian's native **Properties** panel shows again under property cards: day, week,
> quarter, and year cards, plus album, record, and bank cards. The screenshot shows
> `2026/20261125.md` in Live Preview: the day card is mounted with its `Properties · 9`
> foot, and the native panel is visible below it. Only the card-owned `intentions` row is
> hidden.
> ## Root cause (verified in the live Mac Obsidian)
> Environment: `bob-ledger-tools` 1.166.4. The Mac's `main.js` hash equals bob-plugins
> `master` at `8645ed55`, and the Mac runs `bob` 0.6.0. All probes used the Obsidian CLI's

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli The native "Properties" have started showing up on pages that have property
cards again in Obsidian. See the ~/tmp/screenshots/20261126_044708.png screenshot for
context. Can you help me diagnose the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the bob-plugins repo to find where property cards hide Obsidian's native Properties panel, and what changed recently.

Found the CSS that hides native Properties (`bob-property-card-owns-frontmatter` class on the view scope). Now tracing how the day card acquires that ownership and which recent commit broke it.

The `bob` CLI on athena reports `props_v1` correctly, so the capability probe passes here. Next I'm checking the Mac, where the screenshot was taken: its `bob` binary and its deployed plugin build.

Obsidian 1.14.4 on the Mac ships its CLI, so I can inspect the running app's plugin state read-only instead of guessing.

Capability is confirmed and the day card's slot entry is mounted, yet the scope is not owned. Every capability gate passes, so I'm evaluating each remaining eligibility gate inside the live app.

Root cause is pinned down. Before writing the plan, I'm checking open beads for an existing report of this regression or an in-flight phase touching home-card ownership.

The `pl.9.1` epic's agents are live, so the fix must stay narrow and rebase cleanly. One last check: how fixes reach the Mac, since the Mac deploys from its own bob-plugins checkout.

The root cause is confirmed and the fix is small, so I'm writing a single-agent tale plan, then validating it.

Fixing the four validation errors: adding `title`/`goal` and shortening both `why` lines to 100 characters or fewer.

Validation passes. Proposing the plan.

Plan staged. Cleaning up the read-only probe scripts I left in the Mac's `/tmp`, then finalizing.

I found the root cause, confirmed it live in your Mac's Obsidian, and submitted a plan for the fix. I haven't changed any files.

**Root cause:** the Area/Project home card switches off the other property cards' hiding of native Properties. It's a regression from bob-plugins commit `8698046c` (bob-cli-pl.9.1.1, about 01:19Z today), which gave the home card its own Properties takeover.

- **What it does:** the home card's refresh runs in every open note. On a note that isn't an area or project (your day note, for example), it releases Properties ownership through `homeCardReleaseFrontmatter` in `249da-plugin-home-card-ownership.js`. That release only filters by plugin and path, not by card kind. Each note pane has one ownership slot, so it frees whichever card owns it: day/week/quarter/year, album, record, or bank. Every other card's release is already limited to its own kind.
- **Why it sticks:** the home card refreshes on any vault write anywhere: autosave, vault sync, `bob` writers, Tasks cache updates. The day card doesn't refresh on those events, so native Properties stays visible until you scroll or edit that note.
- **Why tests missed it:** the real-Obsidian takeover test only checks that a card takes over Properties right after the note opens, never that it keeps it afterwards.

**How I confirmed it on the Mac** (plugin 1.166.4, matching bob-plugins master `8645ed55`, `bob` 0.6.0):
- Every condition for hiding Properties passed on `2026/20261125.md`, yet nothing owned the Properties panel.
- Calling the day card's own takeover hid Properties immediately.
- Refreshing only the home card made Properties visible again, and it stayed visible until the day card refreshed.

As a side effect, Properties is hidden again on the day note you have open. It will come back after your next vault write until the fix is deployed.

**The plan** (tale, size medium) is staged for your approval:
- Make `homeCardReleaseFrontmatter` release only Area/Project ownership. The bank.md arbitration release stays as it is.
- Add regression tests, written to fail before the fix: a behaviour test, and a source check that every card's release is limited to its own kind.
- Update the architecture docs, build, run the full test suite, and deploy with `bob plugins sync`.

It asks you two questions:
- **`e2e_survival_check`** (default: add): add a required real-Obsidian check that Properties stays hidden after an unrelated vault write.
- **`mac_deploy`** (default: sync): after landing, run `ssh mac 'bob plugins sync -p bob-ledger-tools'`, since the Mac's plugin copy only updates manually.

The open Bank/Area arbitration epic (`bob-cli-pl.9.1.2.1`) is editing the same files right now. The plan tells the implementer to rebase before editing and before committing, and to keep the code change to that one release filter.
