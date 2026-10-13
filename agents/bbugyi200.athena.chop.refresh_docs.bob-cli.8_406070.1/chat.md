# Chat History - ace-run (chop.refresh_docs.bob-cli.8_406070.1)

- **TIMESTAMP:** 2026-10-13 08:09:47 EDT
- **MODEL:** grok/grok-4.7
- **AGENT:** chop.refresh_docs.bob-cli.8_406070.1

## Prompt

#gh:bobs-org/bob-cli
%id(chop.refresh_docs.bob-cli.8_406070.1, tribe=chop)
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

I'll refresh bob-cli's user-facing docs against the current code and the changes since the last documentation pass. First I'm locating the docs tree, the last refresh, and the repository's documentation checks.

The docs live under `docs/` plus the root README. Next I’ll find the last refresh and the checks that guard those files.

Three behavior commits landed after the cascade docs. I’ll read those changes and the guides they should match.

The last full refresh was October 8. I’ll compare the guides with the CLI and the behavior that landed after that.

The guides still describe an older review queue, and a few command summaries omit behavior that landed after October 8. I’ll update those user-facing pages to match the code.

The jobs footer and the two scan schedules disagree. I’ll state what each one actually does.

Link checks on the edits are clean, and whitespace is clean. Next I’ll run the repository’s documentation build and doctests.

Documentation edits are in place and the checks passed. I'll confirm the diff, remove the scratch checker, and submit the final declaration.

The docs diff matches the six files this run wrote. I'll declare that commit and hand it to the finalizer.

The user-facing docs now match the current review walk, project blocking, and the command flags that drifted after the 2026-10-08 refresh. Six documentation files changed. No source, tests, or build files were edited.

**Onboarding.** The README daily workflow and `docs/getting-started.md` now describe schema 14: the walk is PRE → NEW → PROJECTS → PENDING → NEXT → RECURRING → TICKLER → ROTTEN → POST. A due recurring occurrence walks in RECURRING and is never freshness-stamped. TICKLER includes a Ready task whose future schedule has arrived, and one recovered automatically from Blocked on or after its stamp. PRE/POST `#gtd` checklist rows still walk when they are recurring, on the daily note, or linked to Today. A blocked or future-scheduled checklist row stays out. `bob stats` is listed with the other read-only glances.

**Project close.** While a project's `^prj` line is blocked, every open resident is Blocked and tagged `#prj_is_blocked`, and that reason passes through sub-projects. By default (`plan.link_unblocked`), a close links dependents it fully unblocked and can pull an emptied project's `^prj` in as Next.

**Command pages.** Synopses now include `plugins sync -f`, `ref scan -f`, `gkeep pull -P`, `capture-pomodoros --tasks`, and `URL %` listen (standalone `@` is the same listen request). A valid `@route` on a Keep note chooses the clip's parent ahead of `-P` and the prompt. An invalid `-P` fails before any clip. `capture-rewrite` is described as lexical: it does not open the vault, the clipboard, or the URL routing config. `capture-parse` does read that config. `docs/ref-jobs.md` now distinguishes the installed 15-minute Highlights bridge cron, which writes notes, from the separate hourly dry-run scan recipe.

**Checks.** `cargo doc --locked --no-deps` and `cargo test --locked --doc` both exited 0 (0 doc-tests). `git diff --check` was clean. Local Markdown links added in this pass resolve. The compile produced existing rustc warnings in reference and Keep code. Those warnings are outside this docs change.

**Suspected code bug, left unfixed.** `bob capture-parse --help` and its long about text say the command never touches the filesystem. `load_parse_routing` calls `UrlRoutingPolicy::load()` unless `-R` / `--no-ref`. The guides already describe that config read. The help text still does not.

Guides already record three other behaviors: an empty `bob ref jobs` list, including `--all`, still says "nothing in the last 7 days"; in-flight ref dedup compares URL keys across the shared spool without checking the destination vault; import dedup ignores list-valued `source_url` / `url`. The `bob ref jobs` footer always prints that the Mac runs the scan every 15 minutes, which matches the installed cron and does not name the hourly dry-run recipe.
