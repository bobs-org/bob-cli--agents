# Chat History - ace-run (0cv--plan)

- **TIMESTAMP:** 2026-08-24 14:57:02 EDT
- **MODEL:** claude/opus
- **AGENT:** 0cv--plan

**Plan:** /home/bryan/.sase/plans/202608/capture_global_destination_anywhere.md


## Prompt

#gh:gh_bobs-org__bob-cli We recently added support for a global `@@file+id` spec (where `+id` is
optional) to the `bob capture` command and the bob-mac-capture app (see recent, related
git commits). There are a few problems with the design however. Can you help me fix
these issues / make these improvements?

- The syntax shouldn't need to be located on a line by itself at the top of the file.
  Instead, it should be able to be located on any note/task in the capture input at the
  end of any line.
- Let's start making `@@`, if typed anywhere inside a note/task that already has a
  `@file` reference, deletes the other reference and copies it after the `@@` that was
  typed.
- This functionality serves as a convenience so users don't need to manually go back to
  previous lines to delete the previously entered `@file` syntax and also serves as a
  safety net to make sure we don't use `@@file` on a note/task that already uses
  `@file`.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.


## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202608/capture_global_destination_anywhere.md`

> # Plan: Free the `@@` global destination from the header line and teach it to absorb
> ## Background
> `bob capture` recently gained a draft-wide destination declaration: `@@<route>` or
> `@@<route>+<block-id>`. Today it is only recognized as **exactly one whitespace-free
> token on the first nonblank physical line of the draft**. `split_capture_draft` in
> `src/native/capture_language.rs` peels that line off as a `GlobalHeaderLine`, and every
> other `@@…` token anywhere in the draft is rejected by
> `reject_embedded_global_declarations` with `MISPLACED_GLOBAL_DESTINATION_ERROR`.
> Two problems with that design:
> 1. **Placement is rigid.** The declaration is a property of the draft, but the user has

*See full plan file for details.*

