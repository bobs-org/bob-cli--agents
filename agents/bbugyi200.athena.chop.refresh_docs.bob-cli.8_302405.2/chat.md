# Chat History - ace-run (chop.refresh_docs.bob-cli.8_302405.2)

- **TIMESTAMP:** 2026-10-08 04:15:38 EDT
- **MODEL:** grok/grok-4.7
- **AGENT:** chop.refresh_docs.bob-cli.8_302405.2

## Prompt

#gh:bobs-org/bob-cli
%id(chop.refresh_docs.bob-cli.8_302405.2, tribe=chop)
%wait:chop.refresh_docs.bob-cli.8_302405.1
%queue(capacity=1)
Inspect the documentation changes made by the update agent for bob-cli.

Verify every changed description against the current system behavior rather than
assuming it is true. Improve clarity for a new user, especially where terminology or
workflow ordering could be misunderstood. You may only create, modify, or delete
documentation files, such as Markdown or other docs-tree content, READMEs, and
doc-adjacent assets. You MUST NOT create, modify, or delete source code, tests, build
configuration, or any other non-documentation file, even to fix a bug you are
confident about.

When documentation and code disagree, document the actual current behavior; never
change the code to match the prose. If you identify a suspected code bug, describe it
in your final response so a human or separately scoped agent can pick it up (and you
may also note it in the commit message body), but do not fix it. Run the repository's
documentation checks when you change files.

## Response

I'll inspect the update agent's documentation changes and check each claim against the current bob-cli behavior before editing any docs.

The update agent refreshed ten Markdown guides in `4a6d82e`. I'll read that diff and check each claim against the code.

The refresh covers routing, jobs, Keep imports, and renderer prerequisites. I'll check those claims in the code before rewriting anything.

The previous pass verified the update agent's docs against the code. I'll tighten the wording that still disagrees with current behavior, then run the repository's documentation checks.

The update agent's facts mostly match the code. I'll correct the places a new user can still misread: the reading-queue wording, the scan schedule, dry-run side effects, and a few command details.

The wording matches the code. Next I’ll check the Markdown and run the repository’s documentation checks.

The fence mismatch in `docs/capture.md` was already on `HEAD`. I’ll run the documented checks next: `cargo doc`, doctests, and `git diff --check`.

The refresh was mostly accurate. The guides now follow what the commands actually do, especially where "reading queue" was used for two different stages.

A bare `bob capture` link, and a URL-only Keep note, produce a background job or an intake PDF. The success text says "reading queue" at that moment. `bob ref list` shows the note only after `bob ref scan`. Getting started now walks that order: capture, `bob ref jobs`, `bob ref find --include-intake` while the PDF is still in `xlib/`, then scan, then list.

Other corrections, checked against the current code:

- The published Mac scan runbook is hourly and starts as `bob highlights scan --dry-run`. The `bob ref jobs` footer still prints "every 15 minutes."
- `bob ref create --dry-run` skips installing the PDF. A web article still opens the browser and loads the page. A PDF URL and an arXiv target are still downloaded. Markdown returns before pandoc.
- Browser discovery uses Google Chrome at the usual paths, then Playwright's bundled Chromium. Another executable, including a system Chromium package, is used when `BOB_CHROME` points at it.
- Capture previews now include legacy notes (a fresh copy is still queued) and an unavailable library check (the clip is still queued). `placement: "queued"` means a job will be written.
- `capture: false` and `gkeep: false` are silent. An invalid routing file warns on `bob capture` and `bob gkeep`, and stays silent on `bob capture-parse`.
- Human `bob ref list` hides legacy-era rows behind `+ N zorg-era legacy notes hidden` until `-s`. `unread` maps to `queued`, so those notes match the default filter and still appear only in that summary.
- Tasks `by function` instructions, including ones merged from a global query, use a 2-second expression budget and an init budget of 10 seconds plus 5 milliseconds per indexed task, capped at 120 seconds.
- `!note:block-id` completes that open task, retires its Pomodoro Task Links, and returns a Blocked dependent to Ready when that dependent names the task directly, has no other open dependency, and has no future scheduled date.

`git diff --check`, `cargo doc --locked --no-deps`, and `cargo test --locked --doc` passed. Only documentation files were changed.

Suspected code bugs, left unfixed:

- In-flight ref dedup compares URL keys across the shared job spool without checking the destination vault. A pending job for one vault makes the same link look "already clipping" in another. `bob ref jobs` does not print each job's vault.
- Import dedup keeps only string `source_url` and `url` values. YAML lists, including a one-element list, are indexed by `bob ref find` and missed by import dedup.
- The `bob ref jobs` footer hardcodes "the Mac runs it every 15 minutes." The published scan runbook is hourly and starts as a dry run.
- An empty `bob ref jobs --all` list still says "nothing in the last 7 days."
- `bob capture-parse --help` says the command never touches the filesystem. It reads the URL routing config file.
