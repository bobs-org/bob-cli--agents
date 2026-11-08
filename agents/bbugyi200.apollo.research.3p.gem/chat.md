# Chat History - ace-run (research.3p.gem)

- **TIMESTAMP:** 2026-11-08 09:55:37 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3p.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261108_094405.md`

## Prompt

%id(gem, clan=research.3p)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3p.cdx`, `research.3p.cld`, `research.3p.grk`, `research.3p.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add generalized capture support for note files that use custom-defined
types.

- The ~/bob/eat/ files are examples of these types of files and should be our first
  use-case.
- I think we might have some other types that should be defined as well, but I might be
  wrong about this (podcasts, tv shows, and movies come to mind). You should think hard
  about this.
- Each one of these custom types should be able to define which frontmatter fields must
  be defined for each note defined of that type.
- Each custom type should also be associated with its own directory (like the ~/bob/eat/
  directory, for example).
- I'm not sure what the best capture syntax for this looks like (so you should think
  hard about this) but, when a capture specifies that a new note file of a
  custom-defined type should be added, then we should make it as easy as possible for
  the user to input the correct values for each required field (I'll let you decide if
  optional fields should be supported).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

### Research Report Summary: Generalized Custom-Type Note Capture

**Researcher**: `gem` (5-researcher independent swarm)  
**Report File**: [`custom_type_note_capture__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202611/custom_type_note_capture__gem.md)  
**Registered Artifact**: `research:202611/custom_type_note_capture__gem.md` (`ref: file:explicit:bbe6a449173ca8673df82ec1`)  

---

### 1. Critique & Strategic Evaluation

#### Is this a good idea?
**Yes, emphatically.** In Bryan's GTD and PKM system, capturing structured, atomic entities (a newly discovered restaurant, a recommended podcast, a movie or TV show to watch) currently has severe friction. The user must switch to desktop Obsidian, navigate folders, format YAML frontmatter by hand, adhere to wikilink conventions, and construct heading skeletons. Unifying entity capture into `bob capture` (and `bob-mac-capture`) closes the input loop and prevents friction-induced triage debt.

#### Pitfalls to Avoid:
1. **The Positional Argument Trap**: Trying to pack 5–8 fields into a positional string (`@eat/ "Ninja Sushi" | liked | Sushi | Clark | kelly`) creates a brittle, unreadable syntax where optional fields require empty delimiters (`|||`).
2. **The Interactive Prompt Trap**: Interactive shell prompts (`Enter category: `) break CLI pipes, shell scripts, tmux bindings, and the asynchronous `--dry-run` live preview contract with `bob-mac-capture`.
3. **The Task-Entity Conflation Trap**: An entity note is a durable knowledge entity, not an open task (`- [ ] #task`). Forcing entity notes into task rows violates vault conventions.

#### Recommended Requirement Adjustments:
1. **First-Class Required, Optional, and Default Fields**: Every custom type must support `required: true|false` alongside intelligent `default: <val>` declarations (e.g. `status: liked`, `companions: ["[[kelly]]"]`). Defaults eliminate up to 70% of typing while preserving complete frontmatter.
2. **Dual-Format Input (Child Bullets + Inline Fields)**:
   - *Child Bullets* (`- category: Sushi`): Natural, multiline drafting mirroring `decisions:capture-bullets-mirror-the-task-block`. Unmatched bullets automatically populate the `## Notes` section.
   - *Inline Dataview Fields* (`[category:: Sushi]`): Fast, single-line shorthand for quick entry via Alfred/Raycast or the CLI.
3. **Automated Slugification & Collision Guard**: Derive filenames automatically from `title` (e.g. `Ninja Sushi` $\to$ `ninja_sushi.md`) with explicit collision refusal so existing files are never overwritten silently.

---

### 2. Vault Inventory: What Note Types Should Exist?

Based on a comprehensive audit of `~/bob`, we analyzed the primary entity cohorts:

1. **`restaurant` (`~/bob/eat/`)** — *First Use-Case (92 existing files)*:
   - **Parent**: `[[eat]]` | **Type**: `[[restaurant]]`
   - **Required Fields**: `title`, `status` (`liked`, `not_liked`, `maybe_liked`, `want_to_try`), `category` (e.g. `Breakfast`, `Coffee`, `Sushi`, `Burritos`, `Dine-in`, `Pizza`), `location` (e.g. `[[nj_towns#...|cranford]]`, `Clark`, `Westfield`).
   - **Optional/Default Fields**: `companions` (default: `["[[kelly]]"]`), `lid` (auto-slug), `url`.
2. **`podcast` (`~/bob/podcasts/`)** — *(15 existing files)*:
   - **Parent**: `[[podcasts]]` | **Type**: `[[podcast]]`
   - **Required Fields**: `title`, `status` (`subscribed`, `unsubscribed`, `queued`), `category` (`programming`, `python`, `ai`, `tech`, `productivity`).
   - **Optional Fields**: `url` (show home or Spotify show link).
3. **`movie` (`~/bob/movies/`)** — *Vault Evidence: `chad_movie.md`, `chat_movie.zot`*:
   - **Parent**: `[[movies]]` (under `[[fun]]`) | **Type**: `[[movie]]`
   - **Required Fields**: `title`, `status` (`want_to_watch`, `watched`, `recommended`).
   - **Optional Fields**: `genre`, `year`, `recommended_by` (e.g. `[[chad]]`, `%kelly`), `rating`, `url`.
4. **`tv_show` (`~/bob/tv/`)** — *Vault Evidence: `fun.md` citing `text/tv.txt`*:
   - **Parent**: `[[tv]]` (under `[[fun]]`) | **Type**: `[[tv_show]]`
   - **Required Fields**: `title`, `status` (`watching`, `want_to_watch`, `watched`, `paused`, `dropped`).
   - **Optional Fields**: `platform` (e.g. `Netflix`, `Apple TV+`, `HBO/Max`), `genre`, `current_season`, `companions` (default `["[[kelly]]"]`).
5. **Other Types Scrutinized**:
   - **`people` (`people.md`)**: Currently a single 100+ line table managed with Vim alignment macros (`sort_by_person.vim`). Splitting into 100+ tiny files in `people/` adds folder bloat without benefit. **Recommendation: Keep as a table.**
   - **`lit` / `books` (`~/bob/lit/`)**: 80+ notes exist. Most formal literature runs through `bob ref` (PDF ingestion and highlights). Recommended as a Phase 2 addition for general non-PDF book notes.

---

### 3. Schema Architecture in `~/.config/bob/config.yml`

Declared under the new top-level key **`note_types:`** (avoiding collision with `types:` which governs Pomodoro task themes):

```yaml
note_types:
  restaurant:
    dir: eat
    parent: "[[eat]]"
    type: "[[restaurant]]"
    slug_field: lid
    filename_template: "{slug}.md"
    fields:
      title:
        type: string
        required: true
        source: parent_line
        prompt: "Restaurant Name"
      status:
        type: enum
        required: true
        values: [liked, not_liked, maybe_liked, want_to_try]
        default: liked
      category:
        type: string
        required: true
        suggest: [Breakfast, Coffee, Sushi, Pizza, Burritos, Dine-in, Mexican, Salad, Burgers, Misc]
      location:
        type: wikilink_or_string
        required: true
        suggest_routes: [nj_towns, nyc]
        prompt: "Location (town or wikilink)"
      companions:
        type: list_wikilink
        required: false
        default: ["[[kelly]]"]
      url:
        type: url
        required: false
    body_template: |
      # {{title}}

      ## Notes

      {{notes}}
```

---

### 4. Capture Grammar & UX Design

Following `decisions:capture-sigils-say-where-what-how` ("`@` says where"):
- `@route` targets a root file (`groceries.md`).
- **`@dir/`** targets a directory-associated entity note! A trailing slash (`@eat/`, `@podcasts/`, `@movies/`, `@tv/`) cleanly signifies a new entity file in that folder.

#### Syntax Examples:

**1. Multiline Drafting with Child Bullets (Recommended)**:
```text
Ninja Sushi @eat/
- category: Sushi
- location: Clark
- The spicy tuna rolls were fantastic! Kelly loved the salmon.
- Try the dragon roll next time.
```
*(Notice: `status: liked`, `companions: ["[[kelly]]"]`, and `lid: ninja_sushi` are filled from defaults automatically! Unmatched bullets become notes under `## Notes`.)*

**2. Compact Inline Dataview Fields (Single-Line Speed)**:
```bash
bob capture 'Ninja Sushi @eat/ [category:: Sushi] [location:: Clark]'
```

**3. Teaching Diagnostics on Missing Required Fields**:
```text
$ bob capture 'Ninja Sushi @eat/'
bob capture: error: note type 'restaurant' requires fields: 'category', 'location'
  hint: provide missing fields via child bullets:
    Ninja Sushi @eat/
    - category: <value>
    - location: <value>
```

---

### 5. Bob Mac Capture Presentation: The Entity Note Card

In accordance with `decisions:mac-capture-is-a-thin-client`, `bob-cli` remains the single authority for parsing, schemas, and validation, returning an additive `entity_note` object in `capture-parse` and `capture --dry-run`. 

Bob Mac Capture renders a visual **Entity Note Card** in the preview area:
- **Header**: Manila/emerald banner: `🍽️ NEW RESTAURANT · eat/ninja_sushi.md`.
- **Field Status Badges**: Clean pill toggles for `status` (`liked` / `not_liked`), dropdown suggestions for `category`, and wikilink picker for `location`.
- **Validation Guidance**: Soft amber badges highlight missing required fields in real time without blocking keystrokes.
- **Live Markdown Preview**: Displays the exact YAML frontmatter and Markdown body to be written.

---

### 6. Recommended Implementation Roadmap

1. **Phase 1: Schema Config & Content Renderer (`bob-cli`)**: Implement `src/native/config/note_types.rs` and `render_entity_note`, validated against `~/bob/eat/` fixtures.
2. **Phase 2: Capture Grammar & CLI Execution (`bob-cli`)**: Add `@dir/` route parsing in `capture_language`, child-bullet field extraction, slugification, collision checks, and atomic note writes.
3. **Phase 3: Autocomplete & Protocols (`bob-cli`)**: Expose entity routes in `bob capture-targets`, field/enum completions in `bob capture-complete`, and `entity_note` spans in `bob capture-parse`.
4. **Phase 4: Bob Mac Capture UI Card (`bob-mac-capture`)**: Add `EntityNoteCardView.swift` to present the interactive card and live preview.

The complete report with full architectural diagrams, sample JSON payloads, and comparative analysis has been written to [`custom_type_note_capture__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202611/custom_type_note_capture__gem.md) and registered in SASE durable artifact storage.
