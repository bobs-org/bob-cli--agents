#gh:gh_bobs-org__bob-cli Can you help me remove the `freshness.reference_interval` configuration field?

- Ref tasks should be treated just like other tasks when it comes to freshness (i.e.
  they should use `freshness.interval` if ready, `freshness.pending_interval` if
  pending, and `freshness.next_interval` if next).
- Also, we should remove the `REF` review group from my GTD morning review (started via
  the `]s` keymap). Ref tasks should be dispersed across the other review groups.

#plan %m:gpt-6-astra %auto