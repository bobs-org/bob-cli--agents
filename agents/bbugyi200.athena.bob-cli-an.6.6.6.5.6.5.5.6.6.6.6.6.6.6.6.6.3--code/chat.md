# Chat History - ace-run (bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3--code)

- **TIMESTAMP:** 2026-10-27 07:00:44 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-bob_cli_an_6_6_6_5_6_5_5_6_6_6_6_6_6_6_6_6_3__plan-261027_062531.md`
- **2. --code** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-bob_cli_an_6_6_6_5_6_5_5_6_6_6_6_6_6_6_6_6_3__code-261027_062531.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202610/research_hook_stable_recapture.md

The above plan has been reviewed and approved. Implement it now.


## Response

Implemented the approved stable-recapture plan.

Top finding: the research-file hook now derives hash-free names and chooses reread vs overwrite from live JSON state, with all gates green and the phase closed.

Changed (chezmoi only, commit `10e9f1d2` via `/sase_git_commit`):
- [executable_bob_research_capture](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/chezmoi/home/bin/executable_bob_research_capture) — new adapter: strips terminal `-<12 hex>`, resolves via `bob ref show -f json`, follows `later` to newest reading, recaptures with bare `-f` or `-f=overwrite`.
- [sase.yml](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/chezmoi/home/dot_config/sase/sase.yml) — hook command is now `bob_research_capture`; `use` and provider filtering preserved.
- [bob_research_capture_test.sh](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/chezmoi/tests/bash/bob_research_capture_test.sh) — 14 offline tests covering all six required behaviors.

Observed verification:
- Focused suite: 14 passed, 83 assertions.
- `just test-bash`: 283 passed.
- `just check` (chezmoi): pass, including pytest 26 passed.
- `just check` (bob-cli): pass, exit 0.
- `chezmoi diff` for the two targets showed only this change; applied only those targets and verified installed helper/config identical. No live-report smoke capture.

Repairs: read-only proposal registered as `file:explicit:19e2c6c00fdc72a47b88c967` on the phase. Rechecked all five rows (493 chat rows): first two have clean same-title counterparts with saved-source pointers but differing PDF bytes → archive proposals, not `__v2` merges; two `__gem` singles → hash-strip renames (preview currently refuses `not in sync`, needs Mac scan); abandoned annotated fifth with inbound `sase_final_polish.md` link → preserve, gated coordinated archive only. No live repair executed.

Bead `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3` noted and closed; `epic-symbols` empty. `bob-cli-cm` and ancestors left open for the parent lander.
