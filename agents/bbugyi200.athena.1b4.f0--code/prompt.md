%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/redo_survives_disk_reloads.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- reload_history = always (planner default: always). Implement the "reload_history = always" branch; ignore "reload_history = only_when_redo_pending". Context: "Should every disk reload of an open note stay out of that editor's undo history?".
- decision_record = no. Do not edit decisions:disk-reloads-stay-out-of-undo. Context: "Record the policy as a new decisions-web record (disk-reloads-stay-out-of-undo)?".
No other memory note may be edited.
Implement only the branches selected above.
%macros_enabled:true
