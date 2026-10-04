- **PLAN:**
  [202610/ctrl_j_body_start_bullet_removal.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_j_body_start_bullet_removal.md)
- **AGENTS:**
  - [bbugyi200.athena.0w5--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0w5.md)

Can you help me fix a bug with the `<ctrl+j>` keymap used by the bob-mac-capture app?
Namely, we do not delete the bullet and insert a blank line in all of the cases where we
are supposed to. For example, consider the following state:

```
+2
- <cursor>foo bar baz
```

Since the cursor is at the beginning of the line (with the exception of the bullet), if
the user presses `<ctrl+j>`, the result should be the following:

```
+2

<cursor>foo bar baz
```

But, instead, we get the following:

```
+2
-
- <cursor>foo bar baz
```

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
