#gh:gh_bobs-org__bob-cli The `bob capture` command and the corresponding bob-mac-capture app support
using the `+`, `-`, `++`, `--`, `=`, and `=x` syntaxes together as long as they are in
separate parts of a bulk capture. For example, the following input to bob-mac-capture
works as it should:

```
+2

=x
```

Can you help me make it possible to use these on the same line separated by spaces too
so after this change, for example, we should be able to just use `+2 =x` to specify the
same behavior. #plan %m:@xlarge %auto %wait(bead=bob-cli-2n)