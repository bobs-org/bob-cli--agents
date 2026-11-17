- **AGENTS:**
  - [bbugyi200.athena.1da](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1da.md)
- **ARTIFACTS:**
  - [schema_save_lock_wait.md](https://github.com/bobs-org/bob-cli--plans/blob/a8c078bcc0b3e1bf22ce09c4cefffad8bcdc41ca/202611/schema_save_lock_wait.md)

%model:@medium #gh:gh_bobs-org__bob-cli [@plan:202611/schema_save_lock_wait.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- wait_budget = ten_minutes (planner default: ten_minutes). Implement the "wait_budget =
  ten_minutes" branch; ignore "wait_budget = until_stopped". Context: "Should a waiting
  save give up on its own after 10 minutes of lock contention?".
- scan_followup = file (planner default: file). Implement the "scan_followup = file"
  branch; ignore "scan_followup = skip". Context: "Should the implementer file a large
  follow-up task bead to shorten how long writing highlights scans hold bob_sync.lock?".
  Implement only the branches selected above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/a8c078bcc0b3e1bf22ce09c4cefffad8bcdc41ca/202611/schema_save_lock_wait.md
