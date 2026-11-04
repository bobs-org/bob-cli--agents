#gh:gh_bobs-org__bob-cli Can you help me make it possible to type `.` instead of `^` after the `@foo`
capture syntax to perform the same action (prompt for a block ID)?

- The `.` character is easier to type than `^`.
- The `.` character should immediately be replaced with `^` in this context.
- Let's also do something similar for the `;` key and `:` key (i.e. replace `;` with `:`
  and trigger the appropriate completion). This should include the case where `:` is the
  first key pressed in the capture input.

#plan %m:@xlarge