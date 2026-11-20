# Chat History - ace-run (bob-cli-o6.2--plan)

- **TIMESTAMP:** 2026-11-20 12:01:09 EST
- **MODEL:** claude/opus
- **AGENT:** bob-cli-o6.2--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_o6_2__plan-261120_115030.md`
- 2. --code — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_o6_2__code-261120_115030.md`

**Plan:** /home/bryan/.sase/plans/202611/identity_kit.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/identity_kit.md`

> - **PARENT:** [202611/property_card_title_block.md](202611/property_card_title_block.md)
> - **BEAD:** bob-cli-o6.2
> # Identity kit (phase `bob-cli-o6.2`)
> This tale implements phase `identity-kit` of epic `bob-cli-o6`
> (`plan:202611/property_card_title_block.md`). Read that plan's **Design contract** first
> (`sase bead read bob-cli-o6.2 -r "<why>"` prints its path). It is the spec for every
> visual and behavioral rule below. This phase builds only the kit. **No card adopts it
> yet**: the album, record, bank, and intention cards must render pixel-identically before
> and after this change, with one intended exception, the dead `purple` walk-rail rule
> fixed in step 5.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-o6, bead=bob-cli-o6.2)
%model:@large
%auto
Can you complete the work for bead bob-cli-o6.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-o6.2` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-o6.2` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-o6.2 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-o6.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-o6.2 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-o6.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-o6.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
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

I've read the bead and the epic plan; now I'm opening the bob-plugins repo to check its state before planning.

I'm reading the existing property-card kit in bob-plugins (ownership, host, record sheet title-hide CSS) to design the identity-kit plan.

Still surveying: now reading the record walk's reveal-on-touch rule and the intention card's nav-line recognizers, which the new title-ownership range must reuse.

Still exploring (~70% there): checking how the record walk hides its source line in Live Preview and how the intention-card host anchors, so the new title-ownership API fits the later adopters.

Exploration nearly done; checking how existing tests stub CodeMirror's StateField (no real CM6 in node_modules), then I'll write the plan.

Exploration done. Now loading the `/sase_plan` skill to write and propose the implementation plan.

Verifying a couple of facts the recognizers depend on (period scaffold H1 text, day-note H1 shapes) in the bob-cli source, then writing the plan.

Writing the plan now; first a quick check of this phase's epic-symbol entries so the plan covers them.

Now writing the tale plan file.

The plan passes validation. Proposing it now.

I wrote a plan for bead `bob-cli-o6.2` (the identity kit) and proposed it. The proposal is staged, and no code has been written or changed yet. The bead stays in progress. Once the plan is approved, a separate coding agent implements it, deploys the plugin, and closes the bead.

No earlier work on this phase had landed, so the plan starts from scratch. It is a single-agent plan (medium size). The work is all in the `bob-ledger-tools` plugin in the bob-plugins repo, and no card uses the new kit yet:

- **Species registry:** the seven card kinds (album, record, day, week, quarter, year, bank). Each gets its word, tile shape and fallback icon, and an accessible name such as "Album: Restaurants".
- **Builders:** the glyph tile, the title block (kicker word, single heading, pill, subtitle, actions), and the bottom navigation rail with an optional row of child chips. Text only ever goes in as plain text, and any failure returns nothing, so the card falls back to native rendering.
- **Finding the title lines to hide:** a pure function that finds the redundant H1 plus any nav or child-link lines below it. There are matchers for album titles, every daily H1 format, and period titles. An H1 inside a code fence or after prose is never matched.
- **Title ownership:**
  - In Live Preview, those lines are hidden. They reappear for editing as soon as the cursor touches them.
  - In Reading view, only the matching `h1` and `p` elements are hidden, never a section that also holds a card.
  - Embeds, canvas nodes, print, and mobile always keep native rendering, and ownership drops on Source mode, file change, or teardown.
- **CSS:** a new section that applies only to opted-in cards, plus the cyan-based day accent. The broken `purple` rule on the record walk rail is fixed to `violet`.

The plan requires these checks before the bead closes:
- `npm test`, `npm run build:check` and `npm run docs:check` pass.
- Existing album, record, bank and intention cards still render pixel-identically (the `purple` fix is the only allowed difference).
- A new screenshot matrix renders light/dark, 375px/wide, grayscale and forced-colors. It asserts exactly one level-1 heading per card and the contrast targets (4.5:1 for kicker text, 3:1 for the accent stripe).

Two calls I made that the later phases depend on:
- **Cards must be full width to use the kit.** Its narrow-width layout needs this, so the day card will have to drop its current fit-to-content width when it adopts the kit.
- **The new editor hook is opt-in.** Hosts register it only when they pass a new `titleOwnership` option, so the existing cards and their tests are untouched until they choose to use it.

The plan avoids file-name clashes with the title-slot phase (`bob-cli-o6.1`), which is running in parallel, but both edit the same fragment list and test list. The plan covers that: fetch and rebase before starting and before deploying, keep both sides' entries, rebuild `main.js` rather than merging it, and take the next free version number.
