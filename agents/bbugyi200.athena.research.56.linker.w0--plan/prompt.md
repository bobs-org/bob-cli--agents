#gh:gh_bobs-org__bob-cli When the `bob ref scan` command is run on my macbook, it sometimes updates the
`status:` field of some ref PDF markers. This is normally fine, but when I have one of
those PDFs opened in the Highlights app, I trigger a conflict if I try to leave an
annotation on that PDF. I then need to revert that annotation (and any others I've made
before attempting to save) and re-apply it. I think we can probably fix this by having
the `bob ref scan` command automatically close the Highlights app tab corresponding with
that PDF and then re-open that PDF in the Highlights app, right? Can you help me
implement this?

- To make this change safer, we should also attempt to save any unsaved annotations in
  the Highlights app (pressing `<cmd+s>` works in the app but I'm not sure if there is a
  better way to automate this).
- Make sure that we make it clear to the user somehow when we do this (e.g. by sending a
  mac notification).
- Review the highlights_open_pdf_coordinated_marker_writes.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.56.linker