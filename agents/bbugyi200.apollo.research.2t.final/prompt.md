%clan(research.2t, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I recently came to the realization that pomodoro themes are really just "task types" in
disguise. I think we should make this more explicit and improve / automate the
experience of working with task types a bit more.

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
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.2t.final %m:@xlarge
%wait:research.2t.cdx %wait:research.2t.cld %wait:research.2t.grk %wait:research.2t.mus %wait:research.2t.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I recently came to the realization that pomodoro themes are really just "task types" in
disguise. I think we should make this more explicit and improve / automate the
experience of working with task types a bit more.

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
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

When you author or carry over Mermaid diagrams, load `/mermaid_diagrams` before
drafting, even when no image or diagrams companion runs. The skill has the shared
figure-selection, styling, and PDF-render review rules. If the provider skill is not
deployed, verify the edited plugin's guide with `sase macro show skill/mermaid_diagrams --format raw` (or
`sase macro show /mermaid_diagrams --format raw`) and use the form this host supports.
This guidance does not enable a companion diagrams agent.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.2t.cdx`, `research.2t.cld`, `research.2t.grk`, `research.2t.mus`, `research.2t.gem` dependencies, matching by `wait_name` and the canonical research
   label's existing `__<suffix>.md` suffix. Never reassign suffixes from list order.
   Open the research repo with `/sase_repo`, then read each report through its canonical
   research reference (or the `ref` field's `file:<id>` reference if the original has
   moved) using `sase artifact read`. Do not read predecessor chat transcripts. If the
   records above do not identify exactly one report per expected suffix, stop and report
   the missing or ambiguous input instead of guessing.
2. Research the request yourself, prioritizing gaps, weak evidence, and disagreements
   between the reports.
3. Pick a descriptive stem `<name>` that collides with nothing in the month directory
   (do NOT end the name with `_consolidated` or `_<YYYYmmdd>` or anything similar unless
   it relates to the research topic), create `<month-dir>/<name>/`, and move each report
   inside it as `<name>__<suffix>.md`, preserving its existing suffix. Each report's
   `source_path` is provenance for where it lives in your own opened research checkout;
   resolve its canonical repo-relative path there before moving it. Never modify the
   other agents' checkouts or the stored snapshot recorded at `ref` — only the copy in
   your own checkout moves. Preserve every file and never overwrite: on any collision,
   pick a different stem first.
4. Write the consolidated report to `<name>/<name>__final.md`: merge the strongest findings
   from every report above and your own research, resolve conflicts, cut duplication,
   and add missing critical context without unnecessary length.

   Do not create `<name>/<name>.md`, not even as a placeholder, because the linker
   agent `research.2t.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.2t.linker`, can find it:

   sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

   Use the consolidated report's actual absolute path and its path relative to the
   research repo root, for example `research:202609/<name>/<name>__final.md`. Register
   only the consolidated report, and do not pass `--move`. If registration fails,
   report that failure; do not report the task as fully complete.

Final layout:

```text
<month-dir>/<name>/
├── <name>__cdx.md
├── <name>__cld.md
├── <name>__grk.md
├── <name>__mus.md
├── <name>__gem.md
└── <name>__final.md
```