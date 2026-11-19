#gh:gh_bobs-org__bob-cli I would like to add support for a new bob "command chip" to Obsidian. Can you
help me implement this?

- This should take some inspiration from the existing copy chip (see the bob-cli-ni epic
  bead for context). I was even thinking that we should rename the bob-copy-chips plugin
  to bob-chips and include this functionality there, but I'll let you make that call.
- These chips should allow me to run `bob` command's from Obsidian just like I had ran
  the commands (we should support bulk commands) from Obsidian's command mode using the
  `<ctrl+enter>` keymap in the command mode panel.
- The `<cmd+enter>` keymap should be able to be used when the current line (or the
  current task as a fallback) contains a single command chip. Make sure we make it clear
  that this keymap is available for this functionality somehow when a supported line is
  selected.
- We should start using command chips in any existing recurring tasks (in the
  ~/bob/gtd_daily.md file, for example) that contain one or more `bob` commands.
- As a part of this change, we should add a new glossary term for "command chip".
- Review the obsidian_command_chips.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- #beau

#plan %m:@xlarge %w:research.5k.linker