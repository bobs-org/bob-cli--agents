# Chat History - ace-run (0eb--plan)

- **TIMESTAMP:** 2026-08-26 10:04:05 EDT
- **MODEL:** claude/opus
- **AGENT:** 0eb--plan

**Plan:** /home/bryan/.sase/plans/202608/pomodoro_bullet_move.md


## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add support to the `<ctrl+shift+m>` keymap for moving
pomodoro sub-bullets and also add support for "named pomodoros"?

- Named pomodoros are pomodoros that have an em-dash followed by a name (may be one or
  more words). See the pomodoros at the bottom of the ~/bob/2026/20260826.md file for an
  idea of what these should look like.
- When the `<ctrl+shift+m>` keymap is used on a pomodoro sub-bullet, then the user
  should be prompted to select from one of the other open (named or unnamed) pomodoro in
  this file. They may also type in the name of a new pomodoro that should be created and
  added below the current pomodoro instead (the name provided by the user should have
  all of its letters capitalized).
- This keymap should also accept a count. For example, `2<ctrl+shift+m>` would specify
  that we should move this pomodoro sub-bullet and the 2 below it to the same other/new
  pomodoro specified by the user.
- Update the pomodoro glossary entry to reflect these changes. Make sure this glossary
  definition is excellent but also concise. Remember that every token in context either
  helps or hurts us.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %model:opus

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202608/pomodoro_bullet_move.md`

> # Pomodoro sub-bullet moves and named Pomodoros (`<ctrl+shift+m>`)
> ## Goal
> Teach the `<ctrl+shift+m>` keymap a second mode. Today it moves `#task` lines to another
> note. When the cursor sits on a **Pomodoro sub-bullet** it must instead move that bullet
> (and, with a count, the sibling bullets below it) into another **open Pomodoro in the
> same file**, chosen from a picker that also accepts a typed name for a brand-new
> Pomodoro created directly below the current one.
> Alongside that, formalize **named Pomodoros**: a Pomodoro whose ledger body is followed
> by an em dash and an ALL-CAPS name.
> ```

*See full plan file for details.*

