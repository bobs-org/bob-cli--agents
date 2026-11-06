%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/lane_walk_keymaps.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- order = lane (planner default: lane). Implement the "order = lane" branch; ignore "order = note". Context: "Should the walk visit every PENDING task before any NEXT task, with note order inside each lane?".
- endpoints = yes (planner default: yes). Implement the "endpoints = yes" branch; ignore "endpoints = no". Context: "Should [W / ]W jump to the first / last lane-walk task, mirroring [S / ]S?".
- decision_record = no. Do not edit decisions:lane-walk-is-navigation-only. Context: "Should a decisions strand record that ]w is a navigation-only walk over exactly the dash PENDING/NEXT sections?".
No other memory note may be edited.
Implement only the branches selected above.
