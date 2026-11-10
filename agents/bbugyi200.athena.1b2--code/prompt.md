%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/delete_file_confirm.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- old_notes = age (planner default: age). Implement the "old_notes = age" branch; ignore "old_notes = signals". Context: "Should every note older than the fresh window ask before Ctrl+Shift+D deletes it?".
- rapid_repeat = guard (planner default: guard). Implement the "rapid_repeat = guard" branch; ignore "rapid_repeat = signals_only". Context: "Should any delete within 5 seconds of the previous one ask, even for a fresh note?".
- fresh_window = day (planner default: day). Implement the "fresh_window = day" branch; ignore "fresh_window = hour". Context: "Should a note count as fresh (deletable without asking) for 24 hours after its created stamp?".
Implement only the branches selected above.
%macros_enabled:true
