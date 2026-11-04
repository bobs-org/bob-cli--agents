#gh:gh_bobs-org__bob-cli #fork:185.f0 Can you now help me do the same thing for the `\` and `#`
characters when `\` is pressed in a context that accepts `#`?

- The exception should be at the beginning of the line, where we already replace `\`
  with `/`.
- Typing `\` a second time should result in an actual `\` being rendered (dismissing
  completion for types/drawers).

#plan %m:@xlarge