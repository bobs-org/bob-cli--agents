- **PLAN:**
  [202610/ref_create_sase_listen_only.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_sase_listen_only.md)
- **AGENTS:**
  - [bbugyi200.athena.0zi--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0zi.md)

Can you help me have the `bob ref create` command only ever use the `sase listen`
command (never the `sase-listen` command)? See the command output below for context.
Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.

```
❯ bob ref create https://arxiv.org/abs/2609.12039 -i -L -P sase
fetching export.arxiv.org…
fetching arxiv.org…
listen: run sase-listen render https://arxiv.org/abs/2609.12039 -e full -o /tmp/bob-create-3716051-1791668144042163134/reality_is_the_final_verifier_on.mp3
sh: 1: sase-listen: not found
bob ref: error: listen command failed with exit 127
hint: nothing was written to the vault; rerun the same command once the listen error above is fixed

```
