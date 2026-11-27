# Chat History - ace-run (bob-cli-qj.5--plan)

- **TIMESTAMP:** 2026-11-27 07:18:18 EST
- **MODEL:** claude/opus
- **AGENT:** bob-cli-qj.5--plan

**Plan:** /home/bryan/.sase/plans/202611/prose_section_extract_inline.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/prose_section_extract_inline.md`

> - **PARENT:** [202611/prose_note_type.md](202611/prose_note_type.md)
> # Plan: Extract prose sections into prose notes and inline them back
> ## Context
> Bryan renamed the `article` note type to `prose` (epic `bob-cli-qj`,
> `plan:202611/prose_note_type.md`) so that a section inside an area, project, or prose
> note can implicitly be a **prose section**, which one keymap turns into a full prose
> note and back. This epic builds that capability. It carries the research report's Phase
> 2 (extract and inline). Phase 3, reversible projects, is out of scope, but the
> provenance designed here is what Phase 3 will read.
> **Required reading for every phase.**

*See full plan file for details.*

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(5, clan=bob-cli-qj, bead=bob-cli-qj.5)
%model:@xlarge
%w(bob-cli-qj.4, for_epic=false)
%w(bead=bob-cli-qj.4)
Can you complete the work for bead bob-cli-qj.5? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-qj.5` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-qj.5` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-qj.5 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-qj.5 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-qj.5 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-qj.5`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-qj.5 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.
Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.


## Response

Reading the bead had no prior notes. Next I'm loading the planning skill and the research report.

Opened the research sidecar; now reading the report through the audited artifact path.

Now reading `docs/prose.md` and the engine layout to anchor the plan in today's code.

Reading the per-researcher extraction specs (cld §4, gem §4.2, cdx) for round-trip rules and refusal lists.

I have what I need. Writing the epic plan file now (contract spec plus 8 phases, 5 embedded decisions).

The plan is staged. Next I'll run the epic-symbols check, then close the phase bead.

I wrote and proposed the child epic plan for bead bob-cli-qj.5, and closed the phase bead. The plan passed validation with no warnings. `sase plan propose` reported it as Staged, so nothing starts until you approve it.

**What the plan builds:** `bob prose extract NOTE (-s SECTION | -l LINE)` and `bob prose inline NOTE`, plus an Obsidian gesture in the Bob Prose plugin.
- **Contract:** the conversion lives in Rust under `src/native/prose/` and returns a new JSON contract, "ProseConversion v1". The existing ArticlePlan contract is not touched.
- **Safety:** both commands preview by default. A write checks every file's contents first, applies all files or none, and makes one vault commit.
- **The stub left behind:** extraction keeps the heading in the source note and puts a single link bullet under it. Inline looks for that stub to know where to fold the note back.
- **Lossless round trip:** extracting a section and then inlining it restores the original bytes, apart from bob-owned section numbers and the blank lines at the edges. A property test checks this. Anything that would be lost is either refused or shown in the preview.
- **Provenance:** extracted notes carry `extracted_from` and `extracted_heading`, which the later reversible-projects work can read.
- **Shipping together:** `extract` stays hidden from help until `inline` lands, so the inverse ships with it.

**The 8 phases, in dependency order:**
1. `txn-trash-recovery`: the shared vault-rewrite transaction gains file trashing (into the vault's `.trash/`), creates that never overwrite, and a saved journal that recovers an interrupted rewrite. Crash tests cover every write point.
2. `section-model`: picks the heading section at the cursor and decides whether it can be extracted. Every ineligible case refuses with a named reason. This runs in parallel with phase 1.
3. `link-relocation`: repairs links to and from the moved section in every direction, for both commands.
4. `extract`: the extract planner, the JSON types, and the hidden command.
5. `inline`: the inline planner and command, both commands unhidden, and the round-trip property tests.
6. `contract-docs`: the contract written into `docs/prose.md`, a host probe for the new commands, and round trips on real sections in a throwaway clone of the vault.
7. `keymap` (bob-plugins): extract, inline, and toggle commands with a preview modal. The modal closes with Esc, `q`, or `Ctrl+[`. Also Command Mode rows, a deploy marker, and a check that the commit actually reached origin before the phase closes (the earlier Bob Prose plugin commit never did).
8. `prose-catalog`: only runs if you accept that decision. Otherwise it closes with no changes.

**Five decisions for you to answer at review time** (defaults first):
- **Keymap:** a new `Ctrl+Shift+E` (unbound today), or reuse `Ctrl+Shift+Alt+N` depending on cursor position.
- **Stub form:** a plain link bullet, or an embed bullet that shows the note in place but repeats its headings.
- **Text above a note's first heading:** refuse and ask you to type a heading first, or extract it under a generated `## Overview` heading.
- **`## Prose` catalog:** off by default. Turning it on also requires fixing project reversal to skip every generated catalog.
- **Prose Section glossary term:** off by default, because memory edits need your approval.

The plan cites the 11 decision records that govern this work.
