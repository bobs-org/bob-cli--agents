#gh:gh_bobs-org__bob-cli Our capture syntax already supports using bullets of the form `- Some note` or
`- <N> Some note`, where `<N>` is an integer index, when marking a pomodoro as done in
order to add work log entries to the corresponding tasks. Can you now help me add
support for `- * Some note` to specify that the same work log entry should be added to
all targeted tasks that did not have other work log entries specified by this capture
(e.g. via a `- Some other note` bullet)?

#plan %m:@xlarge