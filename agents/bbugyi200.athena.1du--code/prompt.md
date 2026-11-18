%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/sdd_clone_recovery_spares_live_work.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- dirty_clone_policy = preserve (planner default: preserve). Implement the "dirty_clone_policy = preserve" branch; ignore "dirty_clone_policy = unclaimed_only". Context: "How should machine-managed SDD integration treat a clone whose only problem is uncommitted edits?".
- name_snapshot = yes (planner default: yes). Implement the "name_snapshot = yes" branch; ignore "name_snapshot = no". Context: "Should the finalizer's dirty-work-vanished error name the SDD recovery snapshot and its restore command?".
Implement only the branches selected above.
%macros_enabled:true
