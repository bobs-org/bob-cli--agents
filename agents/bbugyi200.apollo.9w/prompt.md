#gh:gh_bobs-org__bob-cli I was planning on using the below prompt to launch a sase agent that improves
the recently added support for undirected relations (see the bob-cli-am epic bead for
context). What do you think about this prompt? Am I missing anything? Make sure your
report is concise and easy to understand. #research %m:@xlarge

## THE PROMPT

Can you help me get rid of the `~~` capture syntax and instead use `<` and `>` in-place
of `|` to specify the direction of the relation when specifying the relation
description?

- The recent introduction of undirected relations (see the bob-cli-am epic bead for
  context) makes the `~~` syntax a lot less intuitive. Make sure the bob-mac-capture
  app's relation card still works after this change (i.e. is triggered when
  appropriate).
- Also, as a part of this change, let's get rid of the capital `L` option from the
  Obsidian task card and make the user specify the directed link direction before typing
  in a relation description somehow.