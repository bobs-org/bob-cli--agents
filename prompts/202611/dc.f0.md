- **AGENTS:**
  - [bbugyi200.apollo.dc.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.dc.f0.md)
- **ARTIFACTS:**
  - [plugins_sync_cwd_and_fetch.md](https://github.com/bobs-org/bob-cli--plans/blob/362e122b4e100d06976c096e625b7bb32220b673/202611/plugins_sync_cwd_and_fetch.md)

%model:@medium #gh:gh_bobs-org__bob-cli [@plan:202611/plugins_sync_cwd_and_fetch.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- cwd_scope = family (planner default: family). Implement the "cwd_scope = family"
  branch; ignore "cwd_scope = sync_only". Context: "Should enclosing-checkout repo
  resolution apply to the whole `bob plugins` family?".
- fetch_fallback = fetch (planner default: fetch). Implement the "fetch_fallback =
  fetch" branch; ignore "fetch_fallback = status_quo". Context: "When the repo-refresh
  `git pull` fails, should sync fall back to `git fetch`?". Implement only the branches
  selected above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/362e122b4e100d06976c096e625b7bb32220b673/202611/plugins_sync_cwd_and_fetch.md
