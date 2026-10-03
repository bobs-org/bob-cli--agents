#gh:gh_bobs-org__bob-cli Can you help me add support to the `bob capture` command and the corresponding
bob-mac-capture app for the new `=*` and `=!` syntaxes?

- `=*<N>` should be a shorthand for `=x*<N>` and `=!<N>` should be a shorthand for
  `=x!<N>`.
- Also, we should start making `<N>` optional and have it default to `1` (for example,
  `=*` should be equivalent to `=*1` which should be equivalent to `=x*1`).
- #beau

#plan %m:gpt-6-astra %auto