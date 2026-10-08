#gh:gh_bobs-org__bob-cli Can you help me make sure that the `bob ref create` command de-duplicates the
target PDF filename that is automatically used unless the `-o|--output` option is given
explicitly? #if_not_plan I'm pretty sure that this command currently fails if the
automatically chosen PDF path already exists (which is not correct). We should still
fail if the same ref note has already been captured (i.e. we already track this
reference in my Obsidian vault). %m:@xlarge %auto