- **AGENTS:**
  - [bbugyi200.apollo.ed](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ed.md)
- **ARTIFACTS:**
  - [ctrl_enter_leaves_pre.md](https://github.com/bobs-org/bob-cli--plans/blob/fe19dfef008a6c7b68ae7eb4e98437ad55f0053f/202611/ctrl_enter_leaves_pre.md)

%model:@medium #gh:gh_bobs-org__bob-cli [@plan:202611/ctrl_enter_leaves_pre.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- exit_guard = guard (planner default: guard). Implement the "exit_guard = guard"
  branch; ignore "exit_guard = plain". Context: "Add a 1.5 s guard after the PRE exit
  landing that swallows a repeated rapid press?".
- post_next = land (planner default: land). Implement the "post_next = land" branch;
  ignore "post_next = stop". Context: "When POST is the only group left after PRE,
  should Ctrl+Enter land on POST's first row?".
- memory_new_record = yes 🧠. Memory edits are authorized for
  decisions:ctrl-enter-leaves-pre only. Context: "Add the decision record
  decisions/ctrl-enter-leaves-pre for this course change?".
- memory_supersede_answering = yes 🧠. Memory edits are authorized for
  decisions:answering-advances-the-walk only. Context: "Mark
  decisions/answering-advances-the-walk superseded in part by the new record?". No other
  memory note may be edited. Implement only the branches selected above.
  %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/fe19dfef008a6c7b68ae7eb4e98437ad55f0053f/202611/ctrl_enter_leaves_pre.md
