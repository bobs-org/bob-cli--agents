%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/schema_save_lock_wait.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- wait_budget = ten_minutes (planner default: ten_minutes). Implement the "wait_budget = ten_minutes" branch; ignore "wait_budget = until_stopped". Context: "Should a waiting save give up on its own after 10 minutes of lock contention?".
- scan_followup = file (planner default: file). Implement the "scan_followup = file" branch; ignore "scan_followup = skip". Context: "Should the implementer file a large follow-up task bead to shorten how long writing highlights scans hold bob_sync.lock?".
Implement only the branches selected above.
%macros_enabled:true
