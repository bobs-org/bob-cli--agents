# Chat History - ace-run (bob-cli-o6.4--plan)

- **TIMESTAMP:** 2026-11-20 13:42:55 EST
- **MODEL:** claude/opus
- **AGENT:** bob-cli-o6.4--plan

**Plan:** /home/bryan/.sase/plans/202611/collection_cards_title_block.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/collection_cards_title_block.md`

> - **PARENT:** [202611/property_card_title_block.md](202611/property_card_title_block.md)
> # Collection cards adopt the title block
> ## Scope and completion
> This child epic completes **bob-cli-o6.4** (`collection-cards`), a phase of the epic
> **bob-cli-o6** ("Property cards become the note title block"). The phase is `large` and
> had no earlier work or notes when this plan was written, so it splits into three phases
> that each fit one coding agent:
> - `album-card` builds the reusable adopter glue (slot mount plus title ownership plus
>   body fallback) with the album card as its first adopter.
> - `record-card` reuses that glue for the record sheet, so it runs after `album-card`.

*See full plan file for details.*

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(4, clan=bob-cli-o6, bead=bob-cli-o6.4)
%model:@large
%w(bob-cli-o6.1,bob-cli-o6.2, for_epic=false)
%w(bead=bob-cli-o6.1)
%w(bead=bob-cli-o6.2)
Can you complete the work for bead bob-cli-o6.4? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-o6.4` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-o6.4` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-o6.4 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-o6.4 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-o6.4 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-o6.4`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-o6.4 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
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

Reading the phase scope and the dependency phases' results; now opening bob-plugins to plan the album/record/bank card adoption.

Exploring the bob-ledger-tools fragments for the album, record, and bank cards, plus the landed kit API, so the plan can follow the code.

Spawning three parallel read-only explorers (album card, record card, bank/editors/previews) while I read the kit host and title-slot primitive myself.

Still mapping the code — checking the plans sidecar for a parallel day-period plan so both phases share kit changes cleanly.

Mapping is done; now checking how a phase-parented child epic is written so its land agent closes bob-cli-o6.4, then drafting the plan.

Nearly ready to write the plan; verifying bob's album title rule so the plugin's local title matches it exactly.

Validation passes. Removing the provenance fields SASE writes itself, then revalidating.

The plan validates cleanly. Proposing it now.

I've planned bob-cli-o6.4 rather than implemented it: I wrote a child-epic plan, it passed validation, and `sase plan propose` staged it. Nothing changes in bob-plugins until the plan is approved. No commit was needed this turn, and I left the bead open.

**Why an epic:** the phase covers three cards and two editors. Both of the main cards have to move into the title slot and take over the note's title, and the existing real-Obsidian e2e scripts have to be updated and run on athena. That is more than one agent can do well, so I split it into three phases:

1. **`album-card` (large).** The album card paints its title immediately from the note's own frontmatter, using the same order bob uses: `title:`, then the H1, alias, and filename. It gets the stack tile and an `ALBUM · <owner>` kicker. The schema folds to one line by default, and the redundant H1 is hidden at render time, with the raw line coming back when the cursor touches it. This phase also builds the shared mount helper: put the card in the title slot, take over the title, and fall back to today's layout when that fails. It updates the album e2e scripts and runs them on athena.
2. **`record-card` (large, after `album-card`).** It reuses that helper. The record card gets the `RECORD · <Album> · <noun>` kicker, the sheet tile, and the paper look, with the walk rail docked inside the card. A walk line on the first body line is hidden at render time and comes back when the cursor touches it. The record-specific CSS that hides the inline title moves onto the shared kit classes. The record e2e now checks the inline title and the hidden Properties rows separately, because the design says the card owns the title even when the rows stay visible.
3. **`bank-and-editors` (medium, runs in parallel).** A small shared badge (tile plus species word) goes on the bank Setup card, the Record Card header, and the album card editor header. The bank card keeps its exact `Bank setup` label, which its e2e checks for.

The land agent re-runs the gates and the card previews, checks the deploy and the e2e reports, and closes only bob-cli-o6.4. It does not close bob-cli-o6 or any of its other phases.

Constraints the plan carries:
- **No memory edits.** The approved glossary updates belong to bob-cli-o6.7.
- **Record-writer harness untouched.** No phase edits `obsidian-record-writer-e2e.cjs`, because bob-cli-ms.8's pending landing tale is still repairing it.
- **Parallel work.** The plan includes merge rules for working alongside bob-cli-o6.5 (day and period cards) in the same plugin.
- **Pixel check.** The card preview script currently fails unless every card's pixels match the old CSS. Each adopting phase replaces that check for its card with structure checks (species word, tile, one level-1 heading).

There were no epic symbols to resolve for this bead.
