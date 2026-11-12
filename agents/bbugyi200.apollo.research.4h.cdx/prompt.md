#gh:gh_bobs-org__bob-cli
%id(cdx, clan=research.4h)
%m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm.
The other researchers, `research.4h.cld`, `research.4h.grk`, `research.4h.mus`, `research.4h.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cdx.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to start (soft) requiring that all external (i.e. not owned by me) Google
Calendar events be acked before becoming event tasks.

- A Google Calendar event should be considered "acked" if the user has either explicitly
  acked it (i.e. acknowledge it with a no-op) or added a note to it (with the
  `bob gcal note` command, for example).
- We can accomplish this by adding a new `bob gmail ack` command that accepts an
  `-n|--next-n-days` option.
- This command will iterate over every external event in that time period (always
  including today) that has not been acked and prompt the user to select one of the
  following options, which they should be able to select with a single keypress:
  - Ack (no-op)
  - Note (requires a note from the user and accepts the same argument form as the
    `bob gcal note` command).
- The `bob gcal sync` command should still create event tasks for external events that
  have not been acked, but we should render a warning of some sort that is hard to miss
  in the event tasks that we create that correspond with unacked events.
- As a part of this change, you should add a new weekly recurring task to the
  ~/bob/gtd_daily.md file that reminds me to run the `bob gcal ack -n 7` command.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cdx)