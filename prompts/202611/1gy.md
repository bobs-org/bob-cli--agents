- **AGENTS:**
  - [bbugyi200.athena.1gy](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gy.md)
- **ARTIFACTS:**
  - [fix_bob_plugins_failing_tests.md](https://github.com/bobs-org/bob-cli--plans/blob/1525e2c04f9d08f2100932a35d53eab1a3cc20a7/202611/fix_bob_plugins_failing_tests.md)

%model:@small #gh:gh_bobs-org__bob-cli
[@plan:202611/fix_bob_plugins_failing_tests.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- tmp_relief = relocate (planner default: relocate). Implement the "tmp_relief =
  relocate" branch; ignore "tmp_relief = delete", "tmp_relief = leave". Context: "Should
  the coder free athena's full /tmp tmpfs so `npm test` and the /tmp-bound e2e scripts
  can pass?". Implement only the branches selected above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/1525e2c04f9d08f2100932a35d53eab1a3cc20a7/202611/fix_bob_plugins_failing_tests.md
