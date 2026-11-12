# Chat History - ace-run (dk--plan)

- **TIMESTAMP:** 2026-11-12 09:44:23 EST
- **MODEL:** claude/claude-fable-5
- **AGENT:** dk--plan

**Plan:** /home/bryan/.sase/plans/202611/gmail_task_open_keymap.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/gmail_task_open_keymap.md`

> # Cmd+Enter Opens A Gmail Task's Email
> ## Goal
> Pressing `<cmd+enter>` (vim normal mode) with the cursor on a **Gmail Task** row opens
> the linked thread in the default web browser. Ship with it: a new `glossary:gmail-task`
> term, and a quiet, truthful availability affordance — a muted `⌘↵ Gmail` chip that
> appears exactly where the keymap will act.
> Three design principles, in order:
> 1. **Intuitive** — the gesture is "Enter the email": Cmd+Enter anywhere on the row, no
>    need to park the cursor inside the `[[mail/…]]` span. The chip teaches the keymap in
>    place; nothing new to memorize.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add support for the `<cmd+enter>` keymap for "gmail tasks"?

- When this keymap is used in this context, we should open the corresponding email in
  the user's web browser.
- As a part of this change, we should add an excellent new "gmail task" glossary term.
- We should make sure that it is clear when this keymap is available for this
  functionality somehow.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:claude-fable-5

## Response

I'll design this feature. First, let me gather context: what "gmail tasks" are in this codebase, where keymaps live, and the existing glossary conventions.

Those newly-surfaced MCP tools aren't relevant here — this is a bob-cli design task. Let me read the Gmail-related docs to understand what a "gmail task" is.

The glossary conventions are clear. Now let me find where plugin keymaps are documented and how the mail note frontmatter identifies the thread (needed to build the browser URL).

There's a `bob-mail` plugin that already opens external URLs. Let me inspect it — it may be the natural home for this keymap.

I have the full design grounded. Before authoring the plan (which will include creating the `glossary:gmail-task` memory strand), I must route the memory change through `/sase_memory_write`.

Memory route is clear: the plan carries a memory decision defaulting to true, quoting the user's request. Now let me load the plan skill.

Vim-mapping test precedent confirmed. Let me check the exact strand file format before drafting the plan.

I now have everything needed. Writing the plan file.

Fixing the frontmatter per the schema: add `title`/`goal`, shorten labels, underscore choice keys, and convert the memory decision to a `memory:` toggle.

Validation passed with zero warnings. Submitting the plan.

The plan is staged. Finishing the turn through `/sase_final`.

The plan is staged and no final declaration is required (`submission_required: false`), so the turn is complete.

## Summary

I designed the feature, authored a validated **tale plan (size: medium)**, and submitted it with `sase plan propose` — it's now staged for your review with **3 plan decisions** (2 design choices + 1 memory decision). No implementation files were touched.

**The design** (`sase_plan_gmail_task_open_keymap.md`):

- **The keymap** lives in the **bob-mail** plugin as vim normal-mode mappings `<M-CR>`/`<M-Enter>` (I verified in the replit/codemirror-vim source that `metaKey` translates to the `M-` prefix, and that `<M-CR>` is unmapped today — Ctrl+Enter's close gesture and the Task Card's modal-scoped Cmd+Enter alias are untouched). It reuses bob-mail's existing `mailOpenGmail` → `openExternal(gmail_url)` path, but widens the context so the cursor can be **anywhere on the row**: first mail wikilink on the line, a gmail task's direct link-only child-bullet hop (mirroring the watch wire in `docs/gmail.md#watch`), or anywhere inside a mail note. Read-only: it never writes, stamps freshness, or advances the `]s` walk.
- **Availability is made visible** by a new display-only mark in the mail-link-marks family (bob-ledger-tools): a muted `⌘↵ Gmail` capsule at the end of the **cursor's row**, shown only when one predicate proves the press will succeed (resolving mail note, valid `gmail_url`, bob-mail enabled with the keymap actually registered, marks toggle on). The chip shows iff the keymap is live — and since `]s` landings move the cursor, morning review reveals it exactly when it matters. It gets its own contract section and conformance vectors in `docs/mail-link-marks.md`.
- **The glossary term** `glossary:gmail-task` ("Gmail Task") is drafted in full in the plan: a task wired to a saved mail thread by the link on its own line or a direct link-only child, with its watch/hold lifecycle, display signals, the new keymap, and crisp "not this" boundaries. I routed it through `/sase_memory_write` — it rides the plan's memory decision (default yes, quoting your request), and `just docs-gen` flows it into the generated docs glossary.

**Decisions awaiting you in the approval gate**: chip on cursor-row only vs. every qualifying row (default: cursor-row), and whether Cmd+Enter works on any mail-linked line vs. task rows only (default: any line — one uniform predicate). The approval gate will launch the coder; nothing runs until you review.
