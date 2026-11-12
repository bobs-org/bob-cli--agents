#gh:gh_bobs-org__bob-cli #fork:dn Can you now help me add a new `-n|--last-n-days` option that accepts an integer value?

- This option should be able to be used to sync the last N days, including today.
- For example, the `bob gcal sync -n 2` command should be equivalent to the `bob gcal sync -D today -D yesterday` command.
- #beau 

#plan %m:claude-fable-5 %w:dn.f0