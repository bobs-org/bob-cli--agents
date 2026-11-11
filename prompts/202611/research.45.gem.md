- **AGENTS:**
  - [bbugyi200.apollo.research.45.gem](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.45.gem/README.md)

%id(gem, clan=research.45) %m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher gem in a 5-researcher swarm. The other
researchers, `research.45.cdx`, `research.45.cld`, `research.45.grk`, `research.45.mus`,
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

We already support targeting specific drawers when capturing notes in specific
area/project notes. I would now like to add support for doing something similar for
notebook H2 sections.

- For example, the `#` key (or `/` capture alias) should trigger completion for known
  notebook sections when typed at the start of a bullet.
- This functionality should have good support when using the project capture syntax or
  when capturing new notes to an existing project by targeting it with the `@<notebook>`
  syntax.
- We should also trigger completion for existing sections and allow the creation of new
  sections using the `@<notebook>#` syntax.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=gem)
