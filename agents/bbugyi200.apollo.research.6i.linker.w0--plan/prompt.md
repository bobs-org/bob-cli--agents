#gh:gh_bobs-org__bob-cli I would like to rename the "article" Obsidian note file type to something more
generic, since I intend to use this type for any file that needs to contain prose. Can
you help me implement this?

- I was thinking of the name "prose" for this, but I'm not sure.
- You should think hard about other names and attempt to come up with a better one.
- The goal is to soon allow for sections ("prose sections"?) to implicitly use this type
  as well, which will allow us to use a keymap to convert that section into a full-blown
  "prose" note (or whatever we decide to call these).
- This functionality will be useful on its own, but will also be required in order to
  eventually make tasks and projects losslessly (or with minimal loss) reversible (since
  projects can have article notes as children).
- Review the prose_rename_and_section_extraction.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.

#plan %m:@xlarge %w:research.6i.linker