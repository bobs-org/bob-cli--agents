# Chat History - ace-run (fl--plan)

- **TIMESTAMP:** 2026-11-22 11:05:01 EST
- **MODEL:** claude/opus
- **AGENT:** fl--plan

**Plan:** /home/bryan/.sase/plans/202611/successor_pool_skips_conflict_copies.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/successor_pool_skips_conflict_copies.md`

> # Plan: Successor offers must skip `_conflicts/` sync copies (task-status-cycler)
> ## Diagnosis
> The Obsidian "Pull in successors of #prj Review … annotations …" picker showed 6 offers:
> three hand-offs from `sase_blog`, and the same three again from a note named
> `sase_blog.apollo-2026-11-22T153045+0000`.
> - That second note is `_conflicts/sase_blog.apollo-2026-11-22T153045+0000.md`.
>   `bob vault-sync` wrote it at 2026-11-22T15:30:45Z when `sase_blog.md` was modified on
>   two hosts. The sync log `_conflicts/sync_conflicts.md` records it as a "both-modified
>   text" conflict. The copy repeats the whole note, including `^merge-future-section`,
>   `^evals-future-zettel`, and `^fill-zettel-album`, each with

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli It looks like I'm seeing duplicate successors for some reason in Obsidian. See
the ~/tmp/screenshots/20261122_105659.png screenshot for context. Can you help me
diagnose the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Now checking `vault_note_paths` in `capture_dependency_tasks.rs` — its doc comment claims `_conflicts` is excluded.

The Obsidian close path lives in the `task-status-cycler` plugin, which runs its own vault scans. I'm checking which of those scans don't skip `_conflicts/`.

I'm checking whether the nav plugin's `&` dependency picker has the same gap; the fix for the successor offers is already clear.

I've audited the cycler's scans. Next I'm reading the dependency doc's description of the Tasks-cache source so the plan can update that doc as well.

I have the full picture. Last check is the plugin's version-bump convention, then I'll write the plan.

Writing the plan now.

I found the cause and submitted a fix plan for your review. Nothing has been changed yet; an implementing agent starts once you approve it.

**Root cause:** the duplicate set isn't really from `sase_blog`. Its subtitle reads `sase_blog.apollo-2026-11-22T153045+0000`, which is `~/bob/_conflicts/sase_blog.apollo-2026-11-22T153045+0000.md`. `bob vault-sync` wrote that copy at 15:30 UTC today because `sase_blog.md` was edited on two machines. The sync log `_conflicts/sync_conflicts.md` records it as a "both-modified text" conflict. The copy contains the same three tasks, each with `[dependsOn:: sase_blog_annotations__prj]`, so they show up as a second set of dependents of the `#prj` you closed.

- **bob-cli already ignores these copies.** Its scans skip `_conflicts`, `_generated`, `_templates` and hidden folders. So does the nav plugin's `&` picker.
- **The `task-status-cycler` plugin does not.** It builds the Obsidian successor list itself, either from the Tasks plugin's task list or from a fallback scan of every note. Neither filters those folders. The plugin already has a function for this (`isExcludedSuccessorVaultPath`), but it's only used for counting note names.

The same gap causes three other problems:
- Picking a conflict-copy row writes a link into the copy.
- Unblocking can edit task statuses inside conflict copies.
- If a copy still holds an open version of a task you closed, the plugin can treat that prerequisite as open, so the tasks waiting on it stay Blocked.

**The plan (one agent, small):**
- Apply that existing filter wherever the plugin builds its successor and unblocking lists:
  - the Tasks plugin task list (one change there covers most callers);
  - open editors showing a conflict copy;
  - the fallback scan of every note;
  - the unblocking fallback;
  - the project-blocking check;
  - the `[id::]` duplicate and rename scans.
- Add tests for each case: the duplicate offers as in your screenshot, an open conflict copy, an open duplicate of the closed task, no writes to conflict copies, and the id scans.
- Add rule SO33 to bob-cli's `docs/task-dependencies.md` and a sentence to the plugin's docs. Then rebuild, bump the plugin version, and run `bob plugins sync`.

The plan leaves your vault's `_conflicts/` files alone. Until the fix lands, you can make the duplicates go away by resolving that copy: it differs from `sase_blog.md` (for example, the live note has `[*]` and `fresh` fields where the copy doesn't), so diff the two before deleting it.
