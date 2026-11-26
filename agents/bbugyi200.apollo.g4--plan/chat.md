# Chat History - ace-run (g4--plan)

- **TIMESTAMP:** 2026-11-26 11:30:11 EST
- **MODEL:** claude/opus
- **AGENT:** g4--plan

**Plan:** /home/bryan/.sase/plans/202611/link_with_note_bullets.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/link_with_note_bullets.md`

> # Link an existing task and file its note bullets in one `@route:id` capture
> Bob task: `^sub-bullet-and-today` in `~/bob/bob.md` ("Add support for `@foo:bar` syntax
> with sub-bullet!").
> ## Problem
> Bryan typed this into Bob Mac Capture:
> ```text
> @bob:h2s-to-area-prj-card
> - foo
> ```
> He wanted one gesture that does two things: link the existing task into today's Pomodoro

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me implement the work associated with the ^sub-bullet-and-today
task in the ~/bob/bob.md file? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Let me look at the images.

I'm still in the read-only exploration phase. Next I'm checking the shared helpers for drawer bullets and reqs, plus the editor (`capture-parse`) side, since both are gated by capture kind.

Execution side is mapped. I'm now checking how the `@route:id=x` close form and the Mac client treat child bullets, which decides the plan's scope.

Checking the Mac capture client now. It has a dedicated single-`pomodoro_link` presentation, and I want to confirm whether that view would hide the new note bullets.

Mac only enforces a minimum grammar revision, so bumping it is safe. Last area to check is the editor (`capture-parse`): how it treats drawer and requirement bullets under a note-less `@route+id`.

Exploration is done. I'm writing the plan file now, then I'll run validation.

Validation passed. I'm checking the edited memory section once more, then running a final validation before proposing.

I've written and proposed a plan for `^sub-bullet-and-today`; it's waiting for your approval in the plan gate. No code has changed yet.

**What's wrong today:** capture rejects `@bob:h2s-to-area-prj-card` followed by `- foo` ("Pomodoro link capture cannot be combined with authored child bullets"). That rejection happens in three places: the capture parser, the live-preview parser (`capture-parse`), and the step that writes to the vault. A same-line note can't stand in for child bullets: `text @route:id` already means "create a new task".

**What the plan does** (a `tale`, size `medium`, bob-cli only):
- **One item, one transaction:** a link with nothing else on its line, followed by bullets, links the task exactly as the bare link does. It then files the bullets exactly as `@route+id` with those bullets does today. Each bullet becomes a note, `- **Drawer**` and `- #drawer` go into drawers, and `- [ ]` becomes a requirement.
- **Forms covered:** `@route:id` and `^route:id`, named links (`#name`), start forms (`=`, `=<X>`), and a `#type` retype on the same line.
- **Order:** the link runs first, then the notes are written after it. Any refusal rolls back the whole batch.
- **Shared code:** the note-filing loop from the existing `@route+id` multi-note path gets pulled into a helper that both paths call, so the bullet rules exist in one place.
- **Still refused, with today's messages:** `%c`, `s:N`, `$N`, forced flags, snooze (`z:`) with bullets, and `&`/`*`/`~` with bullets.
- **Grammar and output:** the grammar revision goes from 33 to 34. The JSON result stays `pomodoro_link` and gains the existing optional `notes` and `drawers` fields, so a plain link's output doesn't change.
- **Mac app:** no change needed. Its preview already shows inserted bullets, and it only requires a minimum grammar revision.
- **Also included:** updates to `docs/capture.md`, plus CLI, parse and completion tests (14 capture scenarios plus a parity check between preview and capture).

**Three choices for you at approval, with my defaults:**
1. **`guarded_notes` = land.** If the link guard leaves a Project-blocked task unlinked, the notes still land and the output says "not linked".
2. **`close_notes` = refuse.** `@route:id=x…` with bullets stays refused, because under a plain `x` close, child bullets are Work Log entries.
3. **`memory_link_notes_record` = on.** This adds a decision record, `existing-task-links-carry-notes`, and marks `capture-bullets-mirror-the-task-block` as superseded in part. That record's list of positions where bullets become notes would otherwise be out of date.
