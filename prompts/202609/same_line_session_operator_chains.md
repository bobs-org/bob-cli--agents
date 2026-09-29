- **PLAN:**
  [202609/same_line_session_operator_chains.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/same_line_session_operator_chains.md)
- **AGENTS:**
  - [bbugyi200.apollo.36--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.36.md)

The `bob capture` command and the corresponding bob-mac-capture app support using the
`+`, `-`, `++`, `--`, `=`, and `=x` syntaxes together as long as they are in separate
parts of a bulk capture. For example, the following input to bob-mac-capture works as it
should:

```
+2

=x
```

Can you help me make it possible to use these on the same line separated by spaces too
so after this change, for example, we should be able to just use `+2 =x` to specify the
same behavior. Think this through thoroughly and create a plan using your `/sase_plan`
skill. Choose and author the appropriate tier, validate and revalidate until it passes,
then submit it with `sase plan propose` (as the skill instructs) before making any file
changes.
