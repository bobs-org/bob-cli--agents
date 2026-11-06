- **AGENTS:**
  - [bbugyi200.apollo.bp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bp.md)
- **ARTIFACTS:**
  - [capture_plus_separator_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/137273775fcc1df32092559c35c747fb77258d7f/202610/capture_plus_separator_toggle.md)

%model:@medium #gh:gh_bobs-org__bob-cli
[@plan:202610/capture_plus_separator_toggle.md][1]

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):

- caret_plus = exempt (planner default: switch). Implement the "caret_plus = exempt"
  branch; ignore "caret_plus = switch". Context: "Should `+` after `@file^id` also
  switch to `@file+id`, though `@file^id+` is the project-note form?".
- reverse_from_plus = three_way (planner default: one_way). Implement the
  "reverse_from_plus = three_way" branch; ignore "reverse_from_plus = one_way". Context:
  "Should `:` or `^` typed after `@file+id` also switch it to `@file:id` or
  `@file^id`?". Implement only the branches selected above.

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/137273775fcc1df32092559c35c747fb77258d7f/202610/capture_plus_separator_toggle.md
