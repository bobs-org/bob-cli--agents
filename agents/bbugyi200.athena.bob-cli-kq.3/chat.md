# Chat History - ace-run (bob-cli-kq.3)

- **TIMESTAMP:** 2026-11-12 05:47:01 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-kq.3

## Prompt

#gh:gh_bobs-org__bob-cli
%id(3, clan=bob-cli-kq, bead=bob-cli-kq.3)
%model:@medium
%auto
Can you complete the work for bead bob-cli-kq.3? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-kq.3` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-kq.3` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-kq.3 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-kq.3 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-kq.3 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-kq.3`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-kq.3 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. `bob-cli-kq.3` (Web-clip network guards and image handling) is implemented and closed.

What changed, in [web_clip_adapter.py](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_21/scripts/web_clip/web_clip_adapter.py) and [web_clip_render.py](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_21/scripts/web_clip/web_clip_render.py):

- **Redirect-chain SSRF (A):** new `_private_landing_url` walks `nav.request.redirected_from` plus `page.url` after every `goto` (headless and headed paths) and raises a `network` refusal on any non-global hop. Skipped for fixture route-hooks and `--html` captures, which serve no live network.
- **WebSocket SSRF (B):** new `_install_ws_guard` installs `context.route_web_socket("**/*", …)` next to each `_install_guard`, proxying only `ws`/`wss` URLs to globally routable hosts via `connect_to_server()` and closing everything else. Verified against the pinned Playwright 1.62 API (`BrowserContext.route_web_socket`, `WebSocketRoute.url/close/connect_to_server` all exist).
- **Positional img parsing (C):** new `_img_attr`/`_set_img_src` helpers in both files replace whole-tag `src=` regex search/substitution in `_localize_images`, `normalize_images`, and `prefix_part_assets`. Removed the now-dead `_SRC_ATTR_RE` in the renderer.
- **Literal origin insertion (D):** the `data-bob-origin` `re.sub` now uses a lambda replacement so `\1`/`\g` in image URLs can't raise `invalid group reference`.

Verification: `just check-web-clip-adapter` gate green (`py_compile` + self-test exit 0, `ok`), with 10 new regression checks (mocked private redirect refusal, WS allow/block, origin query with `src=` surviving render plus prefixing, alt-text `src=` shadowing, backslash-URL localization). A scratch probe confirmed the old code failed all three image cases. The `TargetClosedError` teardown noise reproduces identically on the base tree, and `epic-symbols` reports no leftovers.

Declaration submitted: commit for `main` with bead_action close on `bob-cli-kq.3`.
