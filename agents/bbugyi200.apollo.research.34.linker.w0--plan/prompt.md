#gh:gh_bobs-org__bob-cli Daily files in Obsidian currently link to a monthly file that uses no template.
I would like to start linking to weekly files as the parent of daily files instead. Can
you help me implement this?

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
- Review the period_note_tree_and_stats_strips.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.34.linker