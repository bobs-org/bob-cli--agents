# Chat History - ace-run (0dw--plan)

- **TIMESTAMP:** 2026-08-25 19:02:12 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** 0dw--plan

**Plan:** /home/bryan/.sase/plans/202608/em_dash_snippet.md


## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add a new `--` snippet that expands to an em-dash when the user presses `<tab>`? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.


## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202608/em_dash_snippet.md`

> # Add a Tab-expanded em-dash snippet to Bob Mac Capture
> ## Outcome
> Teach the native Bob Mac Capture editor one local typing snippet: when a collapsed caret
> sits immediately after `--`, pressing plain Tab replaces those two ASCII hyphens with
> the single Unicode em dash `—` and leaves the caret immediately after it. Keep Bob CLI
> authoritative for capture grammar, parsing, completion, preview, and writes; this is an
> AppKit editor assist in the linked `bob-mac-capture` repository only.
> ## Current behavior and constraints
> - `Sources/BobMacCapture/CaptureKeyCommandRouter.swift` routes plain Tab to completion
>   acceptance when completion is visible and otherwise to continuation-bullet

*See full plan file for details.*

