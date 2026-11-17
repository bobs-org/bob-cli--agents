- **AGENTS:**
  - [bbugyi200.apollo.eo.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.eo.f0.md)
- **ARTIFACTS:**
  - [record_card_field_jump_co_landing.md](https://github.com/bobs-org/bob-cli--plans/blob/5b1541c8ab74000f5f24e2eafa50cafc52ed05b1/202611/record_card_field_jump_co_landing.md)

%model:@medium #gh:gh_bobs-org__bob-cli
[@plan:202611/record_card_field_jump_co_landing.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- record_card_digits = pick (planner default: pick). Implement the "record_card_digits =
  pick" branch; ignore "record_card_digits = pick_only", "record_card_digits =
  field_numbers". Context: "What should digits and Shift+J/K do on the Record Card,
  given the Schema Card's field jumps?".
- climb_keeps_field = yes (planner default: yes). Implement the "climb_keeps_field =
  yes" branch; ignore "climb_keeps_field = no". Context: "Should = on the Record Card
  open the album Schema Card already on the same field?".
- scoped_force = yes (planner default: yes). Implement the "scoped_force = yes" branch;
  ignore "scoped_force = no". Context: "May the remaining ms/mu agents pass -F to clear
  a sync refusal when the refused build has provably landed?". Implement only the
  branches selected above. %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/5b1541c8ab74000f5f24e2eafa50cafc52ed05b1/202611/record_card_field_jump_co_landing.md
