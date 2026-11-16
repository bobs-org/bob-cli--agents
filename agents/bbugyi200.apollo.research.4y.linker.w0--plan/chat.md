# Chat History - ace-run (research.4y.linker.w0--plan)

- **TIMESTAMP:** 2026-11-16 11:00:21 EST
- **MODEL:** claude/opus
- **AGENT:** research.4y.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/obsidian_ctrl_w_numbered_tab_jump.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/obsidian_ctrl_w_numbered_tab_jump.md`

> # Plan: Ctrl+W N — numbered tab hints and an in-place tab jump
> ## Context
> Epic `bob-cli-m0` shipped the `Ctrl+W` window prefix in `bob-navigation-hotkeys`:
> `h`/`l`/`w` focus splits, `H`/`L` move a tab, `v` splits, with an armed ring, a card
> after a 300 ms pause, and palette commands. Its plan
> (`plan:202611/obsidian_ctrl_w_window_prefix.md`) reserved digits for later; today an
> armed digit is consumed as "‹N› isn't a window key".
> This epic gives digits to tabs. The design basis is the consolidated research
> `research:202611/obsidian_ctrl_w_numbered_tab_jump/obsidian_ctrl_w_numbered_tab_jump.md`,
> and Bryan accepted every requirement it recommends. Read it with `sase artifact read`

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I recently added support for keymaps that are prefixed with `<ctrl+w>` to make
it easier to manage split windows in Obsidian (see the bob-cli-m0 epic bead for
context). I would now like to add support for the new `<ctrl+w>N` keymaps, which should
trigger a jump to the `N`th Obsidian tab. Can you help me implement this?

- `N` should be determined by a hint that is rendered next to each file's name in
  Obsidian's tab title bar.
- The tab that we jump to should remaining in the same vertical window that it was in
  before invoking the `<ctrl+w>N` keymap.
- Review the obsidian_ctrl_w_numbered_tab_jump.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.4y.linker

## Response

I'm gathering context: the shipped Ctrl+W epic and its plan, plus the tab-jump research report, before designing.

It's a directory; locating the report inside it.

I've read the shipped epic plan and research; now reading the shipped window-prefix code so the plan targets real seams.

Still reading the shipped hint painter and commands; then I'll look at the research mockups and draft the plan.

Research and shipped code are in hand. Now checking a few remaining facts: hotkey-manager usage, the e2e and preview harnesses, the docs page, and any existing bead for the `selectedTab` bug.

Reading the `docs.md` reference memory, since the plan includes a docs change.

Checking Bryan's vault theme and snippets, because the numeral technique relies on an unused `::before` slot.

I have what I need for the design. Checking the raw m0 plan's frontmatter so the epic phase format matches what validation expects.

Design is settled. Quick check that no memory note would become false (e.g. one stating digits are reserved), then I'll write the plan.

No memory note is affected. Writing the epic plan now.

Validation passed. Two small additions before the final validation: a CSS hint for the "you are here" cap, and a fix for an edge case where the flash would be invisible on Linux.

Staged. Finishing the turn through `/sase_final`.

I wrote the plan and submitted it for your approval; it passed validation with no warnings. No files were changed and nothing starts until you approve.

**What you'll get:** every tab in the main editor area shows a small number (1–9) just before its title. `Ctrl+W` then that digit focuses exactly that tab where it already sits. It is never moved, copied or reopened, so its editor state, undo history and scroll position survive. All the research requirements are kept: tabs are numbered across all splits, the numbers are always shown, digits only go up to 9, and the jump never moves a tab.

**How it looks and feels:**
- **At rest:** the numbers sit in the empty space Obsidian leaves before Markdown tab titles, in the same colour as the title beside them. They're always there, so the tab bar never shifts.
- **When the `Ctrl+W` card appears:** the numbers light up as accent-coloured key caps, and the tab you're on gets a plain outlined cap ("you are here").
- **After a jump:** the destination's number flashes solid for 220 ms while the focus ring moves to its split. A quick `Ctrl+W 3` shows only that ring and flash.
- **On the card:** each split's tab-count bubble becomes its number range (`1–3`, `4–6`), and one row is added: "`1–6` # jump to that tab · it stays in its split".

**Behaviour you might not expect:**
- **Linux:** Obsidian's Close tab still owns `Ctrl+W` there (your earlier "keep" choice), so the numbers stay hidden; they appear on their own if you ever rebind it.
- **Reserved keys:** `0` and Shift+digit do nothing for now; Shift+N is kept for a future "bring tab N here".
- **`Cmd+1…9`** still go to the Nth tab within the current split. Nine new commands, "Jump to tab 1…9", make a one-line rebind possible if you want those keys to follow the numbers.
- **Stale numbers:** if the tabs changed between pressing `Ctrl+W` and the digit, it refuses with "Tabs changed — try again" rather than jumping to whichever tab now holds that number.

**Places I deviated from the research:**
- The numbers take each tab title's own colour variables rather than fixed ones, so themes stay coherent.
- If the card ever shows on a machine where the numbers are normally hidden (e.g. Linux via "Show window keys"), they appear while it's up, so the card never names numbers you can't see.
- The screen-reader label says "Control W then N"; the attribute the research suggested can't express a two-key sequence.
- The digit for the tab you're already on still flashes, to confirm it.

**How it's split:** five phases, all in bob-plugins:
1. **model:** numbering logic and digit planning.
2. **actions:** the jump itself, checked against real Obsidian on athena.
3. **paint:** tab numbers, card changes and light/dark previews; runs in parallel with actions.
4. **prefix:** connects digits to `Ctrl+W`, adds the commands and turns the feature on.
5. **finish:** docs, screenshot review in real Obsidian, and polish.

Each phase deploys to your vault as it finishes, so nothing visible appears until the prefix phase turns everything on at once. That avoids a stretch where numbers show but digits don't work.

One fix to existing code is folded in: Obsidian 1.15.1 no longer has the property the shipped `Ctrl+W` code reads to find each split's selected tab. Today that only bites when a failed `H`/`L` move is undone, and it was recorded only as a note on bob-cli-m0, not as its own task.

I didn't add any approval-time decisions (you asked me to lead), and no memory notes need changing.
