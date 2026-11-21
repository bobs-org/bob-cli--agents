# Chat History - ace-run (research.5o.linker.w0--plan)

- **TIMESTAMP:** 2026-11-21 10:27:45 EST
- **MODEL:** claude/opus
- **AGENT:** research.5o.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/prose_wikilink_completion.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/prose_wikilink_completion.md`

> # Plan: Wikilink completion in Bob's prose prompts
> ## Summary
> Bob already has `[[` completion in the Obsidian editor and in the Mac capture panel. It
> does not work in the prompts launched from those surfaces, so Bryan types links like
> `[[sase#^ref-sase-1n6-11-4-restart-readiness]]` by hand. A typo leaves a dangling link
> without any warning. The write side already works: links in Work, Schedule, Rotten, and
> Cancel Log entries become Task Mentions; the Intention Card renders links; and
> `bob periods` repair retargets them. This plan adds the authoring side.
> The design follows the consolidated research report
> `research:202611/prose_prompt_wikilink_completion/prose_prompt_wikilink_completion.md`.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to start supporting Obsidian link completion in any free-form text
input prompt that we show to the user (ex: intentions, work log, etc...). Can you help
me implement this?

- This completion should be triggered by typing `[[`.
- Review the prose_prompt_wikilink_completion.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5o.linker

## Response

Reading the research report done; now exploring bob-cli and bob-plugins code to ground the plan.

Still exploring the existing recall-band code that the new link band must coexist with.

Plugin-side survey is back. Now checking the bob-cli side (capture_links.rs defects, tiers, fixtures).

Quick bob-cli check on tier inputs (Highlights library roots, archive paths) that a JS port would need.

Now checking the Mac app's Pull-In reason prompt and bob's `capture-complete` CLI shape for the Mac phase.

Reading the project memory that governs new CLI options, docs, and the relevant key-handling decisions.

Checking one constraint I spotted: bob suppresses block-link completion in Work Log text — need to know whether log writers reject `#^` links.

Verifying the two known defects live, plus a suspected third one (target replacement eating an authored `#heading|alias`).

Checking whether Rust's block matching uses preview text (affects whether the JS port must read file contents).

I have enough grounding. Let me get the epic plan schema from the validator before authoring.

I have the full picture. Writing the epic plan now.

Validation passed. One fix: per the memory-write rules, a reviewer-declined memory decision should produce no follow-up, so I'll correct that line and revalidate.

Validated clean. Proposing the plan.

I've written the 10-phase plan, it passes validation, and it's staged for your review. Nothing has been implemented yet; work starts once you approve.

**Design decisions I made**
- **One controller.** A shared `proseField` controller in bob-navigation-hotkeys owns two modes: today's USED BEFORE recall and a new LINK band opened by `[[`. Every prose prompt goes through it, so behaviour can't drift between prompts.
- **Fast, local suggestions.** Suggestions come from Obsidian's in-memory note index, not a `bob` call per keystroke (about 0.4–1.2 s each). The JS ranking replays the same shared test cases as bob, so the two can't drift apart.
- **Enter never submits a half-typed link.** While the band is open, Enter and Tab insert the selected link and keep the prompt open. With no matches, Enter just closes the band. Esc and Ctrl+[ close only the band, and `q` still types. One Ctrl+Z restores what you typed, and a held Enter can't insert and then save.
- **Look.** The band sits in the recall band's slot and stays the same height while open, so the field never moves. Rows show an icon, the note name with the match highlighted, its folder, and a small tag only when it matters (Alias, H2, `^id`, Archived). The bottom line shows exactly the link that will be inserted, e.g. `↵ [[sase_blog_zettel]]`. An empty `[[` shows nearby notes (parent, linked, recent). Typing `#` or `^` on a row jumps to that note's headings or blocks.
- **Each prompt opts in explicitly.** The research suggested existing prompts get links with no code changes. Instead, each prompt opts in and states which note `[[#heading` links resolve against. A final lint phase fails the build if any text field in the plugins doesn't declare whether it's prose or literal.

**A third bob bug.** While checking the two known defects, I found another: `See [[sa▏#Overview|our plan]]` returns a replacement range covering `sa#Overview|our plan`, so accepting any suggestion deletes the heading and label. Phase 1 fixes it along with the other two.

**Phases**
1. bob-cli fixes, the shared test cases, and a new decision record.
2. The note matching and ranking engine in the plugins.
3. The band itself, piloted on the Work summary prompt and checked in real Obsidian (undo, IME, Esc layering).
4. Phases 4–7 run in parallel after phase 3:
   - the standalone modal prompts (including Notebook and Mail);
   - the Task Card stages, including the scheduled-date reason;
   - the Intention Card;
   - the Record Card, whose link stage moves onto the same engine.
5. Phases 8–9 run alongside: `capture-complete -L/--links-only`, then the Mac Pull-In reason.
6. The lint and an end-to-end walkthrough.

**Left out on purpose:** `((` task links (they create block IDs, which writes to the vault), the Mac event-note editor (gcal escapes `[`, which would break links), and pop-ups anchored at the caret.

**Two decisions for you at approval:**
- **Inserted link text.** The default is bob's full vault path (`[[2026/2026-11-21]]`); the alternative is Obsidian's shortest form (`[[2026-11-21]]`).
- **Decision record.** On by default: write a decisions-memory record of the `[[` scope rule and the Enter rule. I based that on your agreeing with the research, which says to record them; turn it off if you don't want it.
