# Chat History - ace-run (bob-cli-hg.12.1.4)

- **TIMESTAMP:** 2026-11-06 13:38:14 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-hg.12.1.4

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(4, clan=bob-cli-hg.12.1, bead=bob-cli-hg.12.1.4)
%model:@medium
%w(bob-cli-hg.12.1.3, for_epic=false)
%w(bead=bob-cli-hg.12.1.3)
Can you complete the work for bead bob-cli-hg.12.1.4? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-hg.12.1.4` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-hg.12.1.4` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-hg.12.1.4 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-hg.12.1.4 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-hg.12.1.4 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-hg.12.1.4`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-hg.12.1.4 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. Closed bead `bob-cli-hg.12.1.4`.

Implemented the durable send-recovery engine, kept internal with no public `send` command:

- [state.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/gmail/compose/state.rs): versioned `gmail_send` frontmatter object, file locks, digests, journal helpers.
- [send.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/gmail/compose/send.rs): persist-`sending`, pre-dispatch recheck, draft-id-only dispatch, three-outcome recovery, injectable transport plus 16 fault tests.
- [gog.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/gmail/gog.rs): narrow `drafts send` adapter and receipt decoder.
- [fake_gog.py](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/tests/gmail_support/fake_gog.py): fake `drafts send` and `in:sent` support for the next phase.

Verified: `cargo fmt --check` clean, workspace clippy gate exit 0, `cargo test --lib native::gmail` 226 pass, `gmail_draft` 5 pass, shell/search/peel/pull suites 46 pass. No `--epic-symbol` entries remain.

Declaration accepted. Bead `bob-cli-hg.12.1.4` closed with the durable send-recovery engine commit.
