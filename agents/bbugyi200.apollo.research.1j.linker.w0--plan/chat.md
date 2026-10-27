# Chat History - ace-run (research.1j.linker.w0--plan)

- **TIMESTAMP:** 2026-10-15 14:04:10 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1j.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202610/bulk_capture_templates.md


## Prompt

#gh:gh_bobs-org__bob-cli I want to add support to the `bob capture` command and the corresponding
bob-mac-capture app for defining a template as the first input of a bulk capture. Can
you help me implement this?

- Subsequent capture inputs in that bulk capture should then be treated as templates for
  the first capture input.
- For example, consider the following bulk capture using the new syntax that I was
  thinking of using (think hard about what the best syntax is for this functionality):

  ```
  Apply to {0}! @job_2026_apply_29:{1}
  - **URL**: {2}

  Foobar foo http://foobar.com/career/some_foo_job

  Bazbuz baz http://bazbuz.com/career/some_baz_job
  ```

- After this change, that should be equivalent to the following:

  ```
  Apply to Foobar! @job_2026_apply_29:foo
  - **URL**: http://foobar.com/career/some_foo_job

  Apply to Bazbuz! @job_2026_apply_29:baz
  - **URL**: http://bazbuz.com/career/some_baz_job
  ```

- Review the bulk_capture_template_drafts.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %auto %w:research.1j.linker

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/bulk_capture_templates.md`

> # Plan: Bulk capture templates (`@@template:`)
> ## Why and what
> Bryan creates runs of near-identical captures, for example "Apply to 29 job openings" in
> waves of 10–12 roles. Today each item is typed in full, so a typo in the route or ID
> shape is repeated, or slips into one item only. A **bulk template** lets the first block
> of a draft be a template, and every later line is a **row** of values that fills it:
> ```text
> @@template:
> Apply to {0}! @job_2026_apply_29:{1}
> - **URL**: {2}

*See full plan file for details.*

