%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/plugins_sync_cwd_and_fetch.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- cwd_scope = family (planner default: family). Implement the "cwd_scope = family" branch; ignore "cwd_scope = sync_only". Context: "Should enclosing-checkout repo resolution apply to the whole `bob plugins` family?".
- fetch_fallback = fetch (planner default: fetch). Implement the "fetch_fallback = fetch" branch; ignore "fetch_fallback = status_quo". Context: "When the repo-refresh `git pull` fails, should sync fall back to `git fetch`?".
Implement only the branches selected above.
%macros_enabled:true
