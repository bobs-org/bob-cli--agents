- **AGENTS:**
  - [bbugyi200.apollo.cw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cw.md)
- **ARTIFACTS:**
  - [status_group_trailing_blank_lines.md](https://github.com/bobs-org/bob-cli--plans/blob/c39b1dba971fc221473f4d05065870642c0a5696/202611/status_group_trailing_blank_lines.md)

%model:@small #gh:gh_bobs-org__bob-cli
[@plan:202611/status_group_trailing_blank_lines.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- gap_rule = cap (planner default: cap). Implement the "gap_rule = cap" branch; ignore
  "gap_rule = targeted". Context: "Cap a rewritten Tasks section's trailing gap at one
  blank line (vs. only discounting a dropped group's separator)?".
- vault_cleanup = leave (planner default: leave). Implement the "vault_cleanup = leave"
  branch; ignore "vault_cleanup = trim_now". Context: "Should the coder also hand-trim
  the extra blank lines in the live ~/bob notes now?". Implement only the branches
  selected above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/c39b1dba971fc221473f4d05065870642c0a5696/202611/status_group_trailing_blank_lines.md
