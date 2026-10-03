%id(grk, clan=research.u)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.u.cdx`, `research.u.cld`, `research.u.mus`, `research.u.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
think we may have made a mistake adding the `#now` tag.

- Part of the reason it was deemed necessary is because we were preserving the behavior
  of the `bob task-status-hooks` command that keeps WIP/Next Obsidian task statuses in
  sync with whether or not the task has a task link in the current pomodoro.
- We can remove that, but that would leave one unfilled need: I need a way to query for
  all tasks associated with task links in today's daily file.
- We can fill this need, however, using either a file path filter in the query or by
  using some kind of `#today` tag that the `bob task-status-hooks` command starts
  managing instead of WIP/Next statuses.
- We would then replace the Now/WIP/Next section queries in the ~/bob/dash.md file with
  Today/Pending/Next queries that must be mutually exclusive (i.e. a task can only be
  shown in one of these sections).
- Then, as a part of my daily morning GTD review, I can review all Pending/Next tasks
  first to pull in tasks for today and then, if I don't have enough work for the day,
  pull from the Ready section's tasks.
- This means that what was tracked using `#now` would now start being tracked by the
  Next status. The only thing I think I lose here is the ability to have a task link
  that is not tagged with `#now` (since every task link is either WIP/Pending or--by
  default--Next). That's fine though since I don't really need that I don't think.
- It's important that Pending/WIP tasks not have their statuses wiped by the
  `bob task-status-hooks` command either since that will allow me to remove the
  corresponding task link when I have a task that is in-progress, likely to be done the
  next time I look at it, but I won't be able to look at it for a while (because a swarm
  of agents will take a few hours to implement it, for example--this way I won't forget
  to review this work, since it will be in the Pending section of the ~/bob/dash.md
  file, but it also won't be in my face for the time being, since I can remove it from
  my daily file).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=grk)