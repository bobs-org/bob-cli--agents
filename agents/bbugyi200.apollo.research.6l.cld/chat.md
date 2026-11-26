# Chat History - ace-run (research.6l.cld)

- **TIMESTAMP:** 2026-11-26 13:04:33 EST
- **MODEL:** claude/opus
- **AGENT:** research.6l.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_124105.md`

## Prompt

%id(cld, clan=research.6l)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.6l.cdx`, `research.6l.grk`, `research.6l.mus`, `research.6l.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to implement "ref cards", a new type of property card for ref notes.

- See how other property cards are implemented and the bob-cli-qm epic bead, which is
  in-progress and implements notebook cards and prose cards, for context and
  inspiration.
- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qm epic.
- Think hard about how this card should look. It should contain as much genuinely useful
  information about the reference as possible without cluttering the card.
- Also, think hard about whether or not ref cards should support the `==` keymap and, if
  so, what kinds of operations the schema editor that is triggered should support.
- As a part of this change, we should add an excellent new glossary term for "ref card".
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Reading the in-progress bob-cli-qm plan, then the property card kit, ref notes, and the `==` schema editor code.

Still gathering context: now reading the `bob ref` docs (show/list JSON shapes) to see what data a ref card could display.

Surveying live ref notes in the vault (read-only) to see what frontmatter and body shapes a ref card must handle.

Now inside bob-plugins: reading its AGENTS.md and the property-card kit fragments (`240*`, `248m`) to see how species, `==`, and the foot/drawer work.

Checking how Highlights sync treats hand-edited ref frontmatter — that decides what a ref-card `==` editor can safely write.

Checking live bead state for qm/qi/qj phases (to design the coordination gates against what's actually in flight).

Verifying in bob-cli's Rust whether ref sync rewrites the H1 when `title:` changes (decides how a title edit from the card stays consistent).

Found `[[ref]]`-typed hub notes outside `ref/` (e.g. `sase_ref.md`) — checking what they are, since the card's eligibility rule must not misfire on them.

Reading Bob Mac Capture's Refs inspector doc — the closest existing "what matters about a reference" design precedent.

Enough evidence gathered. Two last quick checks (agent-report stem patterns, legacy chapter books) before writing the report.

Writing the report now.

Report written and registered; submitting the final commit declaration for the research repo.

I wrote the report and registered it as an artifact (`file:explicit:d5f6bf1570ea7ed9af7d13d0`, labelled `research:202611/ref_cards_design__cld.md`). The research repo commit is declared and will be made after this turn ends.

**Recommendation: build ref cards.** Ref notes are the largest typed-note group in your vault: 1,377 references, against 39 notebooks and one prose note. They also have the ugliest native Properties: a median of 14 keys and about 800 characters of YAML, mostly Highlights sync bookkeeping. Meanwhile the useful facts (reading lane, why a reference is snoozed, highlight counts, the PDF) don't show on the note at all.

**The card**
- **Top:** a bookmark-style tile, a kind label (BLOG, PAPER, CHAT, …), and the parent's breadcrumbs.
- **Middle:** the title, then a byline of author, source site and publication date (never a file date).
- **Reading state:** a lane chip using the Reading Board's words (Ready, Next, Reading, Read with its date, Snoozed with its reason), a TODAY pill, and highlight counts that jump to `## Highlights`.
- **Access:** PDF and audio buttons.
- **Data:**
  - What the note itself says (title, author, kind) paints instantly from its frontmatter.
  - Reading state comes from one shared `bob ref list -A -R all` snapshot, refreshed in the background. It covers the whole library in about 1.1 s, while a single `bob ref show` takes 0.94 s, so fetching per note buys nothing.
  - Missing data is left out, never shown as zero.
- **Eligibility:** exactly `[[ref]]` notes under `ref/`. I found 13 root hub notes (`sase_ref.md`, `ai_ref.md`, …) that are also typed `[[ref]]` but are collections, not references; they should not get a card.

**`==`: yes, but as a "Reference editor", not a schema editor.** Refs have no user-defined schema, and most of their keys belong to the sync engine, the reading task, or the file name.
- **Editable fields:** Title, Authors, Published, Source, and an optional one-line Summary. Bob already syncs edits to these fields back into the PDF safely.
- **Title edits** should also update the H1, because bob writes that H1 only once, when the note is created.
- **Routed elsewhere:** reading lane and parent go to the reading task, and the file name goes to `bob ref rename` (preview first).
- **Fallback:** if bob doesn't have the new contract yet, `==` just focuses the `title` field.

**One small bob-cli change is justified.** Today the `+` Property Editor lets you freely edit sync keys like `highlights_marker_hash`, plus `id`, `status` and `parent`. Editing those can break sync, so this is worth fixing even without the card. The same phase adds the editor's field contract behind a new capability check.

**Running it in parallel with bob-cli-qm.** Coordination is needed, but only at four points; ref cards never touch prose, so nothing is needed with the qj epic. I'd make it a sibling epic of seven phases:
- **Start now (no overlap with qm):** the bob-cli phase and a data/model phase in new plugin files.
- **Card shell waits for `qm.1`:** that phase is rewriting the exact shared card-kit lines a ref card needs. Its new test also asserts that `ref` notes get no card, so landing ref first would break it.
- **Acceptance waits for `qm.6`:** it reuses that phase's real-Obsidian test harness, and the two runs shouldn't overlap.
- **Go-live waits for `qm.7`:** that phase holds the only authorized edit to the `property-card` glossary entry.
- **Own preview gate:** the ref epic needs its own switch for keeping the card off in your live vault. `qm.7` deletes qm's switch, so a ref card relying on it would go live before it was accepted.

**Requirement adjustments I'm making (each marked in the report):**
- The narrower eligibility rule above.
- `==` as a Reference editor instead of a schema editor.
- The bob-cli phase is in scope.
- The reading-task embed stays visible below the card, as the Project card keeps its `^prj` line.
- The card reuses the Reading Board's vocabulary.
- The ref epic has its own preview gate.
- An optional `summary:` line on refs.

The report also has a draft glossary entry keyed **"Ref Card"** (also known as "reference card"), seven decisions for you with recommended defaults, and follow-ups. I didn't file a bead for the mis-typed hub notes; it's recorded as follow-up F1 so the lead can decide, rather than five researchers filing duplicates.
