- **AGENTS:**
  - [bbugyi200.apollo.research.5n.gem](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5n.gem/README.md)

%id(gem, clan=research.5n) %m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher gem in a 5-researcher swarm. The other
researchers, `research.5n.cdx`, `research.5n.cld`, `research.5n.grk`, `research.5n.mus`,
are independently investigating the same request and will write their own self-named
reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report
will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add much better (and explicit) support for "micro tasks".

- A "micro task" is a sub-bullet on an Obsidian task that would be converted to a task
  in the new project file if its parent task were converted to a project (e.g. via the
  `<ctrl+shift+alt+n>` keymap).
- We currently consider any sub-bullet that does not belong to a drawer to be a micro
  task (though we don't use this term yet).
  - We should instead start treating these bullets as if they were placed in a "NOTES"
    drawer and require that micro tasks be marked as such explicitly.
  - Any notes added to a task via captures (using the `@foo+bar` capture syntax, for
    example) should be added to the NOTES drawer by default unless another drawer is
    explicitly specified or a micro task marker is specified in the capture.
- I was thinking that we could either use a `TASK:` or `#task` prefix for these
  sub-bullets to mark them as micro tasks, but this is just my first thought. Think hard
  about the best way to mark these.
- We should support nested micro tasks (i.e. micro tasks with micro task parents).
- Regardless of how we decide to mark micro tasks, the mark should be rendered in a
  consistent and concise way. I was thinking we could render 2 or more `#` characters
  (depending on the micro task nesting level) for this micro task marker.
- It needs to be very easy to specify micro tasks in the capture panel. I was thinking
  that we could use `..` as a capture alias for the micro task marker (so `- ..` would
  be converted to `- #task `, for example) and add a new `<ctrl+g>t` keymap that toggles
  the micro task prefix for the current bullet.
- Top-level (i.e. `##`) micro tasks should show up as successors, which are closed by
  default, when their parent task is closed.
  - The user can decide to open these tasks using the `<ctrl+x>` keymap on the successor
    panel, in which case a new Obsidian task should be created for that micro task. The
    micro task bullet in the original task should be crossed out and an appropriate note
    should be placed next to it that links to the original parent task.
  - After opening a micro task successor, the user can also check it (e.g. using the
    `<space>` or `<tab>` keymaps), in which case the new task that is created should
    have a task link added to today's daily file (i.e. it should be pulled in).
  - The user can also canel a micro task successor using the `<ctrl+shift+x>` keymap, in
    which case the micro task sub-bullet should be striked out after closing the parent
    task (to indicate that it was not complete).
  - All non-top-level micro tasks (e.g. `###`, `####`, etc...) should still show up on
    the successor panel but should not be actionable since their status will be
    deteremined by whatever status we decide to give their parent micro task.
- When we merge a task into another task using one of the configured `merge_labels`, we
  should start creating a new micro task in the target task that represents the source
  task. I think this should just involve adding the microtask marker but there might be
  more work involved.
- As a part of this change, we should add an excellent new glossary term for "micro
  task".
- The Goals of this Change
  - Micro task successors will help me make sure that I've really completed all of the
    work that a task commits to before closing it.
  - I would like to soon make it possible to convert any project (regardless of how
    complex) into an equivalent task. This is out of scope for this research report but
    is a motivating factor, since this change will make it possible to convert
    sub-projects into equivalent micro tasks.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=gem)
