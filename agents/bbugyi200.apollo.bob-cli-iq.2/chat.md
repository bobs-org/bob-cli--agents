# Chat History - ace-run (bob-cli-iq.2)

- **TIMESTAMP:** 2026-11-08 10:55:42 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-iq.2

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-iq, bead=bob-cli-iq.2)
%model:@medium
%auto
Can you complete the work for bead bob-cli-iq.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-iq.2` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-iq.2` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-iq.2 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-iq.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-iq.2 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-iq.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-iq.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Bead `bob-cli-iq.2` (pure annotation locator) is done and verified.

What landed in `bob-plugins` (`677a-ref-annotation-locator.js`, wired right after `677-plugin-ref-pdf-open.js` in `fragments.json`):

- `parseRefPageLabel` — `Page N`, `Pages A–B` (en dash/hyphen), `Pages 11, 14`, `p.`/`pp.` forms; first integer wins, non-numeric labels return `page: null`.
- `locateRefAnnotation` — maps a cursor line to its `^h-` block: caption (with `^h-` count), quote/note/image annotation, tombstone, stub (with `stubTarget`), piece-aware pages/rails for continuation groups (ID-line and pre-ID blank resolve to the head page and whole-block rail), section cards/gaps/fences/outside-region all `null`.
- `findRefAnnotationBlockLine`, `parseRefBookmarkLink`, `parseRefArchivePdfLink` per spec.

Verification: 6 golden fixtures under `scripts/fixtures/ref-annotations/`, 14 new tests pass, full `npm test` green (5709 pass, 0 fail), `npm run validate` clean, and `bob-navigation-hotkeys` synced to the vault (forced over a stale bundle from an older uncommitted build; the old bundle was auto-backed-up). No `--epic-symbol` entries remain.
