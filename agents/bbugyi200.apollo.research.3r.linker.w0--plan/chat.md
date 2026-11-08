# Chat History - ace-run (research.3r.linker.w0--plan)

- **TIMESTAMP:** 2026-11-08 11:40:50 EST
- **MODEL:** claude/opus
- **AGENT:** research.3r.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/close_outcome_x_s_typing_aliases.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/close_outcome_x_s_typing_aliases.md`

> # Plan: Close-outcome letter aliases (`x` → `!`, `s` → `*`)
> ## Context
> Bryan wants two new Shift-free typing aliases in Bob Mac Capture, matching the existing
> `,`→`+`, `.`→`^`, `;`→`:`, `=`→`~`, `\`/`/`→`#`, and past-segment `-`→`~` family:
> - `x` types `!` (complete) and `s` types `*` (park) inside the `x` close syntax. For
>   example, `xx` → `x!`.
> - The same letters work after the second `=` of the `x=` past syntax. For example,
>   `x=1=s` → `x=1=*`.
> The consolidated research report
> `research:202611/close_outcome_x_s_typing_aliases/close_outcome_x_s_typing_aliases.md`

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli We already support a few different short-hand characters (ex: `,`, `.`, `=`,
`;`) that are auto-replaced with other characters in the bob-mac-capture app in certain
contexts. I would now like to add support for two new similar short-hand characters. Can
you help me implement this?

- These characters will be `x` and `s`.
- These will be replaced with `!` and `*` respectively, when used with the `x` syntax.
  For example, typing `xx` should result in `x!` in contexts where the `x` capture
  syntax is respected.
- Similarly, these will be repaced with `!` and `*`, respectively, when used instead of
  the second `=` that is supported by the `x=` capture syntax. For example, typing
  `x=1=s` should result in `x=1=*` in contexts where the `x=` capture syntax is
  supported.
- Review the close_outcome_x_s_typing_aliases.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.3r.linker

## Response

Reading the research report on the `x`/`s` typing aliases before exploring the existing alias code.

Still exploring bob-cli's `capture-rewrite` code, next the close lexer and the Mac rewrite lane.

Still mapping the grammar: checking how `draft.rs` splits same-line session chains (needed for the "no alias after inline Work Log text" rule).

Now reading the Mac app's rewrite lane (`CapturePanelController` key filter, `CapturePanelModel` rewrite/submit paths) to size the Mac half.

Checking whether the Mac app already has an editor input-lock or key-buffer mechanism the type-ahead hold could reuse.

Bob side is mapped. Now checking memory rules (CLI/docs/release train) and the memory-write path for the new decision record.

Found a sibling precedent (`relation_equals_alias_and_direction_flips` plan). Reading it to mirror its phase structure.

Invoking the memory-write skill now, since the plan will add a new `decisions` record.

Locating the `capture-rewrite --help` source and checking whether `docs/reference/mac-capture/` is a mounted sibling.

Research and code exploration done; verifying the Mac CI script path and fixture generators, then writing the plan.

I have what I need. Writing the epic plan: three phases (Bob rule ∥ Mac type-ahead hold → Mac x/s forwarding), plus an opt-in memory decision.

Validation passes. Proposing the plan.

I've written and submitted the plan for the `x` → `!` and `s` → `*` aliases. It passed validation and is staged for your review. I haven't changed any code yet.

**How it works:** Bob's `capture-rewrite` decides where the alias fires, as a new part of the existing `expand_sigil_alias` rule. The Mac app only sends the keystrokes to Bob and applies its answer. `bob capture`, `capture-parse`, pasted text and scripts keep the letters as typed. The plan includes every requirement the research recommended (A1–A10), so:

- **Where it fires:**
  - after the `x` of a close and at every later outcome position (`x1s` → `x1*`);
  - after the past token's second `=` (`x=1=s` → `x=1=*`);
  - in Pomodoro links like `@r:id=xx` → `@r:id=x!`.
- **Where it doesn't:** only lowercase letters count, and only where the result can still become a valid close. Session names (`x=1s`), Work Log text (`x log xs`), bullets under an item, and ordinary prose keep the letter.

The hardest part is on the Mac side. Today, any key typed before Bob answers cancels the replacement. So `xx` plus a fast Return would file a junk task called "xx" instead of closing the Pomodoro.

**Three phases:**

| Phase | Repo | Depends on | Size |
|---|---|---|---|
| `bob-close-alias`: the alias rule, a viable-close check in the close lexer, unit and CLI tests, `--help` text and capture docs | bob-cli | — | medium |
| `mac-type-ahead-hold`: holds keys typed while Bob is answering and replays them in order afterwards, with a time limit of about 150 ms and flushes on ⌘-commands, clicks and dismissal | bob-mac-capture | — | medium |
| `mac-close-alias`: sends `x`/`s` to Bob, a cheap pre-check so ordinary prose letters never start a `bob` process, a one-time check for an older `bob`, recorded test files, tests, Mac docs, and an end-to-end check | bob-mac-capture | both above | medium |

The first two phases are in different repos and can run in parallel. The key hold lands before the Mac starts sending `x`/`s`, so there's never a release where typing fast can lose the alias.

**Choices I made that you should check:**
- **The key hold also covers the existing `-` → `~` alias inside `x=` drafts.** That gives the hold something to work on and be tested with in its own phase. It also means a fast `x=2-3` now keeps `x=2~3`.
- **If Bob doesn't answer within about 150 ms,** the letter stays as typed and a held Return is dropped, with the message "Bob did not answer; press Return again". The app never quietly submits the literal draft.
- **With an older `bob`,** the Mac doesn't send `x`/`s` to it and says once that `bob` needs updating.

**One decision for you:** whether to add a decision record, "Close Outcomes Have Letter Aliases In The Editor", to project memory once the feature lands. It's off by default because no existing memory note becomes wrong without it. Turn it on if you want the reasoning and rejected alternatives kept.
