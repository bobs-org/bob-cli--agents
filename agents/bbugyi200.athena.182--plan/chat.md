# Chat History - ace-run (182--plan)

- **TIMESTAMP:** 2026-11-04 13:18:51 EST
- **MODEL:** claude/opus
- **AGENT:** 182--plan

**Plan:** /home/bryan/.sase/plans/202611/mac_capture_backslash_goto.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/mac_capture_backslash_goto.md`

> # Plan: `\` opens the Go To (`/`) task search in Bob Mac Capture
> ## Goal
> In Bob Mac Capture, typing `\` into a blank capture draft opens the same Go To
> task-search picker that typing `/` opens. `/` keeps working. Because `Command-\` is
> already the global Capture alias (Settings › Hotkey › **Also open Capture with
> Command-\\**, on by default), pressing `Command-\` and then `\` from any macOS app
> searches tasks: the first press opens or focuses Capture with the editor focused;
> release Command, and `\` opens Go To. `Command-\` `Command-\` still opens today's
> Pomodoro and is unchanged.
> All work happens in the **`bob-mac-capture`** linked repository. Open it with

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make it possible to activate the `/` task search panel in the
bob-mac-capture app by typing the `\` key (in addition to the `/` key), which will allow
the user to search for tasks from any app on their mac by pressing `<cmd+\>\`? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.

%m:@xlarge

## Response

Exploring the bob-mac-capture repo to find where the `/` task search panel is triggered.

Tracing how typing `/` opens the Go To picker in the Mac app (it's driven by bob's `capture-complete`/`capture-parse` responses).

Key finding: a leading `\` is already a capture-grammar escape (`\#fix`, `\%c`, `\$3`), so the design needs care. Reading the Mac key router next.

Still exploring: checking `hasDraft` semantics and the global Command-\ show path.

Checking which capture escapes start with a leading `\` (to judge how much a `\` alias would collide with them).

Validation passes. Submitting the plan.

I've written the plan and submitted it for your approval. Nothing has changed in either repo yet; the work starts only after you approve it.

**How it would work:** this is a key binding in bob-mac-capture only. Bob's capture grammar doesn't change.
- Typing `\` into a blank draft replaces it with `/` and puts the caret after it. From there it's exactly the existing `/` path: bob reports Go To, the picker opens, and Command-X, Escape, Backspace and Control-C behave as they do now.
- So from any app, `Command-\` opens Capture, and then `\` opens the task search. `Command-\` `Command-\` still opens today's Pomodoro.
- If Capture reopens on a leftover `/` draft, `\` keeps you in Go To (it reopens the picker if it was closed) instead of typing `/\`.
- Holding `\` opens Go To once and does nothing more.
- Everywhere else `\` types normally: a draft that already has text, a Go To search that already has text, other pickers and prompts, and Bob Refs.

**Why not change bob's grammar instead:** a leading `\` is already the capture escape character (`\#fix`, `\# Heading`, `\#now`, `\%c`, `\~`). Making `\` mean Go To in the grammar would break captures like `bob capture '\#now'` and affect every capture client, not just the Mac app.

**One choice for you when you review (`literal_backslash`):** the binding would otherwise stop you starting a draft with one of those escapes.
- **double** (my default): pressing `\` a second time immediately turns the `/` back into a literal `\`. So `\\#fix …` gives `\#fix …`.
- **none**: no escape key. To start a draft with `\` you'd paste it, or type it after other text and move the caret back.

**Limitation:** if Capture reopens with a half-written capture still in it, `\` types a literal backslash, just as `/` would. You'd stash it with Control-C or clear it first. The binding also relies on the "Also open Capture with Command-\\" setting, which is on by default.

The plan also covers router and live tests, and updates to `docs/keyboard.md`, `docs/task-pickers.md` and `docs/settings.md`. For checking, it follows the repo's `AGENTS.md`:
- `just portable-check` on athena;
- a best-effort scratch compile on the Mac, which must be reported as unverified if the Mac is offline;
- `just docs-check`;
- the macOS CI run, reported as observed.
