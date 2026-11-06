- **AGENTS:**
  - [bbugyi200.apollo.research.34.cld](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.34.cld/README.md)

%id(cld, clan=research.34) %m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher cld in a 5-researcher swarm. The other
researchers, `research.34.cdx`, `research.34.grk`, `research.34.mus`, `research.34.gem`,
are independently investigating the same request and will write their own self-named
reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report
will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Daily files in Obsidian currently link to a monthly file that uses no template. I would
like to start linking to weekly files as the parent of daily files instead.

- Weekly files should then link to quarterly files as their parents, which should link
  to yearly files as their parents, which should link to a new ~/bob/all_time.md file as
  their parent, which should link to the ~/bob/org.md file as its parent.
- Each of these weekly/quarterly/yearly files should contain a "stats strip" that breaks
  down the working time for the given time period.
- We should try to automatically summarize the units/parts that make up the whole of
  each of these files. For example, quarterly files should ideally show some kind of
  breakdown of each week.
- I'm also open to making it a routine to have an LLM / agent enrich these
  weekly/quarterly/yearly files with appropriate contents.
  - To support this use-case, each of thee files should be pre-generated with the
    appropriate instructions so an agent who is asked to update its contents doesn't
    need much more instruction than that.
  - Think hard about what instructions each of these (weekly/quarterly/yearly) files
    should contain.
  - We should update the weekly review task in the ~/bob/gtd_daily.md file and add
    appropriate quarterly/yearly tasks to that file.
- We should add a new glossary term for "stats strip" that adequately describes its
  relation to other existing glossary terms (for example, the "day strip" is the stats
  strip used for daily files).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cld)
