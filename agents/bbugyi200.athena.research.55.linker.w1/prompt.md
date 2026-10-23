#gh:gh_bobs-org__bob-cli I would like to add support for a new "rotten log" (a good glossary entry
should be added for this new term--but no new decisions memory web strand should be
added). Can you help me implement this?

- This should work like the work log, but the prompt for an optional rotten log entry
  should occur when a rotten task (during our GTD morning review, for example) is
  refreshed using the `<alt+f>` or `<ctrl+alt+f>` keymaps.
- The goal of this change is to add a visual indication (and an audit trail) that shows
  how many times (and when and why) a task has been manually refreshed.
- Review the rotten_log_keep_history.md file in the research sidecar repo for context
  and inspiration before planning. I agree with all of the requirements recommended in
  that research file (but keep in mind that you are responsible for planning and
  splitting up this work appropriately).
- #beau

#plan %m:@xlarge %w:research.55.linker