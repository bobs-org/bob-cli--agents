#gh:gh_bobs-org__bob-cli Can you help me fix a bug with the `<ctrl+j>` keymap used by the
bob-mac-capture app? Namely, we do not delete the bullet and insert a blank line in all
of the cases where we are supposed to. For example, consider the following state:

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

#plan %m:@xlarge %auto