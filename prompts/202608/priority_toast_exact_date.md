- **PLAN:**
  [202608/priority_toast_exact_date.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/priority_toast_exact_date.md)
- **AGENTS:**
  - [bbugyi200.athena.sj.f0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.sj.f0.md#member-plan)

%xprompts_enabled:false

# Previous Conversations

You are forking from 1 prior source. Source sections are independent parents, and section order carries no priority.
Members inside an agent family section are sequential: each member continued the previous member's work. Carry forward
relevant goals, constraints, decisions, and unfinished work with attribution when it matters. The New Query is the
active request and takes precedence over conflicting source instructions.

## Source 1 of 1 — agent family `sj`

- **Members shown:** 2 of 2 (sequential chain, oldest first)

Family members ran as one sequential chain: each member continued the previous member's work, and the last member
reflects the family's final state. These are transcripts of prior agents' conversations, not your own — attribute
decisions to the named member when it matters.

### Member 1 of 2 — agent `sj--plan`

- **Outcome:** `completed` · **Model:** `claude/opus` · **Launch:** `20260803062957`
- **Transcript:** `~/.sase/chats/202608/gh_bobs_org__bob_cli-ace_run-sj__plan-260803_062957.md`

**User:**

We recently added support for P2, P3, and P4 Obsidian task priorities (see the gh_bobs-org__bob-cli-5 epic bead for
context). Can you help me make sure that the Obsidian toast we show to the user (after selecting a valid priority that
is presented after the `<ctrl+shift+p>` keymap is used and the user selects `priority`) includes the relative number of
days (from today) that the task was scheduled for? Also, try to make this toast look better in general. I want you to
lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least)
beautiful! Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the
appropriate tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill
instructs) before making any file changes.

**Assistant:**

_Plan submitted for review._

**Plan file:** `/home/bryan/.sase/plans/202608/priority_toast.md`

> # Plan: Redesign the priority write toast around relative scheduled days
>
> ## Repositories
>
> This tale spans the plugin monorepo plus documentation in the primary repo. Open the non-primary repository through
> the `/sase_repo` skill and use the printed path for every read and write:
>
> - `sase repo open bob-plugins -r "<reason>"` — owns `plugins/bob-navigation-hotkeys/main.js`, `styles.css`,
>   `manifest.json`, `scripts/test-navigation-hotkeys.cjs`, and `README.md`. **All code in this plan lives here.**
> - The primary `bob-cli` repo owns `docs/projects.md`, which documents the priority property. Run the suite from the
>   `bob-plugins` checkout: `npm test` (shells out to `node --test scripts/*.cjs`) and `npm run validate` (manifest
>   check). Deploy with `bob plugins sync -p bob-navigation-hotkeys -r "$PWD"`; the `-r "$PWD"` is required because the
>   default source path does not exist in a SASE workspace.

_See full plan file for details._

### Member 2 of 2 — agent `sj--code`

- **Outcome:** `completed` · **Model:** `codex/gpt-5.5` · **Launch:** `20260803064100`
- **Transcript:** `~/.sase/chats/202608/gh_bobs_org__bob_cli-ace_run-sj__code-260803_062957.md`

**User:**

@sase/repos/plans/202608/priority_toast.md

The above plan has been reviewed and approved. Implement it now.

**Assistant:**

I’ll read the approved plan and the nearby project context first, then make the scoped changes and run the relevant
checks.

The file is not in the normal tracked file list, so I’m checking hidden and generated paths before touching
implementation files.

I found the plan under the local `sase/repos/plans` checkout. I’m reading it now and then I’ll map it to the CLI code
paths.

The plan targets the linked `bob-plugins` repo for the plugin code, plus one docs update in this repo. I need to open
that linked repo through the SASE repo workflow before reading or changing it.

I’m using the `/sase_repo` workflow for `bob-plugins` because the plan’s code changes are outside this primary checkout.

The linked repo is ready at `sase/repos/linked/bob-plugins`. I’m locating the priority writers, existing notice helpers,
and tests before editing.

The existing implementation has the three notice paths named in the plan, and tests already assert the old strings. I’m
reading the writer implementations and helper exports now so the refactor stays localized.

I’ve got the shape now: the priority-specific rendering can be added as pure helpers plus a `buildNotice` callback,
leaving non-priority property notices on the old string path. I’m going to patch `main.js` first, then update tests and
styles.

The previous read overlapped unrelated sections because the file is large; I’m narrowing to the validation/date helpers
before adding the new model.

I’m starting the patch with pure notice helpers and the byte-identical suffix extractions. This gives the DOM renderer
and plain fallback one shared model without changing the old non-priority strings.

The suffix extraction is in place. I’m adding the relative-day vocabulary and the priority notice model/rendering
functions next.

The new model and renderer are now in `main.js`. I’m wiring the three writers through the model while keeping the
generic property writer’s old notice path intact.

The counted notice suffix now delegates to a top-level extracted parts helper. I’m replacing the class method with that
helper so old counted property notices keep their exact wording.

The counted priority writer is self-contained, so I’m replacing its old semicolon string with a model built from the
actual scheduled values written to each target.

I’m adding the project-writer callback at the point where it already has propagation, hide-removal, Blocked, ambiguity,
and recovery counts. Non-priority project scheduling will still use the existing plain notice.

Now I’m adding the inline-writer callback after its Blocked/recovery decision. The old notice construction remains the
fallback path for scheduled, dependsOn, scalar values, and deletion behavior.

I’m updating the priority entry point so the same rolled base date flows into both the write decision and the notice
math, including the `^prj` frontmatter path.

The three priority write paths are now wired. I’m checking for leftover `noticePrefix` usage and adding helper exports
before updating tests.

I caught an overbroad edit while reviewing: the plain counted property writer briefly referenced `options` even though
it has no options parameter. I’m correcting that before moving on.

The syntax check is clean. I still need the inline writer to use the priority base date for relative math and Blocked
behavior, so I’m tightening that one remaining `today` assignment.

I’m exporting the pure helpers and renderer so the Node test suite can cover the visual model without a real Obsidian
DOM.

I’m updating the Node tests now: first pure helper/model/renderer coverage, then the existing end-to-end notice
expectations.

The fragment stub is in place. I’m adding the model and fallback assertions just ahead of the existing priority picker
tests.

The pure tests are in. I’m changing only the priority end-to-end assertions that intentionally changed wording.

The JS syntax still checks, so I’m running the navigation-hotkeys test file now before touching CSS/docs.

The targeted test run found one model alias gap: project outcomes pass `scheduledTaskCount`, while the shared chip
builder only looked for `propagatedScheduleTaskCount`. I’m fixing the builder rather than weakening the test.

The alias fix is in. I’m rerunning the navigation-hotkeys file to catch any remaining behavioral mismatches before
styling.

The focused navigation-hotkeys tests are green. I’m adding the scoped toast CSS now, following the existing
pill/color-mix conventions.

I’m appending the toast styles at the end of the plugin stylesheet, fully scoped under `.bob-nh-notice` so the notice
chrome cannot leak into other Obsidian notices.

The CSS is added. I’m bumping the plugin metadata and the README row, then I’ll update the primary repo docs section.

Manifest version is bumped. I’m updating the plugin README row to mention the new relative-day priority write notice.

The linked repo docs are updated. I’m adding the priority notice behavior to `docs/projects.md` in the primary checkout.

The implementation and docs are patched. I’m running the full plugin suite and manifest validation from `bob-plugins`
now.

Full `npm test` and manifest validation are green. I’m checking diffs and whitespace in both repos before running the
sync dry-run.

Whitespace checks are clean. I’m doing a quick self-review of the diff before committing and deploying the plugin copy.

The diff review looks coherent. I’m making a small readability cleanup in two long model-builder lines before the final
commit/deploy steps.

That cleanup preserves the tested strings. I’m rerunning the focused navigation-hotkeys file and whitespace checks after
the touch-up.

The focused test file still passes after the cleanup, and both whitespace checks are clean. I’m using the SASE commit
workflow now for the two repositories.

I’m committing the plugin repo first with the feature code, tests, styles, README, and version bump.

The plugin commit message is staged in the ignored `.sase` scratch area. I’m running `sase_git_commit` with explicit
file flags.

The plugin commit succeeded. I’m checking its status, then I’ll commit the primary repo docs change.

The plugin repo is clean and aligned with its upstream. I’m committing the primary repo documentation update next.

The primary docs commit message is ready. I’m committing just `docs/projects.md`.

The primary commit reported success; the process is still closing out, so I’m waiting for the command to finish cleanly
before deploying.

The commit command is taking longer than usual after reporting success. I’m continuing to wait rather than starting
dependent steps while it may still be doing post-commit bookkeeping.

The primary commit has fully exited. I’m checking both repo statuses before running the plugin sync dry-run.

Both repositories are clean and aligned. I’m running the required `bob plugins sync` dry-run from the plugin repo now.

The dry-run would copy only the expected plugin files and reported no dirty-vault blocker. I’m running the actual sync
now.

The plugin sync completed and copied `manifest.json`, `main.js`, and `styles.css` into the vault with backups. I’m doing
final status/hash checks now.

Implemented and deployed.

Changes:

- Added structured priority notices for single, counted, and `^prj` priority writes.
- Added relative day/range formatting and actual counted scheduled spans.
- Kept non-priority notices on the existing plain string path.
- Added scoped `.bob-nh-notice` CSS.
- Bumped `bob-navigation-hotkeys` to `1.15.0`.
- Updated plugin README and `docs/projects.md`.

Committed:

- `bob-plugins`: `6fa6e48 feat(navigation-hotkeys): add structured priority notices`
- `bob-cli`: `102c59f docs(projects): document priority write notices`

Verified:

- `npm test`: 273/273 passing
- `npm run validate`: 6/6 plugins valid
- `git diff --check`: clean in both repos
- `bob plugins sync --dry-run`, then actual sync succeeded
- Vault plugin files match the source repo copies

Reload the Bob Navigation Hotkeys plugin in Obsidian so the synced `main.js` and `styles.css` are picked up. Manual
checks to run after reload: ordinary P2 priority toast, light/dark theme legibility, counted P4 span, and `^prj` showing
`scheduled (project)`.

---

%xprompts_enabled:true

# New Query

This looks great, but I want to keep showing the YYYY-mm-dd date somewhere in the toast. Can you help me fix this? Think
this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate tier,
validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs) before making
any file changes.
