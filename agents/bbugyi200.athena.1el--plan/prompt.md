#gh:gh_bobs-org__bob-cli When linking to other tasks in Obsidian (and maybe in the capture panel, but
I'm not sure) we seem to group blocked (and done?) tasks in their own section at the
bottom. This makes it so, for example, typing "foobar" doesn't necessary immediately
reveal (the user has to scroll down) a blocked "Implement foobar component." task even
if it the best match.

- See the ~/tmp/screenshots/20261113_070944.png screenshot for an example of what I'm
  talking about.
- This is not correct.
- We should only preference open tasks over blocked/done tasks when the filter specified
  by the user matches those tasks equally well (so we fallback to sorting based on task
  status).

Can you help me fix this? #plan %m:@xlarge