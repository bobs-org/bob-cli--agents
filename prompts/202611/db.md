- **AGENTS:**
  - [bbugyi200.apollo.db](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.db.md)
- **ARTIFACTS:**
  - [fix_check_ignore_literal_pathspecs.md](https://github.com/bobs-org/bob-cli--plans/blob/07c8231051a433eeed827feb0526cb6d02f8e1e8/202611/fix_check_ignore_literal_pathspecs.md)

%model:@small #gh:gh_bobs-org__bob-cli
[@plan:202611/fix_check_ignore_literal_pathspecs.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- colon_guard = guard (planner default: guard). Implement the "colon_guard = guard"
  branch; ignore "colon_guard = restore". Context: "Should `check_ignore_quiet` fail
  closed on a rel path that starts with `:`?". Implement only the branches selected
  above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/07c8231051a433eeed827feb0526cb6d02f8e1e8/202611/fix_check_ignore_literal_pathspecs.md
