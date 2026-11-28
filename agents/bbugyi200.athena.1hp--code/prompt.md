%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/bank_note_completion_cold_payees.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- empty_field_fill = fill (planner default: fill). Implement the "empty_field_fill = fill" branch; ignore "empty_field_fill = only_when_none". Context: "When the note field is empty, should other payees' notes fill the list after this payee's own notes?".
- empty_ghost = own_payee_only (planner default: own_payee_only). Implement the "empty_ghost = own_payee_only" branch; ignore "empty_ghost = any_payee". Context: "On an empty field, should the faint ghost text preview the top note even when it came from another payee?".
Implement only the branches selected above.
%macros_enabled:true
