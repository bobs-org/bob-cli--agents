#fork:f4
%model:gpt-6-luna
%effort:xhigh

%macros_enabled:false
# Gate answered

**Decision:** The live vault has bob-copy-chips 0.4.0 from an uncommitted workspace 15 build (

| | |
| --- | --- |
| **Outcome** | ANSWERED — Submit answers |
| **Answered via** | tui |
| **Opened** | 2026-11-19T22:22:34Z |
| **Answered** | 2026-11-19T22:25:44Z |
| **Commands** | 1 of 1 completed |
| **Gate** | question/8be21fdd-3a50-4fea-99d6-354fedaa4e67 |

## Results

### submit — `commands/submit`

```json
{
  "answers": [
    {
      "custom_feedback": null,
      "question": "The live vault has bob-copy-chips 0.4.0 from an uncommitted workspace 15 build (febfc6b) and bob-navigation-hotkeys 2.90.0 from an uncommitted workspace 16 build (d6d2c33). The first carries the current copy-chip grammar and line-only gy; the second carries the current line-only Copy card C row and nav API v3. Neither build has landed in upstream, so the normal sync guard refused both. May I use -F for these two plugins to replace those deployed bundles with the approved bob-copy-chips 0.5.0 and bob-navigation-hotkeys 2.91.0 builds, which add task-scope lookup for C and gy?",
      "selected": [
        "Approve replacing both"
      ]
    }
  ],
  "global_note": ""
}
```

## Your next action

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/copy_card_task_chip.md

The above plan has been reviewed and approved. Implement it now.

% macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- gy_follows_task = yes (planner default: yes). Implement the "gy_follows_task = yes" branch; ignore "gy_follows_task = no". Context: "Should `gy` also fall back to the only chip in the cursor's task, like the Copy card's `C` row?".
- memory_glossary_copy_chip = yes 🧠. Memory edits are authorized for glossary:copy-chip only. Context: "Rewrite the glossary:copy-chip cursor-rule sentence to include the task fallback?".
No other memory note may be edited.
Implement only the branches selected above.
% macros_enabled:true


### Questions and Answers

#### Q1: Replace deployed plugins?

> The live vault has bob-copy-chips 0.4.0 from an uncommitted workspace 15 build (febfc6b) and bob-navigation-hotkeys 2.90.0 from an uncommitted workspace 16 build (d6d2c33). The first carries the current copy-chip grammar and line-only gy; the second carries the current line-only Copy card C row and nav API v3. Neither build has landed in upstream, so the normal sync guard refused both. May I use -F for these two plugins to replace those deployed bundles with the approved bob-copy-chips 0.5.0 and bob-navigation-hotkeys 2.91.0 builds, which add task-scope lookup for C and gy?

- [x] **Approve replacing both** — Overwrite the two protected live bundles and finish syncing this implementation.
- [ ] **Leave them in place** — Keep the current live builds and leave the new versions unsynced.

%macros_enabled:true