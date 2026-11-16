# Chat History - ace-run (research.5x.linker.w0--plan)

- **TIMESTAMP:** 2026-11-07 18:41:53 EST
- **MODEL:** claude/opus
- **AGENT:** research.5x.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/start_timing_later_offset.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/start_timing_later_offset.md`

> # Signed Pomodoro start timing: `+N` starts later
> ## The rule users learn
> > Inside `<X>`, `-` starts earlier and `+` starts later. A sign with no number means
> > five minutes. A space makes it a second step.
> | Glued: one start                           | Spaced: start, then a second operation |
> | ------------------------------------------ | -------------------------------------- |
> | `=-2`: start 10 min earlier                | `= -2`: start, then shorten by 10 min  |
> | `=+2`: start 10 min later (**new**)        | `= +2`: start, then extend by 10 min   |
> | `=fix2+`: FIX starts 5 min later (**new**) | `=fix2 ++`: start, then shift later    |
> Read the design source before starting any phase:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I want to add support for using `+<N>` at the end of the `<X>` in the `=<X>`,
`@file:id=<X>`, and (if you think its appropriate) the `x=<X>` capture syntaxes, where
`<N>` is some positive integer that defaults to 1 if not provided. Can you help me
implement this?

- This syntax should specify that the start of the pomodoro should be have `<N>`
  5-minute positive offsets added to it.
- For example, `=fix2+` should be equivalent to `=fix2 ++` and `@foo:bar=+3` should be
  equivalent to `@foo:bar= ++3`.
- Review the start_timing_later_offset.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5x.linker

## Response

Reading the research report on later-start offsets first, then I'll map the capture code before planning.

Research read. Now verifying the cited code against the current HEAD (research was pinned to `b73ac383`; we're 4 commits later).

Mapping the link-start parser and the clock math next, then the Obsidian plugin side.

Checking which shared fixture carries `se<X>` start vectors (the research's "shared clock vectors").

Reading the docs/CLI-rules memory and the decision records this feature touches.

Checking the one vector that differs between the bob-cli and bob-plugins copies, since the plan will extend that shared fixture.

Checking whether Bob Mac Capture composes start tokens itself (deciding whether it needs a phase), and how past grammar-revision bumps were handled.

Last checks: how `^route:id=` link starts treat trailing text, and the `=- foo` precedent.

Design is settled. Before writing the plan, I'll file the research's recommended "starts in Nm" status follow-up (out of scope for this feature) so the plan can reference it.

Follow-up filed as `bob-cli-ik`. Now drafting the epic plan; first a quick look at a recent epic plan's frontmatter shape.

I have everything I need. Writing the epic plan now.

Validation passes. Two small wording fixes from my self-review, then I'll revalidate and propose.

Plan staged. Finishing the turn through `/sase_final`.

I've written and validated a 4-phase plan for `+N` later starts, and it's waiting for your approval. Nothing has been implemented yet.

**The rule users learn:** inside `<X>`, `-` starts earlier and `+` starts later. A sign with no number means five minutes, and a space makes it a second step. So `=fix2+` writes the same span as `=fix2 ++`, and `@foo:bar=+3` links the task and starts it 15 minutes later in one item.

**Design calls** (this follows the research, with the open details settled):
- **When a glued `+` is timing:** a bare name ends at its last character that is neither a digit nor `+`, and everything glued after it is timing. `=bugs+2` means BUGS, 10 minutes later. `=bob+decks` and `=bob+2fa` keep their current meaning. Names that really end in `+` are written with `#` (`=#c++`, which becomes legal). `=c++` and `=fix++` are refused with a hint showing all three spellings.
- **Swaps and MEETs:** any non-empty `<X>` is fresh timing, exactly like `-`. `=fix+` while BUILD runs starts FIX 5 minutes from now; it does not shift BUILD's span. `=fix ++` stays the keep-and-shift spelling.
- **`x=` gets no offset.** It records finished work, and `+` already means something else there (`x=~1+`). `x=fix+` and `x=3+` get errors that point you to `=fix+` or `x =fix+`.
- **`@foo:bar= ++3`:** today this silently creates a task titled `++3`, so your second example's "equivalent" form doesn't actually work. It will now be refused with a hint to write `@foo:bar=+3`.
- **Other refusals:** `+0` and two offsets in one token (`=3-1+2`) are refused, each with a hint built from what you typed.
- **Output changes:** the JSON gains a `later_units` field that only appears when nonzero, so older readers aren't misled. Conflict-warning suggestions keep the sign and use trailing timing for bare names (`=fix2+1`). Each grammar change is committed as a breaking `feat(capture)!:`. Bob Mac Capture needs no change.

**Phases:**

| # | Phase | Repo | Size | Depends on |
|---|---|---|---|---|
| 1 | `signed_timing`: `+` in `<X>`, later start time, link starts (`@foo:bar=+3`), `+` forms before the name (`=+3`, `=3+1#deep-work`) | bob-cli | medium | — |
| 2 | `bare_plus`: `+` after a bare name (`=fix2+`), `#` for names ending in `+`, completion, fix the stale `=bugs+2` docs, decision record | bob-cli | medium | 1 |
| 3 | `link_body`: refuse `@foo:bar= ++3`, teach the glued spelling | bob-cli | small | 2 |
| 4 | `obsidian_parity`: teach the Obsidian `se<X>` snippet `+`, refresh the shared test cases, `bob plugins sync` | bob-plugins | small | 1 |

Phase 4 can run alongside phases 2–3. The bob-cli phases run one after another because they edit the same files.

**Your one decision at approval:** whether phase 2 should record the design in memory as `decisions:start-timing-is-signed`. It defaults to yes, because you accepted the research's recommendations, which include recording it.

I also filed `bob-cli-ik`, a follow-up the research recommended: `bob pomodoro` and the menu-bar indicator should show "starts in Nm" for a session that hasn't started yet, instead of counting down to its end. The plan deliberately adds no midnight guard; the related wrap-around bug is already tracked as `bob-cli-h1`.
