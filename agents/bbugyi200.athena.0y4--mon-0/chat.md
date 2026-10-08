# Chat History - ace-run (0y4--mon-0)

- **TIMESTAMP:** 2026-10-08 07:39:41 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 0y4--mon-0

## Prompt

sase monitor start --command 'just check' --reason 'final verification for tmux extended-keys-format compat plan'

## Response

sase tool run 2b2aaf8a30b1bcd0e032c10bd211f854

┌───────────────────────────────────────────────────────┐
│                RUNNING: just fmt-check                │
└───────────────────────────────────────────────────────┘

---------- Checking Python formatting with ruff... ----------
.venv/bin/ruff format --check home/lib
14 files already formatted

---------- Checking Markdown formatting with prettier... ----------
prettier --check --prose-wrap=always --print-width=88 "**/*.md"
Checking formatting...
All matched files use Prettier code style!

┌───────────────────────────────────────────────────────┐
│                RUNNING: just lint                     │
└───────────────────────────────────────────────────────┘

---------- Checking keep-sorted blocks in YAML files... ----------
git ls-files '*.yml' '*.yaml' | xargs .venv/bin/keep-sorted --mode lint

---------- Running ruff linter on Python files... ----------
.venv/bin/ruff check home/lib
All checks passed!

---------- Checking Python formatting with ruff... ----------
.venv/bin/ruff format --check home/lib
14 files already formatted

---------- Running mypy on Python files... ----------
.venv/bin/mypy home/lib/xfile
Success: no issues found in 9 source files

---------- Running llscheck linter on Lua files... ----------
llscheck --checklevel Hint ./home/dot_config/nvim
Diagnosis completed, no problems found
llscheck --checklevel Hint ./tests/nvim
Diagnosis completed, no problems found
llscheck --checklevel Hint ./home/lib
Diagnosis completed, no problems found

---------- Running luacheck linter on Lua files... ----------
luacheck --no-global ./home/dot_config/nvim ./tests/nvim ./home/lib
Checking home/dot_config/nvim/after/ftplugin/fugitive.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/harpoon.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/hgcommit.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/man.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/markdown.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/netrw.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/qf.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/query.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/sagafinder.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/sh.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/after/ftplugin/zorg.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/hgxl.lua            [0m[32m[1mOK[0m
Checking home/dot_config/nvim/init.lua            [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/bb_utils/_snip_utils.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/bb_utils/_superlazy.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/bb_utils/_telescope_files.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/bb_utils/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/autocmds.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/bob_keymaps.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/bob_pomodoro_keymaps.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/commands.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/keymaps/delete_buffers.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/keymaps/highlight_long_lines.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/keymaps/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/keymaps/keymaps.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/keymaps/nav_buffers.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/keymaps/swap_words.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/keymaps/yank_path.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/lazy_plugins.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/load_local_configs.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/lsp.lua  [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/options.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/postload.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/preload.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/pyzorg.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/config/remove_zorg.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/extra/codecompanion/extmarks.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/extra/codecompanion/fidget.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/legacy_zorg/config/config.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/legacy_zorg/config/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/legacy_zorg/config/nav_keymaps.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/legacy_zorg/util/literal_run_open_zorg_action.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/legacy_zorg/util/search.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/overseer/template/make_targets.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/aerial.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/autopairs.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/autosession.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/beads.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/bqf.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/bufexplorer.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/bufferline.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/chezmoi.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/cmp.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/common.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/bcc.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/favs.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/paths.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/shared.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/xclip.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/xfile.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/codecompanion/slash_cmds/xpath.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/colorizer.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/colortils.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/comment.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/comment_box.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/conform.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/copilot.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/coverage.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/dap/configure_debuggers.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/dap/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/dap/init_keymap_hooks.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/dashboard.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/demicolon.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/dial.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/diffview.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/fidget.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/firenvim.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/fold_cycle.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/gemini_cli.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/git_messenger.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/ai.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/buganizer.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/cider_agent.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/cmp.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/goose/backend.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/goose/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/goose/log.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/goose/url.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/slash_cmds/bugs.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/slash_cmds/clfiles.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/slash_cmds/cs.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/slash_cmds/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/codecompanion/slash_cmds/xrefs.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/critique.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/glugs.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/goog_terms.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/googlepaths.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/hg.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/init.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/google/neocitc.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/gp.lua  [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/guess_indent.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/harpoon.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/helpview.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/illuminate.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/key_analyzer.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/lazydev.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/lspconfig.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/lspsaga.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/lualine.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/luasnip.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/markdown_preview.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/markview.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/mason.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/neogen.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/neotest.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/netrw.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/nnn.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/notify.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/octo.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/overseer.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/plugins.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/rainbow.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/refjump.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/remove_obsidian.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/remove_sase_neovim.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/rustaceanvim.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/sase_nvim.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/scope.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/scratch.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/silicon.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/snacks.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/sniprun.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/telescope.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/todo_comments.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/toggleterm.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/tokyonight.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/tpope.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/treesitter.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/treewalker.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/trouble.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/troublesum.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/ts_autotag.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/ufo.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/undotree.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vcscommand.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_dispatch.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_eunuch.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_grepper.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_kitty.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_matchup.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_projectionist.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_signify.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_table_mode.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/vim_textobj_entire.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/which_key.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/wilder.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/wit.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/lua/plugins/zorg_nvim.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/all.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/bugged.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/codecompanion.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/dart.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/hgcommit.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/java.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/lua.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/markdown.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/python.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/sh.lua  [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/yaml.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/luasnippets/zorg.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/tests/bob_keymaps_spec.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/tests/bob_pomodoro_keymaps_spec.lua [0m[32m[1mOK[0m
Checking home/dot_config/nvim/tests/minimal_init.lua [0m[32m[1mOK[0m
Checking tests/nvim/smoke_tests.lua               [0m[32m[1mOK[0m
Checking tests/nvim/unit_tests.lua                [0m[32m[1mOK[0m
Checking home/lib/pandoc_code_reader.lua          [0m[32m[1mOK[0m

Total: [0m[0m[1m0[0m warnings / [0m[0m[1m0[0m errors in 180 files

---------- Checking Markdown formatting with prettier... ----------
prettier --check --prose-wrap=always --print-width=88 "**/*.md"
Checking formatting...
All matched files use Prettier code style!

┌───────────────────────────────────────────────────────┐
│                RUNNING: just test                     │
└───────────────────────────────────────────────────────┘

---------- Running Neovim tests using busted... ----------
busted -p _test ./tests/nvim
+++++..+
6 successes / 0 failures / 0 errors / 2 pending : 3.017061 seconds

Pending -> ./tests/nvim/unit_tests.lua @ 8
UNIT TEST: bb_utils.delete_file()

Pending -> ./tests/nvim/unit_tests.lua @ 10
UNIT TEST: bb_utils.copy_to_clipboard()

---------- Running Hammerspoon tests using busted... ----------
busted ./tests/hammerspoon
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
139 successes / 0 failures / 0 errors / 0 pending : 2.371548 seconds

---------- Running bash tests using bashunit... ----------
bashunit ./tests/bash
[1m[32mbashunit[0m - 0.36.0 | Tests: 276
[1mRunning ./tests/bash/bas_test.sh[0m
[32m✓ Passed[0m: Default command is tm sase                                        49ms
[32m✓ Passed[0m: One string command is preserved                                   51ms
[32m✓ Passed[0m: Split command is quoted safely                                    59ms
[32m✓ Passed[0m: Wrapper prefers interactive login zsh                             60ms
[32m✓ Passed[0m: Wrapper refreshes tmux environment before exec                    56ms
[32m✓ Passed[0m: Keepalive tty and host are forwarded to autossh before remote ... 51ms

[1mRunning ./tests/bash/bob_xlib_pull_test.sh[0m
[32m✓ Passed[0m: Real remote probe skips missing and empty queues                 102ms
[32m✓ Passed[0m: Real remote probe skips queues containing only directories        94ms
[32m✓ Passed[0m: Real remote probe pulls nested and hidden files from both hosts  142ms
[32m✓ Passed[0m: Real remote probe treats a dangling symlink as pending           104ms
[32m✓ Passed[0m: Non macos exits without network work                              59ms
[32m✓ Passed[0m: Existing invocation lock exits without network work               82ms
[32m✓ Passed[0m: Both hosts are checked and nonempty hosts are pulled             326ms
[32m✓ Passed[0m: Probe barrier proves both checks start before results are con... 187ms
[32m✓ Passed[0m: Blocked apollo probe does not delay ready athena transfer        177ms
[32m✓ Passed[0m: Empty queues skip rsync and cleanup                               91ms
[32m✓ Passed[0m: Unreachable hosts are no work and do not retry through transfer  109ms
[32m✓ Passed[0m: Later unreachable host still allows first transfer               102ms
[32m✓ Passed[0m: Traversal errors are reported as failures                         85ms
[32m✓ Passed[0m: Transfer failure survives second host success and cleanup        109ms
[32m✓ Passed[0m: Probe transfer and cleanup reuse the same control path           104ms
[32m✓ Passed[0m: Relative xlib dir resolves under bob dir with spaces              96ms
[32m✓ Passed[0m: Absolute xlib dir is preserved                                    89ms
[32m✓ Passed[0m: Home relative xlib dir is expanded                                85ms
[32m✓ Passed[0m: Long spaced tmpdir only holds the invocation lock                110ms
[32m✓ Passed[0m: Rsync source path and stdin sensitive transport are preserved     96ms
[32m✓ Passed[0m: Signal during blocked probe reaps workers and releases lock      158ms
[32m✓ Passed[0m: Signal during transfer reaps worker and releases lock            289ms
[32m✓ Passed[0m: Real rsync ignore existing keeps collisions on the source        197ms
[32m✓ Passed[0m: Real rsync file directory collision retains source data          220ms
[32m✓ Passed[0m: Successful pull runs one no hooks scan after the transfers       135ms
[32m✓ Passed[0m: Empty queues still run the scan                                   84ms
[32m✓ Passed[0m: Unreachable hosts still run the scan                              75ms
[32m✓ Passed[0m: Transfer failure still scans and fails the run                    88ms
[32m✓ Passed[0m: Pre scan hook marker pulls but skips the scan                     97ms
[32m✓ Passed[0m: Held scan lock suppresses the scan and stays in place             93ms
[32m✓ Passed[0m: Scan failure sets a nonzero exit and reports the status          103ms
[32m✓ Passed[0m: Non macos run never scans                                         66ms
[32m✓ Passed[0m: Bob falls back to the cargo bin when missing from path            82ms
[32m✓ Passed[0m: Missing bob reports the lookup path and fails without scanning   103ms
[32m✓ Passed[0m: Signal during scan reaps worker and releases both locks          170ms

[1mRunning ./tests/bash/chezmoi_utils_test.sh[0m
[32m✓ Passed[0m: Can sudo true via passwordless sudo                               44ms
[32m✓ Passed[0m: Can sudo true via tty when sudo n refuses                         45ms
[32m✓ Passed[0m: Can sudo false when sudo n and tty both fail                      46ms
[32m✓ Passed[0m: Exit install exits zero on success                                41ms
[32m✓ Passed[0m: Exit install exits nonzero when interactive                       41ms
[32m✓ Passed[0m: Exit install soft fails non interactive install failure           46ms

[1mRunning ./tests/bash/claude_raw_sudo_guard_test.sh[0m
[32m✓ Passed[0m: Denies plain sudo                                                203ms
[32m✓ Passed[0m: Denies sudo after pipeline and assignment                        200ms
[32m✓ Passed[0m: Denies sudo after newline separator                              199ms
[32m✓ Passed[0m: Denies doas and pkexec                                           381ms
[32m✓ Passed[0m: Denies env and exec wrappers                                     377ms
[32m✓ Passed[0m: Allows sase sudo front door                                      196ms
[32m✓ Passed[0m: Allows plain text mentions and command lookup                    370ms
[32m✓ Passed[0m: Allows when not running as sase agent                            112ms
[32m✓ Passed[0m: Claude settings registers bash guard                             276ms

[1mRunning ./tests/bash/codex_config_test.sh[0m
[32m✓ Passed[0m: Codex hooks feature is enabled                                    33ms
[32m✓ Passed[0m: Codex stop hooks do not include sase commands                     29ms

[1mRunning ./tests/bash/fake_test.sh[0m
[32m✓ Passed[0m: Bazbuz                                                            37ms

[1mRunning ./tests/bash/install_luarocks_test.sh[0m
[32m✓ Passed[0m: All five installs succeed in order                                93ms
[32m✓ Passed[0m: Busted failure survives later luacov success                     103ms
[32m✓ Passed[0m: Multiple failures are summarized once and all installs are at... 102ms
[32m✓ Passed[0m: Existing tree survives failure and successful retry              122ms
[32m✓ Passed[0m: Bootstrap failure stops before rock installs and preserves tree   83ms
[32m✓ Passed[0m: Non interactive failure soft exits with summary                   94ms
[32m✓ Passed[0m: Existing luarocks provisions lua51 via brew before rocks          94ms
[32m✓ Passed[0m: Lua51 provision failure skips rock installs                       76ms

[1mRunning ./tests/bash/install_sase_github_test.sh[0m
[32m✓ Passed[0m: Pull failure is fatal and stops before install                   356ms
[32m✓ Passed[0m: Dirty worktree is fatal                                          367ms
[32m✓ Passed[0m: Aggregated failures report every repo                            329ms
[32m✓ Passed[0m: Clean repos pass the gate and reach install                      426ms
[32m✓ Passed[0m: Sase core rs version skew is fatal before axe maintenance        370ms
[32m✓ Passed[0m: Files changed count is reported for fast forward pull            461ms
[32m✓ Passed[0m: Files changed count uses singular wording                        446ms

[1mRunning ./tests/bash/macscrot_test.sh[0m
[32m✓ Passed[0m: Both hosts succeed                                               104ms
[32m✓ Passed[0m: Uploads overlap in time                                          191ms
[32m✓ Passed[0m: Apollo fails athena succeeds                                      98ms
[32m✓ Passed[0m: Athena fails apollo succeeds                                      86ms
[32m✓ Passed[0m: Both hosts fail                                                   78ms
[32m✓ Passed[0m: Capture cancelled skips upload                                    77ms

[1mRunning ./tests/bash/poseidon_cache_watch_test.sh[0m
[32m✓ Passed[0m: Healthy poseidon is quiet                                        107ms
[32m✓ Passed[0m: Warns at 75 percent once                                         283ms
[32m✓ Passed[0m: Retries notification when delivery fails                         321ms
[32m✓ Passed[0m: Bypass at 80 percent                                             233ms
[32m✓ Passed[0m: Recovery requires hysteresis                                     527ms
[32m✓ Passed[0m: Setup notification is marked                                     210ms
[32m✓ Passed[0m: Old target writable is reported                                  229ms
[32m✓ Passed[0m: Scratch soft target does not notify                              325ms
[32m✓ Passed[0m: Root low space alerts once                                       278ms
[32m✓ Passed[0m: Root hysteresis does not recover early                           276ms
[32m✓ Passed[0m: Root recovers only after alert                                   491ms

[1mRunning ./tests/bash/poseidon_chezmoi_isolation_test.sh[0m
[32m✓ Passed[0m: Apollo ignores poseidon files                                    118ms
[32m✓ Passed[0m: Mac ignores poseidon files                                       106ms
[32m✓ Passed[0m: Athena does not ignore poseidon files                             99ms
[32m✓ Passed[0m: Cargo config renders only on athena                              234ms

[1mRunning ./tests/bash/sase_completion_test.sh[0m
[32m✓ Passed[0m: Apply writes completion loaders without runtime metadata         216ms
[32m✓ Passed[0m: Apply is repeatable                                              190ms
[32m✓ Passed[0m: Hook zcompiles only when needed                                  1.28s
[32m✓ Passed[0m: Repeated apply keeps loader stable while runtime grammar changes 218ms
[32m✓ Passed[0m: Zsh startup loads managed sase completion with framework conf... 705ms
[32m✓ Passed[0m: Zsh startup loads managed sase completion without conflict       679ms

[1mRunning ./tests/bash/sase_rustc_wrapper_test.sh[0m
[32m✓ Passed[0m: Runs real compiler when mount is missing                          92ms
[32m✓ Passed[0m: Runs real compiler when uuid mismatches                           76ms
[32m✓ Passed[0m: Runs real compiler when volume is a symlink                       81ms
[32m✓ Passed[0m: Runs real compiler at 80 percent                                  85ms
[32m✓ Passed[0m: Runs real compiler below 32g floor                                82ms
[32m✓ Passed[0m: Uses sccache when poseidon is healthy                             97ms
[32m✓ Passed[0m: Propagates compiler failure                                       78ms
[32m✓ Passed[0m: Normalizes sccache env and drops remote backend                  101ms
[32m✓ Passed[0m: Falls back when sccache is missing                                94ms
[32m✓ Passed[0m: Metadata incremental runs direct skipping sccache                101ms
[32m✓ Passed[0m: Metadata incremental two word flag runs direct                    92ms
[32m✓ Passed[0m: Codegen incremental strips flag before sccache                   106ms
[32m✓ Passed[0m: Codegen incremental two word flag is stripped                     99ms
[32m✓ Passed[0m: Metadata without incremental still uses sccache                   91ms
[32m✓ Passed[0m: Clippy driver metadata incremental runs direct                    92ms
[32m✓ Passed[0m: Sccache path forces cargo incremental off                         91ms
[32m✓ Passed[0m: Codegen incremental env is off before sccache                     93ms
[32m✓ Passed[0m: Metadata direct preserves cargo incremental env                   83ms
[32m✓ Passed[0m: Clippy driver chain metadata incremental runs direct             118ms

[1mRunning ./tests/bash/sshot_fetch_test.sh[0m
[32m✓ Passed[0m: Union picks nth newest basename                                   94ms
[32m✓ Passed[0m: Skips scp when chosen file is local                               84ms
[32m✓ Passed[0m: Apollo listing fail still returns athena file                     92ms
[32m✓ Passed[0m: Rejects n less than one                                           67ms
[32m✓ Passed[0m: Missing nth entry errors                                          76ms

[1mRunning ./tests/bash/tmp_trash_empty_test.sh[0m
[32m✓ Passed[0m: Purges tmpdir trash dir                                           68ms
[32m✓ Passed[0m: Purges alternate spec layout                                      68ms
[32m✓ Passed[0m: Skips trash dirs that do not exist                                67ms
[32m✓ Passed[0m: Dry run is forwarded                                              71ms
[32m✓ Passed[0m: Dry run does not write the stamp                                  73ms
[32m✓ Passed[0m: Periodic run is skipped when stamp is fresh                       58ms
[32m✓ Passed[0m: Periodic run proceeds when stamp is stale                         68ms
[32m✓ Passed[0m: Unrecognized argument is rejected                                 53ms

[1mRunning ./tests/bash/tmux_ai_window_test.sh[0m
[32m● set_up_before_script[0m                                                       8ms
[32m✓ Passed[0m: Launch grok uses max effort and auto approval                     69ms
[32m✓ Passed[0m: Launch agy uses pinned gemini 37 flash high model                 74ms
[32m✓ Passed[0m: Launch muse uses pinned model ultra effort and yolo               75ms
[32m✓ Passed[0m: Launch muse never uses contributor model                          75ms
[32m✓ Passed[0m: Menu includes grok and muse rows with keys                       134ms
[32m✓ Passed[0m: Partial install menu shows complete catalog with disabled rows   312ms
[32m✓ Passed[0m: Only grok installed makes grok the default choice                290ms
[32m✓ Passed[0m: Launch unknown provider exits 2                                   71ms
[32m✓ Passed[0m: Provider menu keys are unique                                    149ms
[32m✓ Passed[0m: Script avoids bash 4 only features                                51ms
[32m✓ Passed[0m: Menu rows are sorted by menu key                                 130ms
[32m✓ Passed[0m: Menu rows are ordered by provider name matching keys             140ms
[32m✓ Passed[0m: All installed menu has no disabled rows                          131ms
[32m✓ Passed[0m: Claude is the default choice even when not the first row         116ms
[32m✓ Passed[0m: Claude is preferred over an earlier installed provider           113ms
[32m✓ Passed[0m: First installed provider is default when claude is missing       318ms
[32m✓ Passed[0m: No installed providers shows message without menu                 77ms
[32m✓ Passed[0m: Launch known missing provider exits 1                             69ms

[1mRunning ./tests/bash/tmux_conf_portability_test.sh[0m
[32m✓ Passed[0m: Extended keys format is quiet on older tmux                       42ms

[1mRunning ./tests/bash/tmux_load_avg_test.sh[0m
[32m✓ Passed[0m: Render segment both metrics healthy                               67ms
[32m✓ Passed[0m: Render segment cpu only                                           63ms
[32m✓ Passed[0m: Render segment mem only                                           60ms
[32m✓ Passed[0m: Render segment neither is empty                                   55ms
[32m✓ Passed[0m: Render segment has no trailing newline                            81ms
[32m✓ Passed[0m: Render segment visible text strips to plain words                 60ms
[32m✓ Passed[0m: Render segment percent sign is always followed by markup or end   70ms
[32m✓ Passed[0m: Cpu threshold boundaries                                         128ms
[32m✓ Passed[0m: Mem threshold boundaries                                         111ms
[32m✓ Passed[0m: Render segment mixed healthy cpu and critical mem                 67ms
[32m✓ Passed[0m: Load 2556 on 64 cpus gives 40                                     65ms
[32m✓ Passed[0m: Load 420 on 8 cpus gives 53                                       68ms
[32m✓ Passed[0m: Comma decimal load is accepted via uptime parsing                 62ms
[32m✓ Passed[0m: Integer only load pads to two fraction digits                     63ms
[32m✓ Passed[0m: One digit fraction is right padded                                59ms
[32m✓ Passed[0m: Three digit fraction is truncated not rounded                     64ms
[32m✓ Passed[0m: Leading zeroes are not read as octal                              66ms
[32m✓ Passed[0m: Half up rounding of small load                                    62ms
[32m✓ Passed[0m: Cpu percent can exceed one hundred                                59ms
[32m✓ Passed[0m: Zero cpu count is unavailable                                     58ms
[32m✓ Passed[0m: Invalid cpu count is unavailable                                  62ms
[32m✓ Passed[0m: Overlong integer part is unavailable                              65ms
[32m✓ Passed[0m: Linux cpu list full range                                         68ms
[32m✓ Passed[0m: Linux cpu list single cpu                                         65ms
[32m✓ Passed[0m: Linux cpu list mixed ranges                                       67ms
[32m✓ Passed[0m: Linux cpu list singles and range                                  65ms
[32m✓ Passed[0m: Linux cpu list empty input fails                                  62ms
[32m✓ Passed[0m: Linux cpu list reversed range fails                               59ms
[32m✓ Passed[0m: Linux cpu list non digits fail                                    61ms
[32m✓ Passed[0m: Linux cpu list dangling hyphen fails                              60ms
[32m✓ Passed[0m: Linux cpu list dangling comma fails                               60ms
[32m✓ Passed[0m: Linux cpu list unreadable file fails quietly                      66ms
[32m✓ Passed[0m: Darwin dispatch invokes sysctl and vm stat once each             121ms
[32m✓ Passed[0m: Darwin sysctl failure yields empty and skips vm stat              96ms
[32m✓ Passed[0m: Darwin invalid cpu line renders mem only                          90ms
[32m✓ Passed[0m: Darwin zero cpu line renders mem only                             87ms
[32m✓ Passed[0m: Darwin invalid memsize renders cpu only with no vm stat call      94ms
[32m✓ Passed[0m: Darwin zero memsize renders cpu only with no vm stat call         91ms
[32m✓ Passed[0m: Darwin missing vm stat renders cpu only                           91ms
[32m✓ Passed[0m: Darwin failing vm stat renders cpu only                          100ms
[32m✓ Passed[0m: Darwin failing uptime renders mem only                            84ms
[32m✓ Passed[0m: Linux success reads uptime once                                   79ms
[32m✓ Passed[0m: Linux load failure still renders mem and exits zero with quiet... 77ms
[32m✓ Passed[0m: Linux missing cpu count renders mem only                          69ms
[32m✓ Passed[0m: Linux memory failure renders cpu only                             80ms
[32m✓ Passed[0m: Unsupported ostype renders nothing and logs no calls              60ms
[32m✓ Passed[0m: Help flag prints usage exits zero and logs no calls               74ms
[32m✓ Passed[0m: Unrecognized argument is rejected before metrics                  69ms
[32m✓ Passed[0m: Linux meminfo calculates total minus available                    69ms
[32m✓ Passed[0m: Linux meminfo treats leading zeroes as decimal                    61ms
[32m✓ Passed[0m: Linux meminfo uses available not free or cache totals             61ms
[32m✓ Passed[0m: Linux meminfo rounds half up                                      60ms
[32m✓ Passed[0m: Linux meminfo all available is zero percent                       63ms
[32m✓ Passed[0m: Linux meminfo none available is one hundred percent               60ms
[32m✓ Passed[0m: Linux meminfo accepts reordered fields and ignores unrelated f... 61ms
[32m✓ Passed[0m: Linux meminfo missing field fails quietly                         60ms
[32m✓ Passed[0m: Linux meminfo malformed field fails quietly                       60ms
[32m✓ Passed[0m: Linux meminfo unreadable input fails quietly                      62ms
[32m✓ Passed[0m: Linux meminfo zero total fails                                    61ms
[32m✓ Passed[0m: Linux meminfo available greater than total fails                  62ms
[32m✓ Passed[0m: Darwin vm stat uses counter formula with 4096 byte pages          62ms
[32m✓ Passed[0m: Darwin vm stat calculates captured mac snapshot                   65ms
[32m✓ Passed[0m: Darwin vm stat accepts old compressor label and zero counts       59ms
[32m✓ Passed[0m: Darwin vm stat missing required field fails                       63ms
[32m✓ Passed[0m: Darwin vm stat malformed value fails                              66ms
[32m✓ Passed[0m: Darwin vm stat bad page size fails                                68ms
[32m✓ Passed[0m: Darwin vm stat bad total fails                                    69ms
[32m✓ Passed[0m: Darwin vm stat purgeable greater than anonymous fails             65ms
[32m✓ Passed[0m: Darwin vm stat used bytes greater than physical ram fails         63ms

[1mRunning ./tests/bash/tmux_ping_test.sh[0m
[32m✓ Passed[0m: Contract fixtures parse as valid                                 130ms
[32m✓ Passed[0m: Empty results dash parses to empty window                        100ms
[32m✓ Passed[0m: Ninety nine sample state parses                                  115ms
[32m✓ Passed[0m: Invalid forms are rejected                                       212ms
[32m✓ Passed[0m: Append to empty window starts fresh                              119ms
[32m✓ Passed[0m: Append after long gap resets window                              102ms
[32m✓ Passed[0m: Append at exactly window seconds appends                         113ms
[32m✓ Passed[0m: Append trims to thirty samples                                   102ms
[32m✓ Passed[0m: Load window size fixture table                                   270ms
[32m✓ Passed[0m: Load window size missing key falls back                           96ms
[32m✓ Passed[0m: Summarize mixed window                                           119ms
[32m✓ Passed[0m: Classify tier boundaries                                         177ms
[32m✓ Passed[0m: Non darwin prints nothing and forks nothing                      113ms
[32m✓ Passed[0m: Help flag describes shared state role                            106ms
[32m✓ Passed[0m: Unrecognized argument is rejected                                110ms
[32m✓ Passed[0m: Fresh hammerspoon heartbeat renders without ping or flock        199ms
[32m✓ Passed[0m: Hammerspoon heartbeat at handoff age pings and claims tmux       175ms
[32m✓ Passed[0m: Tmux sample under interval skips ping                            184ms
[32m✓ Passed[0m: Tmux sample at interval pings                                    169ms
[32m✓ Passed[0m: Missing state pings into fresh window                            168ms
[32m✓ Passed[0m: Empty state pings into fresh window                              173ms
[32m✓ Passed[0m: Invalid states ping into fresh windows                           287ms
[32m✓ Passed[0m: Failing ping appends miss                                        168ms
[32m✓ Passed[0m: Busy lock renders without pinging                                175ms
[32m✓ Passed[0m: Missing flock pings unlocked                                     159ms
[32m✓ Passed[0m: Long gap resets window end to end                                155ms
[32m✓ Passed[0m: Gap edge appends end to end                                      148ms
[32m✓ Passed[0m: Full window drops oldest end to end                              156ms
[32m✓ Passed[0m: Configured twenty sample window end to end                       166ms
[32m✓ Passed[0m: Configured gap resets at forty one seconds                       151ms
[32m✓ Passed[0m: Larger state clamps to configured window                         155ms
[32m✓ Passed[0m: Config directory falls back quietly                              143ms
[32m✓ Passed[0m: Unreadable config falls back quietly                             159ms
[32m✓ Passed[0m: Online tier output                                               174ms
[32m✓ Passed[0m: Lossy tier output                                                146ms
[32m✓ Passed[0m: Down tier output                                                 141ms
[32m✓ Passed[0m: Offline tier output                                              153ms
[32m✓ Passed[0m: Stale tier output for paused hammerspoon                         172ms
[32m✓ Passed[0m: Stale tier output for empty window                               165ms
[32m✓ Passed[0m: Perfect window hides count end to end                            158ms
[32m✓ Passed[0m: Full window with miss keeps count end to end                     139ms
[32m✓ Passed[0m: Stale perfect window keeps count end to end                      153ms
[32m✓ Passed[0m: Render helper exact strings                                      212ms
[32m✓ Passed[0m: Written state matches contract and leaves no temp files          132ms

[1mRunning ./tests/bash/zshrc_portability_test.sh[0m
[32m✓ Passed[0m: Shared zshrc has no linux home references                         39ms
[32m✓ Passed[0m: Pyenv bin path is home relative and directory guarded             52ms
[32m✓ Passed[0m: Broot launcher is xdg relative and optional                       39ms
[32m✓ Passed[0m: Ssh agent bootstrap does not use pgrep or agent thing             37ms
[32m✓ Passed[0m: Ssh agent bootstrap uses stable socket                            36ms

[1mRunning ./tests/bash/zshrc_ssh_agent_test.sh[0m
[32m✓ Passed[0m: Live socket spawns nothing                                        76ms
[32m✓ Passed[0m: Empty agent spawns nothing                                        69ms
[32m✓ Passed[0m: Dead socket starts one agent and removes stale path               94ms
[32m✓ Passed[0m: User unset behaves like live socket                               76ms
[32m✓ Passed[0m: Foreign inherited sock is replaced                                67ms
[32m✓ Passed[0m: Sourcing twice is idempotent                                      81ms

[90mTests:     [0m [32m276 passed[0m, 276 total
[90mAssertions:[0m [32m909 passed[0m, 909 total

[42m[30m[1m All tests passed [0m
[1mTime taken: 48.59s[0m

---------- Running Python tests using pytest... ----------
cd home/lib/xfile && ../../../.venv/bin/pytest test
============================= test session starts ==============================
platform linux -- Python 3.14.7, pytest-9.1.1, pluggy-1.6.0 -- /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/chezmoi/.venv/bin/python
cachedir: .pytest_cache
rootdir: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/chezmoi
configfile: pyproject.toml
plugins: cov-7.1.0, asyncio-1.4.0
asyncio: mode=Mode.AUTO, debug=False, asyncio_default_fixture_loop_scope=function, asyncio_default_test_loop_scope=function
collecting ... collected 26 items

test/test_xfile_main.py::test_main_list_xfiles PASSED                    [  3%]
test/test_xfile_main.py::test_main_missing_xfiles_arg PASSED             [  7%]
test/test_xfile_main.py::test_main_nonexistent_xfile PASSED              [ 11%]
test/test_xfile_main.py::test_main_with_glob_pattern_in_xfile PASSED     [ 15%]
test/test_xfile_main.py::test_expand_braces_no_braces PASSED             [ 19%]
test/test_xfile_main.py::test_expand_braces_simple PASSED                [ 23%]
test/test_xfile_main.py::test_expand_braces_multiple_options PASSED      [ 26%]
test/test_xfile_main.py::test_format_output_path_relative PASSED         [ 30%]
test/test_xfile_main.py::test_format_output_path_absolute PASSED         [ 34%]
test/test_xfile_main.py::test_format_output_path_outside_cwd PASSED      [ 38%]
test/test_xfile_main.py::test_make_relative_to_home_inside_home PASSED   [ 42%]
test/test_xfile_main.py::test_make_relative_to_home_outside_home PASSED  [ 46%]
test/test_xfile_main.py::test_get_global_xfiles_dir PASSED               [ 50%]
test/test_xfile_main.py::test_get_local_xfiles_dir PASSED                [ 53%]
test/test_xfile_main.py::test_parse_xfile_metadata_with_header PASSED    [ 57%]
test/test_xfile_main.py::test_parse_xfile_metadata_without_header PASSED [ 61%]
test/test_xfile_main.py::test_parse_xfile_metadata_with_descriptions PASSED [ 65%]
test/test_xfile_main.py::test_format_xfile_with_custom_header PASSED     [ 69%]
test/test_xfile_main.py::test_format_xfile_with_single_file_description PASSED [ 73%]
test/test_xfile_main.py::test_format_xfile_with_group_description PASSED [ 76%]
test/test_xfile_main.py::test_format_xfile_with_xref_inherits_descriptions PASSED [ 80%]
test/test_xfile_main.py::test_format_xfile_with_xref_override_description PASSED [ 84%]
test/test_xfile_main.py::test_inline_target_single_file PASSED           [ 88%]
test/test_xfile_main.py::test_inline_target_command PASSED               [ 92%]
test/test_xfile_main.py::test_inline_target_multi_file_in_bullet PASSED  [ 96%]
test/test_xfile_main.py::test_inline_target_glob_in_bullet PASSED        [100%]

================================ tests coverage ================================
_______________ coverage: platform linux, python 3.14.7-final-0 ________________

Name            Stmts   Miss  Cover   Missing
---------------------------------------------
main.py            48      5    90%   105-111, 117, 129
rendering.py      157    147     6%   22-30, 35-110, 117-261
targets.py         97     24    75%   56-60, 64-68, 110-135, 159-161
utils.py           69     15    78%   22, 36-38, 64-74, 97, 105
xfile_refs.py     186     22    88%   28-29, 36-37, 56, 87, 135-136, 163-164, 179-181, 201, 230, 266-268, 290, 306, 316, 330-331
---------------------------------------------
TOTAL             867    213    75%

4 files skipped due to complete coverage.
Coverage HTML written to dir htmlcov
Required test coverage of 50% reached. Total coverage: 75.43%
============================== 26 passed in 0.17s ==============================
succeeded  exit=0  duration=68718ms

