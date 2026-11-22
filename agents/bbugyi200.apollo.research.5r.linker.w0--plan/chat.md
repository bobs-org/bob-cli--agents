# Chat History - ace-run (research.5r.linker.w0--plan)

- **TIMESTAMP:** 2026-11-21 14:55:13 EST
- **MODEL:** claude/opus
- **AGENT:** research.5r.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/spotify_episode_refs.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/spotify_episode_refs.md`

> # Plan: Spotify episodes become first-class podcast references
> ## Context
> The current output is wrong in several ways. `~/bob/ref/blogs/4ugvfwty2i8hgagsvt7pjc.md`
> (_Software factories and code reviews with Harjot Gill_, The Pragmatic Engineer) came in
> through share-to-Keep and is filed like this:
> - it is filed under `blogs/` with an opaque base62 stem and id;
> - its `source_url` still carries `si`/`sci` share tokens;
> - it has no `author` or `published`;
> - its PDF is one page of Spotify player chrome: the duplicated title, a half-page cover,
>   a relative date ("Wednesday"), the masthead URL with `nd=1&dlsi=…` tracking, "56

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to make the `bob ref create` command much smarter about how it
handles spotify URLs currently. Can you help me implement this?

- See the ~/bob/ref/blogs/4ugvfwty2i8hgagsvt7pjc.md ref note (and the corresponding ref
  task and ref PDF) for an example of what these spotify refs look like now.
- Fix any issues you find and make any objective improvements that you can think of
  (make sure every improvement is justified).
- Review the spotify_episode_capture_route.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (except for any sase memory file changes, which
  should only be implemented if I approve them or explicitly asked for them in this
  prompt), but keep in mind that you are responsible for planning and splitting up this
  work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5r.linker

## Response

Reading the Spotify research report first; the research sidecar needs to be opened in this workspace.

Current Spotify output confirmed: a one-page player-chrome stub. Now surveying the `highlights_ref` code that the research cites.

Now the arXiv route and its overwrite variant — the closest precedent for a Spotify route.

Still mapping the render path: the reader template renders an `article.json`, so a Spotify route can hand it Bob-built content without fetching or Defuddle extraction.

Spinning up two parallel read-only explorers (ingest/intake paths, and cross-repo ref-kind surfaces) while I read the fetcher and memory notes myself.

Both explorers confirmed the research's defect ledger at HEAD (the ingest path skips the source store, and the masthead prints `final_url`). Next, the fetcher and the governing memory notes.

Still in research: checking how the source store converts the printed HTML into Markdown, since the Spotify route has to persist one too.

Checking whether any existing memory note would become false after this work, which I'd have to plan a correction for.

No existing memory note becomes false. One optional branch of the plan would add a decision record, so I'm loading the memory-write skill as required.

Design is settled; checking the epic plan schema before writing it.

The schema is clear. Checking two more things that the plan will cite: the reader visual-testing guide and how the fake adapter serves ops in tests.

Last check before writing: the repo's standard verification commands, so each phase can name its gate.

Validation passed with 0 warnings. Revalidating without `--explain`, then proposing.

The proposal is staged. Finishing through the final-declaration skill.

I've written the plan as an epic with 10 phases, validated it (0 warnings), and submitted it for your approval. No code changes yet.

**What the current Spotify refs look like.** I opened the example ref and its PDF. The PDF is a single page of Spotify player chrome:
- The title appears twice and the cover takes half the page.
- The date is relative ("Wednesday") and it reports "56 words".
- The show notes are cut off mid-word ("Built for th"), followed by "See all episodes".
- The URL printed at the top keeps tracking parameters (`nd=1&dlsi=…`).

The note itself is filed under `blogs/` with an unreadable 22-character id as its name, and its source URL keeps Spotify's share tokens. I fetched the episode page with bob's own HTTP client and got the full metadata: exact title, publish date, duration, show and publisher, cover art, and the complete show notes including 16 timestamps. Today's empty capture comes from the headless Chrome browser being served a stripped-down page.

**Design**
- **One parser for every Spotify link format:**
  - web links, including regional (`/intl-xx/`) and embed links;
  - `spotify:episode:…` links;
  - short links, which are followed first.

  Episodes get a canonical link with the id's case preserved (a lowercased id doesn't work on Spotify). Both existing Spotify refs then count as duplicates of a fresh share with no migration.
- **Refusals with a hint.** Shows, music, audiobooks, `-L` and `-H` on Spotify links, and Spotify links mixed into multi-URL captures are refused with a hint saying what to do instead. Capture and Keep treat non-episode links like hosts they already skip, so they become ordinary items.
- **An episode summary PDF**, filed under `ref/podcasts/` with a name taken from the episode title:
  - a cover beside the show name, the title (once), the publisher, the full date and the duration;
  - "Listen on Spotify" and "Shared at 20:35" buttons;
  - clickable chapters placed where the publisher listed them, and the full show notes;
  - sponsor blocks moved into a quiet box at the end;
  - a footer saying where each part came from.

  It reuses the existing reader fonts and colours.
- **Transcripts only when proven.** bob looks up the show's public podcast feed and attaches the publisher's own transcript only when exactly one feed episode matches on two of three checks (title, date, duration). Every time it falls back to something less, it prints exactly one warning.
- **Three general bugs, fixed for all web refs:**
  - unreadable random ids no longer become file names;
  - refs created from Keep and capture save their source Markdown, so `bob ref links` and `bob ref code` work for them;
  - the PDF header prints the recorded URL instead of the post-redirect one with tracking.

**Choices I made where the research didn't settle them:**
- The on/off setting for the feed lookup is `highlights.podcasts.enrich`. It's named after the feed lookup rather than Spotify, and turning it off makes no Apple or feed requests at all.
- A `?t=` share timestamp is kept for capture and Keep links too, carried through to the PDF's "Shared at" button.
- `%l` on a Spotify episode in capture or Keep is ignored with a hint rather than failing the item.
- Chapter times stay plain text in the saved Markdown, so `bob ref links` lists the publisher's links rather than 16 Spotify jump links.
- Bob Mac Capture shows podcast refs in purple, the colour Apple uses for podcasts.

**Phases:** general bug fixes and Spotify link handling first (they can run in parallel); then episode metadata, the PDF layout, the `bob ref create` route, and capture/Keep; then feed matching and transcript parsing (in parallel), transcript pages; and a final step that updates Bob Mac Capture, the reading board plugin, and your vault's `refs.base`.

**Two decisions for you at approval:**
- **Upgrading the two existing Spotify refs** (on by default): rename each onto its title, then rebuild its PDF in place. Their tasks, links and the zettel link are kept; they stay in `blogs/`.
- **A memory decision record for this policy** (off by default): you said memory changes need your approval, so it is only written if you turn it on.
