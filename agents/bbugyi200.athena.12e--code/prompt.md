%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/refs_panel_remembers_view.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- scroll_up_key = ctrl_shift_u (planner default: ctrl_y). Implement the "scroll_up_key = ctrl_shift_u" branch; ignore "scroll_up_key = ctrl_y", "scroll_up_key = ctrl_b". Context: "Which key should take over the preview's half-page-up scroll, now that Ctrl-U resets the panel?".
- esc_closes = keep (planner default: keep). Implement the "esc_closes = keep" branch; ignore "esc_closes = ladder". Context: "Should Esc close Bob Refs at once, keeping the query, filters, selection, and preview scroll?".
- tabs_entry = restore (planner default: restore). Implement the "tabs_entry = restore" branch; ignore "tabs_entry = fresh". Context: "Should Shift-⌘O (Bob Refs in Tabs) also restore the remembered query, scope, selection, and scroll?".
Implement only the branches selected above.
