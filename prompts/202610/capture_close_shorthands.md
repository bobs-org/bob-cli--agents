- **PLAN:**
  [202610/capture_close_shorthands.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_close_shorthands.md)
- **AGENTS:**
  - [bbugyi200.athena.0vf--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vf.md)

Can you help me add support to the `bob capture` command and the corresponding
bob-mac-capture app for the new `=*` and `=!` syntaxes?

- `=*<N>` should be a shorthand for `=x*<N>` and `=!<N>` should be a shorthand for
  `=x!<N>`.
- Also, we should start making `<N>` optional and have it default to `1` (for example,
  `=*` should be equivalent to `=*1` which should be equivalent to `=x*1`).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
