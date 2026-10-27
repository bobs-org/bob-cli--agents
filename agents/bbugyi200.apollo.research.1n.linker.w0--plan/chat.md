# Chat History - ace-run (research.1n.linker.w0--plan)

- **TIMESTAMP:** 2026-10-16 08:18:29 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1n.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202610/saved_capture_templates.md


## Prompt

#gh:gh_bobs-org__bob-cli We recently added support to the `bob capture` command and the corresponding
bob-mac-capture app for capture templates (see the bob-cli-7w epic bead for context).
Can you now help me add support for persisting templates to disk automatically when they
are used?

- We should then allow the user to access and modify the templates that have been saved
  in the bob-mac-capture app.
- This should work in a similar way to the capture stash.
  - We should use a new `<ctrl+t>` keymap that allows the user to view/modify saved
    templates.
  - Just like with the stash, we should pop a template when it is selected (it will just
    get re-added when the capture is submitted if the template is used).
- Review the capture_template_shelf.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %auto %w:research.1n.linker

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/saved_capture_templates.md`

> # Plan: Saved capture templates (the Control-T template shelf)
> ## Why and what
> Epic `bob-cli-7w` shipped `@@template:` drafts. Bryan's job-application waves reuse the
> same template every time:
> ```text
> @@template:
> Apply to {0}! @job^apply-{1}
> - **URL**: {2}
> Foobar foo https://foobar.com/careers/1
> "Two Sigma" two-sigma https://www.twosigma.com/careers/2

*See full plan file for details.*

