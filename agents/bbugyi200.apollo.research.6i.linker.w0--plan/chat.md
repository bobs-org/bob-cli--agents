# Chat History - ace-run (research.6i.linker.w0--plan)

- **TIMESTAMP:** 2026-11-26 10:53:56 EST
- **MODEL:** claude/opus
- **AGENT:** research.6i.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/prose_note_type.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/prose_note_type.md`

> # Plan: Rename the article note type to prose
> ## Context
> Bryan wants the `article` note type renamed to something generic, because he will use it
> for any file whose job is to hold prose. Two goals sit behind the name:
> - Soon, a section inside an area, project, or prose note should implicitly be a **prose
>   section**, so that one keymap can turn it into a full prose note (and back).
> - Eventually, tasks and projects should be reversible with little or no loss. Projects
>   can have article notes as children today, and that blocks reversal.
> **Required reading for every phase:**
> `research:202611/prose_rename_and_section_extraction/prose_rename_and_section_extraction.md`

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to rename the "article" Obsidian note file type to something more
generic, since I intend to use this type for any file that needs to contain prose. Can
you help me implement this?

- I was thinking of the name "prose" for this, but I'm not sure.
- You should think hard about other names and attempt to come up with a better one.
- The goal is to soon allow for sections ("prose sections"?) to implicitly use this type
  as well, which will allow us to use a keymap to convert that section into a full-blown
  "prose" note (or whatever we decide to call these).
- This functionality will be useful on its own, but will also be required in order to
  eventually make tasks and projects losslessly (or with minimal loss) reversible (since
  projects can have article notes as children).
- Review the prose_rename_and_section_extraction.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.6i.linker

## Response

I'm opening the research sidecar so I can read the prose-rename report before planning.

I'm mapping where the article type is used in bob-cli (the matcher, CLI, catalog, completion, and docs) before I look at the plugins and the vault.

I found a precedent (the earlier `bob themes` → `bob types` rename), so I'm checking how it handled the hidden alias and the catalog row IDs.

Hosts track bob-cli master rather than crates.io releases, so I'm checking how `bob` gets onto each host. That decides how the vault retype phase waits for the new binary.

There's a precedent: the drawers cutover gated its vault migration with `scripts/dev/bob-host-currency` probes. I'm reading how that plan structured the gate.

I've confirmed the vault footprint: one live note, the type note, its template, the base, `type.md`, and the vault `AGENTS.md`. Next I'm checking the plugin's user-visible strings and command IDs.

Mac Capture's only hits are the web-article Refs kind, so it's out of scope. Now I'm checking chezmoi (cron, scripts) for other `bob articles` callers, which the research left as an open question.

I have enough context on the code, plugins, vault, and docs. Before writing the plan, I'm loading the memory-write rules, since the plan proposes glossary and decision-record changes.

Memory routing is clear: no existing note goes stale, so each memory decision defaults to `false` and waits for your approval. Next I'm checking the CLI alias mechanism and the help fixtures.

I have what I need for the plan. Now I'm writing a minimal epic skeleton and running the validator with `--explain` to get the exact schema.

I've settled the phase graph and decisions. Before drafting, I'm listing the type-sense article mentions in docs, so the CLI phase gets a concrete file list instead of a blind grep.

Docs mentions are concentrated in a dozen files. One detail before drafting: what `bob articles format` does by default (write vs. preview), so the new numbering flag fits its modes.

I have everything needed. Writing the epic plan now.

The validator wants `web:keyword` selectors for the new strands. Fixing those and revalidating.

Validation passed with two warnings, and the validator rewrote the file. I'm checking what it changed and what the memory-coverage warnings point at.

The validator only re-wrapped lines, which is fine. The coverage check doesn't match the new-strand selectors to the body paths, so I'm testing selector forms on a scratch copy.

Even a whole-web selector leaves the warnings, so the checker is matching the literal `sase/memory/...` paths in the body. I'll refer to the strands by selector in the body instead.

Validation passes with no warnings. The validator re-wrapped the file again, so I'm skimming it to make sure the callouts and lists survived intact before proposing.

The plan is intact. Proposing it now.

The proposal is staged. Finishing the turn through `/sase_final`.

I've submitted an epic plan for the rename. It's waiting for your approval, and nothing changes in the code, plugins, or vault until you approve it.

**The name:** I looked hard and couldn't beat **`prose`**, which matches what the research's five independent passes concluded. It's the only candidate that reads right at all three scales the roadmap needs: a "prose note", a "prose section", and the `bob prose` command. It also collides with nothing in the CLI, vault, glossary, or refs. Bob already uses the word in the same sense (the plugins' "prose field", "never changes prose"). The strongest runner-up was `page`, but every note is a page, refs already use "page" for PDF pages, and "page section" reads oddly. Genre words like essay, memo, or post have the same narrowness problem as "article". Words like note, text, section, sheet, leaf, and copy are already taken in Bob. The one cost is that "prose" is a mass noun, so copy always says "prose note(s)", never "a prose".

**Phases (run in order):**
1. **`engine-rename`** (small): rename the Rust module `articles` to `prose` with no visible change, so "article" stops mixing with the web-article code in searches.
2. **`prose-cli`** (medium):
   - bob reads both `[[prose]]` and `[[article]]` permanently, and writes only `[[prose]]`.
   - `bob prose` becomes the command, and `bob articles` stays as a permanent hidden alias.
   - The docs move to `docs/prose.md`, with redirects from the old URLs.
   - It adds a `--section-numbers on|off` flag and a host check used in phase 4.
3. **`prose-plugins`** (medium): the plugin shows as "Bob Prose" in Obsidian, four plugins recognize both spellings, and there's a new **Toggle section numbers** command. Plugin and command IDs don't change.
4. **`prose-vault`** (small): waits until every host has the new `bob` and plugins, then:
   - retypes `sase_blog_contents.md` to `[[prose]]`;
   - renames `article.md`, the template, and `articles.base`, and updates `type.md` and the vault's `AGENTS.md`;
   - switches the plugin to call `bob prose`.
5. **`prose-sections`** (xlarge, planning only): writes a separate epic for section extract/inline and its keymap, using the research's requirements. Its open questions come back to you as decisions in that plan: stub form, keymap, intro text above a project's first heading, and a generated prose catalog.

**Kept as they are:** the plugin ID `bob-articles`, the JSON schema version and keys, refusal codes, and command-catalog IDs. Only text you read changes, so the rename isn't a breaking change.

**Decisions for you at approval:**
- **Name:** `prose` (default) or `page`.
- **Section numbering:** stays on by default, or off by default. Turning it off is a breaking change, and the one live note would first get an explicit `section_numbers: true`.
- **Memory:** two changes, a Prose Note glossary term and a decision record. Both default to **off**, as you asked; turn either on to approve it.

**Out of scope:** making projects reversible (the research's Phase 3), renaming the plugin ID, and Mac Capture, which I checked and found unaffected.
