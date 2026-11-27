# Chat History - ace-run (1gw--plan)

- **TIMESTAMP:** 2026-11-27 06:13:35 EST
- **MODEL:** claude/opus
- **AGENT:** 1gw--plan

**Plan:** /home/bryan/.sase/plans/202611/embedded_catalog_cards.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/embedded_catalog_cards.md`

> # Plan: Keep host catalog cards out of block embeds and hover previews
> ## Problem
> Opening `ref/chat/property_card_cabinets.md` (a reference note) shows a standalone
> **Projects** card ("Projects 3 open · 0 blocked · 4 closed", `＋ project`, `Closed · 4`
> with the two-row peek `bob_command_mode_improvements`, `bob_gtd`) above the embedded
> reading task. That card belongs to `bob.md`, the note that holds the reading task. Every
> reference note shows its reading task through the managed embed
> `![[<residence>#^ref-<slug>]]`, so the same leak hits every reference note whose parent
> is a Projects or Areas catalog host. It also hits any other note that embeds a block
> from such a host, and hover previews of those blocks. In the live vault about 42

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Why am I seeing these projects listed in a ref note? See the
~/tmp/screenshots/20261127_055010.png screenshot for context. Can you help me diagnose
the root cause of this issue and fix it?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm reading the note and the plugin code to find what renders the "Projects" card in the embed.

Gate appears off on athena, so I'm checking the Projects-card paint paths (callout vs standalone) to match what the screenshot shows.

Still diagnosing: checking how the deployed plugin on the Mac renders block embeds.

Found the likely culprit (the Projects catalog's standalone-anchor path firing inside a block embed). Now checking the real-Obsidian e2e harness so I can confirm it by reproduction.

I'm writing a small real-Obsidian reproduction in a scratch vault to confirm the root cause before planning.

Initial render in my repro doesn't paint the card, so I'm comparing against the real `bob.md` history around the screenshot time.

Reproduced: with the Tasks + Dataview plugins enabled, every block embed of a `host.md` task paints the host's Projects card. Narrowing down which plugin supplies the trigger.

Confirmed the Tasks plugin is the enabler. Grabbing the final embed DOM to pin down exactly which element the card attaches to.

The repro matches your screenshot exactly. Checking whether the sibling catalogs (Areas, Albums, Notebooks) have the same flaw before I write the plan.

Confirmed the Projects path. Quickly testing whether Areas embeds hit the same bug, since its anchor-line fallback looks identical.

Root cause is pinned down; I'm reading the existing docs and unit-test patterns now so the plan cites the right files.

Verifying one more thing for the acceptance test: whether a paragraph-block embed reproduces the Projects leak without the Tasks plugin (so the existing e2e harness can catch it).

Scope in your vault: about 42 ref-note embeds target Projects hosts and 9 target Areas hosts. Checking the repo's validation conventions so the plan's acceptance steps match them.

Writing the plan file now.

Plan is staged; finishing the turn's final declaration now.

The cause is a bug in the `bob-ledger-tools` plugin, not in your note. I reproduced it in real Obsidian 1.15.1 (the same version your Mac runs), and I've written a fix plan and submitted it for your approval. No code is changed yet.

**Why the projects appear:** every ref note shows its reading task through an embed, here `![[bob#^ref-property-card-cabinets]]`. `bob.md` has 7 child projects, so the plugin draws `bob.md`'s Projects card inside that embed.

1. **Obsidian hands the plugin a fragment.** For an embed, Obsidian renders only the embedded line, tagged with `bob.md` as its source. The plugin's own section lookup then sees just that one line as if it were the whole note.
2. **The plugin treats the fragment as the whole note.** `renderProjectsCatalogInReading` (`241ae-plugin-projects-catalog.js`) finds no `## Projects` heading and no stored projects list in that one line. It concludes the note needs a standalone card at line 0.
3. **The embed check doesn't fire.** There is a rule that embeds never get a standalone card, but the element isn't attached to the page yet when it runs, so it can't see that it's inside an embed.
4. **So the card gets drawn.** It's the same `Projects 3 open · 0 blocked · 4 closed` card, `＋ project` button and two-row Closed preview (`bob_command_mode_improvements`, `bob_gtd`) shown in your screenshot. The Tasks plugin's task rendering is what triggers it for task embeds; a paragraph embed triggers it even without Tasks.
5. **Nothing removes it afterwards.** In Live Preview the periodic refresh skips content inside the editor, so the card stays.

**How widespread:**
- In your vault, about 42 ref-note embeds point at notes with a Projects list and about 9 at notes with an Areas list. Any other note that embeds a block from one of those notes is affected too.
- The Areas card has the same flaw and leaks on every embed from an area note with sub-areas, Tasks plugin or not.
- The Albums and Notebooks cards use the same logic, though they only draw in less common states.

**The fix (in `bob-plugins`):**
- Add one shared check that recognises an embed or hover preview: either the live container Obsidian passes in sits inside an embed or popover, or the rendered text is missing the note's frontmatter.
- With that check, Projects, Areas, Albums and Notebooks never draw a standalone card in an embed. A stored Projects or Areas list inside an embed still renders as a card, and host notes themselves don't change.
- The plan also covers unit tests, an extension of the real-Obsidian Projects test with embed cases and screenshots, a short docs note, a patch version bump, the build checks, and `bob plugins sync`.

The Mac deploys from its own `bob-plugins` checkout, so the fix reaches it on that machine's next sync.
