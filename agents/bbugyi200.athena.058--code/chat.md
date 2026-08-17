# Chat History - ace-run (058--code)

- **TIMESTAMP:** 2026-08-17 17:59:29 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** 058--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202608/gh_bobs_org__bob_cli-ace_run-058__plan-260817_173917.md`
- **2. --code** — `~/.sase/chats/202608/gh_bobs_org__bob_cli-ace_run-058__code-260817_173917.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @sase/repos/plans/202608/task_id_prompt_focus.md

The above plan has been reviewed and approved. Implement it now.


## Response

I'll implement the approved Add-block-ID focus plan, starting by opening `bob-mac-capture` through the repo skill so all edits stay on that checkout.

Repo is open. Next I’ll read the capture model, view, tests, and README so the focus-adoption and deferred lock match the existing code.

The model already publishes the focus request; next I’ll inspect the tests and README so the deferred lock and adoption match the existing patterns.

The model already raises the focus request; I’ll add the deferred editor lock and control-level focus adoption next.

Model lock is in place. Next I’ll add focus adoption on the editor and block-ID field, and switch the editor disable path to the deferred lock.

View adoption is in. Next I’ll add the model tests and document the focus hand-off in the README.

The approved focus hand-off is implemented in the linked `bob-mac-capture` repo. Accepting a **Needs block ID** row still opens the Add block ID card; that card should now take keyboard focus in the same interaction so the ID can be typed immediately.

### What changed

Two independent fixes, as specified:

1. **Control-level focus adoption.** `CaptureFocusAdoption` lets the capture editor and the `^` block-ID field claim `model.focusRequest` after they are installed. The panel’s existing `onAppear` / `onChange` assignment stays as the synchronous fast path. When the adopter actually takes focus, it emits a `focus-adopted` signpost (`subsystem == "org.bobs.bob-mac-capture"`).

2. **Deferred editor lock.** `CapturePanelModel` now publishes `editorInputLocked`. Presenting the prompt still raises `.taskIDPromptBlockID` immediately, but the editor is not disabled until the next main-actor turn, and only if that same prompt is still open. Every prompt-clearing path (`cancelTaskIDPrompt`, successful assignment, `resetAnalysisState`, `prepareForDismissal`, plus retained-close / discard / empty-draft) unlocks the editor and invalidates a stale deferred lock.

The editor now uses `.disabled(model.isSubmitting || model.editorInputLocked)`. Footer buttons still disable immediately while the prompt is visible.

### Tests and docs

`CapturePanelModelTests` now covers:

- editor stays unlocked in the presenting turn, then locks on the next turn
- canceling before the deferred set never locks the editor
- successful assignment unlocks (`@Cash+new-id` and `@file+new-id`)
- a Bob failure keeps the prompt open and the editor locked
- `prepareForDismissal()` clears both the prompt and the lock

The README `@route+` bullet and Keyboard section now state the focus hand-off as a contract.

### Not verified here

`just format-lint`, `just build`, and `just test` cannot run on this Linux host (`platforms: [.macOS("26.0")]`, AppKit/SwiftUI). Land this through the normal stitch flow and require the **macOS 26 SwiftPM** job (lint, build, test, bundle, launch smoke test) to be green.

The `.task(id:)` adopter has **no automated coverage**. SwiftUI focus resolution needs a hosted window and an active app, which CI does not provide. Before the bead is closed, install the bundle on the Mac and run the plan’s keyboard-only checks: type into `^` without clicking, Return splices the ID and returns focus to the editor, Escape returns to the task list, an invalid ID keeps focus in the field, and a **Ready to use** row still inserts in one action.

I'll commit the implemented focus-handoff changes in `bob-mac-capture` using the git-commit skill, then confirm the repo is clean.

I'll record the commit skill, then inspect the `bob-mac-capture` working tree so the message matches only these changes.

The workspace root is clean; I'll inspect the linked `bob-mac-capture` checkout next.

The diff matches the approved focus hand-off. I'll write the commit message and commit it.

The commit ran in the workspace root by mistake. I'll rerun it from the linked `bob-mac-capture` checkout.

The commit is still running; I’ll wait for it to finish in this turn.

Commit landed and the tree looks clean. I’ll confirm it isn’t still ahead of upstream.

Committed the Add block ID focus hand-off in the linked `bob-mac-capture` repo.

**Commit:** `0350c8c` — `fix(capture): focus the Add block ID field when a missing-ID task is selected`

That stitch is on `master` and matches `origin/master`. The working tree is clean.

The change is the approved pair of fixes: control-level focus adoption on the editor and `^` field, plus a deferred editor lock so the prompt can take first responder before the editor is disabled. Model tests and README contract notes are in the same commit.

**Still unverified:** `just format-lint`, `just build`, and `just test` cannot run on this Linux host. The macOS 26 SwiftPM job still has to go green, and the `.task(id:)` adopter still needs the plan’s keyboard-only checks on a Mac before the bead is closed.
