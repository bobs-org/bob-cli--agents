- **AGENTS:**
  - [bbugyi200.athena.research.4g.grk](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4g.grk/README.md)

%id(grk, clan=research.4g) %m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher grk in a 4-researcher swarm. The other
researchers, `research.4g.cdx`, `research.4g.cld`, `research.4g.gem`, are independently
investigating the same request and will write their own self-named reports ending in
`__cdx.md` and `__cld.md` and `__gem.md`. Your report will end in `__grk.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new `*` syntax.

- This syntax should work a lot like the `&` syntax, which allows the user to specify
  that the new task should have a task dep link to a different task.
- This new syntax, however, should allow the user to specify that the new task blocks
  the specified task (i.e. specify a task dependency in the opposite direction).
- When we block a task that has a corresponding task link in today's daily file using
  this method, we should remove that task link (and the pomodoro iff that pomodoro
  section becomes empty after removing that task link).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=grk)
