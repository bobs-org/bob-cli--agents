%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/command_mode_keys_and_run_indicator.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- indicator_label = brand (planner default: brand). Implement the "indicator_label = brand" branch; ignore "indicator_label = title", "indicator_label = icon". Context: "What should the footer run indicator show beside its spinner?".
- indicator_runs = all (planner default: all). Implement the "indicator_runs = all" branch; ignore "indicator_runs = sheet". Context: "Should the indicator count every run the command-mode engine owns, not only `:` sheet runs?".
Implement only the branches selected above.
