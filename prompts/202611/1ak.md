- **AGENTS:**
  - [bbugyi200.athena.1ak](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ak.md)
- **ARTIFACTS:**
  - [hourly_gmail_sync_cron.md](https://github.com/bobs-org/bob-cli--plans/blob/f55bff9503e63fcd2de9a5f9b2ff36c35f080b40/202611/hourly_gmail_sync_cron.md)

%model:@small #gh:gh_bobs-org__bob-cli [@plan:202611/hourly_gmail_sync_cron.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- retire_cleanup = delete (planner default: delete). Implement the "retire_cleanup =
  delete" branch; ignore "retire_cleanup = keep". Context: "Also delete the spent
  cron.retire migration aid and close bead bob-cli-if in this change?". Implement only
  the branches selected above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/f55bff9503e63fcd2de9a5f9b2ff36c35f080b40/202611/hourly_gmail_sync_cron.md
