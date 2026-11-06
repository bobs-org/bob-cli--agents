- **AGENTS:**
  - [bbugyi200.apollo.research.2z.gem](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.2z.gem/README.md)

%id(gem, clan=research.2z) %m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher gem in a 5-researcher swarm. The other
researchers, `research.2z.cdx`, `research.2z.cld`, `research.2z.grk`, `research.2z.mus`,
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

We recently / are in the middle of adding support for the `#untracked` tag to Google
Calendar events. The plan (see the bob-cli-f6 epic bead for context) was to not track
the pomodoros corresponding to untracked event tasks at all, but I'm not sure this is
the best approach. I'd like to start tracking these pomodoros as a part of a separate,
"untracked" group of stats instead somehow.

- I think we can probably implment this by using the `u::` task property for untracked
  pomodoro (this way we still track the duration of each pomodoro somehow).
- The stats dash and the `bob stats` command would then need some way to toggle over to
  showing untracked time (preferably with an option to show just untracked time and all
  time, including untracked).
- As a part of this change, we should generalize this concept of an "untracked pomodoro"
  a bit (which should maybe be named something else, since the time will techinically
  still be tracked after this change?).
  - Add an excellent new glossary term for "untracked pomodoro" (or whatever we decide
    to call these).
  - A pomodoro should be untracked iff all of its task links correspond with tasks that
    have the `#untracked` tag.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=gem)
