# Chat History - ace-run (1ha--plan)

- **TIMESTAMP:** 2026-11-27 12:44:58 EST
- **MODEL:** claude/opus
- **AGENT:** 1ha--plan

**Plan:** /home/bryan/.sase/plans/202611/tie_chords_settle.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/tie_chords_settle.md`

> # Plan: ⌃L and ⌃B tie chords settle the task
> ## Context
> **The keys.** In the Task Card's relationship stages (`docs/task-card.md` "Card
> gestures"; `docs/task-relations.md`, the paragraph that defines `⌃B` / `⌃⇧B` / `⌃L` /
> `⌃⇧L`):
> - `⌃L` in **Depends on** (the dependency panel, `b`) is `plain-out`. It releases the
>   dependency and leaves a plain 🪢 link out.
> - `⌃B` in **Links to** (the link panel, `l`) is `owner-waits`. It turns the plain link
>   into a dependency.
> Both run `tieCommitChord`

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make the `<ctrl+l>` keymap (on the dependency panel in
Obsidian) and the `<ctrl+b>` keymap (on the link panel in Obsidian) start settling the
task? See the bob-cli-q4 epic bead for more context about what I mean by "settling the
task".

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the q4 epic's settle plan to pin down what "settling the task" means before planning.

Searching bob-plugins for the dependency and link panels that own Ctrl+L / Ctrl+B.

Found the tie-change writer; now checking which nav writers already call the taskSettle API and whether the dependency/blocks writers do.

The dependency writer already settles, so I'm tracing why the newer tie-chord path (Ctrl+L/Ctrl+B) misses it.

Checking how the tie writer finds the owner's editor — the chord passes no editor, which may skip the settled write path.

Writing a quick reproduction harness (in /tmp) to confirm whether Ctrl+L/Ctrl+B tie changes leave the note unsettled today.

Now running a repro of Ctrl+L (plain-out from Depends-on) and Ctrl+B (owner-waits from Links) against the real ledger-tools settle.

Same-note with the owner's note open settles correctly in the harness. Checking the remaining paths: cross-note owners, closed notes, and the ID-prompt dispatch.

Same-note cases settle fine; now running the cross-note variant (owner open, prerequisite in a closed note).

Both directions settle in the harness, same-note and cross-note. Checking the real vault history for evidence of what Bryan actually saw.

Found a real instance: commit f4b643441 shows a Ctrl+L release in `bob.md` that left the task `[?]` in `### Blocked`. Tracing what happened next.

Key finding: in the real vault, Ctrl+L removed the dependency but left the task `[?]` in `### Blocked`; the 12:15 reconcile tick then unblocked and moved it. Now looking for a real Ctrl+B instance.

Reproducing with the real `bob.md` preimage from just before that Ctrl+L press.

Reproduced: the writer reports "Still blocked" and leaves `[?]`. Finding which rule keeps it blocked.

The recovery returns `deferred` ("recent activity could not be resolved safely"), so the writer keeps `[?]`. Checking whether that's a harness artifact or the real cause.

The recovery reads the whole vault and any unresolved Depends-On or Pomodoro reference anywhere sets `rankSafe=false`. Checking that against the real vault.

Still deferred with the full vault. Instrumenting the `rankSafe=false` sites to see exactly which references trip it.

Re-running against a consistent snapshot of the vault at commit f4b643441^, with and without the `_conflicts/` copies, to confirm the cause.

Only nav carries this filter. Now replaying a Ctrl+B (Links → owner-waits) against the real vault snapshot to see whether that direction has its own gap.

Root cause and scope are clear. Checking where the recovery contract is documented (ADJ-8 / rank safety) so the plan can point the implementer at the right doc sections.

Have enough on the root cause; checking existing tests that pin the current "defer on any unresolved reference" behavior before drafting.

Reading the remainder of the decisions roster (entries 61–82) to cite every governing record.

Reading the two decisions that govern the recovery side effects (`unblocked-tasks-resurface-as-ticklers`, `task-status-is-derived`).

Checking one more interaction: after a chord the Task Card reopens from the editor cursor, so the cursor must follow the owner task when the settle moves it.

The mirror chord ⌃⇧B has the same gap: the promoted prerequisite's note stays unsettled. Checking which writers share `prepareDependencyTargetNote`, so the fix lands once for all of them.

Fragment 580 is at 983/1000 lines, so the fix needs a new fragment. Checking how the existing chord tests drive `tieCommitChord`, so the plan can name the right harness.

Fixing the reported issues: adding `title`/`goal` and shortening the `rank_poison` choice labels to ≤100 chars.

Validation passes. Proposing the plan.

I've proposed a plan (a single-agent "tale", size medium), and it's waiting for your approval; nothing is implemented yet. Short version: Ctrl+L already calls the settle, but the task never leaves Blocked, so there's nothing to move. Ctrl+B settles its own task but not the other task it promotes when that task is in a different note.

**Ctrl+L (Depends on panel)**
- **What you saw:** vault commit `f4b643441` (today 12:15, `bob.md`). Ctrl+L on `^next-for-notebooks-prose-and-refs` swapped the dependency for a 🪢 link, but the task stayed `[?]` in `### Blocked`. The 12:15 reconcile run moved it 18 seconds later.
- **Why:** to decide what status a released task gets back, the plugin scans every note in the vault. Two problems in that scan:
  - It doesn't skip `_conflicts/` the way bob-cli's reconcile does, and three sync-conflict copies there have links to tasks that no longer exist.
  - One such broken link anywhere makes it give up, so the task stays Blocked.
- **Confirmed:** I replayed that exact `bob.md` against the vault as it was then. With `_conflicts/` it gives up ("Still blocked"). Without it, the task becomes `[ ]` and the existing settle moves it to intake with correct badges.
- **Fix:** skip `_conflicts/` in that scan. This also fixes ⌃⇧L, Enter-release, and Ctrl+D.

**Ctrl+B (Links panel)**
- The task you press it on already settles into `### Blocked`. I checked same-note, cross-note, and a real vault snapshot.
- The gap: if that task is Next or In Progress, its new prerequisite gets promoted to `[*]`. When that prerequisite lives in another note, its note is never settled, so it stays in intake with stale badges until reconcile runs.
- **Fix:** after the gesture's other writes land, run one extra settle on that note.

The vault has no real Ctrl+B use yet, so the Ctrl+B gap comes from my test runs, not from history.

**Decisions for you at approval**
- **Ignoring links to tasks that no longer exist** (recommended: yes): reconcile keeps these links on purpose, so even after the `_conflicts/` fix, one of them anywhere in the vault would make Ctrl+L fail the same way again.
- **Fixing ⌃⇧B too** (recommended: yes): it has the same unsettled-promotion gap and uses the same fix.

The plan also covers regression tests (including a synthetic version of today's case), a fix to `docs/task-dependencies.md` §6.6, which still says nav never regroups lines, and redeploying only the navigation plugin. I didn't change any files or the vault; my test scripts are in `/tmp/tie-settle-repro`.
