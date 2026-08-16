- **PLAN:**
  [202608/dated_entry_snippet.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/dated_entry_snippet.md)
- **AGENTS:**
  - [bbugyi200.athena.03h--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.03h.md)

We already have a `d[-]<N>` snippet that expands to the date specified by `[-]<N>` where
`-` is optional and `<N>` is some integer (`0` means today). Can you now help me add a
new `D[-]<N>` snippet that works the same way but expands to `_YYYY-mm-dd_ — $1` (use an
em-dash instead of a regular dash if possible), where `$1` is where the user's cursor
should be after expansion, instead of just `YYYY-mm-dd`? Think this through thoroughly
and create a plan using your `/sase_plan` skill. Choose and author the appropriate tier,
validate and revalidate until it passes, then submit it with `sase plan propose` (as the
skill instructs) before making any file changes.
