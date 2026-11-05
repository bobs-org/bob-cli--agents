%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/close_selection_explicit_mode.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- drop_lists_explicit = any_number (planner default: any_number). Implement the "drop_lists_explicit = any_number" branch; ignore "drop_lists_explicit = drop_only". Context: "Should a `~<K>` list alone (for example `x~2`) also switch the close to explicit mode?".
- event_clock_in_explicit = keep_clock (planner default: defer_unlisted). Implement the "event_clock_in_explicit = keep_clock" branch; ignore "event_clock_in_explicit = defer_unlisted". Context: "In explicit mode, should unlisted Event Task links defer instead of taking their clock default?".
- memory_close_selection_record = yes 🧠. Memory edits are authorized for decisions:close-selections-list-explicitly, decisions:event-task-links-close-by-the-clock only. Context: "Add decision record close-selections-list-explicitly and mark the Event Task clock record superseded-in-part?".
No other memory note may be edited.
Implement only the branches selected above.
