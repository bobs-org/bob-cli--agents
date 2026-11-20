- **AGENTS:**
  - [bbugyi200.athena.1ek](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ek.md)
- **ARTIFACTS:**
  - [install_all_mac_capture_skip_unchanged.md](https://github.com/bobs-org/bob-cli--plans/blob/f19a0ebb2a92d007ae9dfdef40ff7b34a9221e3d/202611/install_all_mac_capture_skip_unchanged.md)

%model:@medium #gh:gh_bobs-org__bob-cli
[@plan:202611/install_all_mac_capture_skip_unchanged.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- rebuild_trigger = app_inputs (planner default: app_inputs). Implement the
  "rebuild_trigger = app_inputs" branch; ignore "rebuild_trigger = any_change". Context:
  "Should install-all also skip the rebuild when only docs, tests, or repo metadata
  changed since the last install?". Implement only the branches selected above.
  %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/f19a0ebb2a92d007ae9dfdef40ff7b34a9221e3d/202611/install_all_mac_capture_skip_unchanged.md
