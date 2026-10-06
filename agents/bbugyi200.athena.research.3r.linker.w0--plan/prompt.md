#gh:gh_bobs-org__bob-cli I would like to add a new `--listen` option to the `bob highlights create`
command that uses the `sase-listen render <target> -e full` command (see the
sase-org/sase-listen repo on GitHub) to create a new podcast episode (that gets
published to a feed that I subscribe to from the AntennaPod app on my phone) alongside
the PDF and ref note that is linked to from the PDF we generate. Can you help me
implement this?

- The goal of this change is to make sure that I am always tracking articles / papers
  that I listen to via AI audio transcriptions in my Obsidian ref note system.
- We should not depend directly on the `sase-listen` command, but should instead make
  this configurable (make the appropriate changes to my bob config, which is defined in
  my chezmoi repo).
- Also, as a part of this change, i want to make sure that the `bob highlights create`
  command supports the same values for `<target>` that the `sase-listen render` command
  does. Namely, it should support URLs that point to PDFs. It should also have the same
  special support for arxiv that sase-listen does. When `<target>` points to a PDF, we
  obviously don't need to create a new PDF (just use that one), but make sure to add the
  appropriate Highlghts note and store it in the proper location still.
- The `sase-listen render` command's output should be shown in full if it is run by the
  `bob highlghts create` command.
- Review the web_url_reference_pdf_capture.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the recommendations made in that research file.
- #beau

#plan %m:@xlarge %auto %w:research.3r.linker