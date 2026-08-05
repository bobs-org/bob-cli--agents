#gh:gh_bobs-org__bob-cli We recently added support to the `<ctrl+shift+p>` Obsidian keymap for the new `priority` property. We originally went with the priorities P2, P3, and P4, with the idea that any obsidian task that does not have an explicit priority should be treated as a P1. Can you now help me instead migrate all of these to P1, P2, and P3, respecitvely?

- I think this makes more sense since we can treat any Obsidian task without a priority as a P0 (the highest priority).
- Also, let's add support for a new P4 priority that works like the others, but uses a random `scheduled` date betweeen 91 and 365 days from today.

#plan #m_opus