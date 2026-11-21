# Chat History - ace-run (bob-cli-om.8)

- **TIMESTAMP:** 2026-11-21 12:21:54 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-om.8

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(8, clan=bob-cli-om, bead=bob-cli-om.8)
%model:@small
%w(bob-cli-om.1, for_epic=false)
%w(bead=bob-cli-om.1)
Can you complete the work for bead bob-cli-om.8? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-om.8` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-om.8` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-om.8 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-om.8 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-om.8 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-om.8`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-om.8 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. Bead `bob-cli-om.8` is closed.

- Added `-L/--links-only` and `-S/--source-note PATH` to `bob capture-complete` ([cli.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/src/native/capture_complete/cli.rs), flag guard). `-S` requires `-L` via clap; help lists both alphabetically with examples.
- Links-only engine path ([engine.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/src/native/capture_complete/engine.rs)): only note/heading/block fields complete; everything else is an empty success. Capture grammar never runs, Work Log block suppression is skipped, and same-note `[[#…`/`[[#^…` without `-S` returns empty. Wikilink result construction was extracted and shared with the normal path, so the JSON shape is unchanged (schema 1, grammar 28).
- New tests in [complete_links_only.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/tests/cli/capture/complete_links_only.rs) (5 tests: trailing-prose replacement `{7,9}`, grammar-literal drafts, same-note with/without `-S`, suppression exemption, `-S`-without-`-L` exit 2), plus the help-order update and a `Kind::VaultNote` shell-completion entry for `--source-note`.
- Docs: `docs/capture.md` section and usage line updated, `just docs-gen` regenerated the golden CLI reference.

Verification observed: `cargo fmt` clean, `just lint` green, full `cargo test --workspace --no-fail-fast` exit 0. The one `just docs-check` failure (plugin-apis/vault-format word budgets) reproduces identically on the clean base and is already tracked by beads bob-cli-ob/bob-cli-oc, recorded as a follow-up note.

Declaration accepted. Bead `bob-cli-om.8` work (capture-complete `-L/--links-only` and `-S/--source-note`) declared for commit with `bead_action: close`.
