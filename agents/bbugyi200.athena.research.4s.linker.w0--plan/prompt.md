#gh:gh_bobs-org__bob-cli I currently run the `bob ref create` command from multiple different machines
(any of the three on my tailnet), but I am not able to use the PDF file that is
generated until I run the `bob ref scan` command somehow. I would like to think of a way
to make this much more convenient/automatic somehow so I rarely need to run the
`bob ref scan` command manually, but I'm not sure how to achieve this reliably.

Can you help me implement this? Review the ref_create_auto_ingest_across_tailnet.md file in the research sidecar
repo for context and inspiration before planning. I agree with all of the requirements
recommended in that research file (but keep in mind that you are responsible for
planning and splitting up this work appropriately).

#plan %m:@xlarge %auto %w:research.4s.linker