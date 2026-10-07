#gh:gh_bobs-org__bob-cli We just finished adding support to the `bob highlights create` command for URLs
and migrated that command to the `bob ref create` command (see the bob-cli-4s and
bob-cli-4w, respectively, epic beads for more context). I would now like to add support
to the `bob capture` command and the corresponding bob-mac-capture app for passing URls
that are provided as capture input to the `bob ref create` command. Can you help me
implement this?

- Specifically, when a URL is provided as the only capture input (bulk capture with URLs
  should be supported though), then we should run the appropriate `bob ref create`
  command on the URL instead of capturing a note or task.
- I would also like to add support for doing something similar when capturing from
  Google Keep.
- Namely, any Google Keep note that is pulled down using the `bob gkeep pull` command
  that contains only a URL should not be added to the ~/bob/gkeep_inbox.md file.
  Instead, the appropriate `bob ref create` command should be run.
- Review the url_capture_ref_intake_routing.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the recommendations made
  in that research file.
- #beau

#plan %m:@xlarge %auto %w:research.3w.linker