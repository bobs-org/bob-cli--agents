#gh:gh_bobs-org__bob-cli We recently added the `just install-all` and `just install-all-and-restart`
commands. I would like to get rid of the `just install-all-and-restart` command in favor
of merging this functionality into the `just install-all` command with one change: We
should only restart Obsidian if the `bob plugins sync` command made changes to my
Obsidian vault (i.e. if the bob-plugins repo had changes, which justifies updating
Obsidian). Can you help me implement this?

#plan %m:@xlarge %auto