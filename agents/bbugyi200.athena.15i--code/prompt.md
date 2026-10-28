%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/stats_window_bars.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- theme_contract = full (planner default: full). Implement the "theme_contract = full" branch; ignore "theme_contract = top5". Context: "Should bob keep every theme in the JSON window summary so the theme bar can show them all?".
- legend_values = time (planner default: time). Implement the "legend_values = time" branch; ignore "legend_values = share". Context: "Should each legend item show that row's time in the window, such as bob 28h 36m?".
- window_morph = morph (planner default: morph). Implement the "window_morph = morph" branch; ignore "window_morph = still". Context: "Should the bars glide from the old window's proportions to the new one's on a range change?".
Implement only the branches selected above.
