#gh:gh_bobs-org__bob-cli I would like to add better support for multiple captures on the same line to
the `bob capture` command and the corresponding bob-mac-capture app.

- The `-`, `+`, and `=` syntaxes already support this well when used together.
- For example, the `++2 =x =` capture works to perform the 3 corresponding capture
  actions all at once (without needing to put these on multiple lines).
- We should be able to always support this for these syntaxes. In other words, the `-`,
  `+`, and `=` syntaxes should always be able to be used at the end of other capture
  lines (even in task sub-bullets).

Can you help me implement this? #plan %m:@xlarge %w:0zy