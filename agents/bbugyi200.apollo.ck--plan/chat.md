# Chat History - ace-run (ck--plan)

- **TIMESTAMP:** 2026-11-05 08:56:05 EST
- **MODEL:** claude/opus
- **AGENT:** ck--plan

**Plan:** /home/bryan/.sase/plans/202611/merge_label_block_id_prompt.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/merge_label_block_id_prompt.md`

> # Plan: Prompt for missing block IDs when committing a merge label
> ## Problem
> In the Obsidian Links stage (Task Card `l` / `⇧L`, Ctrl+Shift+L, Ctrl+Shift+Alt+L,
> counted and marked batches), choosing a configured merge label such as `merged into`
> with `⇧↵` fails with the notice **"Merging needs a ^block-id on every source and the
> target"** unless every task already has a `^block-id`. Plain and other labelled
> relations do not fail here. Their id-less targets go through the existing new-block-ID
> prompt (`docs/task-relations.md` §5 and LG5), and the ID is written before the link.
> The merge path refuses before it ever reaches that prompt. `bob task merge` addresses
> tasks only as `note:block-id` locators (bob-ledger-tools `taskMergeLocatorText`), so it

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When linking a task to another using the "merged into" relation label, we
should be prompted for the block IDs that need to be added. Currently, an error is shown
unless both tasks already have a block ID. See the ~/tmp/screenshots/20261105_061344.png
screenshot for context. Can you help me fix this?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Not in bob-cli. It's in bob-plugins; let me open that repo.

Tracing the existing block-ID prompt (LG5) to see how a merge could reuse it — specifically how the prompt stage resumes, handles Escape, and how source refs pick up a newly minted ID.

Still mapping the prompt flow — now checking how Escape/Back leaves the block-ID prompt so a merge prompt can return cleanly.

Reviewing the existing LG5 prompt tests and docs so the plan can mirror them for merge.

Plan shape is clear. Before writing it, reading the docs memory (the plan touches bob-cli `docs/task-relations.md`) and checking for related beads.

Checking how the vault stage exposes `sources`, to decide whether the minted IDs should update session state or go into an overrides map.

I have what I need. Writing the plan: a single-agent tale (medium), with the fix in bob-plugins and a contract note in bob-cli docs.

Validation passes. Proposing the plan now.

I've written a plan to fix this, it passed validation, and I've proposed it for your approval. I haven't changed any files.

**Cause.** The error comes from bob-plugins, in `plugins/bob-navigation-hotkeys/src/429a-relation-merge-commit.js` (`commitRelationMergeLabel`). When you link with a merge label, it checks block IDs first and shows "Merging needs a ^block-id on every source and the target" as soon as one is missing. Plain and other labelled links don't fail this way: a target without an ID gets the new-block-ID prompt. The merge path needs IDs on both tasks because `bob task merge` only finds tasks by `note:block-id`.

**The plan** (one coding agent, medium size):
- **Prompt instead of refusing.** Collect every task in the merge that has no ID, sources first and then the target. Run the existing block-ID prompt for each one, prefilled from the task text. It shows `⤵ Merging needs an ID · 1 of 2 · line N`, and Return reads `Next`, then `Create & merge` on the last one.
- **Then merge as usual.** After the last ID is written, the relation field comes back with your label and the merge carries on: preview, the second-Return confirm when two or more tasks merge, the offer picker, apply, and Undo merge.
- **Already-closed source.** If the source is already closed, the plain-link path runs before any ID check. Today that case is also refused.
- **Save open tabs first.** Before `bob` reads the vault, save every open tab of the notes involved. An ID written into a note open in another tab could otherwise not be on disk yet.
- **Escape.** Escape at a prompt closes the picker. IDs you already confirmed in that run stay written, the same as the existing multi-target prompt.
- **Small edit to a full file.** `426-picker-relation-stage.js` is at 994 of its 1000-line limit, so it only gets two one-line hooks; the new logic goes in `429a`.
- **Tests, docs and release.** Tests are planned in `test-navigation-relation-merge.cjs` plus a realistic flow in `test-navigation-relation-links-stage.cjs`. The merge paragraph in bob-plugins `docs/bob-navigation-hotkeys.md` and the merge-label section (§21) of bob-cli `docs/task-relations.md` get updated. The plugin goes to version 2.74.1, followed by `bob plugins sync`.

One choice for you: a plain link adds a missing source ID silently, without asking. The plan prompts for every missing ID, source and target, because that's what you asked for.
