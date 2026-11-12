%model:@small
#gh:gh_bobs-org__bob-cli @plan:202611/gcal_sync_last_n_days.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- day_interaction = union (planner default: union). Implement the "day_interaction = union" branch; ignore "day_interaction = conflict". Context: "Should -n combine with explicit -D days into one deduped run?".
- n_bound = capped (planner default: capped). Implement the "n_bound = capped" branch; ignore "n_bound = uncapped". Context: "Should -n reject values above 366?".
Implement only the branches selected above.
%macros_enabled:true
