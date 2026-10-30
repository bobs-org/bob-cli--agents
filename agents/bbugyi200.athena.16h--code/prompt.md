%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/command_mode_recent_rerun.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- recent_enter = guarded (planner default: guarded). Implement the "recent_enter = guarded" branch; ignore "recent_enter = verbatim". Context: "Should Enter on a RECENT row honor its preview-first/confirm guard, with Ctrl+Enter as the immediate rerun?".
- replay_guards = fix (planner default: fix). Implement the "replay_guards = fix" branch; ignore "replay_guards = leave". Context: "Should Retry/Apply toasts, Rerun last command, and pager r stop refusing applied preview-first or confirm runs?".
Implement only the branches selected above.
