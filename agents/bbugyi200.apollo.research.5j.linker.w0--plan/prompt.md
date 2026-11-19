#gh:gh_bobs-org__bob-cli I would like to add a new `-D|--delete` option to the `bob bank import`
command, so I can run `bank import -D ~/Downloads/*.qfx` from bob's command mode in
Obsidian. Can you help me implement this?

- When this option is specified, the QFX files that are imported should be deleted iff
  all imports were successful.
- Review the bank_import_delete_flag.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- #beau

#plan %m:@xlarge %w:research.5j.linker