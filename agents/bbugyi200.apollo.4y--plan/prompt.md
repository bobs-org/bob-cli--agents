#gh:gh_bobs-org__bob-cli I think that the `bob` command could organize its sub-commands more effectively
to make them easier / more intuitive to understand, but I'm not sure which sub-commands
(if any) deserve to be grouped together under one sub-command. For example, maybe we
should consider grouping some of bob's current sub-commands under a new `bob task`
sub-command?

Can you help me implement this? Review the bob_cli_command_tree_reorganization.md file
in the research sidecar repo for context and inspiration before planning. I agree with
all of the recommendations made in that research file (implement all of them). Make sure
to update all references to commands that will be moved/renamed in my chezmoi repo (I'm
not sure that any updates will be necessary here, but you should check). #beau

#plan %m:@xlarge %auto