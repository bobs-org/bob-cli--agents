# Chat History - ace-run (18r--plan)

- **TIMESTAMP:** 2026-11-05 14:02:05 EST
- **MODEL:** claude/opus
- **AGENT:** 18r--plan

**Plan:** /home/bryan/.sase/plans/202611/relation_dash_alias.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/relation_dash_alias.md`

> # `-` as a shorthand for `~` (relation picker) in Bob Mac Capture
> ## Goal
> In Bob Mac Capture, typing `-` after a space where a real `~` would open the Links To
> relation picker becomes `~` and opens that picker. This works the way `,` already works
> for `+`. Bob decides where the alias applies. The app forwards the key, applies Bob's
> swap natively, and requests completion so the existing picker opens.
> You asked whether this only happens after spaces. Mostly yes, but a space alone is not
> enough. A `-` aliases only when **all** of these hold:
> - A space or tab sits directly before it.
> - Real text precedes it on the same physical line. A line start, indentation, or a bare

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me make `-` a short-hand for `~` in the bob-mac-capture app when
it is safe and appropriate to do so? I think this is only after spaces for `~foo:bar`
style links, right? I want this to work like `,` does for `+` where the `-` is replaced
with a `~` and then the task relation menu is triggered.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the bob-mac-capture repo to find how the existing `,` → `+` sigil alias works, so the plan for `-` → `~` can follow the same pattern.

Still mapping the Mac-side plumbing: I'm reading how the controller forwards alias keys (`.`/`;`/`,`/`\`) to bob and how the backslash double-tap literal is armed, to size the `-` change accurately.

I now have the full picture on both sides. Let me check the Mac test fixtures for existing relation-picker support, then verify a couple of bob-side gate cases empirically.

Research is done; I'm now writing the plan file (bob-cli rule + Mac forwarding and literal-escape arm), then validating it.

The plan passes validation. Submitting it.

I've written the plan and submitted it for your review. It's validated and staged; nothing gets implemented until you approve it.

**Your question: is it only after spaces?** Mostly, but a space alone isn't enough. A `-` becomes `~` only when all three of these hold:

1. A space or tab is directly before it.
2. There's real text before it on the same line. A line start, indentation, or a bare list marker (`- -`, `* -`) doesn't count. This keeps bullets and the whole-item Pomodoro `-N`/`--N` shapes literal.
3. A bare `~` in that spot would open the Links To relation picker. In practice that's the end of a task line, e.g. `Fix it -` → `Fix it ~` with the picker open.

Like the `,` alias, bob decides the swap through `capture-rewrite` (rule `expand_sigil_alias`). The Mac app forwards the key, applies bob's swap, and the existing picker opens. Hyphens inside words, mid-line prose dashes, and positions like `x -`, `=bugs -` and Work Log text stay literal.

I ran `bob capture-complete` against the installed bob to check positions. Two places would wrongly open the picker unless bob blocks them explicitly, so the plan adds checks for both:
- **Inside an unclosed backtick:** ``run `cargo -`` would become a relation.
- **Inside an unfinished wikilink:** `[[foo -` and `((foo -` are claimed by the wikilink pickers, which bob checks first.

**The main risk** is that ` -` at the end of a line is also how you'd type a prose dash (`Call Bob - about`), a CLI flag (`Add --json`), or the existing `--` + Tab em dash. So the plan adds a one-shot escape: while the picker's filter is still empty, the next key decides.

| Next key | Result |
| --- | --- |
| Space | You get `- ` (a prose dash) |
| `-` | You get `--`, so flags and `--` + Tab still work |
| Escape | You get the literal `-` back |
| Anything else | You stay in the relation picker |

The plan also covers tests, docs and CLI help in both repos. bob-cli lands first; an older bob just leaves `-` literal.

**Two choices for you when you review:**
- **`double_dash`:** should `--` stay literal (my default) or become `~~` (Linked From), the way `,,` becomes `++`? I defaulted to literal because `~~` would break spaced `--` + Tab em dashes.
- **`escape_restores`:** should Escape put the `-` back (my default), or keep `~` and show the reopen chip like every other picker?
