# Chat History - ace-run (bob-cli-ph.9--1)

- **TIMESTAMP:** 2026-11-25 20:52:20 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-ph.9--1

## Prompt

%macros_enabled:false
# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first projections of exact continuation nodes; any historical source without recoverable node provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `2`
- **Shared ancestry reused:** `1` attributed node(s)

## Continuation Block `block:v1:a53b907644d43998674bc202d090a031`

- **Node:** `agent-delta:20261125060504:9dd439856e0c3c2d`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:** `local:continuation/records/agent_delta/agent-delta:20261125060504:9dd439856e0c3c2d.json`
- **Checkpoint:** `local:continuation/checkpoints/gate_handoff-de49bcbf0d4c3243.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update supersedes it.

%auto
#gh:gh_bobs-org__bob-cli
%id(9, clan=bob-cli-ph, bead=bob-cli-ph.9)
%model:@small
%w(bob-cli-ph.5,bob-cli-ph.6,bob-cli-ph.7, for_epic=false)
%w(bead=bob-cli-ph.5)
%w(bead=bob-cli-ph.6)
%w(bead=bob-cli-ph.7)
Can you complete the work for bead bob-cli-ph.9? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-ph.9` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-ph.9` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-ph.9 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-ph.9 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-ph.9 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-ph.9`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-ph.9 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

### Checkpoint

- **Kind:** `gate_handoff`

### Assistant

<!--sase:budget-span:open:kind=checkpoint;id=1;checkpoint_ref=local%3Acontinuation%2Fcheckpoints%2Fgate_handoff-de49bcbf0d4c3243.json;covered=agent-delta%3A20261125060504%3A9dd439856e0c3c2d-->
Migration prep for `bob-cli-ph.9` is done and the decision is now with Bryan — no declaration required (clean tree, submission not required), so ending the turn here.

**What this turn completed (phase steps 0–3):**

- **Writer gate passes behaviorally on all hosts.** Installed `bob` on athena, apollo, and mac each write `- **Books to Read**` (verified with throwaway-vault dry-runs; the real vault untouched), all pass the `bold-drawer-read` probe, and all deployed plugin bundles carry the dual-read and bold-writes markers. No release tag contains the writer commits yet, so the probe/behavioral evidence stands in for the release check, recorded on the bead.
- **Inventory:** 10 legacy drawers (NOTES ×6 in 5 notes, NOTES: ×1, OPTIONS: ×1, MOTIVATION ×1, DONE ×1), 0 duplicate identities, plus 2 keeps (empty bold drawer in archived `done/sase_done.md`, `**Note:**` lead which is a note by the colon rule). Census difference explained on the bead note (plan said ~7; bob-cli-on filing added NOTES lines).
- **Dry-runs all clean, 0 merges:** `NOTES→Notes`, `NOTES:→Notes`, `OPTIONS:→Options`, `MOTIVATION→Motivation`. DONE proposed for release (no bytes written).
- **Staged gate** `custom-c6e923fd-8268-40d2-a180-917022869008` (staged id `76fafa6f…`): `(rename_notes AND rename_notes_colon AND rename_options AND rename_motivation AND release_done) OR reject`, each rename executing one verified `bob task rename-drawer OLD NEW -a` commit; reject path ends with no follow-up. The gate-turn successor verifies (re-inventory, dry-run no-ops, artifact record for `bob-cli-ph.10`) and closes `bob-cli-ph.9` only if everything is renamed or released.

**Intentionally not done:** the vault apply itself (needs Bryan's per-line confirmation — the plan forbids automated recasing), bead close, and `epic-symbols` closeout — all belong to the gate successor. The bead stays `in_progress` with the prep and staged gate recorded in its notes.
<!--sase:budget-span:close:1-->

## Continuation Block `block:v1:25b2e6bcfb615a51d8de03fc41247dea`

- **Node:** `legacy-boundary:20261125191239:69cea6a20e711b0c`
- **Kind:** `legacy_boundary`
- **Parents:** `agent-delta:20261125060504:9dd439856e0c3c2d`
- **Content:** `compat:legacy-boundary:69cea6a20e711b0c`

### Opaque Legacy Boundary

This source lacks recoverable continuation node provenance, so replay does not guess transcript turns from Markdown headings.

- **Source:** agent session `bob-cli-ph.9` member `bob-cli-ph.9--gate`
- **Reason:** source lacks a recoverable continuation node
- **Transcript:** `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_ph_9__gate-20261125191239.md`

### Protected Legacy Content

**Protected.** This opaque snapshot is included within budget and is not reconstructed into guessed local turns.

````text
# Chat History - ace-run (bob-cli-ph.9--gate)

- **TIMESTAMP:** 2026-11-25 20:40:30 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-ph.9--gate

## Prompt

sase gate answer --id custom-c6e923fd-8268-40d2-a180-917022869008 --kind custom

## Response

# Apply drawer migration: 4 renames, release DONE

Gate state: answered
Reason: gate answered
Selected options: rename_notes, rename_notes_colon, rename_options, rename_motivation, release_done

Branches:

- [x] Rename 6 NOTES drawers to Notes + Rename NOTES: drawer to Notes + Rename OPTIONS: drawer to Options + Rename MOTIVATION drawer to Motivation + Release DONE line (leave in place) (rename_notes+rename_notes_colon+rename_options+rename_motivation+release_done)
- [ ] Do not migrate yet (reject)

Option results:

[
  {
    "id": "rename_notes",
    "result": {
      "changes": [
        {
          "archive": false,
          "drawers": [
            {
              "block_id": "ranked-task-links",
              "from": [
                "NOTES"
              ],
              "line": 127,
              "merged": 0,
              "status": "open",
              "task": "Rank each task link with a number starting at 1!"
            },
            {
              "block_id": "foo",
              "from": [
                "NOTES"
              ],
              "line": 618,
              "merged": 0,
              "status": "closed",
              "task": "foo"
            }
          ],
          "links": [],
          "path": "bob.md",
          "sections": []
        },
        {
          "archive": true,
          "drawers": [
            {
              "block_id": "better-refs",
              "from": [
                "NOTES"
              ],
              "line": 377,
              "merged": 0,
              "status": "closed",
              "task": "Better `^ref` task tracking!"
            }
          ],
          "links": [],
          "path": "done/bob_done.md",
          "sections": []
        },
        {
          "archive": true,
          "drawers": [
            {
              "block_id": "final",
              "from": [
                "NOTES"
              ],
              "line": 614,
              "merged": 0,
              "status": "closed",
              "task": "Improve and generalize sase's finalizer!"
            }
          ],
          "links": [],
          "path": "done/sase_done.md",
          "sections": []
        },
        {
          "archive": false,
          "drawers": [
            {
              "block_id": "artifact-create",
              "from": [
                "NOTES"
              ],
              "line": 60,
              "merged": 0,
              "status": "open",
              "task": "Improve `sase artifact create` command!"
            }
          ],
          "links": [],
          "path": "sase_art_links.md",
          "sections": []
        },
        {
          "archive": false,
          "drawers": [
            {
              "block_id": "at-least-one-rec-in-sect",
              "from": [
                "NOTES"
              ],
              "line": 58,
              "merged": 0,
              "status": "closed",
              "task": "Add at least one record to every [[sase_blog_zettel]] section (or remove that section)!"
            }
          ],
          "links": [],
          "path": "sase_blog.md",
          "sections": []
        }
      ],
      "command": "rename-drawer",
      "commit": {
        "sha": "8fb55784c5a1dfd91237f63d44e6c5267df7830b",
        "subject": "bob task rename-drawer: NOTES \u2192 Notes (5 notes)"
      },
      "counts": {
        "archive_drawers": 2,
        "closed_drawers": 2,
        "excluded": 9,
        "links_repaired": 0,
        "merges": 0,
        "notes_changed": 5,
        "notes_scanned": 5885,
        "open_drawers": 2,
        "project_sections": 0,
        "refused": 0,
        "template_hits": 0,
        "unresolved_links": 0
      },
      "dry_run": false,
      "excluded": [
        {
          "line": 32,
          "path": "2024/20240829.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 33,
          "path": "2024/20240923.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 39,
          "path": "2024/20240924.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 19,
          "path": "prj_bbxo.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 166,
          "path": "prj_gbd.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 23,
          "path": "prj_mcr_cats.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 24,
          "path": "prj_pa_trouble.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 21,
          "path": "prj_protect.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        },
        {
          "line": 140,
          "path": "prj_yserve.md",
          "reason": "an ordinary heading outside a project note",
          "text": "## NOTES"
        }
      ],
      "io_errors": [],
      "new": {
        "drawer_title": "Notes",
        "input": "Notes",
        "key": "NOTES",
        "section_title": "Notes"
      },
      "ok": true,
      "old": {
        "input": "NOTES",
        "key": "NOTES"
      },
      "refused": [],
      "schema_version": 1,
      "sync": {
        "post": "ok",
        "pre": "ok"
      },
      "templates": [],
      "unresolved_links": [],
      "warnings": []
    }
  },
  {
    "id": "rename_notes_colon",
    "result": {
      "changes": [
        {
          "archive": false,
          "drawers": [
            {
              "block_id": null,
              "from": [
                "NOTES:"
              ],
              "line": 26,
              "merged": 0,
              "status": "open",
              "task": "260214 250421#1U #dad Put $660 back in %abby piggy bank!"
            }
          ],
          "links": [],
          "path": "needs_attn_tasks.md",
          "sections": []
        }
      ],
      "command": "rename-drawer",
      "commit": {
        "sha": "82d2185f68955effc3d9fa7f9140463f7c555382",
        "subject": "bob task rename-drawer: NOTES: \u2192 Notes (1 note)"
      },
      "counts": {
        "archive_drawers": 0,
        "closed_drawers": 0,
        "excluded": 439,
        "links_repaired": 0,
        "merges": 0,
        "notes_changed": 1,
        "notes_scanned": 5885,
        "open_drawers": 1,
        "project_sections": 0,
        "refused": 0,
        "template_hits": 0,
        "unresolved_links": 0
      },
      "dry_run": false,
      "excluded": [
        {
          "line": 41,
          "path": "2024/20240721_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 81,
          "path": "2024/20240727_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 96,
          "path": "2024/20240727_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 55,
          "path": "2024/20240731_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 27,
          "path": "2024/20240802_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 48,
          "path": "2024/20240805_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 32,
          "path": "2024/20240828_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 42,
          "path": "2024/20240909_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 31,
          "path": "2024/20240913_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 56,
          "path": "2024/20240915_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 21,
          "path": "2024/20241004_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "2024/20241121_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 36,
          "path": "2024/20241224_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 57,
          "path": "2025/20250208_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "2025/20250209_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "2025/20250212_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 20,
          "path": "2025/20250302_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 96,
          "path": "2025/20250308_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 48,
          "path": "2025/20250312_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 49,
          "path": "2025/20250315_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "2025/20250317_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "2025/20250318_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 35,
          "path": "2025/20250324.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 48,
          "path": "2025/20250324_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 55,
          "path": "2025/20250324_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 48,
          "path": "2025/20250325_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 75,
          "path": "2025/20250325_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 66,
          "path": "2025/20250406_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 72,
          "path": "2025/20250406_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 68,
          "path": "2025/20250407_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 50,
          "path": "2025/20250409_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "2025/20250414_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 45,
          "path": "2025/20250415_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "2025/20250415_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 30,
          "path": "2025/20250416_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "2025/20250417_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 52,
          "path": "2025/20250418_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 45,
          "path": "2025/20250419_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 49,
          "path": "2025/20250419_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 61,
          "path": "2025/20250421_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 47,
          "path": "2025/20250422_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "2025/20250423_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 48,
          "path": "2025/20250423_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 53,
          "path": "2025/20250423_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "2025/20250424_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "2025/20250425_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "2025/20250425_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "2025/20250428_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 58,
          "path": "2025/20250428_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 58,
          "path": "2025/20250429_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 76,
          "path": "2025/20250429_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 42,
          "path": "2025/20250430_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 50,
          "path": "2025/20250430_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "2025/20250430_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 63,
          "path": "2025/20250430_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 62,
          "path": "2025/20250506_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 45,
          "path": "2025/20250507_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 49,
          "path": "2025/20250507_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "2025/20250507_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 78,
          "path": "2025/20250507_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 86,
          "path": "2025/20250507_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 58,
          "path": "2025/20250508_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 62,
          "path": "2025/20250508_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 70,
          "path": "2025/20250508_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "2025/20250509_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 47,
          "path": "2025/20250509_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 63,
          "path": "2025/20250509_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 69,
          "path": "2025/20250512_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 44,
          "path": "2025/20250513_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "2025/20250513_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 58,
          "path": "2025/20250515_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 64,
          "path": "2025/20250515_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "2025/20250517_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 55,
          "path": "2025/20250519_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 67,
          "path": "2025/20250519_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 42,
          "path": "2025/20250520_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 42,
          "path": "2025/20250527_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "2025/20250605_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 44,
          "path": "2025/20250607_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 48,
          "path": "2025/20250608_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 46,
          "path": "2025/20250609_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 58,
          "path": "2025/20250610_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 66,
          "path": "2025/20250611_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 44,
          "path": "2025/20250619_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 49,
          "path": "2025/20250619_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 55,
          "path": "2025/20250619_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 64,
          "path": "2025/20250619_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 69,
          "path": "2025/20250619_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "2025/20250620_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 59,
          "path": "2025/20250711_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "2025/20250714_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 65,
          "path": "2025/20250714_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 47,
          "path": "2025/20250722_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 53,
          "path": "2025/20250730_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "2025/20250821_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 59,
          "path": "2025/20250821_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "2025/20250905_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 48,
          "path": "2025/20251001_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 70,
          "path": "2025/20251017_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 70,
          "path": "2025/20251113_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "2025/20251119_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "2025/20251207_done.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 39,
          "path": "ads.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 103,
          "path": "best_practice.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 28,
          "path": "book_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 34,
          "path": "book_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "book_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 35,
          "path": "books.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 107,
          "path": "books.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 27,
          "path": "dart.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 109,
          "path": "design_dips.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 118,
          "path": "design_dips.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 123,
          "path": "design_dips.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 131,
          "path": "design_dips.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 156,
          "path": "design_dips.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 20,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 29,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 37,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 57,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 63,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 67,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 72,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 83,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 97,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 106,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 111,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 119,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 123,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 130,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 142,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 155,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 166,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 171,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 176,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 181,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 186,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 192,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 198,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 204,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 213,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 221,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 239,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 249,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 260,
          "path": "dev_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 134,
          "path": "dev_ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 143,
          "path": "dev_ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 23,
          "path": "dev_tools.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 76,
          "path": "dev_tools.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 104,
          "path": "dev_tools.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 14,
          "path": "done_books.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 27,
          "path": "done_projects.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 34,
          "path": "done_projects.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 28,
          "path": "eval_docs.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 19,
          "path": "feat.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 39,
          "path": "fscarpel_meet_2025Q2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 42,
          "path": "fscarpel_meet_2025Q2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 49,
          "path": "fscarpel_meet_2025Q2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 52,
          "path": "fscarpel_meet_2025Q2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 141,
          "path": "fscarpel_meet_2025Q2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 132,
          "path": "gam.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 21,
          "path": "gam_ids.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 19,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 40,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 52,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 82,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 93,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 107,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 119,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 125,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 131,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 137,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 154,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 164,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 177,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 202,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 224,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 231,
          "path": "gtd_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 44,
          "path": "h3_goal.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 16,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 76,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 95,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 104,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 112,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 117,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 147,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 160,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 195,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 201,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 213,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 218,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 243,
          "path": "ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 19,
          "path": "inbox_overflow.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 20,
          "path": "kellys_salary_info.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 29,
          "path": "kellys_salary_info.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 23,
          "path": "legacy_gkeep_notes.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 18,
          "path": "legacy_kelly.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 14,
          "path": "lenard.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 140,
          "path": "mac.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 72,
          "path": "maybe_book.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 212,
          "path": "maybe_work.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 73,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 76,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 85,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 112,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 125,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 148,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 153,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 159,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 165,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 176,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 182,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 189,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 198,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 202,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 205,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 210,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 238,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 243,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 255,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 276,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 294,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 312,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 323,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 354,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 359,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 368,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 377,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 384,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 400,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 422,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 428,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 433,
          "path": "now_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "now_fun.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 63,
          "path": "now_fun.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 38,
          "path": "now_gtd.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 73,
          "path": "now_gtd.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 96,
          "path": "now_gtd.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 56,
          "path": "now_love.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 65,
          "path": "now_love.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 71,
          "path": "now_love.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 31,
          "path": "now_prjs.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 46,
          "path": "now_work.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 88,
          "path": "now_work.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 30,
          "path": "now_zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 32,
          "path": "nvim.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 91,
          "path": "nvim_plugins.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 128,
          "path": "nvim_plugins.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 566,
          "path": "nvim_ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 717,
          "path": "nvim_ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 23,
          "path": "outlive.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 18,
          "path": "phd.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 17,
          "path": "pomodoro.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 30,
          "path": "prj/rap/now_rap_target.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "prj/rap/rap.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 163,
          "path": "prj/rap/rap.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 97,
          "path": "prj/rap/rap_meet_2024Q3.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 158,
          "path": "prj_gbd.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 49,
          "path": "prj_mcr_cats.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 66,
          "path": "prj_mcr_cats.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 114,
          "path": "prj_mcr_cats.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 118,
          "path": "prj_mcr_cats.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 45,
          "path": "prj_pd_local.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 53,
          "path": "prj_pd_local.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 49,
          "path": "prj_zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 79,
          "path": "prj_zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 130,
          "path": "prj_zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 136,
          "path": "prj_zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 27,
          "path": "python.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 37,
          "path": "ref/zorg/dev_ref/guide_to_mutt.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 36,
          "path": "ref/zorg/dev_ref/lynx_user_guide.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/nvim_ref/cc_workflow_code.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 44,
          "path": "ref/zorg/nvim_ref/harpoon_v2_nvim.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 59,
          "path": "ref/zorg/outlive/outlive_ref.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/prj_mcr_cats/mcr_cats.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/prj_mcr_cats/mcr_cats_prd.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/prj_pd_local/drx_deals_localhost.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/prj_pd_local/localhost_dd.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 42,
          "path": "ref/zorg/ref/five_stages_of_fascism.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 88,
          "path": "ref/zorg/system_for_writing/system_for_writing_ref.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/work_ref/autogfe.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/work_ref/bug_reviver.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "ref/zorg/work_ref/drx_fatcat_infra.md",
          "reason": "inside a code fence",
          "text": "* NOTES:"
        },
        {
          "line": 29,
          "path": "ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 34,
          "path": "rpc_studio.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 26,
          "path": "sase_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 52,
          "path": "sase_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 59,
          "path": "sase_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 75,
          "path": "sase_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 82,
          "path": "sase_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 87,
          "path": "sase_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 63,
          "path": "security.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 28,
          "path": "soon_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 51,
          "path": "soon_dev.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 29,
          "path": "soon_work.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 35,
          "path": "soon_work.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 62,
          "path": "soon_work.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 33,
          "path": "soon_zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 64,
          "path": "soon_zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 30,
          "path": "system_for_writing.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 35,
          "path": "team_meet_2025Q2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 59,
          "path": "team_meet_2025Q2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 116,
          "path": "the_monthly.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 20,
          "path": "tick_month_04.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 24,
          "path": "tick_month_04.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 28,
          "path": "tick_month_04.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 31,
          "path": "tick_month_04.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 34,
          "path": "tick_month_04.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 30,
          "path": "ticktock.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 109,
          "path": "vim.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 23,
          "path": "wait.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 30,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 44,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 52,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 70,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 77,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 82,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 88,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 95,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 103,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 122,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 142,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 152,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 165,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 174,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 186,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 200,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 208,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 311,
          "path": "work_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 97,
          "path": "work_ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 121,
          "path": "work_ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 338,
          "path": "work_ref.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 15,
          "path": "z_bullets.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 22,
          "path": "z_tags.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 31,
          "path": "z_tags.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 172,
          "path": "zorg.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 75,
          "path": "zorg_accepted_ideas.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 17,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 24,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 29,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 38,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 47,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 60,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 68,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 77,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 92,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 97,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 109,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 114,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 125,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 135,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 139,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 152,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 160,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 169,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 175,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 183,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 190,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 201,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 223,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 230,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 237,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 246,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 251,
          "path": "zorg_ideas_24.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 20,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 32,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 43,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 54,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 66,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 78,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 83,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 90,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 99,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 108,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 118,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 129,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 134,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 142,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 153,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 167,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 174,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 183,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 210,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 219,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 231,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 238,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 245,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 253,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 264,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 272,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 281,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 296,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 304,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 310,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 325,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 331,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 337,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 344,
          "path": "zorg_ideas_2501.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 18,
          "path": "zorg_ideas_2502.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 27,
          "path": "zorg_ideas_2502.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 36,
          "path": "zorg_ideas_2502.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 52,
          "path": "zorg_ideas_2502.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 65,
          "path": "zorg_ideas_2502.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 77,
          "path": "zorg_ideas_2502.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 19,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 59,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "+ NOTES:"
        },
        {
          "line": 68,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 77,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 82,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 91,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 102,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 110,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 130,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 141,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 152,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 158,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 173,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 181,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 212,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 220,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 229,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 237,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 252,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 263,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 268,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 278,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 283,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 296,
          "path": "zorg_ideas_2503.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 20,
          "path": "zorg_ideas_2504.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 28,
          "path": "zorg_ideas_2504.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 36,
          "path": "zorg_ideas_2504.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 45,
          "path": "zorg_ideas_2504.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 66,
          "path": "zorg_ideas_2504.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 81,
          "path": "zorg_ideas_2504.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 18,
          "path": "zorg_ideas_25H2.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 41,
          "path": "zorg_v2_design.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        },
        {
          "line": 58,
          "path": "zorg_v2_design.md",
          "reason": "not a direct child of a #task",
          "text": "* NOTES:"
        }
      ],
      "io_errors": [],
      "new": {
        "drawer_title": "Notes",
        "input": "Notes",
        "key": "NOTES",
        "section_title": "Notes"
      },
      "ok": true,
      "old": {
        "input": "NOTES:",
        "key": "NOTES:"
      },
      "refused": [],
      "schema_version": 1,
      "sync": {
        "post": "ok",
        "pre": "ok"
      },
      "templates": [],
      "unresolved_links": [],
      "warnings": []
    }
  },
  {
    "id": "rename_options",
    "result": {
      "changes": [
        {
          "archive": false,
          "drawers": [
            {
              "block_id": "prompt-when-used",
              "from": [
                "OPTIONS:"
              ],
              "line": 22,
              "merged": 0,
              "status": "closed",
              "task": "Prompt the user for next action if they attempt to explicitly use disabled provider!"
            }
          ],
          "links": [],
          "path": "sase_better_llm_disable.md",
          "sections": []
        }
      ],
      "command": "rename-drawer",
      "commit": {
        "sha": "9a0ee13b5a6520cc073e85c4995a68c51171de4c",
        "subject": "bob task rename-drawer: OPTIONS: \u2192 Options (1 note)"
      },
      "counts": {
        "archive_drawers": 0,
        "closed_drawers": 1,
        "excluded": 0,
        "links_repaired": 0,
        "merges": 0,
        "notes_changed": 1,
        "notes_scanned": 5885,
        "open_drawers": 0,
        "project_sections": 0,
        "refused": 0,
        "template_hits": 0,
        "unresolved_links": 0
      },
      "dry_run": false,
      "excluded": [],
      "io_errors": [],
      "new": {
        "drawer_title": "Options",
        "input": "Options",
        "key": "OPTIONS",
        "section_title": "Options"
      },
      "ok": true,
      "old": {
        "input": "OPTIONS:",
        "key": "OPTIONS:"
      },
      "refused": [],
      "schema_version": 1,
      "sync": {
        "post": "ok",
        "pre": "ok"
      },
      "templates": [],
      "unresolved_links": [],
      "warnings": []
    }
  },
  {
    "id": "rename_motivation",
    "result": {
      "changes": [
        {
          "archive": false,
          "drawers": [
            {
              "block_id": "chezmoi",
              "from": [
                "MOTIVATION"
              ],
              "line": 22,
              "merged": 0,
              "status": "open",
              "task": "Initialize chezmoi as sase project! #prj_is_blocked"
            }
          ],
          "links": [],
          "path": "sase_projects.md",
          "sections": []
        }
      ],
      "command": "rename-drawer",
      "commit": {
        "sha": "dff55514dcaa207dc011af0eb9121814f59eb6e6",
        "subject": "bob task rename-drawer: MOTIVATION \u2192 Motivation (1 note)"
      },
      "counts": {
        "archive_drawers": 0,
        "closed_drawers": 0,
        "excluded": 0,
        "links_repaired": 0,
        "merges": 0,
        "notes_changed": 1,
        "notes_scanned": 5885,
        "open_drawers": 1,
        "project_sections": 0,
        "refused": 0,
        "template_hits": 0,
        "unresolved_links": 0
      },
      "dry_run": false,
      "excluded": [],
      "io_errors": [],
      "new": {
        "drawer_title": "Motivation",
        "input": "Motivation",
        "key": "MOTIVATION",
        "section_title": "Motivation"
      },
      "ok": true,
      "old": {
        "input": "MOTIVATION",
        "key": "MOTIVATION"
      },
      "refused": [],
      "schema_version": 1,
      "sync": {
        "post": "ok",
        "pre": "ok"
      },
      "templates": [],
      "unresolved_links": [],
      "warnings": []
    }
  },
  {
    "id": "release_done",
    "result": {
      "line": "DONE (sase_agent_recovery.md) left in place; cutover treats it as an ordinary note",
      "status": "released"
    }
  }
]

Output tail:

```text
$ commands/rename_notes
{"changes":[{"archive":false,"drawers":[{"block_id":"ranked-task-links","from":["NOTES"],"line":127,"merged":0,"status":"open","task":"Rank each task link with a number starting at 1!"},{"block_id":"foo","from":["NOTES"],"line":618,"merged":0,"status":"closed","task":"foo"}],"links":[],"path":"bob.md","sections":[]},{"archive":true,"drawers":[{"block_id":"better-refs","from":["NOTES"],"line":377,"merged":0,"status":"closed","task":"Better `^ref` task tracking!"}],"links":[],"path":"done/bob_done.md","sections":[]},{"archive":true,"drawers":[{"block_id":"final","from":["NOTES"],"line":614,"merged":0,"status":"closed","task":"Improve and generalize sase's finalizer!"}],"links":[],"path":"done/sase_done.md","sections":[]},{"archive":false,"drawers":[{"block_id":"artifact-create","from":["NOTES"],"line":60,"merged":0,"status":"open","task":"Improve `sase artifact create` command!"}],"links":[],"path":"sase_art_links.md","sections":[]},{"archive":false,"drawers":[{"block_id":"at-least-one-rec-in-sect","from":["NOTES"],"line":58,"merged":0,"status":"closed","task":"Add at least one record to every [[sase_blog_zettel]] section (or remove that section)!"}],"links":[],"path":"sase_blog.md","sections":[]}],"command":"rename-drawer","commit":{"sha":"8fb55784c5a1dfd91237f63d44e6c5267df7830b","subject":"bob task rename-drawer: NOTES → Notes (5 notes)"},"counts":{"archive_drawers":2,"closed_drawers":2,"excluded":9,"links_repaired":0,"merges":0,"notes_changed":5,"notes_scanned":5885,"open_drawers":2,"project_sections":0,"refused":0,"template_hits":0,"unresolved_links":0},"dry_run":false,"excluded":[{"line":32,"path":"2024/20240829.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":33,"path":"2024/20240923.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":39,"path":"2024/20240924.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":19,"path":"prj_bbxo.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":166,"path":"prj_gbd.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":23,"path":"prj_mcr_cats.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":24,"path":"prj_pa_trouble.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":21,"path":"prj_protect.md","reason":"an ordinary heading outside a project note","text":"## NOTES"},{"line":140,"path":"prj_yserve.md","reason":"an ordinary heading outside a project note","text":"## NOTES"}],"io_errors":[],"new":{"drawer_title":"Notes","input":"Notes","key":"NOTES","section_title":"Notes"},"ok":true,"old":{"input":"NOTES","key":"NOTES"},"refused":[],"schema_version":1,"sync":{"post":"ok","pre":"ok"},"templates":[],"unresolved_links":[],"warnings":[]}
$ commands/rename_notes_colon
{"changes":[{"archive":false,"drawers":[{"block_id":null,"from":["NOTES:"],"line":26,"merged":0,"status":"open","task":"260214 250421#1U #dad Put $660 back in %abby piggy bank!"}],"links":[],"path":"needs_attn_tasks.md","sections":[]}],"command":"rename-drawer","commit":{"sha":"82d2185f68955effc3d9fa7f9140463f7c555382","subject":"bob task rename-drawer: NOTES: → Notes (1 note)"},"counts":{"archive_drawers":0,"closed_drawers":0,"excluded":439,"links_repaired":0,"merges":0,"notes_changed":1,"notes_scanned":5885,"open_drawers":1,"project_sections":0,"refused":0,"template_hits":0,"unresolved_links":0},"dry_run":false,"excluded":[{"line":41,"path":"2024/20240721_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":81,"path":"2024/20240727_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":96,"path":"2024/20240727_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":55,"path":"2024/20240731_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":27,"path":"2024/20240802_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":48,"path":"2024/20240805_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":32,"path":"2024/20240828_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":42,"path":"2024/20240909_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":31,"path":"2024/20240913_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":56,"path":"2024/20240915_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":21,"path":"2024/20241004_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"2024/20241121_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":36,"path":"2024/20241224_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":57,"path":"2025/20250208_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"2025/20250209_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"2025/20250212_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":20,"path":"2025/20250302_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":96,"path":"2025/20250308_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":48,"path":"2025/20250312_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":49,"path":"2025/20250315_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"2025/20250317_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"2025/20250318_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":35,"path":"2025/20250324.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":48,"path":"2025/20250324_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":55,"path":"2025/20250324_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":48,"path":"2025/20250325_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":75,"path":"2025/20250325_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":66,"path":"2025/20250406_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":72,"path":"2025/20250406_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":68,"path":"2025/20250407_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":50,"path":"2025/20250409_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"2025/20250414_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":45,"path":"2025/20250415_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"2025/20250415_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":30,"path":"2025/20250416_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"2025/20250417_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":52,"path":"2025/20250418_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":45,"path":"2025/20250419_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":49,"path":"2025/20250419_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":61,"path":"2025/20250421_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":47,"path":"2025/20250422_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"2025/20250423_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":48,"path":"2025/20250423_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":53,"path":"2025/20250423_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"2025/20250424_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"2025/20250425_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"2025/20250425_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"2025/20250428_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":58,"path":"2025/20250428_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":58,"path":"2025/20250429_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":76,"path":"2025/20250429_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":42,"path":"2025/20250430_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":50,"path":"2025/20250430_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"2025/20250430_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":63,"path":"2025/20250430_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":62,"path":"2025/20250506_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":45,"path":"2025/20250507_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":49,"path":"2025/20250507_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"2025/20250507_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":78,"path":"2025/20250507_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":86,"path":"2025/20250507_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":58,"path":"2025/20250508_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":62,"path":"2025/20250508_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":70,"path":"2025/20250508_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"2025/20250509_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":47,"path":"2025/20250509_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":63,"path":"2025/20250509_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":69,"path":"2025/20250512_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":44,"path":"2025/20250513_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"2025/20250513_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":58,"path":"2025/20250515_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":64,"path":"2025/20250515_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"2025/20250517_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":55,"path":"2025/20250519_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":67,"path":"2025/20250519_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":42,"path":"2025/20250520_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":42,"path":"2025/20250527_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"2025/20250605_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":44,"path":"2025/20250607_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":48,"path":"2025/20250608_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":46,"path":"2025/20250609_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":58,"path":"2025/20250610_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":66,"path":"2025/20250611_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":44,"path":"2025/20250619_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":49,"path":"2025/20250619_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":55,"path":"2025/20250619_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":64,"path":"2025/20250619_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":69,"path":"2025/20250619_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"2025/20250620_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":59,"path":"2025/20250711_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"2025/20250714_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":65,"path":"2025/20250714_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":47,"path":"2025/20250722_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":53,"path":"2025/20250730_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"2025/20250821_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":59,"path":"2025/20250821_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":41,"path":"2025/20250905_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":48,"path":"2025/20251001_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":70,"path":"2025/20251017_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":70,"path":"2025/20251113_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"2025/20251119_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"2025/20251207_done.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":39,"path":"ads.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":103,"path":"best_practice.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":28,"path":"book_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":34,"path":"book_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":41,"path":"book_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":35,"path":"books.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":107,"path":"books.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":27,"path":"dart.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":109,"path":"design_dips.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":118,"path":"design_dips.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":123,"path":"design_dips.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":131,"path":"design_dips.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":156,"path":"design_dips.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":20,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":29,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":37,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":57,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":63,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":67,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":72,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":83,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":97,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":106,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":111,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":119,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":123,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":130,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":142,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":155,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":166,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":171,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":176,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":181,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":186,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":192,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":198,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":204,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":213,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":221,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":239,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":249,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":260,"path":"dev_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":134,"path":"dev_ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":143,"path":"dev_ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":23,"path":"dev_tools.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":76,"path":"dev_tools.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":104,"path":"dev_tools.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":14,"path":"done_books.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":27,"path":"done_projects.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":34,"path":"done_projects.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":28,"path":"eval_docs.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":19,"path":"feat.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":39,"path":"fscarpel_meet_2025Q2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":42,"path":"fscarpel_meet_2025Q2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":49,"path":"fscarpel_meet_2025Q2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":52,"path":"fscarpel_meet_2025Q2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":141,"path":"fscarpel_meet_2025Q2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":132,"path":"gam.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":21,"path":"gam_ids.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":19,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":40,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":52,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":82,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":93,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":107,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":119,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":125,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":131,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":137,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":154,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":164,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":177,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":202,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":224,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":231,"path":"gtd_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":44,"path":"h3_goal.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":16,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":76,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":95,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":104,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":112,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":117,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":147,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":160,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":195,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":201,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":213,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":218,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":243,"path":"ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":19,"path":"inbox_overflow.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":20,"path":"kellys_salary_info.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":29,"path":"kellys_salary_info.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":23,"path":"legacy_gkeep_notes.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":18,"path":"legacy_kelly.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":14,"path":"lenard.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":140,"path":"mac.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":72,"path":"maybe_book.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":212,"path":"maybe_work.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":73,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":76,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":85,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":112,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":125,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":148,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":153,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":159,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":165,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":176,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":182,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":189,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":198,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":202,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":205,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":210,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":238,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":243,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":255,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":276,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":294,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":312,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":323,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":354,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":359,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":368,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":377,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":384,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":400,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":422,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":428,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":433,"path":"now_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"now_fun.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":63,"path":"now_fun.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":38,"path":"now_gtd.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":73,"path":"now_gtd.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":96,"path":"now_gtd.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":56,"path":"now_love.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":65,"path":"now_love.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":71,"path":"now_love.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":31,"path":"now_prjs.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":46,"path":"now_work.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":88,"path":"now_work.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":30,"path":"now_zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":32,"path":"nvim.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":91,"path":"nvim_plugins.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":128,"path":"nvim_plugins.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":566,"path":"nvim_ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":717,"path":"nvim_ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":23,"path":"outlive.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":18,"path":"phd.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":17,"path":"pomodoro.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":30,"path":"prj/rap/now_rap_target.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"prj/rap/rap.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":163,"path":"prj/rap/rap.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":97,"path":"prj/rap/rap_meet_2024Q3.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":158,"path":"prj_gbd.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":49,"path":"prj_mcr_cats.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":66,"path":"prj_mcr_cats.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":114,"path":"prj_mcr_cats.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":118,"path":"prj_mcr_cats.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":45,"path":"prj_pd_local.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":53,"path":"prj_pd_local.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":49,"path":"prj_zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":79,"path":"prj_zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":130,"path":"prj_zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":136,"path":"prj_zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":27,"path":"python.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":37,"path":"ref/zorg/dev_ref/guide_to_mutt.md","reason":"inside a code fence","text":"* NOTES:"},{"line":36,"path":"ref/zorg/dev_ref/lynx_user_guide.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/nvim_ref/cc_workflow_code.md","reason":"inside a code fence","text":"* NOTES:"},{"line":44,"path":"ref/zorg/nvim_ref/harpoon_v2_nvim.md","reason":"inside a code fence","text":"* NOTES:"},{"line":59,"path":"ref/zorg/outlive/outlive_ref.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/prj_mcr_cats/mcr_cats.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/prj_mcr_cats/mcr_cats_prd.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/prj_pd_local/drx_deals_localhost.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/prj_pd_local/localhost_dd.md","reason":"inside a code fence","text":"* NOTES:"},{"line":42,"path":"ref/zorg/ref/five_stages_of_fascism.md","reason":"inside a code fence","text":"* NOTES:"},{"line":88,"path":"ref/zorg/system_for_writing/system_for_writing_ref.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/work_ref/autogfe.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/work_ref/bug_reviver.md","reason":"inside a code fence","text":"* NOTES:"},{"line":41,"path":"ref/zorg/work_ref/drx_fatcat_infra.md","reason":"inside a code fence","text":"* NOTES:"},{"line":29,"path":"ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":34,"path":"rpc_studio.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":26,"path":"sase_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":52,"path":"sase_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":59,"path":"sase_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":75,"path":"sase_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":82,"path":"sase_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":87,"path":"sase_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":63,"path":"security.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":28,"path":"soon_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":51,"path":"soon_dev.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":29,"path":"soon_work.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":35,"path":"soon_work.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":62,"path":"soon_work.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":33,"path":"soon_zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":64,"path":"soon_zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":30,"path":"system_for_writing.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":35,"path":"team_meet_2025Q2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":59,"path":"team_meet_2025Q2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":116,"path":"the_monthly.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":20,"path":"tick_month_04.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":24,"path":"tick_month_04.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":28,"path":"tick_month_04.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":31,"path":"tick_month_04.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":34,"path":"tick_month_04.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":30,"path":"ticktock.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":109,"path":"vim.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":23,"path":"wait.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":30,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":44,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":52,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":70,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":77,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":82,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":88,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":95,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":103,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":122,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":142,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":152,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":165,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":174,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":186,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":200,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":208,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":311,"path":"work_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":97,"path":"work_ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":121,"path":"work_ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":338,"path":"work_ref.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":15,"path":"z_bullets.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":22,"path":"z_tags.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":31,"path":"z_tags.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":172,"path":"zorg.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":75,"path":"zorg_accepted_ideas.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":17,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":24,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":29,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":38,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":47,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":60,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":68,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":77,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":92,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":97,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":109,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":114,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":125,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":135,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":139,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":152,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":160,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":169,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":175,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":183,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":190,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":201,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":223,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":230,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":237,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":246,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":251,"path":"zorg_ideas_24.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":20,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":32,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":43,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":54,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":66,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":78,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":83,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":90,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":99,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":108,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":118,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":129,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":134,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":142,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":153,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":167,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":174,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":183,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":210,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":219,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":231,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":238,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":245,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":253,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":264,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":272,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":281,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":296,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":304,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":310,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":325,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":331,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":337,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":344,"path":"zorg_ideas_2501.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":18,"path":"zorg_ideas_2502.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":27,"path":"zorg_ideas_2502.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":36,"path":"zorg_ideas_2502.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":52,"path":"zorg_ideas_2502.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":65,"path":"zorg_ideas_2502.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":77,"path":"zorg_ideas_2502.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":19,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":59,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"+ NOTES:"},{"line":68,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":77,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":82,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":91,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":102,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":110,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":130,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":141,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":152,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":158,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":173,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":181,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":212,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":220,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":229,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":237,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":252,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":263,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":268,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":278,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":283,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":296,"path":"zorg_ideas_2503.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":20,"path":"zorg_ideas_2504.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":28,"path":"zorg_ideas_2504.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":36,"path":"zorg_ideas_2504.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":45,"path":"zorg_ideas_2504.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":66,"path":"zorg_ideas_2504.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":81,"path":"zorg_ideas_2504.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":18,"path":"zorg_ideas_25H2.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":41,"path":"zorg_v2_design.md","reason":"not a direct child of a #task","text":"* NOTES:"},{"line":58,"path":"zorg_v2_design.md","reason":"not a direct child of a #task","text":"* NOTES:"}],"io_errors":[],"new":{"drawer_title":"Notes","input":"Notes","key":"NOTES","section_title":"Notes"},"ok":true,"old":{"input":"NOTES:","key":"NOTES:"},"refused":[],"schema_version":1,"sync":{"post":"ok","pre":"ok"},"templates":[],"unresolved_links":[],"warnings":[]}
$ commands/rename_options
{"changes":[{"archive":false,"drawers":[{"block_id":"prompt-when-used","from":["OPTIONS:"],"line":22,"merged":0,"status":"closed","task":"Prompt the user for next action if they attempt to explicitly use disabled provider!"}],"links":[],"path":"sase_better_llm_disable.md","sections":[]}],"command":"rename-drawer","commit":{"sha":"9a0ee13b5a6520cc073e85c4995a68c51171de4c","subject":"bob task rename-drawer: OPTIONS: → Options (1 note)"},"counts":{"archive_drawers":0,"closed_drawers":1,"excluded":0,"links_repaired":0,"merges":0,"notes_changed":1,"notes_scanned":5885,"open_drawers":0,"project_sections":0,"refused":0,"template_hits":0,"unresolved_links":0},"dry_run":false,"excluded":[],"io_errors":[],"new":{"drawer_title":"Options","input":"Options","key":"OPTIONS","section_title":"Options"},"ok":true,"old":{"input":"OPTIONS:","key":"OPTIONS:"},"refused":[],"schema_version":1,"sync":{"post":"ok","pre":"ok"},"templates":[],"unresolved_links":[],"warnings":[]}
$ commands/rename_motivation
{"changes":[{"archive":false,"drawers":[{"block_id":"chezmoi","from":["MOTIVATION"],"line":22,"merged":0,"status":"open","task":"Initialize chezmoi as sase project! #prj_is_blocked"}],"links":[],"path":"sase_projects.md","sections":[]}],"command":"rename-drawer","commit":{"sha":"dff55514dcaa207dc011af0eb9121814f59eb6e6","subject":"bob task rename-drawer: MOTIVATION → Motivation (1 note)"},"counts":{"archive_drawers":0,"closed_drawers":0,"excluded":0,"links_repaired":0,"merges":0,"notes_changed":1,"notes_scanned":5885,"open_drawers":1,"project_sections":0,"refused":0,"template_hits":0,"unresolved_links":0},"dry_run":false,"excluded":[],"io_errors":[],"new":{"drawer_title":"Motivation","input":"Motivation","key":"MOTIVATION","section_title":"Motivation"},"ok":true,"old":{"input":"MOTIVATION","key":"MOTIVATION"},"refused":[],"schema_version":1,"sync":{"post":"ok","pre":"ok"},"templates":[],"unresolved_links":[],"warnings":[]}
$ commands/release_done
{"status":"released","line":"DONE (sase_agent_recovery.md) left in place; cutover treats it as an ordinary note"}
```


````

---

%macros_enabled:true
# New Query
%model:muse-spark-1.3-contributor
%effort:high

%macros_enabled:false
# Gate answered

**Decision:** Apply drawer migration: 4 renames, release DONE

| | |
| --- | --- |
| **Outcome** | ANSWERED — Rename 6 NOTES drawers to Notes, Rename NOTES: drawer to Notes, Rename OPTIONS: drawer to Options, Rename MOTIVATION drawer to Motivation, Release DONE line (leave in place) |
| **Answered via** | tui |
| **Opened** | 2026-11-26T00:12:40Z |
| **Answered** | 2026-11-26T01:40:30Z |
| **Commands** | 5 of 5 completed |
| **Gate** | custom/custom-c6e923fd-8268-40d2-a180-917022869008 |

## Results

### rename_notes — `commands/rename_notes`

```json
{
  "changes": [
    {
      "archive": false,
      "drawers": [
        {
          "block_id": "ranked-task-links",
          "from": [
            "NOTES"
          ],
          "line": 127,
          "merged": 0,
          "status": "open",
          "task": "Rank each task link with a number starting at 1!"
        },
        {
          "block_id": "foo",
          "from": [
            "NOTES"
          ],
          "line": 618,
          "merged": 0,
          "status": "closed",
          "task": "foo"
        }
      ],
      "links": [],
      "path": "bob.md",
      "sections": []
    },
    {
      "archive": true,
      "drawers": [
        {
          "block_id": "better-refs",
          "from": [
            "NOTES"
          ],
          "line": 377,
          "merged": 0,
          "status": "closed",
          "task": "Better `^ref` task tracking!"
        }
      ],
      "links": [],
      "path": "done/bob_done.md",
      "sections": []
    },
    {
      "archive": true,
      "drawers": [
        {
          "block_id": "final",
          "from": [
            "NOTES"
          ],
          "line": 614,
          "merged": 0,
          "status": "closed",
          "task": "Improve and generalize sase's finalizer!"
        }
      ],
      "links": [],
      "path": "done/sase_done.md",
      "sections": []
    },
    {
      "archive": false,
      "drawers": [
        {
          "block_id": "artifact-create",
          "from": [
            "NOTES"
          ],
          "line": 60,
          "merged": 0,
          "status": "open",
          "task": "Improve `sase artifact create` command!"
        }
      ],
      "links": [],
      "path": "sase_art_links.md",
      "sections": []
    },
    {
      "archive": false,
      "drawers": [
        {
          "block_id": "at-least-one-rec-in-sect",
          "from": [
            "NOTES"
          ],
          "line": 58,
          "merged": 0,
          "status": "closed",
          "task": "Add at least one record to every [[sase_blog_zettel]] section (or remove that section)!"
        }
      ],
      "links": [],
      "path": "sase_blog.md",
      "sections": []
    }
  ],
  "command": "rename-drawer",
  "commit": {
    "sha": "8fb55784c5a1dfd91237f63d44e6c5267df7830b",
    "subject": "bob task rename-drawer: NOTES \u2192 Notes (5 notes)"
  },
  "counts": {
    "archive_drawers": 2,
    "closed_drawers": 2,
    "excluded": 9,
    "links_repaired": 0,
    "merges": 0,
    "notes_changed": 5,
    "notes_scanned": 5885,
    "open_drawers": 2,
    "project_sections": 0,
    "refused": 0,
    "template_hits": 0,
    "unresolved_links": 0
  },
  "dry_run": false,
  "excluded": [
    {
      "line": 32,
      "path": "2024/20240829.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 33,
      "path": "2024/20240923.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 39,
      "path": "2024/20240924.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 19,
      "path": "prj_bbxo.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 166,
      "path": "prj_gbd.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 23,
      "path": "prj_mcr_cats.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 24,
      "path": "prj_pa_trouble.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 21,
      "path": "prj_protect.md",
      "reason": "an ordinary heading outside a project note",
      "text": "## NOTES"
    },
    {
      "line": 140,
      "path": "prj_yserve.md",
      "reason": "an ordinary heading 
… 421 characters elided …
```

### rename_notes_colon — `commands/rename_notes_colon`

```json
{
  "changes": [
    {
      "archive": false,
      "drawers": [
        {
          "block_id": null,
          "from": [
            "NOTES:"
          ],
          "line": 26,
          "merged": 0,
          "status": "open",
          "task": "260214 250421#1U #dad Put $660 back in %abby piggy bank!"
        }
      ],
      "links": [],
      "path": "needs_attn_tasks.md",
      "sections": []
    }
  ],
  "command": "rename-drawer",
  "commit": {
    "sha": "82d2185f68955effc3d9fa7f9140463f7c555382",
    "subject": "bob task rename-drawer: NOTES: \u2192 Notes (1 note)"
  },
  "counts": {
    "archive_drawers": 0,
    "closed_drawers": 0,
    "excluded": 439,
    "links_repaired": 0,
    "merges": 0,
    "notes_changed": 1,
    "notes_scanned": 5885,
    "open_drawers": 1,
    "project_sections": 0,
    "refused": 0,
    "template_hits": 0,
    "unresolved_links": 0
  },
  "dry_run": false,
  "excluded": [
    {
      "line": 41,
      "path": "2024/20240721_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 81,
      "path": "2024/20240727_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 96,
      "path": "2024/20240727_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 55,
      "path": "2024/20240731_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 27,
      "path": "2024/20240802_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 48,
      "path": "2024/20240805_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 32,
      "path": "2024/20240828_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 42,
      "path": "2024/20240909_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 31,
      "path": "2024/20240913_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 56,
      "path": "2024/20240915_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 21,
      "path": "2024/20241004_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 54,
      "path": "2024/20241121_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 36,
      "path": "2024/20241224_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 57,
      "path": "2025/20250208_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 60,
      "path": "2025/20250209_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 60,
      "path": "2025/20250212_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 20,
      "path": "2025/20250302_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 96,
      "path": "2025/20250308_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 48,
      "path": "2025/20250312_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 49,
      "path": "2025/20250315_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 54,
      "path": "2025/20250317_done.md",
      "reason": "not a direct child of a #task",
      "text": "* NOTES:"
    },
    {
      "line": 43,
      "path": "2025/20250
… 58395 characters elided …
```

### rename_options — `commands/rename_options`

```json
{
  "changes": [
    {
      "archive": false,
      "drawers": [
        {
          "block_id": "prompt-when-used",
          "from": [
            "OPTIONS:"
          ],
          "line": 22,
          "merged": 0,
          "status": "closed",
          "task": "Prompt the user for next action if they attempt to explicitly use disabled provider!"
        }
      ],
      "links": [],
      "path": "sase_better_llm_disable.md",
      "sections": []
    }
  ],
  "command": "rename-drawer",
  "commit": {
    "sha": "9a0ee13b5a6520cc073e85c4995a68c51171de4c",
    "subject": "bob task rename-drawer: OPTIONS: \u2192 Options (1 note)"
  },
  "counts": {
    "archive_drawers": 0,
    "closed_drawers": 1,
    "excluded": 0,
    "links_repaired": 0,
    "merges": 0,
    "notes_changed": 1,
    "notes_scanned": 5885,
    "open_drawers": 0,
    "project_sections": 0,
    "refused": 0,
    "template_hits": 0,
    "unresolved_links": 0
  },
  "dry_run": false,
  "excluded": [],
  "io_errors": [],
  "new": {
    "drawer_title": "Options",
    "input": "Options",
    "key": "OPTIONS",
    "section_title": "Options"
  },
  "ok": true,
  "old": {
    "input": "OPTIONS:",
    "key": "OPTIONS:"
  },
  "refused": [],
  "schema_version": 1,
  "sync": {
    "post": "ok",
    "pre": "ok"
  },
  "templates": [],
  "unresolved_links": [],
  "warnings": []
}
```

### rename_motivation — `commands/rename_motivation`

```json
{
  "changes": [
    {
      "archive": false,
      "drawers": [
        {
          "block_id": "chezmoi",
          "from": [
            "MOTIVATION"
          ],
          "line": 22,
          "merged": 0,
          "status": "open",
          "task": "Initialize chezmoi as sase project! #prj_is_blocked"
        }
      ],
      "links": [],
      "path": "sase_projects.md",
      "sections": []
    }
  ],
  "command": "rename-drawer",
  "commit": {
    "sha": "dff55514dcaa207dc011af0eb9121814f59eb6e6",
    "subject": "bob task rename-drawer: MOTIVATION \u2192 Motivation (1 note)"
  },
  "counts": {
    "archive_drawers": 0,
    "closed_drawers": 0,
    "excluded": 0,
    "links_repaired": 0,
    "merges": 0,
    "notes_changed": 1,
    "notes_scanned": 5885,
    "open_drawers": 1,
    "project_sections": 0,
    "refused": 0,
    "template_hits": 0,
    "unresolved_links": 0
  },
  "dry_run": false,
  "excluded": [],
  "io_errors": [],
  "new": {
    "drawer_title": "Motivation",
    "input": "Motivation",
    "key": "MOTIVATION",
    "section_title": "Motivation"
  },
  "ok": true,
  "old": {
    "input": "MOTIVATION",
    "key": "MOTIVATION"
  },
  "refused": [],
  "schema_version": 1,
  "sync": {
    "post": "ok",
    "pre": "ok"
  },
  "templates": [],
  "unresolved_links": [],
  "warnings": []
}
```

### release_done — `commands/release_done`

```json
{
  "line": "DONE (sase_agent_recovery.md) left in place; cutover treats it as an ordinary note",
  "status": "released"
}
```

## Your next action

Verify the drawer migration outcome for bead bob-cli-ph.9: re-run `bob task rename-drawer -l -f json` and confirm only released/kept lines remain (DONE plus the two keeps); confirm each approved rename dry-run now reports nothing; store the approved rename/release record plus the passing writer-gate evidence as a SASE artifact for cutover (bob-cli-ph.10) to read; if every legacy drawer is renamed or released, close bead bob-cli-ph.9 with a note citing the verification, otherwise record the remainder on the bead and leave it open. Never close the parent epic or any other bead.
%macros_enabled:true

## Response

Drawer migration verified and bead closed.

- Applied per gate: 4 renames committed in the live vault (`8fb55784` NOTES→Notes, `82d2185f` NOTES:→Notes, `9a0ee13b` OPTIONS:→Options, `dff55514` MOTIVATION→Motivation), DONE released in place.
- Verification: legacy inventory (5885 notes) shows only the released DONE line plus the two keeps (empty bold drawer in `done/sase_done.md`, `**Note:**` lead); all 4 rename dry-runs now report 0 changes.
- Stored migration record as artifact `file:explicit:1d4db13a0a6ed86a7c2d0374` for `bob-cli-ph.10` cutover.
- `epic-symbols` clean; closed `bob-cli-ph.9` with verification note. No repo changes in this workspace; no declaration required.
