- **PLAN:**
  [202610/mac_menu_bar_ping_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_menu_bar_ping_indicator.md)
- **AGENTS:**
  - [bbugyi200.apollo.57--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.57.md)

I use the `tmux_ping` script (defined in my chezmoi repo) to show a count of the last 20
ping results (to 8.8.8.8) in the tmux status bar with the goal of giving the user some
sense as to whether or not they have internet connectivity.

- The problem is that it is only shown in the tmux bar, so if my terminal is not active
  I don't see it.
- I would like to show this count in my mac menu bar (on my macbook) in addition to my
  tmux status bar.
- I think we can accomplish this using Hammerspoon (in my chezmoi repo) maybe?
- Think hard about the best way to do this without increasing the network traffic on my
  macbook (i.e. without pinging more than we need to).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Can you help me implement this? Think this through thoroughly and create a plan using
your `/sase_plan` skill. Choose and author the appropriate tier, validate and revalidate
until it passes, then submit it with `sase plan propose` (as the skill instructs) before
making any file changes.
