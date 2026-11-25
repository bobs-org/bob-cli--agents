# Chat History - ace-run (research.65.linker.w0--plan)

- **TIMESTAMP:** 2026-11-24 10:34:02 EST
- **MODEL:** claude/opus
- **AGENT:** research.65.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/meeting_notes_event_refs.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/meeting_notes_event_refs.md`

> # Plan: Meeting notes become event-linked references
> ## Why and what
> Bryan records meetings with Wispr Flow Notetaker and wants the notes filed against the
> meeting as an excellent reference. The reference should sit under the right area or
> project and be properly linked to the Event Task. Today this takes hand work. For the
> first meeting, Bryan hand-built a review chore (`job#^whisperflow-meeting`). It is
> blocked on the bob build task and in turn gates a follow-up task.
> The design follows the consolidated research report `meeting_notes_event_refs.md`
> (research sidecar; read it with `sase artifact read` if you need the rationale). Bryan
> accepted all of its requirements:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I've been using Wispr Flow to automatically transcribe meeting notes. I would
like to integrate AI meeting notes into event tasks by making it as easy as possible for
users to create excellent ref notes for these meetings that are associated with the
correct area/project and are properly linked to the corresponding event task. Can you
help me implement this?

- As our first use-case for this functionality, I would like to create a ref note from
  the ~/tmp/bryan_derrick_meet_notes.txt file (contains a Wispr Flow meeting transcript)
  and link it to the ^bryan-bugyi-derrick task in the ~/bob/2026/20261123.md file.
- Think hard about what the best UX for this functionality is.
- Review the meeting_notes_event_refs.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.65.linker

## Response

I'm reading the research report on meeting-note event refs from the sidecar before I explore the codebase.

Now reading the glossary terms and decision records that govern references, Event Tasks, and relations.

Exploration maps are in. Now I'm verifying a few specifics myself: the print profile precedent, task mentions, ref-type lists in the plugins, and the tool availability on this host.

I'm comparing the two existing PDF renderers (the HTML web-clip adapter that prints podcast dossiers vs. the LaTeX note-snapshot profile) to pick the meeting dossier's renderer.

Checking the Obsidian Reading Board's per-type icon table (a meetings type would need an entry there too).

I have the design shaped. Before writing memory-touching steps into the plan, I'm loading the memory-write skill as required.

Note: the plans sidecar is public, so I'm checking whether the research sidecar (which already names these meeting details) is public too before deciding how much real detail the plan may carry.

I have everything I need. Writing the epic plan now.

Validation passed on the first run. Re-validating without `--explain`, then proposing.

The proposal is staged. Finishing the turn through the final declaration.

I've proposed an 8-phase epic plan for this feature; it's waiting for your approval and nothing has been built or written to the vault yet. It follows the research report and builds its phases 1–2, plus filing the Derrick notes as the first use case.

**The design.** Every surface ends in one new command, `bob ref meet`, so filing behaves the same everywhere.
- **Mac Capture:** copy the notes in Wispr, open Capture, press the Meeting Notes key, then Return. That's 3 keys. The sheet picks the meeting from the clipboard notes, previews the outline and where it will be filed, then files it. Ended meetings in the agenda also get a **Notes** button.
- **Obsidian:** with the cursor on the event row, `:` offers "File meeting notes from clipboard". Shift+Enter previews, Ctrl+Enter files.
- **CLI:** `bob ref meet -c`, `-i FILE`, or `-i -` for stdin. Bare `bob ref meet` lists recent meetings and which ones still need notes.
- **What one filing writes:**
  - A `ref/meetings/` note with a searchable recap section that bob owns. If you edit it, bob never overwrites it.
  - A dossier PDF: one or two pages with a title card, TL;DR box and next-steps table, and no table of contents.
  - A reading task born Next in the event's root note, with a `notes from` link to the event.
  - All of this lands in one vault commit. The event row itself is never edited, and its back-link appears on the next reconcile.
- **Reliability:**
  - Your notes are restructured but no word is changed, and a test checks this.
  - It only picks a meeting automatically when exactly one matches strongly; otherwise it asks.
  - A filing that has to wait in the queue still gets the link and recap when `bob ref scan` picks it up later.
  - One set of notes per Google event; filing again needs `-O` to replace.

**Phases.** The normalizer and the meeting lookup start in parallel. The PDF layout and the link-and-recap step follow, then the command itself. After that, three phases run in parallel: filing your Derrick notes, Obsidian, and Mac.

The first-use phase depends only on the CLI, so it doesn't wait on the Obsidian or Mac work. It runs the new build against `~/bob`, because the daily release may not have shipped yet.

**Not in this plan.** These are recorded as follow-ups rather than built:
- Reading Wispr's local database directly (undocumented, and nothing to test it against).
- A dedicated parser for Wispr's "Copy as Markdown". A real paste from you would let me build it from fact; until then, pasted Markdown is handled generically.
- AI enrichment.

**Decisions to answer when you approve:**
1. **Review chain** (default: rehang). The `job#^whisperflow-meeting` chore is closed as superseded by the new reading task. The task it was blocking then waits on that reading task instead.
2. **Recap scope** (default: full). Obsidian search can't see inside PDFs, and the notes are only about 3 KB.
3–4. **Memory notes** (both off unless you turn them on): a decision record and a glossary term.

**Privacy:** bob-cli, bob-plugins, bob-mac-capture, the plans sidecar and the research sidecar are all public GitHub repos. The plan therefore requires invented test fixtures and keeps the meeting's content out of the plan text. The research report already published there does contain the meeting's details, including company and interview specifics, so you may want to look at that.
