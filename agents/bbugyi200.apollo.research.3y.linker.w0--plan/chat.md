# Chat History - ace-run (research.3y.linker.w0--plan)

- **TIMESTAMP:** 2026-11-09 12:14:48 EST
- **MODEL:** claude/opus
- **AGENT:** research.3y.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_alias_typing_tips.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_alias_typing_tips.md`

> # Capture alias typing tips
> ## Goal
> Bob Mac Capture swaps easy keys for capture sigils (`Buy milk .` → `Buy milk @`), but
> nothing teaches that. When Bryan pays for Shift to type a sigil that an unshifted alias
> key would have typed at that exact spot, the list or picker the sigil opens shows one
> quiet line at its foot:
> ```text
>  Buy milk @▌
>  ╭───────────────────────────────────────────────╮
>  │ ▌errands                            area      │  ← row 0 selected, unchanged

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to display a little hint to the user in the bob-mac-capture app
when they type a character that they could have used a capture alias for. Can you help
me implement this?

- For example, if they press `@` to select an area/project note, we should show a hint
  teaching them about the `.` alias.
- Review the capture_alias_typing_tips.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.3y.linker

## Response

Reading the alias-tips research report now, then I'll explore the Mac app and bob's capture code.

Research read. Now checking the newest `&`/`*` aliases (landed today, after the research) and the bob rewrite code.

Now exploring the Mac app (its AGENTS.md, the key-down filter, completion list, picker key hints, settings).

Checking how BobProcessClient lanes and the analysis debounce work, to size the tip's race budget.

Now the CompletionList view and picker key hints.

Checking the Mac Settings pattern and the docs word-budget constraint (several mounted Mac docs were already over the 6000-word cap).

Running a few read-only `bob capture-rewrite` probes to confirm the reverse-check behaviour for the newest `&`/`*` aliases.

Looking at the picker's detail strip, which already hosts "teach follow-up keystrokes" lines — a candidate home for picker tips.

Design is mostly settled. Before writing memory steps into the plan, I need the memory-write skill's routing rules.

Checking the Mac test harness conventions (design render tests, stubbed bob) so the plan points phases at real patterns.

I have what I need. Writing the epic plan now (bob contract → Mac core in parallel → completion-list host → picker host).

Fixing the frontmatter: adding title/goal/phases, converting memory decisions to `memory:` toggles, and shortening one label.

Validation passes. A quick sanity check that the plan has no workspace paths and the memory callouts landed in the right spot:

The plan is staged. Finishing the turn through the SASE finalizer.

I wrote an epic plan for the typing tips and submitted it with `sase plan propose`; it is staged for your review. I haven't changed any code. The plan follows the research report's requirements (R1–R12) and passes validation.

**How it works**

- **bob decides every tip.** `bob capture-rewrite --cursor` gains a `sigil_alias_tip` field. To fill it, bob puts the alias key in place of the sigil you typed and runs its normal alias rewrite. It sends a tip only if that rebuilds your draft and caret exactly. This is what stops a wrong tip: `.` typed at the start of a line stays a dot, so a leading `@` gets no tip. The Mac app never keeps its own list of aliases.
- **Only physical, costly keystrokes count.** The app asks only when you typed the sigil yourself with Shift or Option. Paste, Undo, picker accepts, held-down keys and the app's own alias output never trigger a tip. The check runs on its own background request and never delays the list, the preview or Return.
- **The tip appears where you're looking.** It is one line at the bottom of the list or picker the sigil opened: `Next time  [.] → @  after a word`. The key is drawn in the same keycap style as the picker's key hints, and the `@` uses the color it has in your draft. It has no icon, button or animation. It is there when the list first appears or not at all, and it stays put while you filter.
- **Tips fade as you learn.** Each alias gets a tip on its first 3 chances, then less and less often while you keep using the Shift key. It goes quiet once you use the alias on 75% of recent chances, and comes back if that drops below 50%. You see at most one tip per capture. Settings gets a "Show typing tips" toggle (on by default) and a "Reset typing tips" button.

**Phases**

1. **bob:** give each alias a stable id, add the tip check and JSON fields, and add tests so that every alias has a matching tip test plus a list of positions that must never get a tip.
2. **Mac core:** decoding, the fading rules and the local usage record. This needs nothing from phase 1, so the two can run at the same time.
3. **Mac list tips:** the flagship `.`→`@` and `/`→`#` tips in the completion list, end to end, plus Settings and a new `typing-tips.md` docs page.
4. **Mac picker tips:** `^ : + ~ & *` and move bullets in the pickers.

**Where I departed from the research**

- **New aliases included.** `.`→`&` and `;`→`*` landed after the research was written, so they're in the first release. The `&` tip says "once routed", because in `Buy milk .` the dot becomes `@`, not `&`.
- **Old bob is detected.** A new bob always includes `sigil_alias_tip`, set to `null` when there's no tip. When the field is missing, the app knows bob is older and stops asking.
- **Usage counts are kept by week.** The record is stored as readable JSON, so after about three weeks you can see whether you're using the aliases more and decide to keep or delete the feature.
- **Docs avoid over-budget pages.** Several Mac docs pages are already over the 6000-word limit, so the new behavior goes on its own page instead of growing those.

**Decisions for you at review**

- **`picker_tip_slot`:** I recommend `card_foot`, putting the picker tip at the bottom of the picker card, the same place as in the list. The research put it in the panel's key-hint footer, but it also warned against putting a "next time" key next to keys you can press right now.
- **Two memory updates, both off by default:** a sentence about tips in the Capture Alias glossary entry, and a new decision record for the design. Turn them on if you want them.

The in-progress `bob-cli-j6.2` Mac work (the escapes for `&` and `*`) touches the same code. Phases 3 and 4 are told to build on it, or to record a follow-up if it hasn't landed by then.
