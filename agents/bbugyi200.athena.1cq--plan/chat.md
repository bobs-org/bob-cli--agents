# Chat History - ace-run (1cq--plan)

- **TIMESTAMP:** 2026-11-15 13:18:19 EST
- **MODEL:** claude/opus
- **AGENT:** 1cq--plan

**Plan:** /home/bryan/.sase/plans/202611/drawer_title_punctuation.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/drawer_title_punctuation.md`

> # Allow punctuation in task drawer titles
> ## Goal
> Bryan wants to rename the `WHAT IS SASE` drawer under `^section-field` in `sase_blog.md`
> to `WHAT IS SASE?` and still use the bullet-start `#` drawer menu in Bob Mac Capture.
> That means drafting `@sase_blog+section-field` and then `- #`, choosing the drawer, and
> adding notes. The drawer must be listed under "On this task", and choosing it must
> insert `- WHAT IS SASE?`. On commit, that bullet must merge into the existing drawer,
> never write a second header.
> Today none of this works. `capture_drawers::is_drawer_title` accepts only `A-Z`, `0-9`,
> space, tab, and `& ' ( ) , . / -` (lead character `A-Z` or `0-9`, and at least one

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me start allowing punctuation in drawers? For example, consider
the ~/tmp/screenshots/20261115_130249.png screenshot. I would like to be able to change
this `WHAT IS SASE` drawer to `WHAT IS SASE?` and still have `#` completion work in the
bob-mac-capture app.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the drawer-title rules in bob-cli to find where punctuation like `?` gets rejected.

Mapping where the drawer-title grammar is enforced (bob-cli scanner, capture parser, gcal, project-note promotion) before checking the plugin and Mac app repos.

Still mapping the bob-cli side: next the slug/selector functions and project-section handling, then the plugin and Mac app repos.

Now checking the bob-plugins and bob-mac-capture repos for their own copies of the drawer-title rule.

Found the plugin's mirrored regex; checking for other copies across plugins and the Mac app.

Checking how the shared task-split fixtures sync between repos, then the docs that state the drawer grammar.

Before choosing which punctuation to allow, I'll scan the vault for ALL-CAPS bullets that would newly become drawers under each candidate character.

No grammar conflicts in the capture parser. Checking the Mac app's completion code for any local filtering that could drop a `?` title.

The Mac app is purely data-driven (no local drawer charset), so it needs no changes. Looking at the resolver's near-duplicate messages, which would print an unusable `#what-is-sase?` suggestion.

Checking two remaining modules (`task_text_escape`, `capture_flag_guard`) that mention drawers, to see whether they hard-code the charset.

I have the full picture. Reading the docs and CLI-rules memory so the plan's doc steps match project conventions.

Validation passes with no warnings. Submitting the plan.

I've submitted the plan for your approval (a single-agent plan, medium size); nothing has been changed yet. The vault is untouched — renaming `WHAT IS SASE` to `WHAT IS SASE?` stays with you.

**Why `?` breaks completion today:** bob-cli's drawer-title check only allows `& ' ( ) , . / -` as punctuation. So `WHAT IS SASE?` isn't recognised as a drawer at all, and the `- #` menu can't list it. A typed `- WHAT IS SASE?` bullet would also be filed as a plain note instead of joining the drawer. I confirmed this with the installed `bob capture-parse`: the same draft without the `?` is recognised as a drawer, and with it, it isn't.

**What the plan changes:**
- **One rule for drawer titles.** bob-cli adds the new punctuation, and a second Rust copy of the old rule is replaced by a call to the first. Pomodoro names keep their current rules.
- **Plugins:** the two copies of the rule in bob-plugins (task split, and turning a task into a project note and back) get the same rule. A new shared task-split test case keeps them in step with bob-cli.
- **Cache:** the drawer list is cached per file, so its version is bumped. Otherwise existing drawers like yours would never be re-read.
- **Error message:** the near-duplicate error currently suggests `#what-is-sase?`, which can't be typed as a selector. It will suggest `#"WHAT IS SASE?"` instead.
- **Mac app:** no change needed. It only shows what `bob` returns, so it picks this up once the new `bob` ships.
- **Docs and checks:** `docs/capture.md` gets the new rule. The coder will check it end to end with the same `bob capture-complete` command the Mac app runs, against a throwaway vault.

**Side effects to know about:**
- Existing ALL-CAPS bullets under tasks that match the new rule become drawers too. A vault scan found `OPTIONS:` (`sase_better_llm_disable.md`) and `NOTES:` (`needs_attn_tasks.md`).
- Google Calendar event descriptions with lines like `WHY?` will be rewritten once on the next sync, with those lines shown in bold so they don't turn into drawers.

**Two decisions for you at approval:**
1. **Which punctuation (default `sentence`):** `?`, `!` and `;` anywhere, plus `:` only at the end (`OPTIONS:`), so `LABEL: value` notes stay notes. The alternatives are `question_bang` (only `?` and `!`) and `broad` (`:` anywhere too, so a note like `PHONE: (609)…` would also become a drawer).
2. **Whether typing `#what-is-sase` should select `WHAT IS SASE?` (default `exact`: no):** with the default, the `?` is part of the drawer's name, the same as `Q&A` today. The `- #` menu works either way. The other option makes typed names ignore the punctuation, at the cost of more code and new "matches more than one drawer" errors.
