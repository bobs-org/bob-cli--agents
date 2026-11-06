#gh:gh_bobs-org__bob-cli I would like to improve the way the `bob ref create` command renders tables in
PDF files somehow to make them work better with annotations made in the Highlights app
(it can be hard to highlight cell contents for some reason--I think the Highlights app
tries to select the table cell or something, but I'm not sure) and make them easier to
read (or, at the very least, don't decrease readability).

Can you help me implement this? Review the ref_create_table_layout_for_highlights.md file in the research sidecar
repo for context and inspiration before planning. I agree with all of the requirements
recommended in that research file (but keep in mind that you are responsible for
planning and splitting up this work appropriately).

#plan %m:@xlarge %w:research.2u.linker %auto