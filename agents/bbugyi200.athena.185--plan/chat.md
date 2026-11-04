# Chat History - ace-run (185--plan)

- **TIMESTAMP:** 2026-11-04 14:02:32 EST
- **MODEL:** claude/opus
- **AGENT:** 185--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_sigil_aliases.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_sigil_aliases.md`

> # Capture sigil aliases: `.` types `^`, `;` types `:`
> ## Goal
> In Bob Mac Capture, the unshifted keys `.` and `;` should work as the shifted sigils `^`
> and `:` wherever those sigils open a Bob picker:
> - `@foo.` becomes `@foo^` right away. The Block ID picker then opens on its New ID
>   composer, exactly as if `^` had been typed.
> - `@foo;` becomes `@foo:` right away and opens the Block ID picker (Link mode for a
>   marker-only item, New ID on an item with text), exactly as `:` does.
> - `;` typed as a whole capture item, including the first key in a blank draft, becomes
>   `:` and opens the Task Link picker, exactly as `:` does.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make it possible to type `.` instead of `^` after the `@foo`
capture syntax to perform the same action (prompt for a block ID)?

- The `.` character is easier to type than `^`.
- The `.` character should immediately be replaced with `^` in this context.
- Let's also do something similar for the `;` key and `:` key (i.e. replace `;` with `:`
  and trigger the appropriate completion). This should include the case where `:` is the
  first key pressed in the capture input.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm exploring where capture keystrokes are handled (likely the Bob Mac Capture app) before planning the `.`→`^` and `;`→`:` rewrites.

Still exploring: finding which picker `@foo^` opens in Mac Capture and how `:` opens the task-link picker.

Studying the existing "separator toggle" rewrite lane (`:`/`^`/`+`/`|`), which looks like the right hook for `.`/`;` aliases.

I'm reading bob's `capture-rewrite` rules. `attach_relation_label` checks eligibility against the completion grammar, and the new aliases can work the same way.

Checking bob's route-token grammar to see whether `.` or `;` can legally appear in a route, since that decides when the alias is safe.

The plan is taking shape: a new bob `capture-rewrite` rule plus Mac Capture forwarding `.`/`;` on the existing rewrite lane. Next I'm checking how the picker decides to auto-open after a rewrite.

Checking whether bob-plugins also has a capture input that would need the same aliases.

Checking repo conventions (justfile targets, Mac test patterns) and the sigil decision record so the plan uses the right commands and doesn't contradict an accepted decision.

Verifying the completion entry point's signature so the plan names the right function.

Checking how the previous new rewrite rule was committed, to tell the implementer whether a `!` contract-break marker is warranted.

I have enough context. Writing the plan file now.

The plan passes validation. Submitting it with `sase plan propose`.

I wrote the plan, it passed validation, and `sase plan propose` has staged it for your approval. No code has changed in either repo yet.

**What the plan does:** it adds one editor-only rewrite to bob. The capture grammar itself doesn't change: `bob capture` still reads `@foo.` and `;` as plain text.

**Where the logic lives:**
- **bob-cli** gets a new `capture-rewrite` rule, `expand_sigil_alias`. It swaps the typed `.` for `^` or `;` for `:`, but only when Bob's completion grammar says the real sign would open a picker at that spot. That covers `@foo.` → `@foo^` (block ID prompt), `@foo;` → `@foo:` (block ID picker), and `;` as a whole capture item → `:` (task-link picker). The whole-item case includes `;` as the first key in a blank draft.
- **bob-mac-capture** sends `.` and `;` keystrokes to that rule, the same way it already sends `^`, `:`, `+` and `|`. It applies the swap as one undoable edit and then asks for completion, so the picker opens right away.

Bob decides when a key qualifies, so Mac Capture still never parses capture grammar. The swap costs one call to bob, which took about 4–5 ms per call when I timed it here, so it should look instant. With an older bob, `.` and `;` just type normally.

`.` and `;` are left alone elsewhere: ordinary sentences, `foo@bar.com`, and the `&`, `~`, `*`, `!` and `^route` forms. The plan also covers tests and docs in both repos. The Mac app code must be compiled on the Mac before it lands.

**Two decisions for you at approval time:**
- **`scope`** (default `route`): whether `.` and `;` should also work at the other picker spots. Those are a `.` typed as a whole item (opens the active-task picker) and `- .`, `- ;`, or a trailing ` .` / ` ;` on project-note bullets. I defaulted to no, because text starting with `.`, like `.bashrc`, would then open a picker.
- **`literal_escape`** (default `undo`): how you get a literal `.` or `;` after the swap fires. The default is ⌘Z, which restores the key you typed, as it does for the other capture rewrites. The alternative is pressing the same key twice, like the `\\` escape you just added for Go To; it needs extra state in the Mac app.
