# Chat History - ace-run (chop.refresh_docs.bob-cli.9_066735.1)

- **TIMESTAMP:** 2026-08-19 22:30:11 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** chop.refresh_docs.bob-cli.9_066735.1

## Prompt

#gh:bobs-org/bob-cli
%id(chop.refresh_docs.bob-cli.9_066735.1, tribe=chop)
%wait(runners=0)
Refresh the documentation for bob-cli.

Review the current repository behavior and the changes since the last documentation
refresh. Update user-facing documentation so it is accurate, complete, and clear to
someone new to the project. You may only create, modify, or delete documentation
files, such as Markdown or other docs-tree content, READMEs, and doc-adjacent assets.
You MUST NOT create, modify, or delete source code, tests, build configuration, or any
other non-documentation file, even to fix a bug you are confident about.

When documentation and code disagree, document the actual current behavior; never
change the code to match the prose. If you identify a suspected code bug, describe it
in your final response so a human or separately scoped agent can pick it up (and you
may also note it in the commit message body), but do not fix it. Run the repository's
documentation checks when you change files.

## Response

I'll start by reviewing the project's documentation workflow and current docs so the refresh matches actual repository behavior.

I’ll load CLI docs conventions and then compare the existing docs against git history since the last refresh.

Next I’ll inspect git history, remaining README content, and current CLI help so the docs match live commands.

I’ll look for the last dedicated docs refresh, the docs-check pipeline, and CLI/help output that the README might be missing.

I’ll dump live CLI help and compare it with the README and the rest of the docs tree.

I’ll scan for undocumented flags, env vars, and docs files that lagged behind the code.

Capture docs still mention Hammerspoon; I’ll confirm whether `bob-mac-capture` is the current frontend before rewriting that section.

I’ll extract the capture contract into its own guide, then slim the README into a newcomer-oriented overview.

I’ll rewrite the README into a shorter overview that points at the detailed command guides.

User-facing documentation now matches current `bob` behavior and is structured for a first-time reader.

The last dedicated refresh was 2026-07-19. Since then capture grew into a full editor protocol (batch items, nested bullets, `^`/`+`/`#` markers, parse/complete, task sections), Highlights gained `xlib` intake, and Pomodoro gained `--show-stale`. Most of that had been appended to the README, which had become a 1,500-line contract dump.

## What changed

**README is the onboarding page again** (~680 lines). It now has a contents list, a daily workflow, a vault-layout map, a command index, short per-command summaries, and a complete environment-variable list.

**Capture moved to [`docs/capture.md`](docs/capture.md).** That is the full grammar, JSON, and picker protocol, with a marker cheat sheet at the top. Editor wording now describes Bob Mac Capture (Control-Shift-Command-I), not the retired Hammerspoon panel.

**[`docs/README.md`](docs/README.md)** indexes the detailed contracts.

Accuracy and completeness fixes include:

- `--section` with no matching heading falls back to the pre-heading section (same as `@route#prefix`)
- `bob highlights scan -v/--verbose`
- Environment vars that were missing from the README list: `BOB_CONFIG_FILE`, `BOB_HIGHLIGHTS_XLIB_DIR`, `BOB_PANDOC_COMMAND`, `BOB_PRIORITY_ROLL_SEED`, plus `XDG_*` lock/cache/config paths
- `bob nightly` lock, skipped `ob` / already-running sync, and exit-0 when another maintenance run holds the lock
- `bob pomodoro --debug/--verbose/--show-stale` and `bob notify -v`
- Retired `@route::id` spelling called out in migration notes

The other command guides (`query`, Highlights, plugins, projects, task-status-hooks) got contents lists and short “when to run this” intros. Leftover “MVP” wording in Highlights is gone.

## Documentation checks

`just package-list` refuses a dirty worktree (`cargo package` requires a commit). The same listing with `--allow-dirty` includes `README.md` and every file under `docs/`, including the two new pages. There is no separate markdown linter in this repo.

## Suspected code issue (not fixed)

`bob notify --help` still prints `usage: bob_notify ...` because the native command hard-codes the legacy script name. Behavior is otherwise native; only the help banner is stale. `-v` is documented as verbose, but extra debug tracing only appears at `-vv`, matching the embedded script’s `log::debug` gate.

I'll commit the documentation refresh using the project's git commit skill, then summarize what landed.

I'll record the commit skill, then inspect the uncommitted docs so the message matches what actually changed.

The dirty files are the documentation refresh. Next I’ll write the commit message and run the stitch.

The commit is still running; I’ll wait for stitch to finish rather than leave it hanging.

Committed and pushed the documentation refresh as `b64f393` (`docs: refresh user-facing docs to match current bob CLI`). `master` is clean and in sync with `origin/master`.

The commit covers:

- **README.md** — slimmer onboarding page (workflow, vault layout, command index, env vars)
- **docs/capture.md** — capture grammar, JSON, and picker protocol (Bob Mac Capture, not Hammerspoon)
- **docs/README.md** — index of the detailed guides
- Updates to query, Highlights, plugins, projects, and task-status-hooks docs

Noted but not fixed: `bob notify --help` still prints `usage: bob_notify ...`, and extra debug tracing only appears at `-vv`.
