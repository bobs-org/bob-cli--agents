%id(mus, clan=research.59)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.59.cdx`, `research.59.cld`, `research.59.grk`, `research.59.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to move the day strip to above the badges instead of below them, which
makes sense I think since the working time bar (see below) can act as a natural
separator.

- See the bob-cli-bz epic bead for context on day strips.
- Also, I liked the old look better. You were just supposed to fix the overlap.
- I think you just needed to change the way / where the working time bar, which shows
  which areas were worked on, is rendered.
- As a part of this change, let's also change that working time bar so we prefer to
  aggregate by the "top-level project" (i.e. the project in a task's ancestry--ancestry
  refers to walking the `parent` frontmatter fields--associated with a prj note that has
  an area note as its parent, not another project). We should aggregate by area iff the
  task lives in an area note. We will call this top-level project / area note the "root
  parent" for a task. In other words, the working time bar should aggregate by root
  parent.
- Make sure that the ~/bob/dash_stats.md file (the "stats dash") also allows for a good
  view that aggregates by root parent. We already have a button that supports
  aggregating by theme, so I was thinking we could just add a third button for this? Or
  maybe we should just always aggregate by the root parent (unless the theme button is
  used)? I'll let you decide this one.
- We should add new glossary memory web strands for:
  - "top-level project" (aka "top project")
  - "root parent"
  - "day strip"
  - "stats dash" (an easy way to refer to the ~/bob/dash_stats.md file)
- Finally, this change should allow us to obsolete a few things:
  - We should stop aggregating the total working time for the day in the "Pomodoros" H2
    section title in daily files, since this now duplicates data that can be found in
    the day strip.
  - We should remove support for the frontmatter field that allows projects to specify
    that aggregation should ignore sub-children (root parent aggregation makes this a
    lot less useful).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=mus)