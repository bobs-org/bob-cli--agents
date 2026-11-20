# Chat History - ace-run (bob-cli-o6.3--plan)

- **TIMESTAMP:** 2026-11-20 12:00:41 EST
- **MODEL:** claude/opus
- **AGENT:** bob-cli-o6.3--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_o6_3__plan-261120_115031.md`
- 2. --code — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_o6_3__code-261120_115031.md`

**Plan:** /home/bryan/.sase/plans/202611/album_title_cli.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/album_title_cli.md`

> - **PARENT:** [202611/property_card_title_block.md](202611/property_card_title_block.md)
> - **BEAD:** bob-cli-o6.3
> # Album `title:` key, H1-less album create, and `bob albums tidy`
> Phase `album-title-cli` (bead `bob-cli-o6.3`) of epic `bob-cli-o6`
> (`plan:202611/property_card_title_block.md`). bob-cli only. This phase does not apply
> tidy to the live vault. Release policy: never edit the `Cargo.toml` version or
> `CHANGELOG.md` (`decisions:bob-cli-releases-ride-a-daily-train`). Read
> `sase memory read cli_rules.md docs.md -r "<why>"` before touching CLI help or docs.
> Make no memory edits: the epic authorizes memory edits only in its `glossary` phase, and
> no album glossary strand states a title rule.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli
%id(3, clan=bob-cli-o6, bead=bob-cli-o6.3)
%model:@large
%auto
Can you complete the work for bead bob-cli-o6.3? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-o6.3` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-o6.3` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-o6.3 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-o6.3 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-o6.3 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-o6.3`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-o6.3 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
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

No earlier work landed for this phase, so I'm starting fresh: loading the planning skill, then surveying the album/record code.

Read the `bob records tidy` precedent; now reading the H1-strip helper and the album title readers.

Mapping every reader that titles albums (capture, note catalog, walk lines, catalogs) before writing the plan.

Single choke point found: every album title reader flows through `parse_album_declaration`. Now reading album create and update code.

Tidy needs to insert a `title:` key into existing frontmatter byte-safely; checking for an existing YAML span helper to reuse.

Readers and the YAML span helper are mapped. Next: where `bob records tidy` is registered (catalog, completion, runner) so the plan names every spot.

Registration sites are clear. Checking the docs pages and the e2e/integration test layout for album fixtures.

Survey nearly done; checking the existing albums sync test harness and help tests so the plan's test list is concrete.

Survey is complete. One quick read-only check of the live vault: do any albums already carry a `title:` key? That would change what readers show once `title:` wins.

No live album has `title:` yet (6 albums, all with simple H1s), so the reader change alone causes no churn. Checking the docs-reference gates that a new JSON command must satisfy.

Budgets understood (reference pages cap at 6000 words; json-outputs.md is at ~5943). Checking whether `records tidy` has a json-outputs row to mirror.

Precedent found: `bob periods migrate` is dry-run by default with `-a/--apply`. Reading its arg shape so albums tidy matches.

Command Mode precedent: one-time migrations are excluded ("One-time migration; run it from a terminal"). Checking how `bob albums update` resolves its STEM so tidy can share the refusal.

Survey complete. Before writing the plan, checking whether the Album Note glossary strand states a title rule this phase would make false (memory edits here are restricted).

I have what I need. No memory note is falsified, so no memory decision is required. Writing the tale plan now.

The plan passes validation. Submitting it.

I've written and submitted the implementation plan for `bob-cli-o6.3`. Nothing in the repo has changed yet: the plan is waiting for your approval, and a coder agent will implement it after that. The bead stays in progress until then. There was no earlier work on this phase, and the plan passed validation.

**What I found:**
- **One place to change for readers.** Every place bob shows an album's title gets it from `parse_album_declaration` in `src/native/albums/mod.rs`. That covers the albums report, the `[!albums]` catalog rows, the `↑ <Album title>` walk lines, record pages, capture, and `bob records show`. Changing that one function to prefer frontmatter `title:` covers them all.
- **Live vault.** I checked it read-only. Its 6 albums (`eat`, `movies`, `podcasts`, `sase_blog_zettel`, `subscriptions`, `tv`) have no `title:` key yet, and each has one plain H1. So the reader change alone changes nothing live until tidy runs.

**What the plan says:**
- **Readers:** a frontmatter `title:` that is one nonblank line wins. Otherwise the title comes from the H1, then the first alias, then the file name, as today. `bob albums check` warns when a `title:` exists but isn't usable.
- **Create:** `bob albums create` writes `title:` right after `type:` and no H1.
- **`bob albums tidy [STEM]`:**
  - It previews by default and only writes with `-a/--apply`, like `bob periods migrate`.
  - It fills in `title:` with exactly the title bob shows today, so walk lines, record indexes, and owner catalogs don't change.
  - It removes the H1 only when that heading is the first thing in the note and matches `title:` exactly. Otherwise it keeps the H1 and says why: it differs, it comes after other text, it is inside a code block, or it is a later H1.
  - An apply makes one commit, `albums: tidy (N notes)`. It is not added to `bob nightly`, and Obsidian's command sheet leaves it out, like other one-time migrations.
- **Registration:** the command is added everywhere the last two landings missed: the command list, completion, `bob albums --help`, and the command-sheet exclusion.
- **Key test:** run `bob albums sync`, then `bob albums tidy -a`, then `bob albums sync` again. The second sync must change nothing, and record files and both generated lists must be byte-identical.
- **Docs:** updates to `docs/records.md`, the album notes section of `vault-format.md`, one row in `json-outputs.md`, and regenerated CLI docs via `just docs-gen`.
- **Wrap-up:** the coder runs the gates, then `just install` on athena, then a preview-only `bob albums tidy -f json` on the live vault as evidence, and never `-a`. It then closes only this bead.

**Before anyone applies tidy for real:** an older bob still takes the album title from the H1. If an older bob runs `bob albums sync` after tidy removes the H1s, it will rename every walk line and catalog row to the file name ("Eat" instead of "Restaurants"). Every machine that runs album sync needs the new bob first. That check is already part of the epic's final proof phase. Albums created with the new bob before every machine updates carry the same small risk, and the plan has the coder note it for follow-up.
