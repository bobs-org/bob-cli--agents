#gh:gh_bobs-org__bob-cli Can you help me have the `bob ref create` command only ever use the
`sase listen` command (never the `sase-listen` command)? See the command output below
for context. #plan %m:gpt-6-astra %auto

```
❯ bob ref create https://arxiv.org/abs/2609.12039 -i -L -P sase
fetching export.arxiv.org…
fetching arxiv.org…
listen: run sase-listen render https://arxiv.org/abs/2609.12039 -e full -o /tmp/bob-create-3716051-1791668144042163134/reality_is_the_final_verifier_on.mp3
sh: 1: sase-listen: not found
bob ref: error: listen command failed with exit 127
hint: nothing was written to the vault; rerun the same command once the listen error above is fixed

```