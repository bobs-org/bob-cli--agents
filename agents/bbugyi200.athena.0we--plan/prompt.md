#gh:gh_bobs-org__bob-cli Can you help me add new `just install-all` and `just install-all-and-restart`
commands?

- The `just install-all` command should first sync the repo by running `git pull`. It
  should then run `just install` for the bob-cli project, then install the bob-plugins
  and bob-mac-capture projects by running the `git pull` and `bob plugins sync` (for the
  bob-plugins repo) / `just install` (for the bob-mac-capture repo) commands in those
  directories. Think hard about this and make sure to get these installations right
  (make any changes to my requirements you think are necessary but clearly call these
  out in your plan).
- We should check for these project directories in the parent directory of the bob-cli
  project (in the ~/projects/github/bobs-org/ directory on this machine, for example).
  If one of those directories does not exist, we should skip the install for that
  project gracefully.
- The `just install-all-and-restart` command should first run the `just install-all`
  command and should then restart the Obsidian app, if it is running on that machine.
- I intend to use this to make it easier to re-install bob-cli, bob-plugins, and
  bob-mac-capture all at once and then restart Obsidian on my macbook.
- #beau

#plan %m:@xlarge %auto