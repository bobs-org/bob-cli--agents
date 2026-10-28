- **AGENTS:**
  - [bbugyi200.apollo.research.2s.mus](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.2s.mus/README.md)

%id(mus, clan=research.2s) %m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher mus in a 5-researcher swarm. The other
researchers, `research.2s.cdx`, `research.2s.cld`, `research.2s.grk`, `research.2s.gem`,
are independently investigating the same request and will write their own self-named
reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report
will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start inferring which theme we should suggest for a task (by making it
the default choice in completion menus) based on the task.

- Project notes and area notes should be able to specify the default theme used by their
  tasks and/or sub-projects via a new `theme` frontmatter field. We should add
  `theme: BUILD` to the ~/bob/dev.md file, `theme: CHORE` to the ~/bob/love.md file, and
  `WRITE` to the ~/bob/job.md and ~/bob/sase_blog.md files as our first use-cases.
- Ref tasks should suggest the `READ` theme by default. This should override any
  area/project theme default.
- We should make it clear in completion menus why a particular theme is being suggested.
- We should also allow a theme to be overridden explicitly for a given task via a new
  `[theme::<theme]` property on the task.
  - Make sure this property is rendered in a concise and visually appealing way in
    Obsidian.
  - We should automatically set this property on a task when a theme other than the
    sugested theme is selected when adding a task link for a task (via the
    `<ctrl+enter>` keymap, for example). This way I don't need to re-override the theme
    again for that task the next day if it happens to roll over.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=mus)
