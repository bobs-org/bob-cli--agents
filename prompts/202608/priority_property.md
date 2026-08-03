- **PLAN:**
  [202608/priority_property.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/priority_property.md)
- **AGENTS:**
  - [bbugyi200.athena.s8--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.s8.md#member-plan)

Can you help me add support for a new `priority` property name to the `properties` field in the bob/config.yml file (in
my chezmoi repo)?

- Let's use a `values` value of `priority` for this new property type.
- This new property type will show only three values at first: `P2`, `P3`, and `P4` (an Obsidian task without a priority
  is implicitly considered to have a `P1` priority).
- When the user selects `priority` and picks a value (`P2`, `P3`, or `P4`) when using the `<ctrl+shift+p>` keymap, this
  will cause the `scheduled` property to be set to a random date range, which needs to be configured in the
  bob/config.yml file somehow (you figure this out).
- A different random date range should be used depending on whether the user selected `P2`, `P3`, or `P4`.
- Configure my date ranges as follows:
  - For `P2`: A random date between 2 days from today and 7 days from today.
  - For `P3`: A random date between 8 days from today and 30 days from today.
  - For `P4`: A random date between 31 days from today and 90 days from today.
- If the user selects `scheduled` when using the `<ctrl+shift+p>` keymap, and the current Obsidian task has the
  `priority` field set, then we should automatically recommend a new random date within that range and display it to the
  user in the date selection menu that pops up. Make sure this date is visually distinct from the others (since it is
  random and related to the `priority` property).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last
  but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate tier,
validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs) before making
any file changes.
