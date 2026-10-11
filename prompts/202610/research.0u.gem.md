- **AGENTS:**
  - [bbugyi200.apollo.research.0u.gem](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.0u.gem/README.md)

%id(gem, clan=research.0u) %m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher gem in a 5-researcher swarm. The other
researchers, `research.0u.cdx`, `research.0u.cld`, `research.0u.grk`, `research.0u.mus`,
are independently investigating the same request and will write their own self-named
reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report
will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to start tracking my daily habits/stats somehow.

- Each of the stats I would like to track (ATM at least) boils down to a single integer
  per day:
  - The total number of morning GTD review tasks I completed each day (by iterating over
    and processing each one using the `]s` keymap).
  - The total number of pomodoro hours and minutes worked each day. Note that I already
    show this via an inline query in the "Pomodoro" section of each daily file.
  - The total number of tasks that I complete each day.
  - The total number of tasks that I create each day.
  - Think hard about what other metrics I should consider tracking in this v1
    implementation.
- It also needs to be easy to start tracking new daily metrics like these that I think
  of later.
- I'm not sure what the UX should look like for this, but it should make it easy to
  visualize my progress for a given metric over a given time period (which I should be
  able to adjust).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=gem)
