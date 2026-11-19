# Chat History - ace-run (research.5g.linker.w0--plan)

- **TIMESTAMP:** 2026-11-19 10:00:04 EST
- **MODEL:** claude/opus
- **AGENT:** research.5g.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/copy_chips.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/copy_chips.md`

> # Plan: Copy chips
> ## Context
> Bryan asked for a button or link in Obsidian that copies author-chosen text to the
> clipboard and is easy to create by typing. The consolidated research report
> (`sase artifact read research:202611/obsidian_copy_chips/obsidian_copy_chips.md "<why>"`)
> designed a **copy chip**. Bryan accepted every requirement in it: the adjustments
> A1–A10, the reliability rules R1–R14, the code-span syntax, the `bob-copy` fence, and
> Mod+Shift+Y. Every phase worker should read that report first. This plan carries out the
> report's phases 1 and 2 and their adoption in the vault. Its phase 3 (snippet picker,
> masked chips, rich text) is deferred, and the adopt phase records it as proposed

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I wish there was some way to create a button/link in Obsidian that, when
pressed, copied some (configurable at the point of button/link creation) text to my
clipboard. Can you help me implement this?

- It should be aasy to create a new instance of these buttons/links in Obsidian by
  typing (think hard about the best way to implement this).
- As our first use-case for this functionality, I would like to start using a copy chip
  for the agent prompts recommended in some daily tasks in the ~/bob/gtd_daily.md file.
  Leave appropriate notes on the bob-cli-nh epic bead so that epic lander knows that a
  copy chip should be used for that epic's related GTD task.
- Review the obsidian_copy_chips.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5g.linker

## Response

Reading the copy-chip research report first, then the bob-plugins architecture, the GTD note, and the `bob-cli-nh` epic.

Research is thorough. Now the bob-plugins repo layout and conventions.

Mapped the plugin conventions. Two things remain: the vault conventions memory note (the plan edits `gtd_daily.md`) and whether bob-cli's own docs list the plugins.

I have enough context to design. Before writing the plan I'm loading the memory-write skill, since the plan will propose a decision record and a glossary term for copy chips.

Design settled. Writing the epic plan skeleton first to learn the validator's schema.

Writing the full epic plan now.

Valid. Proposing it now.

Staged. Next I'm adding the copy-chip note to the `bob-cli-nh` epic, so I need the archived plan reference.

Both notes are recorded. Finishing the turn with the SASE final declaration.

I've submitted the copy-chips plan for your review, and nothing is built yet. Typing `` `copy: ssh apollo` `` in a note gives a small pill with a copy icon, and one click copies exactly that text. The design follows the research report you agreed with; I added a few choices of my own, listed below.

**How you'd use it**
- **Type it.** Use an inline code span starting with `copy:`, or `copy[Label]:` to show a short name instead of the text. Text with backticks inside uses a double-backtick run.
- **Long text.** Put it in a `bob-copy` fenced block, which renders as a titled card with a Copy button.
- **Make one without typing the syntax.** `Mod+Shift+Y` opens a small card prefilled from your selection, the clipboard, or the chip or code span under the cursor. It shows a live preview and the exact Markdown, handles all escaping, and Enter writes it in one undo step.
- **Copy it.** Click (or tap) the chip. From the keyboard, `gy` in normal mode copies the chip on the cursor line, and so does `Mod+Y` then `C`. The chip flashes green like a Vim yank.
- **What it looks like.** A thin-bordered pill using only theme colours. A labeled chip's tooltip shows the full text. Success swaps the icon to a green check with no toast; a failed copy always shows a Notice.

**Design choices I added beyond the research**
- `Mod+Shift+Y` on an ordinary code span turns it into a chip in one step.
- `gy` and `Mod+Y C` pick a chip the same way: the one under the cursor, otherwise the only one on the line. With two or more on the line and the cursor on neither, they refuse rather than guess.
- The card refuses to write if the note changed while it was open.
- Alt+Click on a chip opens it for editing; there's no pencil icon on hover.
- The GTD prompt chips are labeled ("⧉ last-week prompt") so the walk rows stay short; hovering shows the full prompt.

**How the work is split:** six phases, built in Bob Plugins as a new `bob-copy-chips` plugin plus a `C` row in the Copy card.
1. Create the plugin and the shared rules for reading and writing chips. This includes adding it to the plugin list in your chezmoi config, since `bob plugins sync` only deploys plugins listed there.
2. Chips in Live Preview and Reading view, the click and keyboard copy, and the look.
3. The `bob-copy` block card.
4. The Copy card's `C` row (runs alongside phases 3 and 5).
5. The `Mod+Shift+Y` card and Alt+Click.
6. Adoption: add `gy` to your vimrc, then turn the agent prompts in the open rows of `gtd_daily.md` into labeled chips. That covers the last-week, last-quarter and last-year prompts, plus "Summarize yesterday" once it exists.

**Decisions for you:** two memory toggles, both off by default because you didn't ask for memory changes: a decision record saying chips are code spans with literal text, and a "Copy Chip" glossary entry.

**`bob-cli-nh`:** I added a note on the epic and a short pointer on its adopt phase (`bob-cli-nh.8`), which writes the new GTD rows. They give the exact chip Markdown for the "Summarize yesterday" prompt, say to keep existing chips when rewording the review rows, and ask the lander to check before closing. The note says to write the chip even if the plugin hasn't shipped yet, since it reads as plain inline code until then. If that row lands with a quoted prompt anyway, phase 6 converts it.

**Things you'll need to do**
- Reload Obsidian after each deploy.
- On apollo and the Mac, run `chezmoi apply` and `bob plugins sync` before chips show up there.
- If Obsidian overwrites the enabled-plugins list before you reload, turn the plugin on in Settings → Community plugins.

One unrelated problem I found: `bob-emoji`'s plugin folder is tracked in the vault's git and missing from its `.gitignore`. Phase 6 records it as a proposed follow-up.
