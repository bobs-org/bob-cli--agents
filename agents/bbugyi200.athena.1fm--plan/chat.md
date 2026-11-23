# Chat History - ace-run (1fm--plan)

- **TIMESTAMP:** 2026-11-23 11:31:01 EST
- **MODEL:** claude/opus
- **AGENT:** 1fm--plan

**Plan:** /home/bryan/.sase/plans/202611/highlights_ctrl_return_task_key.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/highlights_ctrl_return_task_key.md`

> # Plan: Highlights Control-Return opens the reference's reading task
> ## Goal
> Add a Highlights-frontmost takeover key, **Control-Return** by default, to Bob Mac
> Capture. It opens the focused PDF's reading task (the reference's single `#task #ref`
> line, called the Reference Task in the glossary) in Obsidian. The result must match what
> the user gets today by pressing **Command-T** in Highlights (Bob Refs opens in Tabs from
> fresh defaults with the focused PDF selected) and then **Control-Return** in Bob Refs
> (open the selected row's reading task).
> All code and docs changes live in the linked **`bob-mac-capture`** repo. Open it with
> `/sase_repo` (`sase repo open bob-mac-capture -r "<why>"`) and read its `AGENTS.md`

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add a new `<ctrl+enter>` keymap to the highlights app that
opens the corresponding ref task (like the user pressed `<cmd+t>` before
`<ctrl+enter>`)? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Looking at the Bob Refs / Highlights keymap docs to pin down what `<cmd+t>` and `<ctrl+enter>` currently do.

Now the coordinator paths: `toggleRefsTabs` and `openRefsCopyFromHighlights` (the latter likely resolves the current Highlights tab to a ref).

Reading how Control-Return's `openSelected(.task)` actually opens the task, and whether it hides the panel.

Now checking where the takeover keys are documented and tested, so the plan covers docs, settings, and tests.

Mac-capture docs in bob-cli are generated from bob-mac-capture's `docs/`. Checking the hotkey-conflict guide and the docs memory note, since the plan will touch user-visible docs.

I have the code shape. Reading the glossary definition of "Reference Task" so the plan uses the project's terminology correctly.

Fixing the validator errors: adding `title`/`goal` and shortening the decision strings to fit the length limits.

Validation passes with 0 warnings. Submitting the plan.

I've written and submitted the plan. It passed validation with no warnings and is now waiting for your approval; nothing has been implemented yet, and the only file I created is the plan itself.

**Where the work goes.** "The Highlights app" turned out to be the Highlights hotkeys in Bob Mac Capture, so every change is in the linked `bob-mac-capture` repo. Those hotkeys only work while Highlights is the active app. Today, ⌘T there opens Bob Refs on its Tabs view with the current PDF selected, and ⌃↩ in Bob Refs opens that reference's reading task in Obsidian. No bob-cli change is needed: the mac-capture docs in bob-cli are generated copies.

**What the plan adds:**
- **The key:** ⌃↩ in Highlights opens the current PDF's reading task, using the same Obsidian link Bob Refs' ⌃↩ uses, so both land on the same task line.
- **A setting:** "Reading task key in Highlights" in Settings › References, with Control-Return (default) or Off, wired up like the existing ⌘Y/⌘B/⌘L keys.
- **No clash with Capture:** the Capture panel doesn't make Bob the active app, so Highlights stays in front while Capture is open over it. Capture uses ⌃↩ heavily (capture and open, picker actions, Go To). The new key therefore switches itself off while Capture or Bob Refs is open, so their own ⌃↩ keeps working. The existing ⌘O/⌘T/⌘Y/⌘B/⌘L keys are left as they are.
- **When the task can't open:** you land on the same Tabs view ⌘T shows, with a banner saying why. The reasons are: the PDF isn't in your Bob library, two references match it, no document is open, Highlights didn't answer within 2 seconds, or the reference has no reading task. If Bob lacks Accessibility permission, the existing permission card explains instead.
- **Tests, docs and checks:** tests for when the key is active, the routing, and every failure case. Docs updates to `keyboard.md`, `refs.md`, `settings.md` and `permissions.md`. The checks the repo's `AGENTS.md` requires: compile on the Mac, the macOS CI pre-check, and watching CI go green after the push.

**One decision for you at approval:**
- **headless (default):** pressing ⌃↩ takes you straight to the task in Obsidian, and Bob Refs only appears when something goes wrong.
- **panel:** Bob Refs briefly appears on Tabs first, then the task opens, exactly like pressing ⌘T then ⌃↩. I defaulted to headless because on success the panel would appear only to vanish when Obsidian comes forward.

One thing I couldn't confirm: whether Highlights itself uses ⌃↩, for example in its note editor. The plan has the implementer check this on the Mac; if it does, the Off setting gives the key back to Highlights.
