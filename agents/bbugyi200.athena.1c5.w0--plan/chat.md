# Chat History - ace-run (1c5.w0--plan)

- **TIMESTAMP:** 2026-11-13 08:41:05 EST
- **MODEL:** claude/opus
- **AGENT:** 1c5.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/plugins_sync_config_allowlist.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/plugins_sync_config_allowlist.md`

> # Require bob config to list every plugin `bob plugins sync` deploys
> ## Goal
> `bob plugins sync` currently deploys every plugin folder under `<repo>/plugins/`. After
> this change it deploys only plugin ids that bob's config file lists explicitly. A
> missing list is a setup error, not "sync everything". Bryan's chezmoi-managed bob config
> gains the list, naming every plugin he deploys today.
> Below, `plugins.sync` is the config key (decision `config_key`). If the reviewer picks
> `enabled`, use `plugins.enabled` everywhere `plugins.sync` appears: code constants,
> messages, docs, tests, and the chezmoi config. The JSON field names `configured` and
> `not_configured` stay the same under both choices.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli %w:1c5 I would like to start requiring that all plugins synced by the
`bob plugins sync` command be listed explicitly in bob's config file (so users need to
enable each plugin by adding that plugin's name to this configuration field). Can you
help me implement this? As a part of this change, you should update the bob
configuration in my chezmoi repo appropriately.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Exploring `bob plugins sync` internals and bob's config system so I can plan the explicit plugin allowlist.

Found the 11 plugins in bob-plugins and bob's config in chezmoi. Now reading the config file, the vault's enabled plugins, and the chezmoi rules.

Still mapping the change surface — now checking `just install-all`, the plugin tests, and the bob-plugins smoke gate that consume `bob plugins sync`.

Nearly done exploring — checking for install_all test coverage and the docs reference pages before writing the plan.

Exploration nearly complete; one last check for existing `bob plugins` integration tests, then I'll write the plan.

Checking that a new top-level `plugins:` key won't collide with anything that already reads `config.yml` (bob itself or the Obsidian plugins).

Checking whether shell completion offers plugin ids for `-p`, since that should follow the config too.

I have the full picture. Writing the plan now.

Plan passes validation. Submitting it.

I've written the plan as a single-agent plan sized medium and submitted it for your approval; it passed validation. No files outside the plan itself have changed yet, and implementation starts once you approve it.

**The core change**
- **New config key:** bob's config gets a `plugins.sync` list of plugin ids, and `bob plugins sync` deploys only the plugins named there.
- **Missing list:** if the config doesn't have the list, sync stops with exit code 2. It does this before pulling the plugins repo or touching the vault. The error message includes a YAML snippet listing every plugin id in your checkout, ready to paste.
- **Empty list:** `plugins.sync: []` is valid and deploys nothing.
- **Plugins left off the list:** sync skips them and names them in its output, including a new `not_configured` field in the JSON output.
- **A listed id the repo doesn't have:** sync reports an error and exits 1, but still deploys the other plugins.
- **`-p <id>` for a plugin not on the list:** sync refuses it. There's no override flag, since an explicit list is the point.
- **Old bob versions:** they ignore the new key, so you can roll out the config before the new bob reaches every machine.
- **Breaking change:** the commit is marked as a breaking CLI change.

**Your chezmoi config:** I'll add a commented `plugins:` block to `home/dot_config/bob/config.yml` listing all 11 plugins the vault deploys and enables today (block-id-prompt, bob-articles, bob-command-mode, bob-emoji, bob-ledger-tools, bob-mail, bob-navigation-hotkeys, bob-project-tasks, bob-vim-surround, bob-vim-yank-flash, task-status-cycler).

**Also covered**
- Updated help text and docs, plus a short note in bob-plugins' deployment doc that a new plugin has to be added to the list before sync will deploy it.
- `just install-all` will show bob's actual error when the sync preview fails, instead of just "could not preview plugin sync".
- Unit and integration tests. Every existing sync test needs a config file added, because the test setup points at a missing config.
- A dry-run check against your real vault using the new chezmoi config. No real sync will be run.

**Two choices for you at approval:**
1. **Key name:** `plugins.sync` (my default) or `plugins.enabled`, which matches how you phrased it. I lean toward `sync` because bob already uses "enabled" for Obsidian's own on/off state, so "enabled" would end up meaning two things.
2. **Showing unlisted plugins outside sync (default: on):** `bob plugins list` marks repo plugins that aren't on the list, and `just install-all` only checks listed plugins for drift. It also names any unlisted ones.

**After it lands:** chezmoi's rule is to run `chezmoi update -a --force` after a commit. That commit is made after the coding agent finishes, so you'll need to run it on athena, apollo and the Mac yourself.

**Not included**
- Removing plugins you drop from the list from the vault. They just stop being updated.
- Turning plugins on or off in Obsidian.
- Limiting tab-completion for `-p` to listed plugins.
- Changing the bob-plugins startup check. It still passes, because every plugin is listed.
