# Chat History - ace-run (17i--plan)

- **TIMESTAMP:** 2026-11-03 12:45:19 EST
- **MODEL:** claude/opus
- **AGENT:** 17i--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_clip_existing_task_notes.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_clip_existing_task_notes.md`

> # Clipboard notes under an existing task: `@route+id %c`
> ## Problem
> In Bob Mac Capture, Bryan typed `@sase+restart-failed-athena %c` to paste the clipboard
> as notes under the existing `^restart-failed-athena` task in `sase.md`. Both the preview
> and Capture failed with:
> ```text
> capture item 1 starting on line 1: task text is required; pass TEXT or pipe it on stdin
> ```
> Reproduced against a scratch vault (`cash.md` with task `^goog-exit`):
> | Draft                                  | Today                                                                            |

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add support for using the `%c` capture syntax with an existing
note? See the ~/tmp/screenshots/20261103_123156.png screenshot for context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Still exploring: I'm reading the capture docs on how `%c` and existing-task `@note+id` routes interact.

Found it: a bare `@route+id` counts as an Ensure Next toggle only when nothing else is on the line. Adding `%c` makes the parser expect note text and fail. I'm now tracing that parse branch.

Planning the design next: `@route+id %c` should file the clipboard lines as direct notes under the existing task. First I'm checking what `capture-parse`, which the Mac app relies on, reports today.

Still planning. Completion already offers `%c` after `@route+id`, so no menu change is needed. Before writing the plan, I'm reading the project's docs and CLI-help rules.

I have enough to write the plan. One open question is whether it should also add a decision record to the `decisions` memory web, so I'm loading the memory-write rules first.

Not a duplicate. Creating the bug bead now.

Bead `bob-cli-gk` is filed and marked ready. One more check before writing: how the ownership resolver treats `%c` as a "creation modifier", which matters for the relationship decision.

I have what I need. Writing the plan now.

Validation flagged a missing title and goal, over-long decision strings, and the wrong shape for the memory decision. Fixing the frontmatter.

Now I'll add a body callout for the memory decision, then revalidate.

Validation passes with 0 warnings. A quick look at the frontmatter-to-body boundary before proposing:

Proposing the plan.

I've written and proposed the plan. It passed validation and is staged for your review; I made no code changes.

**Why it fails.** For `@route+id` with nothing else on the line, the parser picks one of two meanings. Alone, it means "make this task Next" (Ensure Next). With bullets under it, each bullet becomes its own note. When the line's only extra is `%c`, it fits neither case and falls into the "task text is required" error. The check is in `resolve_sub_bullet_kind` in `src/native/capture_language/item.rs`. `bob capture-parse` already accepts `@cash+goog-exit %c`, so only the capture and its preview refuse it. I reproduced this in a scratch vault, including `%c` at the start of the line, `@route+id#drawer %c`, `#fix %c`, and `--clip`.

**What the plan does:**
- **Clipboard notes:** `@sase+restart-failed-athena %c` puts the clipboard lines directly under the task, with no wrapper bullet. They go in clipboard order, before any Schedule, Work or Rotten Log. Each kind of clipboard content (plain text, lists, file paths, long snippets) is handled as it is today, and `%c3` flattens all three clips in order.
- **Drawers:** `@route+id#drawer %c` puts the lines inside that drawer and creates it if it's missing. On a project's `^prj` task it targets a `##` section.
- **Type marker:** `#fix %c` retypes the task in the same capture. The task is never made Next or otherwise changed, and the daily note is untouched.
- **`--clip`:** `bob capture --clip '@route+id'` now does the same as `%c`. The explicit `@route+id!` toggle still refuses it.
- **`s:2` and `$2`:** with `%c` and no note text, these now refuse with the existing "decorates a single note" message instead of "task text is required".
- **Previews:** a dry run previews the exact lines. A dry run with `--no-clip` writes nothing. Batches stay all-or-nothing.
- **Editor:** the editor stops showing a "needs drawer text" hint for the drawer form and a "`#fix` needs a task" error for `#fix %c`. That same fix also clears a false `#fix` error on the existing bullets form.
- **Docs and tests:** `docs/capture.md`, the syntax reference, the JSON reference and the `bob capture --help` text get updated, with CLI tests that check the exact note contents.
- **Bob Mac Capture:** I expect no app change. Once a bob release includes this, the panel should work as you typed it.

**Decisions for you at approval:**
1. **Relationships:** should `@route+id %c &dep` (also `*` or `~`) be allowed? The default keeps today's refusal, whose message still shows the working spelling (`Note @route+id &dep %c`). Allowing it touches the relationship check in several places.
2. **Memory record:** should the coder add a `decisions:` memory entry for this capture shape? The default is off, because no memory note becomes false.

**Also filed:** bead `bob-cli-gk`. The editor never shows the "decorates a single note" error that the capture raises for the bullets form (for example `@route+id s:2` plus `- a`). That's a separate gap, so it isn't in this plan.

The epic `bob-cli-gj` (pulling a note's ready tasks with a lone `@route`) is in progress and edits the same grammar code and `docs/capture.md`, so the plan tells the coder to rebase first.
