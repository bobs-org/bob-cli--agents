- **PLAN:**
  [202608/priority_property.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/priority_property.md)
- **AGENTS:**
  - [bbugyi200.athena.gh_bobs-org__bob-cli-5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.gh_bobs-org__bob-cli-5.land/README.md)

[#gh:gh_bobs-org__bob-cli](https://github.com/sase-org/sase-github/blob/7dd02fcec77649b34cba23ae33f30793311869dd/src/sase_github/xprompts/gh.yml)
%id(land, clan=gh_bobs-org**bob-cli-5, bead=gh_bobs-org**bob-cli-5) %model:@big_epic_lander %auto
%w:gh_bobs-org**bob-cli-5.1,gh_bobs-org**bob-cli-5.2,gh_bobs-org**bob-cli-5.3,gh_bobs-org**bob-cli-5.4,gh_bobs-org**bob-cli-5.5
%w(bead=gh_bobs-org**bob-cli-5.1) %w(bead=gh_bobs-org**bob-cli-5.2) %w(bead=gh_bobs-org**bob-cli-5.3)
%w(bead=gh_bobs-org**bob-cli-5.4) %w(bead=gh_bobs-org**bob-cli-5.5)
[#bd/land_epic:gh_bobs-org__bob-cli-5](https://github.com/sase-org/sase/blob/fe0d71e09fc1ce0984d67df49917c8e2055c0b4b/src/sase/default_config.yml#L949)

<!-- sase:section:rendered -->

<details>
<summary><b>Agent Prompt</b> — rendered, 2.5 KB</summary>

```markdown
You are the land agent for epic bead gh_bobs-org__bob-cli-5: verify the epic is truly complete, integrate it with
changes that landed since it started, then close it out.

1. Verify. Run `sase bead show gh_bobs-org__bob-cli-5` (children, linked plan file), review the epic bead's own notes,
   then run `sase bead show` on every child and review every child note. Confirm each note was addressed, and read the
   actual source code and the epic's commits (bead IDs appear in commit messages) to confirm the work previous agents
   reported complete really is. While reviewing child beads, collect every `PROPOSED FOLLOW-UP:` note entry.

2. Integrate. Changes committed since this epic started could not integrate with this epic's feature while it was
   incomplete. Find them (e.g. `git log` since the first commit mentioning gh_bobs-org__bob-cli-5, excluding the
   epic's own commits; in a PR workflow also review commits on the base branch) and update anything that should now use
   what this epic added or that duplicates or conflicts with it. This integration is part of the epic's work.

3. Land. Unresolved issues caused by this epic remain epic work: plan and finish them before closing. For each genuinely
   distinct follow-up that is not caused by the epic, use `/sase_new_task` with details identifying the proposing bead;
   it will corroborate a duplicate, attach a causally related active-epic issue, or create a sized task as appropriate.
   Record every outcome, including why any proposal was declined, in your close note. Close the epic with
   `sase bead close gh_bobs-org__bob-cli-5 --note "<what you verified in steps 1-2>"`. AFTER closing, run
   `just symvision` if available (epic-symbol whitelist entries for gh_bobs-org__bob-cli-5 expire at close) and remove
   the stale entries and unused code it reports. Finally, set `status: done` in the frontmatter of the epic's plan file
   (the PLAN path shown by `sase bead show`). If the close is rejected, the named phases were never completed: finish or
   reopen them, or record the outcome deliberately with `--force --reason ... --resolution canceled|superseded`. Never
   force merely to make the command succeed.

If steps 1-2 uncover remaining work, use your /sase_plan skill to plan it and complete the skill's tier-aware
validate/revalidate/propose loop. Make step 3 the plan's final phase (close, run symvision, mark the plan file done) so
the agent that executes the plan finishes the landing. Otherwise do step 3 now.
```

</details>

<!-- /sase:section:rendered -->
