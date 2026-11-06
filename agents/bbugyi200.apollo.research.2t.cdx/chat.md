# Chat History - ace-run (research.2t.cdx)

- **TIMESTAMP:** 2026-10-29 14:36:23 EDT
- **MODEL:** codex/gpt-6-astra
- **AGENT:** research.2t.cdx
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261029_142426.md`

## Prompt

#gh:gh_bobs-org__bob-cli
%id(cdx, clan=research.2t)
%m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm.
The other researchers, `research.2t.cld`, `research.2t.grk`, `research.2t.mus`, `research.2t.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cdx.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

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
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cdx` suffix, i.e. `<stem>__cdx.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I’ll trace how themes, task types, and task links work across Bob, the Obsidian plugins, and Mac Capture, then write an independent design critique and recommendation. I’ll use the SASE repository, memory, and artifact skills to keep the research and saved report auditable.

The existing theme system already has task-level overrides, inherited suggestions, colors, and a configured vocabulary. The central design question is how to turn those suggestions into reliable routing rules—especially for merged Pomodoros, defaults, and completed work that should retain its history.

I found a naming mismatch that matters for migration: the current stored field is `[theme:: …]`, not `[type:: …]`. I also confirmed that `PLAN` is rejected by the Task Card because budget exemption is being used as a type-validity rule. I recommend separating those rules so exempt types remain valid without changing their budget treatment.

The largest risk is consistency across files: a type change may need to update a task note and several daily notes together. The current Task Card writes fields locally, and Pomodoro moves edit the ledger separately. The recommendation will use one mutation planner for both, with explicit rules for merged sessions, future links, stale edits, and rollback.

My recommendation is taking shape: give each task one effective type, route new links by that type, and make deliberate moves to a different type update the task and its other live links. I’ll call out two adjustments: changing an unscheduled task’s type should not add it to today’s agenda, and completed sessions should keep their historical classifications.

The report is drafted. It recommends a virtual CHORE default, visible `#TYPE` labels, explicit support for PLAN, and a staged migration from `[theme::]` to `[type::]`. I’m checking the migration details and report references before registering the durable snapshot.

The report is saved and registered as a permanent snapshot. It also flags a migration hazard: Dataview inherits page fields onto tasks, so a raw `task.type` lookup can return the note’s kind rather than the intended work category. I’m using the SASE finalizer skill to declare the completed research.

Created the independent [research report](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/research/202610/task_types_as_a_reliable_routing_contract__cdx.md).

Recommendation: adopt task types with a CHORE fallback, coordinated link routing, composite-session support, and preserved history. The report details requirement adjustments, migration risks, visual design, and acceptance tests.

Registered [durable snapshot](/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261029142426/task_types_as_a_reliable_routing_contract__cdx-845b97aa00b4.md): `file:explicit:af0651500863d71c6cb7575c`.
