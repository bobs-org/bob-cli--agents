# Chat History - ace-run (1f9--plan)

- **TIMESTAMP:** 2026-11-22 17:35:20 EST
- **MODEL:** claude/opus
- **AGENT:** 1f9--plan

**Plan:** /home/bryan/.sase/plans/202611/copy_card_task_links.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/copy_card_task_links.md`

> # Plan: Copy card follows a Task Link to its task
> ## Why
> In Bryan's daily note, the cursor sits on a Pomodoro Task Link such as
> `- [[sase#^commit-failures-show]]`. `Cmd+Y` then shows only the file rows (Path,
> Absolute path, File name, Note name). The `I` Block ID row and his custom `t` template
> (`"the ^{block_id} task in the {path} file"`, key `t`, in `~/.config/bob/config.yml`
> under `copy.templates`) are missing. The card has no "task at the cursor" because
> Pomodoro rows and Task Link bullets are not `#task` lines. This is the documented
> **same-file invariant** in `docs/copy-card.md`: "a `[[other#^id]]` link or Task Link
> under the cursor never supplies the block ID".

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add support to the copy card in Obsidian for task options which
target the corresponding task when a task link is selected in a daily file (like the
custom `t`, for example)? See the ~/tmp/screencasts/20261122_172328.mp4 screencast for
context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

The copy card is in bob-plugins (`bob-navigation-hotkeys`). Right now it deliberately ignores Task Links, so I'm reading its resolver and modal code to plan the change.

I found an existing Task Link parser (`parseLinkPickerTaskLink`, used by Ctrl+Shift+P). Now I'm checking how that feature resolves a link to its target file, so the copy card can reuse it.

I'm reviewing the existing copy card tests. The common path must stay synchronous, because those tests call `openCopyCard()` and check the card immediately.

Existing tests pin today's rule: a Pomodoro Task Link line gets no task group, in both the model test and the real-Obsidian e2e. The plan will reverse those pins. Checking the model test now.

I'm checking whether bob-cli's copy of the Copy card doc is generated from bob-plugins or authored, then I'll write the plan.

I have what I need. The work is all in bob-plugins. bob-cli's copy of the Copy card doc is a gitignored mount, so bob-cli itself won't change. I'm writing the plan now.

The plan passes validation. Submitting it now with `sase plan propose`.

I've written a plan to make the copy card target the linked task when the cursor is on a Task Link, and submitted it for your review. Nothing changes until you approve it.

**Why this happens today.** The copy card in bob-plugins (`bob-navigation-hotkeys`) only shows task rows when the cursor is inside a `#task`. A Pomodoro row and its Task Link bullets aren't `#task` lines, so the card shows only the file rows. This is on purpose: `docs/copy-card.md` says a Task Link under the cursor never supplies the block ID. The plan changes that rule.

**What the plan does:**
- **Which lines:** if the cursor is on a Task Link bullet and no task owns that line, the card uses the linked task. Every line inside a task keeps its current behavior. The line rule is the same one Ctrl+Shift+P uses, so it covers 🍅, struck, embedded, aliased and same-note `[[#^id]]` links, plus links into `done/…_done`.
- **What gets copied:** on a link to `sase#^commit-failures-show`, `I` copies `commit-failures-show`. `t` copies `the ^commit-failures-show task in the ~/bob/sase.md file`. Any template that uses `{block_id}` gets its `{path}`-style variables from the linked task's note. The `P`/`A`/`F`/`N` rows and the subtitle still describe the daily note.
- **Finding the task:** the card reads the linked note in the same order as Ctrl+Shift+P: open editor, then open buffer, then the vault. Done and closed tasks count. If you press `Cmd+Y` again or the note changes while it's reading, the older card is dropped.
- **Broken links:** if the link can't be followed (note missing, ID missing or duplicated, or the target isn't a `#task`), the group is shown dimmed with the reason.
- **Labelling:** the group's divider reads `LINKED TASK`.
- **Unchanged:** the `C` chip row still only looks at the current file. The palette `yank-block-id` command follows Task Links the same way.
- **Tests and docs:** the plan updates the model, view and real-Obsidian tests, which currently assert that a Task Link line shows no task group. It also rewrites `docs/copy-card.md` and ends with `bob plugins sync`.

**Decision for you — which Task Link lines count:**
- **Default:** any Task Link bullet that no task owns, in any note. This only adds the task group where the card shows nothing today.
- **Daily notes only:** only Pomodoro Task Links in daily notes.
- **Every Task Link:** also a Task Link nested under another task, which would then target the link instead of that task.

The plan is in `sase_plan_copy_card_task_links.md`, sized as a medium single-agent job.
