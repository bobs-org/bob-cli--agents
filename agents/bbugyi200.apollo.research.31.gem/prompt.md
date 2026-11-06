%id(gem, clan=research.31)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.31.cdx`, `research.31.cld`, `research.31.grk`, `research.31.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to make it so the `#off` tag is accepted in a Google Calendar event instead of
`#offclock` or `#untracked` (both of which should still work but should produce a
deprecation warning message by the `bob gcal sync` command).

- Let's start using `#off` instead of `#offclock` in Obsidian as well (to be
  consistent). Make sure to update all past event tasks that used the deprecated tags to
  now use `#off`.
- Also, as a part of this change, we should add support for a new `offclock: true`
  frontmatter field to area / project notes that specifies that tasks belonging to that
  area/project should always be treated as offclock.
- This new field should be respected for all child areas/projects of that area/project
  note, recursively, but children should be able to override this via their own
  `offclock: false` frontmatter field. Individual tasks should be able to override this
  via a new `#on` tag, which the `bob gcal sync` command should start looking for on
  Google Calendar events.
- As our first use-case I would like to set `offclock: true` in the ~/bob/love.md file
  so all "love" tasks (including event tasks) are treated as offclock.
- See the bob-cli-fl epic bead for context.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=gem)