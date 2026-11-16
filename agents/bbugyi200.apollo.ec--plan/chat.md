# Chat History - ace-run (ec--plan)

- **TIMESTAMP:** 2026-11-16 06:40:49 EST
- **MODEL:** claude/opus
- **AGENT:** ec--plan

**Plan:** /home/bryan/.sase/plans/202611/area_link_cards_and_workspace_scroll.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/area_link_cards_and_workspace_scroll.md`

> # Plan: Fix dead and duplicated catalog-card links and the white workspace after area-link clicks
> All code changes live in the **bob-plugins** linked repo (open it with `/sase_repo`;
> read its `AGENTS.md` first). Edit only `plugins/bob-ledger-tools/src/` fragments, then
> regenerate `main.js` with `npm run build`; never hand-edit `main.js`.
> ## What Bryan sees
> After clicking area links in a note's `## Areas` section, the Obsidian window on the Mac
> goes white. The ribbon, tab bar, and editor are gone; a thin strip at the very top shows
> a Dataview `[root:: gtd]` field (the "ROOT gtd" chip). Only the floating status bar
> stays visible. The status bar matched `bob.md` (9 properties, about 35.5k characters).
> The Mac's `.obsidian/workspace.json` shows one tab group with pinned `2026/20261116` and

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I keep winding up with screens like the one shown in the ~/tmp/screenshots/20261116_060105.png screenshot when I click on area note links in H2 area sections. Can you help me diagnose the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:opus

## Response

I'm looking through the bob-plugins source to see what runs when you open a note from an area link.

I'm reading the Areas card code in bob-ledger-tools, since that's what draws the `## Areas` sections.

I'm zooming into the screenshot's top-left corner to identify the stray "ROOT gtd" element.

I'm checking the vault CSS snippets: the "ROOT" chip may be a styled Dataview inline field.

I'm looking at the repo's real-Obsidian e2e harness to see whether I can reproduce the click here instead of guessing from the screenshot.

No Obsidian or Xvfb on apollo, so I can't reproduce the click here. I'm going back to reading the code and the screenshot.

The "ROOT gtd" bar might be Obsidian's top tab/header strip pushed mostly off-screen. I'm checking whether any plugin injects a root chip into tab or view headers.

I'm comparing against Bryan's other recent screenshots to see what a normal window looks like.

I'm checking for plugins that intercept internal-link clicks and open notes with a scroll/line target, since a bad target line would scroll the view into blank space.

The plugin code makes many DOM edits, so I want a real repro. Obsidian isn't installed on apollo; I'm checking the tailnet note to see whether athena can run the real-Obsidian harness.

Athena has Obsidian and xvfb, so I'll reproduce there. I'm reading how the existing e2e harness launches an isolated Obsidian.

I'm writing a throwaway CDP repro script (outside any repo) to run on athena.

Script ready. Copying it to athena, building the scratch vault, and running the repro under Xvfb (this takes a few minutes).

The click on `gtd_daily` in gtd.md's Areas card didn't navigate at all; the active file stayed gtd.md. I'm pulling the screenshots back to look.

I'm reading the dashboard scroll-restore code in `040-editor-and-daily.js`; restoring a saved scroll onto the wrong editor could blank the view.

`170-open-task-jump.js` scrolls a line to the top with `y: "start"`, which fits the bar pinned at the window top. Reading it.

I'm checking the root-marks DOM surgery that wraps native `[root::]` Dataview fields, since that's the one place plugin code moves this exact element.

One anomaly: on love→kelly, the active file became kelly.md, but the only active markdown leaf still shows love.md, scrolled 639px. Pulling that screenshot.

The notebook catalog and notebook header call `.focus()` without `preventScroll`, and the misplaced Areas card lands inside the Notebooks callout. Reading those spots.

Checking whether the Mac is reachable, so I can read its Obsidian `workspace.json` (read-only) for the actual layout, panes, and active note at the time.

The exact path doesn't reproduce the white screen on Linux: no ancestor scrolls and navigation works. Glancing at the bob.md landing.

I have enough to plan. Cleaning up the athena scratch vault and making sure no repro Obsidian process is still running.

Diagnosis is done. I'm writing the plan now.

The plan passes validation. Submitting it.

I found one confirmed cause of the dead area links, but I couldn't reproduce the white screen itself. The plan fixes the confirmed causes and adds a guard so the white screen can't stick. It's submitted as a medium tale with one decision for you.

**How I tested.** I copied your vault to athena and opened it in real Obsidian with the deployed plugins, then made real mouse clicks. I also read your Mac's `workspace.json` to get the actual layout: one tab group with `20261116` and `dash` pinned, and recent files `area.md → dev.md → bob.md`. The status bar in your screenshot (9 properties, ~35.5k characters) matches `bob.md`.

**What causes the dead links (reproduced, all in bob-ledger-tools):**
1. **Areas cards land in the wrong places.** The Areas card code also runs on content Obsidian renders outside the note itself. So a full second Areas card gets painted inside the `## Notebooks` callout in cash.md and love.md, and inside a task row in cash.md's Reading view. It looks exactly like the real one.
2. **Reading view shows the card twice.** Every note with an Areas section gets an extra card under `## Areas` on top of the real `[!areas]` callout.
3. **Links in those extra cards don't work.** The plugin rebuilds those cards' rows on every editor update, including the one your mouse-down causes. The link under the pointer is replaced before you release, so the click never registers and nothing opens. Links in the real `[!areas]` callout still work.
4. **The Projects and Albums cards have the same placement flaw.** A hover preview of bob.md showed a second Projects header on the note's title.
5. **Some focus calls can scroll the whole window.** Notebook-header and notebook-summary code moves focus without preventing scroll, and the header code can pick a matching link in any pane. That can push the whole workspace off-screen.

**The white screen.** It means Obsidian's main workspace area was scrolled off-screen: only the status bar stays put, which is what your screenshot shows. The "ROOT gtd" strip is the `[root:: gtd]` field from your pinned daily note. Replaying your exact path on Linux (`area.md → [[dev]] → [[bob]]`, same tab layout and window size) left everything at scroll 0, so I can't prove which call scrolled it.

**What the plan does:**
- Only paints a standalone card in the note's own Reading view, and only when the note has no stored callout. This applies to Areas, Projects and Albums.
- Stops rebuilding unchanged Areas rows, and makes those row links open their note in both Reading view and Live Preview.
- Makes every focus call skip scrolling and stay in the pane that had focus.
- Adds tests for all of the above, plus a real-Obsidian check on athena. Then build, docs, and `bob plugins sync`.

**Decision for you — `scroll_guard` (default: add it).** The guard snaps the workspace back if anything scrolls it, and logs a console line naming what was focused and which file was active. The white screen then can't stick, and the next time it happens on the Mac the log shows what triggered it. Choose `skip` to fix only the confirmed defects; if the white screen comes back, it would need another investigation.

The scratch vault and test Obsidian process on athena have been removed.
