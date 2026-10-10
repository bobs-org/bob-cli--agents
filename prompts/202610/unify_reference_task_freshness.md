- **PLAN:**
  [202610/unify_reference_task_freshness.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unify_reference_task_freshness.md)
- **AGENTS:**
  - [bbugyi200.apollo.65--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.65.md)

Can you help me remove the `freshness.reference_interval` configuration field?

- Ref tasks should be treated just like other tasks when it comes to freshness (i.e.
  they should use `freshness.interval` if ready, `freshness.pending_interval` if
  pending, and `freshness.next_interval` if next).
- Also, we should remove the `REF` review group from my GTD morning review (started via
  the `]s` keymap). Ref tasks should be dispersed across the other review groups.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
