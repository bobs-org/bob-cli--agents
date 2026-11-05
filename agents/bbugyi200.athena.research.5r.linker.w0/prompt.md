#gh:gh_bobs-org__bob-cli The `%c` capture directive works well when there is no index (i.e. we only
fetch the last clipboard entry), but when we attempt to fetch more than one clipboard
entry, only the first seems to ever be correct.

- I'm not really sure what's causing this, but I'm wondering if we maybe integrated with
  the wrong clipboard manager running on my macbook?
- Regardless of what the underlying root cause of this issue is, I would like to make
  the `%c` capture directive much more resiliant and reliable.

Can you help me implement this? Review the percent_c_history_agrees_with_live.md file in the research sidecar
repo for context and inspiration before planning. I agree with all of the requirements
recommended in that research file (but keep in mind that you are responsible for
planning and splitting up this work appropriately).

#plan %m:@xlarge %w:research.5r.linker