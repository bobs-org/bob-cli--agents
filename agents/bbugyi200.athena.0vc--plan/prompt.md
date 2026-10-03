#gh:gh_bobs-org__bob-cli The `bob capture` command and the corresponding bob-mac-capture app currently
support the syntax demonstrated below (using bulk-capture syntax) which allows users to
add work log entries when using the `=`, `=*`, and `=x` syntaxes:

```
=x
- 1 foo bar baz

=1,3,4
- 3 boom
```

Can you help me make this case (a single work log entry) easier to type by making it
equivalent to the following syntax? Note that, when we omit the number, we should start
assuming the first index (i.e. 1):

```
=x foo bar baz

=1,3,4 3 boom
```

We should still require the sub-bullet syntax be used if the user wants to add multiple
work log entries. #beau #plan %m:@xlarge %auto