- **AGENTS:**
  - [bbugyi200.athena.1av](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1av.md)
- **ARTIFACTS:**
  - [dot_alias_prefers_dependency_once_routed.md](https://github.com/bobs-org/bob-cli--plans/blob/08fdb8430884df8477ca06b64a86f060280a3609/202611/dot_alias_prefers_dependency_once_routed.md)

%model:@medium #gh:gh_bobs-org__bob-cli
[@plan:202611/dot_alias_prefers_dependency_once_routed.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- routed_scope = any_route (planner default: any_route). Implement the "routed_scope =
  any_route" branch; ignore "routed_scope = block_id". Context: "Should a bare `@route`
  or `@route#section` also make a spaced `.` prefer `&`, not just
  `@route:id`/`^id`/`+id`?".
- memory_glossary_capture_alias = yes 🧠. Memory edits are authorized for
  glossary:capture-alias only. Context: "Should the glossary capture-alias strand be
  updated for the new spaced `.` precedence?". No other memory note may be edited.
  Implement only the branches selected above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/08fdb8430884df8477ca06b64a86f060280a3609/202611/dot_alias_prefers_dependency_once_routed.md
