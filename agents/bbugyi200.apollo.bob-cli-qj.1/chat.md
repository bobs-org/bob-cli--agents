# Chat History - ace-run (bob-cli-qj.1)

- **TIMESTAMP:** 2026-11-26 12:15:44 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-qj.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-qj.1, bead=bob-cli-qj.1)
%clan(bob-cli-qj, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@small
%auto
Can you complete the work for bead bob-cli-qj.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-qj.1` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-qj.1` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-qj.1 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-qj.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-qj.1 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-qj.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-qj.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Bead `bob-cli-qj.1` done — engine rename complete and verified.

- Moved `src/native/articles/` to `src/native/prose/` and renamed every Rust identifier to prose names (`ProsePlan`, `ProseContext`, `Kind::ProseNote`, `NativeCommand::Prose`, `frontmatter_is_prose`, etc.), plus `tests/cli/articles.rs` to `prose.rs`.
- Kept the wire frozen: `COMMAND_NAME`, all user strings, refusal codes, catalog rows, nightly step name, and the serialized `summary.articles` field are byte-identical (one near-miss caught by the JSON schema test and reverted).
- Verified: fmt/clippy clean, 39 prose lib tests and 28 CLI tests pass, `just docs-gen` leaves generated docs untouched. The 34 lib + 39 CLI failures elsewhere reproduce identically on the clean base, recorded as follow-up.
- Committed as `refactor(prose): rename the article engine module to prose`, bead closed, final declaration accepted.
