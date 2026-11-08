#gh:gh_bobs-org__bob-cli We already support a few different short-hand characters (ex: `,`, `.`, `=`,
`;`) that are auto-replaced with other characters in the bob-mac-capture app in certain
contexts. I would now like to add support for two new similar short-hand characters. Can
you help me implement this?

- These characters will be `x` and `s`.
- These will be replaced with `!` and `*` respectively, when used with the `x` syntax.
  For example, typing `xx` should result in `x!` in contexts where the `x` capture
  syntax is respected.
- Similarly, these will be repaced with `!` and `*`, respectively, when used instead of
  the second `=` that is supported by the `x=` capture syntax. For example, typing
  `x=1=s` should result in `x=1=*` in contexts where the `x=` capture syntax is
  supported.
- Review the close_outcome_x_s_typing_aliases.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

#plan %m:@xlarge %w:research.3r.linker