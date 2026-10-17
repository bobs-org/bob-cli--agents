#gh:gh_bobs-org__bob-cli A ref note's ID, which is recorded in the marker note left on the corresponding
PDF file, should always match the basename of the ref note (i.e. `foo` if the reference
file is ~/bob/ref/chat/foo.md) with exceptions being made only to prevent duplicate IDs
(they should be distinct across the entire ~/bob/ref/ directory). The `bob ref rename`
command doesn't seem to respect this constraint. Can you help me fix this?

#plan %m:@xlarge