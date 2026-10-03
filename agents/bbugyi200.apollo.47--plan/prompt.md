#gh:gh_bobs-org__bob-cli Can you help me make it so the `bob capture` command and the corresponding
bob-mac-capture app only require the leading index for the `=x` sub-bullets that are
added as work log entries when necessary to disambiguate? For example, consider the
following capture input:

```
=x3,4
- 3 foo bar
- 4 baz bam
```

This should be equivalent to the following since there are only two task links to
associate with two sub-bullets (we associate them based on their order):

```
=x3,4
- foo bar
- baz bam
```

#plan %m:@xlarge %auto