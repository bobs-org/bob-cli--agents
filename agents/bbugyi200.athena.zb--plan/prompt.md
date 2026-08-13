#gh:gh_bobs-org__bob-cli The `bob highlights create` command currently creates a new PDF file in the
~/bob/lib/chat/ directory. Can you help me have it start using the new ~/bob/xlib/chat/
directory instead?

- This Obsidian directory, unlike the ~/bob/lib/ directory, should be tracked by
  Obsidian Sync (make sure this is the case).
- As a part of this change, you should also modify the `bob highlights scan` command to
  always check this directory for any PDF files and, if found, move them to the
  corresponding subdirectory in ~/bob/lib/.
- Make sure the `bob highlights scan` command does this before creating any Obsidian ref
  note files (since a PDF moved to the ~/bob/lib/ directory may change which note files
  we should create).

#plan #m_opus