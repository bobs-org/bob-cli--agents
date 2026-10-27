- **AGENTS:**
  - [bbugyi200.apollo.al--code](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.al.md)
- **ARTIFACTS:**
  - [command_mode_keys_and_run_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/8da5f85aa092b50da24da9f7bf5e102c03ca03f2/202610/command_mode_keys_and_run_indicator.md)

%model:@medium #gh:gh_bobs-org__bob-cli
[@plan:202610/command_mode_keys_and_run_indicator.md][1]

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):

- indicator_label = brand (planner default: brand). Implement the "indicator_label =
  brand" branch; ignore "indicator_label = title", "indicator_label = icon". Context:
  "What should the footer run indicator show beside its spinner?".
- indicator_runs = all (planner default: all). Implement the "indicator_runs = all"
  branch; ignore "indicator_runs = sheet". Context: "Should the indicator count every
  run the command-mode engine owns, not only `:` sheet runs?". Implement only the
  branches selected above.

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/8da5f85aa092b50da24da9f7bf5e102c03ca03f2/202610/command_mode_keys_and_run_indicator.md
