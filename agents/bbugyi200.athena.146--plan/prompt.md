#gh:gh_bobs-org__bob-cli Can you help me add new keymaps that are only active when the Highlights app is
active on my macbook?

- Think hard about the best way to do this. The options I've thought of (feel free to go
  with your own option if better): (1) Hammerspoon config in my chezmoi repo (2) Achieve
  this with the bob-mac-capture app somehow (I think it sets some Highlights app keymaps already).
- The keymaps:
  - `\\`: Close all other Highlights app tabs except for the currently selected tab.
  - `\<`: Close all Highlights app tabs to the left of the currently selected tab.
  - `\>`: Close all Highlights app tabs to the right of the currently selected tab.

#plan %m:@xlarge