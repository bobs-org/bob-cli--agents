- **AGENTS:**
  - [bbugyi200.apollo.fr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.fr.md)
- **ARTIFACTS:**
  - [links_stage_event_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/1455235e44b34d5d678843505defb350ebf1aa89/202611/links_stage_event_tasks.md)

%model:@medium #gh:gh_bobs-org__bob-cli [@plan:202611/links_stage_event_tasks.md][1]

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false Reviewer decisions for this plan (final · reviewer via ACE):

- daily_scope = events (planner default: events). Implement the "daily_scope = events"
  branch; ignore "daily_scope = all". Context: "Should the Links stage admit only Event
  Tasks from daily notes?".
- day_window = all_days (planner default: all_days). Implement the "day_window =
  all_days" branch; ignore "day_window = recent". Context: "Should Event Tasks from
  every past day be linkable?".
- chip_names = clean (planner default: clean). Implement the "chip_names = clean"
  branch; ignore "chip_names = leave". Context: "Should LINKS and LINKED FROM chips also
  name Event Tasks as `HHMM-HHMM Title`?". Implement only the branches selected above.
  %macros_enabled:true

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/1455235e44b34d5d678843505defb350ebf1aa89/202611/links_stage_event_tasks.md
