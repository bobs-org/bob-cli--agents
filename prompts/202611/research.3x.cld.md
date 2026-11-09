- **AGENTS:**
  - [bbugyi200.apollo.research.3x.cld](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.3x.cld/README.md)

%id(cld, clan=research.3x) %m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher cld in a 5-researcher swarm. The other
researchers, `research.3x.cdx`, `research.3x.grk`, `research.3x.mus`, `research.3x.gem`,
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

I would like to add a new "notebook" Obsidian note file type (i.e. supported value for
the `type` frontmatter field).

- Notebooks will only contain note bullets (optionally organized into H2 sections) and
  will be a useful way to organize notes by giving us a way to group related notes
  without creating a new area note or project note. It will likely be useful at some
  point, for example, to have the ability to factor a large H2 section in an area note /
  project note out into its own child notebook.
- These files should always be children of (i.e. point to via their `parent` frontmatter
  field) an area note, project note, or another notebook.
- We should add an excellent new "notebook" glossary term to describe this concept.
- We should render an excellent, visually appealing section in the root parent of
  notebooks (for any root parent that has notebook children or has non-root chilren that
  do, recursively) that links to each notebook and includes a good summary of each
  notebook (maybe via a required notebook frontmatter field?).
- Capture Syntax
  - We should be able to create a new notebook using the `@foo^bar@` project capture
    syntax with the `%n` directive (which will have two related purposes now--notes and
    notebooks).
  - We should be able to add notes to existing notebooks or notebook H2 sections using
    the `@@foo` or `@@foo#bar` syntaxes, respectively, which would add a new note the
    the ~/bob/foo.md notebook file either at the top-level (for `@@foo`) or in the "Bar"
    H2 section (for `@@foo#bar`).
  - We should also support the `@@foo+baz` syntax to add a sub-bullet to the note bullet
    with the `^baz` block ID in the ~/bob/foo.md file.
  - Make sure that we support assigning block IDs to captured notes using the
    `@@foo^some-id` syntax as well (with a block ID prompt that pre-fills a suggested
    block ID).
  - Make sure all single character capture aliases (`.` to `@`, `.` to `^`, and `/` to
    `#`, for example) work properly with this new syntax.
- You should dig through my Obsidian vault (i.e. the ~/bob/ directory) in search of the
  most useful candidate notebooks. Search for any notes in my vault that contain
  relevant information (I think I have a lot of these) but are not currently linked into
  my Obsidian system properly (live in a file without a parent, for example). The
  selected notes should be migrated, as a part of this change, to my first new
  notebooks.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cld)
