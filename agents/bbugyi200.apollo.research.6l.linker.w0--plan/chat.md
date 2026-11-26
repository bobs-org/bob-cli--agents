# Chat History - ace-run (research.6l.linker.w0--plan)

- **TIMESTAMP:** 2026-11-26 14:11:19 EST
- **MODEL:** claude/opus
- **AGENT:** research.6l.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/ref_cards.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/ref_cards.md`

> # Plan: Ref Cards
> ## Why
> Bryan wants a Property Card for reference notes. It should hold as much useful
> information about the reference as possible without clutter. It should support `==` if
> that makes sense, get an excellent glossary term, and ship in parallel with the
> in-progress `bob-cli-qm` epic (Notebook and Prose Cards).
> **Required reading for every phase:** `research:202611/ref_cards/ref_cards.md`. Read it
> with `sase artifact read`; if the research sidecar is not cloned, use
> `sase artifact read file:explicit:4b16f0c00db1c7b9850e7343`. Bryan agreed with every
> requirement it recommends, so this plan adopts its nine recommended defaults:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to implement "ref cards", a new type of property card for ref
notes. Can you help me implement this?

- See how other property cards are implemented and the bob-cli-qm epic bead, which is
  in-progress and implements notebook cards and prose cards, for context and
  inspiration.
- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qm epic.
- Think hard about how this card should look. It should contain as much genuinely useful
  information about the reference as possible without cluttering the card.
- Also, think hard about whether or not ref cards should support the `==` keymap and, if
  so, what kinds of operations the schema editor that is triggered should support.
- As a part of this change, we should add an excellent new glossary term for "ref card".
- Review the ref_cards.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.6l.linker

## Response

I'm gathering context: I've read the bob-cli-qm epic and the related bead, and next I'm finding the ref_cards.md research report.

I've read the research report; now reading the approved qm plan to mirror its structure and coordination gates.

Reading the landed kit code in bob-plugins (species registry, precedence, preview gate) so the plan's seams match reality.

Checking the live `bob ref list` JSON shape (1,378 refs, ~1 s) to pin down exactly what data the card can show.

Now checking how the area/project settings contract is emitted, since the Reference editor will reuse that shape.

Good find: nav-hotkeys already exposes `openReferencePdf` on its v3 API, so no new PDF seam is needed. Checking its existing consumers and the audio path.

Checking where the kit's precedence function and kind lists are consumed, to decide how ref can slot in with minimal overlap with qm's in-flight edits.

Reading the governing decision records and the related glossary strands so the plan cites them accurately.

Now invoking the memory-write skill, since the plan will add a glossary strand and propose edits to existing strands.

Quick status: I've verified the kit code, the `bob ref list` data, and the props roles gap. Now sizing the shared report and checking a few last details before writing the plan.

Context gathering is done; I have the design worked out. Now checking the epic plan schema before writing.

Key finding: Bryan's hosts track bob-cli master (per the release-train decision), so go-live doesn't need to wait for a crates.io release. Checking one last detail (the Today source) before writing.

I have everything I need. Writing the epic plan now: 8 phases, with three starting immediately beside qm.

Validation passed with 0 warnings. Re-running without `--explain` as the skill requires, then proposing.

The proposal is staged. Finishing the turn through `/sase_final`.

I've written the Ref Cards plan as an 8-phase epic and submitted it with `sase plan propose`. It passed validation with 0 warnings and is staged, so nothing starts until you approve it. No files beyond the plan changed this turn.

**Running it beside bob-cli-qm.** Coordination is needed, but only at four points. Merging into qm would hold up 1,378 references behind 39 notebooks; skipping coordination would cause real collisions.
- **Shared card code:** only one ref phase (`ref-kit`) touches it, and only by adding lines. While ref's own on/off switch is off, those additions change nothing for any existing card.
- **The on/off switch:** ref gets its own preview switch and never uses qm's, because qm.7 deletes that one. Without a separate switch, adding a ref card would make it live on the next plugin sync. `ref-kit` also leaves coordination notes on qm.6 and qm.7 so their agents keep ref's code intact.
- **Acceptance testing:** `ref-acceptance` waits for qm.6 to finish.
- **Go-live, docs and the family glossary entry:** `ref-go-live` waits for qm.7 to finish.

Three phases start right away: `ref-props` (the bob-cli changes), `ref-kit`, and `ref-service`.

**How the card looks.** Every element answers one of four questions: what is this, where did it come from, where am I with it, and what useful material is here. A typical finished reference is about four quiet lines:
- a bookmark-shaped "ribbon" tile with the kind's icon and `REF · Blog`, plus the parent's breadcrumbs;
- the reading status (Reading, Next, Snoozed with its date or prerequisite, Read with its date, and so on) plus a Today pill;
- a summary line, then author · site ↗ · publication date;
- annotation counts, plus PDF and Listen buttons.

Anything a note lacks is simply left out, never shown as zero. Data from `bob ref list` only fills lines that are already there, so the card never jumps when it arrives.

**`==` support: yes.** It opens a Reference editor built on the existing Property Editor, not a schema editor. You can edit Title, Summary, Authors, Published, Source and Aliases. Reading status, where it lives, and the file name are shown read-only, and Enter takes you to where each one is actually changed: the reading task, or `bob ref rename`. With an older bob on a host, `==` just focuses the `title` property instead.

**bob-cli side.** `ref-props` fixes the bug in bob-cli-qn: `bob props` stops allowing generic edits to sync, identity and reading-task keys, and the 13 root `*_ref.md` hub notes are no longer treated as references. That commit is marked `!` because some edits that work today will be refused. The phase closes bob-cli-qn.

**Where I departed from the research report:**
- **No wait for a crates.io release.** Per the release-train decision, your hosts run bob from master, and the plugin checks each host for the new capability anyway.
- **Dropped the Topics and Kind rows.** No note in the vault uses `topics:`, and the kind already shows on the card.
- **Authors is one text line.** All 33 existing authors are plain strings.
- **PDF works on every desktop.** It opens in Highlights on the Mac and in Obsidian elsewhere. The report's proposed new PDF hook already exists as nav-hotkeys `api.openReferencePdf`.
- **No legacy chapter counts.** bob doesn't report them, and I didn't want the plugin re-deriving bob's legacy rules.

**Decisions for you:**
- **Glossary entry for "Ref Card":** defaults to yes, because you asked for it. The draft text is in the go-live phase.
- **Adding the Ref Card to the Property Card glossary entry:** defaults to yes, because the entry's list of card types will be wrong once this ships.
- **Retitling leaves the reading task's link text unchanged.** That link text sits in another note, and `bob props` edits only one note at a time. The editor says so plainly and offers a jump to the task. A proper `bob ref retitle` command that updates all of them is follow-up F6; tell me if you'd rather it be part of this epic.
