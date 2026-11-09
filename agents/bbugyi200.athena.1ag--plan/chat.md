# Chat History - ace-run (1ag--plan)

- **TIMESTAMP:** 2026-11-09 10:28:00 EST
- **MODEL:** claude/opus
- **AGENT:** 1ag--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_alias_glossary_term.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_alias_glossary_term.md`

> # Plan: Add the Capture Alias glossary term
> ## Goal
> Add one glossary strand, **Capture Alias** (alias: `sigil alias`). It defines the
> single-character substitutions Bob Mac Capture makes while you type, such as `.` → `^`,
> `,` → `+`, `\` → `#`, `=` → `~`, and `x` → `!`. Then regenerate everything derived from
> the glossary web: the always-loaded roster in `AGENTS.md` / `CLAUDE.md`, the memory
> README, and the public glossary page `docs/reference/glossary.md`.
> No code changes. Nothing in `bob-mac-capture` changes; that repo is a read-only source.
> ## Background (verified while planning)
> - **bob owns every alias.** Following `decisions:mac-capture-is-a-thin-client`, the app

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add an excellent new "capture alias" glossary term that
describes the various single-character substitutions that the bob-mac-capture app makes?
Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm planning a new "Capture Alias" glossary term. Next I'll open the bob-mac-capture repo to list every single-character substitution the app makes.

Still researching: I'm now listing bob's capture-rewrite alias rules and checking which substitutions the Mac app does on its own.

Still mapping the app's rewrite lane — finding which typed keys it forwards to bob — before I write the plan.

I have the full alias list. Now I'm reading the related decision records so the new term links to them correctly.

Found that the docs site may generate pages from glossary memory. Checking whether a new term needs a docs regeneration step.

The public docs glossary page is generated from these memory strands and is already out of date (it's missing Project Note Capture). Reading the docs memory note before planning that regeneration.

The plan validates. One warning remains because the strand doesn't exist yet, even though the memory decision already covers it as "new". I'm checking the final frontmatter, then submitting.

I've submitted a plan for the new **Capture Alias** glossary term and it's waiting for your approval. No files have changed yet. It's a small single-agent plan (tale tier) with one built-in decision, on by default because you asked for it: allow creating the new glossary entry and regenerating the files built from it.

**What the term covers.** Each capture alias is decided by bob, not the Mac app: bob's `capture-rewrite` returns it as the `expand_sigil_alias` rule. A typed key is swapped only where the sign it stands for would actually do something at the caret:
- `.` becomes `^` after `@route`, `;` becomes `:`, and `- .` / `- ;` open the Move picker on project-note bullets.
- A `.` after a space following text becomes `@` where route completion would open.
- `,` becomes `+` where the Parent Task picker would open.
- `\` or `/` becomes `#` where a `#` menu would open.
- `-` becomes `~` inside `x=` past entries.
- `=` becomes `~` where Links To would open; `~=` and `~~=` flip direction.
- `x` and `s` become `!` and `*` when they end a close.

It also covers:
- the in-picker aliases;
- the one alias the app handles itself (a blank draft's `\` becomes `/` to open Go To);
- the ways to undo an alias: Undo, a fast `==` or `..`, a second `\` or `/`, and Space or Escape on an empty picker;
- why edits and Return wait for bob's answer on aliases that change meaning;
- that `bob capture`, paste and piped input always keep the literal text.

**Things I found while researching:**
- **The name is already taken in the Mac app.** "Capture alias" is the setting for the global `Command-\` shortcut. Bob also uses "alias" for frontmatter, wikilink, deprecated-tag and owner aliases. Since you asked for "capture alias", I kept the name; the entry says plainly that it is none of those. Its secondary name is "sigil alias", which is what bob's own docs call it.
- **The public glossary page is already out of date.** `docs/reference/glossary.md` is generated from these memory entries and was never rebuilt after the Project Note Capture term was added, so the drift check reports it as out of date. The plan regenerates that page, which also fixes the old drift, and then requires `just docs-check` to pass.
- **Reading a term pulls in other terms.** Any glossary term mentioned in plain text gets printed in full alongside it. The plan tells the implementer to avoid stray words like "drawer" or "keeps" and to check what gets pulled in.

The plan validator still shows one warning, because the new entry doesn't exist yet even though the decision already marks it as new; the plan itself passes.
