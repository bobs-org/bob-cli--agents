#gh:gh_bobs-org__bob-cli I would like to improve the way that the `bob ref create` command renders PDFs
from markdown files. Can you help me implement this?

- Namely, I would like to add support for backlinks that make it very easy for the user
  reading the PDF to use local links to jump to a part of a document and then jump back
  to where they were originally.
- I think we can accomplish this by searching for any local links in the markdown,
  figuring out which part of the document they link to, adding a unique alphanumeric ID
  to the rendered local link text, and then adding a new local link at the original
  link's target destination that uses that same alphanumeric ID as rendered link text
  but links back to the original link.
- Review the ref_create_pdf_return_links.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the recommendations made in that research file.
- #beau

#plan %m:@xlarge %auto %w:research.3x.linker