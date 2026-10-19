#gh:gh_bobs-org__bob-cli I wish the screenshot utility that I use, which is triggered by the
`<ctrl+shift+opt+s>` keymap (defined in my chezmoi repo I believe), was easier to use
when I want to take a screenshot of a very specific rectangular space on my screen. Can
you help me implement this?

- Namely, i want to be able to click and drag from one corner of the specific
  rectangular space to the other to trigger a resize of the screenshot capture area.
- Currently, I need to drag the corners of the screenshot area box itself to get the
  screenshot area right.
- I still need the ability to click and drag the screenshot area, but I was thinking
  that I could support that by requiring that I hold the `<cmd>` key while dragging.
- Review the screenshot_region_draw_first_selection.md file in the research sidecar repo
  for context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).

#plan %m:@xlarge %w:research.50.linker