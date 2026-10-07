- **PLAN:**
  [202610/url_capture_ref_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)
- **AGENTS:**
  - [bbugyi200.athena.research.3w.linker.w1--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md)

We just finished adding support to the `bob highlights create` command for URLs and
migrated that command to the `bob ref create` command (see the bob-cli-4s and
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
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
