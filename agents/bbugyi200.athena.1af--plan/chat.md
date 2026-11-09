# Chat History - ace-run (1af--plan)

- **TIMESTAMP:** 2026-11-09 10:06:46 EST
- **MODEL:** claude/opus
- **AGENT:** 1af--plan

**Plan:** /home/bryan/.sase/plans/202611/project_note_capture_glossary_term.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/project_note_capture_glossary_term.md`

> # Add the "Project Note Capture" glossary term
> ## Goal
> Add one memory-web strand, `glossary:project-note-capture` (keyword **Project Note
> Capture**, aliases `project capture` and `project-note capture`). It defines the sealed
> capture marker `@<route>^<block-id>@` / `@<route>:<block-id>@` (Bryan's shorthand is
> `@foo[:^]bar@`), which creates a brand-new project note instead of a task. This is a
> memory-only change: no Rust, docs, or plugin edits.
> ## Why this term, and why these names
> - The form is one of capture's largest grammar families: two forms, a Pomodoro suffix,
>   task-ID bullets, move bullets, `- ^^`, offers, and a set of refusals. But no glossary

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add an excellent new "project note capture" (aka "project
capture") glossary term that describes the `@foo[:^]bar@` capture syntax? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.

%m:@xlarge

## Response

Reading the capture docs on project-note creation (`@route^id@` / `@route:id@`) so the glossary strand is grounded in the real grammar.

Still researching: checking the reference syntax doc's "Project captures" section and how glossary closure links work, then I'll write the plan.

Checking Mac Capture's surface for project captures (footer verb, preview, Move card) so the term covers both clients accurately.

I have what I need. Writing the tale plan now: one new glossary strand (`project-note-capture`), the full draft text embedded, with source-verification and regen steps.

Validation passes; the one remaining warning is because the new strand doesn't exist yet, so its selector can't resolve at plan time. Re-reading the final plan before proposing it.

I wrote the plan and submitted it with `sase plan propose`. It passed validation and is staged for your review. I haven't changed any memory files yet; the approved coder will do that.

**Tier and size:** a `small` tale. The whole job is one new glossary entry plus a `sase memory init` regen, so one agent can do it directly.

**The term:** `glossary:project-note-capture`
- **Keyword:** Project Note Capture
- **Aliases:** `project capture` (yours) and `project-note capture`. The second is the spelling the codebase already uses, for example in the error "project-note capture cannot be combined with %c". No existing glossary entry uses either alias, so adding them won't pull this term into any other entry's reads.
- **Roster:** it will appear between Project Note and Project Task.

**What the plan's draft definition covers** (it's included in full, checked against `docs/capture.md`, `docs/reference/capture-syntax.md` and the parser code):
- **What it is:** a capture item whose `@<route>^<id>@` or `@<route>:<id>@` marker ends in a closing `@` (optionally followed by `#<pomodoro>`). It creates a new project note, `<route>_<id>.md`, instead of a task. The item's text becomes the note's `^prj` line, which is never linked. The parent note must exist, and a note that already exists is refused.
- **The two forms:** `^` creates the note and links only the bullets marked ` :<id>`. `:` also offers the note's open tasks as successors, and links only the ones you pick with `-p`.
- **Bullets:** ` :<id>` makes a task Next and links it, ` ^<id>` only names it, and an ALL-CAPS bullet with nested notes becomes a `##` section. A bare `^<id>` or `:<id>` bullet moves an existing task in from the parent note, and `- ^^` lets you pick several. Everything is written together or not at all.
- **Refused:** `%c`, `--clip`, `=`/`=x` suffixes, `!`, `@@`, and the retired `+` forms.
- **What it isn't:** `@route^id`, `@route:id`, `@route+id`, or record-note capture.

The plan gives the coder nine specific claims to check against the docs and code. Where the docs and the draft disagree, the docs win.

**Two decisions for you at approval:**
1. **Add the new entry** (default yes, since you asked for it).
2. **Link to the new term from the Capture entry** (default no). The term already shows in the always-loaded roster, and the link would make every read of the Capture entry longer.

The validator gives one warning: it can't match the plan's decision to the new entry because the entry doesn't exist yet. That should go away once the coder creates it.

**Docs mismatch:** I found an inconsistency but left it out of scope. The syntax reference page says a ` :id` bullet links into "the current/next Pomodoro", while `docs/capture.md` says it goes to the Pomodoro matching the task's type. The plan tells the coder to file a bug for this if they confirm it, rather than fix it in this change.
