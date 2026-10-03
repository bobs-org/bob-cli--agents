# Chat History - ace-run (37)

- **TIMESTAMP:** 2026-09-29 17:26:29 EDT
- **MODEL:** claude/opus
- **AGENT:** 37

## Prompt

#gh:gh_bobs-org__bob-cli If I were to follow the advice of the pomodoro_closed_day_now_tag_automation.md
file in the research sidecar repo, how would a task tagged with `#now` be different from
an in-progress (i.e. `[/]`) task? Make sure your report is concise but beautiful.

Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete. %m:@xlarge

## Response

I've read the consolidated report. Next I'm checking `bob-cli`'s task-status-hooks docs so the `[/]` semantics in my write-up are accurate.

Found the relevant rules in both sources. Now I'm writing the report into the research repo's `202609/` directory.

Registration succeeded. Now the final declaration.

I wrote the report to `sase/repos/research/202609/now_tag_vs_in_progress_status.md` and registered it as `research:202609/now_tag_vs_in_progress_status.md` (artifact `explicit:f47ba24effac04843a1ab2c2`). The commit to the research repo has been declared.

**In short: `[/]` records work you've done; `#now` is a promise you've made.**

| | `#now` | `[/]` In Progress |
|---|---|---|
| What it is | A tag in the task text. It works alongside any checkbox status. | A checkbox status, the highest of `[ ] < [*] < [/]`. |
| Question it answers | "What have I committed to this week?" | "What have I actually been working on?" |
| Set by | You, by typing it or with capture `… #now @route^id`. | The tools: an `=x` close turns a worked-on link into `[/]`. |
| Cleared by | Only you, at the Monday review. | `task-status-hooks`, automatically, about a day after the task was last linked in your daily notes. |
| Lifespan | About a week. | About one day of grace. |
| Tie to today's Pomodoros section | None, by design. | Tight: the status comes from recent links there. |
| Cap | ≤ 15 (the `NOW n/15` chip turns red). | None. About 50 today. |
| Effect on other statuses | None. It never makes a task Next. | Highest active rank. It spreads to linked subtasks. |

**Why the report wants both:** today, removing a link from your Pomodoros section demotes the task, and nothing else remembers it mattered. So everything stays linked, and you end up with about 50 `[/]` and 25 `[*]` tasks. `#now` is what remembers that a task matters this week. That lets you drop links from today freely, and lets `[/]` shrink back to meaning "touched recently."

The report also covers:
- **Combinations:** a 2×2 of the four tag/status mixes (on track, owed, drive-by, backlog).
- **A one-week timeline** showing how long each marker lasts.
- **Fine print.** Two practical gotchas stand out:
  - **Deferring doesn't remove the tag.** Deferring a task with `Ctrl+Shift+P` hides it from the dash's NOW list, but it reappears when its date arrives unless you remove `#now`.
  - **Pulling a `#now` task into today.** The `^` capture picker only offers `[/]` and `[*]` tasks, so a Ready `#now` task won't show up there. Pull it from the dash instead, or type the full id.
