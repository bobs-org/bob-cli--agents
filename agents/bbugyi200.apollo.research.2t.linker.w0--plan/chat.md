# Chat History - ace-run (research.2t.linker.w0--plan)

- **TIMESTAMP:** 2026-10-29 16:11:31 EDT
- **MODEL:** claude/opus
- **AGENT:** research.2t.linker.w0--plan

## Prompt

#gh:gh_bobs-org__bob-cli I recently came to the realization that pomodoro themes are really just "task
types" in disguise. I think we should make this more explicit and improve / automate the
experience of working with task types a bit more. Can you help me implement this?

- We should rename the "pomodoro theme" glossary entry to "task type" and update it
  accordingly.
- MOTIVATION:
  - Even though I would like to continue to support ad-hoc themes (with a warning) and
    themes recommended by productivity research, I think this is still supported well
    after this change. For example, using projects like we use "themes" today by putting
    all tasks for a specific project in their own task type pomodoros and then merging
    those pomodoros (the project name then renders on the pomodoro line). We will want
    to add better support for duplicate task type pomodoros for this use-case, but that
    can be considered out-of-scope for now.
  - The name "task types" also just seems to be a good match for this feature (tasks are
    like issues in an issue tracker, most of which support types, and the themes I
    currently use look a lot like types).
- IMPROVEMENTS:
  - Let's start giving every task a type by default. This should be configurable
    (configure mine to be `CHORE` in my chezmoi repo).
  - We need to make sure that a task's type (implicit or explicit) is always consistent
    with any current / future task links associated with that task. Namely:
    - When we update the task type via the Obsidian task card, we should move any task
      links for that task to existing task type pomodoros for that type if any exist in
      the current daily file; otherwise, we should create a new task type pomodoro for
      that type and add the task to that pomodoro.
    - When moving a task link to a different pomodoro (via the `<ctrl+shift+m>` Obsidian
      keymap or the bob-mac-capture app, for example), if that pomodoro has a different
      type than the task that is being moved, we should update the `type` task property
      for that task appropriately.
  - When adding new task links via the bob-mac-capture app , we should always use the
    suggested task type for that task by default (we currently always add the task link
    to the current/next pomodoro). If the `#type` suffix syntax is used to specify the
    `type` pomodoro block, we should update the `task` property for that task if
    necessary.
  - We should start allowing users to explicitly set exempt task types. I sometimes use
    the `PLAN` task type, for example, in the middle of the day to work a planning task
    that breaks down a project more. I should be allowed to give that task a
    `[type::PLAN]` property.
  - I don't like the way that we currently render the `type` task property in Obsidian
    (as a chip). Instead, let's start altering the `#` symbol that we render for `#task`
    to `#<type>` when the task has the `type` property (e.g. `#BUILD`). This tag should
    be colored appropriately.
- Review the task_types_from_pomodoro_themes.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.2t.linker

## Response

# Gate handoff

This agent handed the remaining decision to a gate turn.
Decision: Epic ready for review: task_types.md
Gate ID: 426d27fd-3bfa-43dc-bf09-64dd30ee7e89
Inspect with: sase gate show --id 426d27fd-3bfa-43dc-bf09-64dd30ee7e89 --kind epic_plan
Gate turn: research.2t.linker.w0--gate

