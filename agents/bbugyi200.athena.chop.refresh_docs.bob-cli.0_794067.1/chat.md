# Chat History - ace-run (chop.refresh_docs.bob-cli.0_794067.1)

- **TIMESTAMP:** 2026-09-29 15:16:57 EDT
- **MODEL:** grok/grok-4.7
- **AGENT:** chop.refresh_docs.bob-cli.0_794067.1

## Prompt

#gh:bobs-org/bob-cli
%id(chop.refresh_docs.bob-cli.0_794067.1, tribe=chop)
%queue(capacity=1)
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

I'll refresh the bob-cli docs against the current code and the changes since the last documentation update, and I'll only touch documentation files. First I'm reading the repo layout, existing docs, and recent history.

The README and command guides are the user-facing surface. Next I’ll compare them with the CLI and with commits since the last documentation refresh.

Several guides lag the code: plugins has not been updated since August, and a randomize fix landed after its guide. I’ll compare those contracts, plus the README index, against the current CLI.

The guides mostly track the code. The gaps are the project-note capture forms, randomize’s date-range rules, a wrong block-ID character class, and a few command synopses that omit flags the CLI actually accepts. I’ll update those docs to match the current behavior.

The documentation edits are in place. I'll check them against the current CLI behavior, run the repo's documentation checks, and finish the refresh.

The new pages match the CLI. I'll tighten a few sentences so the overflow, charset, and width rules read as the behavior itself, then check links.

User-facing docs now match the current CLI. Only Markdown changed: `README.md`, `docs/README.md`, `docs/capture.md`, `docs/randomize.md`, `docs/highlights-ref-sync.md`, `docs/plugins.md`, and `docs/gkeep.md`.

The guides now cover the behavior that had drifted since the last refresh:

- `bob randomize` rejects an `--until +N` that cannot be added to today (exit 2, stderr only, stdout empty). A representable cutoff whose priority roll or 35-day load horizon leaves the calendar fails at plan time (exit 1) with `priority window rolls beyond the supported date range from <date>`, and that failure has no hint line. Ordinary windows and dates such as `9999-12-31` still roll.
- `bob capture` rejects an `s:<N>` or `p:<N>` roll that leaves the calendar with `scheduled offset is out of range` (exit 2). A `p:<N>` past the configured level count names `p:1` through `p:<count>` and the configured labels. Routes may contain `_`; block IDs may contain letters, digits, and `-`.
- The README now includes project-note markers (`@route^id+` and `@route:id+`), the vault files those commands write, the real `bob randomize` and `bob highlights` flags, and the shared config file used by priority rolls, randomize, highlights hooks, and `bob gkeep`.
- `COLUMNS`, when it is a positive integer, is the width `bob plugins list` and `bob gkeep` use for human tables. Otherwise those tables use 100 columns. `bob randomize` lays task lines out for a fixed 100 columns.
- `bob highlights --no-hooks` before `scan` or `doctor` skips the pre-scan hook. The same parent flag before `create`, `marker`, or `sync` is accepted and ignored.

This repository has no documentation-check recipe (`just all` is format, clippy, and tests). I checked relative links and heading anchors in `README.md` and `docs/`; they resolve.

Two help one-liners in `src/runner.rs` are stale, and the source was left unchanged:

- `nightly` is labeled "Run the nightly Obsidian sync and maintenance steps". `bob nightly --help` and the command run Git `vault-sync`, then `move-done-tasks`, then `vault-sync`.
- `query` is labeled "Run Dataview queries against the Bob vault". `bob query --help` and the command also run Obsidian Tasks queries.

The guides describe those commands as they actually run. `docs/README.md` tells readers to use `bob <command> --help` for usage, and to treat the one-line labels in `bob --help` as a short index.
