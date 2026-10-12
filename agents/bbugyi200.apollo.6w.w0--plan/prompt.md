#gh:gh_bobs-org__bob-cli %w:6w The `bob task reconcile` command currently places comment lines under
"Tasks" sub-sections like `<!-- bob:task-status-group:v1:active -->`, for example. I
would like to get rid of these somehow, but am not sure how to solve this without
breaking something or reducing the reliability and/or robustness of this functionality.
As a part of this change, I would also like to start removing these sub-sections when
they are empty (i.e. contain no tasks).

Can you help me implement this? Review the recently added related research in the
research sidecar repo for context and inspiration before planning. #plan %m:@xlarge