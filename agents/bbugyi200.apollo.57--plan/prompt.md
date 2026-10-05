#gh:gh_bobs-org__bob-cli I use the `tmux_ping` script (defined in my chezmoi repo) to show a count of
the last 20 ping results (to 8.8.8.8) in the tmux status bar with the goal of giving the
user some sense as to whether or not they have internet connectivity.

- The problem is that it is only shown in the tmux bar, so if my terminal is not active
  I don't see it.
- I would like to show this count in my mac menu bar (on my macbook) in addition to my
  tmux status bar.
- I think we can accomplish this using Hammerspoon (in my chezmoi repo) maybe?
- Think hard about the best way to do this without increasing the network traffic on my
  macbook (i.e. without pinging more than we need to).
- #beau

Can you help me implement this? #plan %m:@xlarge %auto