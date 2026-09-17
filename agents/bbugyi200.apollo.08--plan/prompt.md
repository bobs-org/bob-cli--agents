#gh:gh_bobs-org__bob-cli Can you help me make it so the `bob_xlib_pull` script, which is defined in
my chezmoi repo, always checks both athena and apollo instead of using apollo as a
fallback only? Make sure this doesn't slow down the script at all / too much. I'm
thinking we can probably parallelize the checks for the athena/apollo machines? Also,
the `bob_xlib_pull` command is already pretty slow, so you should look for any other
optimizations we can make to this script to make it faster.

#plan %m:gpt-6-astra