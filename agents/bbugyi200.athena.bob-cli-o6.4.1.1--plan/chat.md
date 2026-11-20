# Chat History - ace-run (bob-cli-o6.4.1.1--plan)

- **TIMESTAMP:** 2026-11-20 13:58:08 EST
- **MODEL:** claude/opus
- **AGENT:** bob-cli-o6.4.1.1--plan

**Plan:** /home/bryan/.sase/plans/202611/album_card_title_block.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/album_card_title_block.md`

> - **PARENT:**
>   [202611/collection_cards_title_block.md](202611/collection_cards_title_block.md)
> - **BEAD:** bob-cli-o6.4.1.1
> # Album card becomes the title block (phase `album-card`, bead bob-cli-o6.4.1.1)
> ## Context and binding inputs
> This tale implements phase `album-card` of the child epic
> `plan:202611/collection_cards_title_block.md` (bead bob-cli-o6.4.1). That epic's phase
> section "Phase `album-card`" and its "Shared rules for every phase" are binding. The
> outer design contract `plan:202611/property_card_title_block.md` is also binding: "The
> rule", "One skeleton for every card", the Album row of "The species", "States", "Title

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-o6.4.1.1, bead=bob-cli-o6.4.1.1)
%clan(bob-cli-o6.4.1, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@large
%auto
Can you complete the work for bead bob-cli-o6.4.1.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-o6.4.1.1` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-o6.4.1.1` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-o6.4.1.1 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-o6.4.1.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-o6.4.1.1 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-o6.4.1.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-o6.4.1.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
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

I'm gathering context for the album-card phase (size guidance, design contract, kit API notes) before writing the plan.

Read the design contract; now checking the title-slot and identity-kit API notes and sibling phase status.

Now exploring the album card code in bob-ledger-tools.

Reading the kit's ownership and host code; next the title-slot primitive and host dispose paths.

Confirmed hosts are only disposed on plugin unload. Now reading the title-slot primitive.

Next: the title-source rule (`notebookHeaderNoteTitle`), the album recognizer, and other album-title readers.

Mapping the existing tests, e2e probes, previews, and CSS that this phase must update.

Now checking other users of the summary text and the default-expanded rule, plus the record-sheet and kit exports.

Checking the album e2e invocation, docs sections, and host test extension counts.

I have what I need. Writing the tale plan now.

Plan validates. Submitting it.

I've written and submitted the plan for bead bob-cli-o6.4.1.1 (the album-card phase). Nothing is implemented yet: no plugin files were changed, and the plan now goes to review before a coding agent starts.

The plan is a single-agent tale sized `medium`. This phase had no earlier work, and it is one connected change, so it doesn't need splitting into a child epic. The plan has no open decisions for the reviewer, and it edits no memory, as the epic's decisions require.

What the plan covers, all in the bob-ledger-tools plugin:

- **Album title:** the plugin will choose an album's title the way bob does: a valid `title:`, then the first H1 before any `##` or bullet, then the first alias, then the stem cleaned up the way bob does it. The walker-footer tooltip gets the same rule.
- **Card before the report:** the album card paints its title, tile, owner links and summary right away from local note data. When bob's report arrives, the schema section and the `＋ <noun>` / `⊞ Schema` buttons join the same card without it being rebuilt.
- **Reusable mount helper:** a new piece of shared code mounts a card in the title slot and takes over the note's title. The record-card phase will reuse it unchanged. If it can't mount, or loses the slot, the note goes back to normal rendering immediately, and a card that doesn't own the title drops its heading role.
- **Mounting:** in both Live Preview and Reading, the album card sits above Properties and hides the duplicate H1 until the cursor touches it. Embeds, Source mode and mobile keep today's layout.
- **Schema fold:** a healthy schema starts folded to one line: `▸ Schema · N fields · grouped by … · dated notes · <record count>`. Invalid and empty schemas still start expanded with today's text.
- **CSS, tests, previews, docs:**
  - CSS for the new layout.
  - Unit tests for the mount helper, the title rule, painting before the report, and the fold.
  - Album end-to-end checks in real Obsidian, including hiding and revealing the H1.
  - The preview script checks the album card's structure instead of requiring pixel-identical captures.
  - Updates to `docs/albums.md` and `docs/develop/architecture.md`.
- **Wrap-up:** gates, the end-to-end runs on athena with their reports attached, a version bump, and a deploy with `bob plugins sync`.

Two things I checked while planning:

- **Teardown:** the plugin only shuts down card hosts when it unloads. So one card type releasing all title ownership can't strip another card's ownership while Obsidian is running, and that code needs no change.
- **Stem fallback:** bob tidies the stem when an album has no title, H1 or alias, but the plugin used the raw file name. The plan ports bob's version so the card and bob agree.

Two sibling phases are changing the same plugin in parallel (bob-cli-o6.5 for day and period cards, bob-cli-o6.4.1.3 for bank and editors). The plan has the coder merge their work first and reuse any shared helper they've already landed instead of writing a second one.

No commit was needed this turn, and the bead stays in progress until the coding agent finishes.
