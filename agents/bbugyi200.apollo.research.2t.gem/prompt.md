%id(gem, clan=research.2t)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.2t.cdx`, `research.2t.cld`, `research.2t.grk`, `research.2t.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=gem)