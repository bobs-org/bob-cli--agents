#gh:gh_bobs-org__bob-cli I would like to add a new `:` keymap to Obsidian that triggers a new bob
command-mode. Can you help me implement this?

- The goal of this change is to make it so the user doesn't need to leave Obsidian to
  run common `bob` commands.
- This command-mode should support any bob command that might be useful to run from
  Obsidian. Think hard about which commands to add support for.
- It should be very easy to filter commands and select one to run from this new
  command-mode window.
- When the user runs a command from this command-mode, they should be notified of its
  completiono (on success or failure) with support for showing the full command output
  of the command that was run somehow.
- Review the bob_colon_command_mode.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.5c.linker