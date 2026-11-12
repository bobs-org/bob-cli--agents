- **AGENTS:**
  - [bbugyi200.apollo.dn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.dn.md)
- **ARTIFACTS:**
  - [gcal_sync_multi_day.md](https://github.com/bobs-org/bob-cli--plans/blob/3fe156c637f6a514e7b82b911cc68f34fff91a00/202611/gcal_sync_multi_day.md)

%model:@medium #gh:gh_bobs-org__bob-cli [@plan:202611/gcal_sync_multi_day.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- fetch_batching = runs (planner default: runs). Implement the "fetch_batching = runs"
  branch; ignore "fetch_batching = per_day". Context: "Should one run batch Google event
  fetches across the requested days?".
- json_shape = wrapper (planner default: wrapper). Implement the "json_shape = wrapper"
  branch; ignore "json_shape = jsonl". Context: "Should multi-day JSON print one wrapper
  document instead of one line per day?".
- error_mode = stop (planner default: stop). Implement the "error_mode = stop" branch;
  ignore "error_mode = continue". Context: "When one day fails mid-run, should the
  remaining days stop?". Implement only the branches selected above.
  %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/3fe156c637f6a514e7b82b911cc68f34fff91a00/202611/gcal_sync_multi_day.md
