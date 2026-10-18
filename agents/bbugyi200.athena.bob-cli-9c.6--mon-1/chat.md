# Chat History - ace-run (bob-cli-9c.6--mon-1)

- **TIMESTAMP:** 2026-10-18 16:45:34 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-9c.6--mon-1

## Prompt

sase monitor start --command 'ssh -o BatchMode=yes -o ConnectTimeout=15 -o ForwardX11=no apollo \'set -eu\nsrc=/tmp/chezmoi-v2.13.1\ntest ! -e "$src"\ngit clone --depth 1 --branch v2.13.1 https://github.com/twpayne/chezmoi.git "$src"\ncd "$src"\ngo install .\n/home/bryan/go/bin/chezmoi --version\n/home/bryan/go/bin/chezmoi update -a --force\'' --reason 'Build chezmoi v2.13.1 from its upstream main module on Apollo and apply the committed dotfiles source'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
Cloning into '/tmp/chezmoi-v2.13.1'...
Note: switching to 'e2e199bd48b9abb89e9a38fb2a5e42970e9267c4'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

go: downloading github.com/Masterminds/sprig/v3 v3.2.2
go: downloading github.com/go-git/go-git/v5 v5.4.2
go: downloading github.com/charmbracelet/glamour v0.5.0
go: downloading github.com/bradenhilton/mozillainstallhash v1.0.0
go: downloading github.com/coreos/go-semver v0.3.0
go: downloading github.com/google/go-github/v42 v42.0.0
go: downloading github.com/google/gops v0.3.22
go: downloading github.com/gregjones/httpcache v0.0.0-20190611155906-901d90724c79
go: downloading github.com/mitchellh/mapstructure v1.4.3
go: downloading github.com/rs/zerolog v1.26.1
go: downloading github.com/spf13/afero v1.8.1
go: downloading github.com/spf13/cobra v1.3.0
go: downloading github.com/spf13/viper v1.10.1
go: downloading github.com/twpayne/go-pinentry v0.2.0
go: downloading github.com/twpayne/go-shell v0.3.1
go: downloading github.com/twpayne/go-vfs/v4 v4.1.0
go: downloading github.com/twpayne/go-xdg/v6 v6.0.0
go: downloading github.com/zalando/go-keyring v0.2.0
go: downloading go.etcd.io/bbolt v1.3.6
go: downloading go.uber.org/multierr v1.8.0
go: downloading golang.org/x/sys v0.0.0-20220224120231-95c6836cb0e7
go: downloading golang.org/x/term v0.0.0-20210927222741-03fcf44c2211
go: downloading howett.net/plist v1.0.0
go: downloading github.com/peterbourgon/diskv v2.0.1+incompatible
go: downloading github.com/Masterminds/goutils v1.1.1
go: downloading github.com/Masterminds/semver/v3 v3.1.1
go: downloading github.com/google/uuid v1.3.0
go: downloading github.com/huandu/xstrings v1.3.2
go: downloading github.com/imdario/mergo v0.3.12
go: downloading github.com/mitchellh/copystructure v1.2.0
go: downloading github.com/shopspring/decimal v1.3.1
go: downloading github.com/spf13/cast v1.4.1
go: downloading golang.org/x/crypto v0.0.0-20220214200702-86341886e292
go: downloading github.com/bradenhilton/cityhash v1.0.0
go: downloading golang.org/x/text v0.3.7
go: downloading filippo.io/age v1.0.0
go: downloading github.com/bmatcuk/doublestar/v4 v4.0.2
go: downloading github.com/google/renameio/v2 v2.0.0
go: downloading github.com/pelletier/go-toml v1.9.4
go: downloading github.com/sergi/go-diff v1.1.0
go: downloading github.com/ulikunitz/xz v0.5.10
go: downloading golang.org/x/oauth2 v0.0.0-20220223155221-ee480838109b
go: downloading golang.org/x/sync v0.0.0-20210220032951-036812b2e83c
go: downloading github.com/google/renameio v0.1.0
go: downloading gopkg.in/yaml.v3 v3.0.0-20210107192922-496545a6307b
go: downloading github.com/fsnotify/fsnotify v1.5.1
go: downloading github.com/magiconair/properties v1.8.6
go: downloading github.com/spf13/jwalterweatherman v1.1.0
go: downloading github.com/spf13/pflag v1.0.5
go: downloading github.com/subosito/gotenv v1.2.0
go: downloading gopkg.in/ini.v1 v1.66.4
go: downloading github.com/godbus/dbus/v5 v5.0.6
go: downloading go.uber.org/atomic v1.9.0
go: downloading github.com/google/btree v1.0.1
go: downloading github.com/ProtonMail/go-crypto v0.0.0-20220113124808-70ae35bab23f
go: downloading github.com/go-git/go-billy/v5 v5.3.1
go: downloading github.com/muesli/termenv v0.11.0
go: downloading github.com/yuin/goldmark v1.4.7
go: downloading github.com/yuin/goldmark-emoji v1.0.1
go: downloading github.com/mitchellh/reflectwalk v1.0.2
go: downloading github.com/google/go-querystring v1.1.0
go: downloading github.com/hashicorp/hcl v1.0.0
go: downloading gopkg.in/yaml.v2 v2.4.0
go: downloading github.com/alecthomas/chroma v0.10.0
go: downloading github.com/microcosm-cc/bluemonday v1.0.18
go: downloading github.com/muesli/reflow v0.3.0
go: downloading github.com/olekukonko/tablewriter v0.0.5
go: downloading github.com/jbenet/go-context v0.0.0-20150711004518-d14ea06fba99
go: downloading github.com/mitchellh/go-homedir v1.1.0
go: downloading github.com/emirpasic/gods v1.12.0
go: downloading golang.org/x/net v0.0.0-20220225172249-27dd8689420f
go: downloading github.com/lucasb-eyer/go-colorful v1.2.0
go: downloading github.com/mattn/go-runewidth v0.0.13
go: downloading github.com/mattn/go-isatty v0.0.14
go: downloading github.com/go-git/gcfg v1.5.0
go: downloading github.com/kevinburke/ssh_config v1.1.0
go: downloading github.com/xanzy/ssh-agent v0.3.1
go: downloading github.com/rivo/uniseg v0.2.0
go: downloading github.com/aymerick/douceur v0.2.0
go: downloading gopkg.in/warnings.v0 v0.1.2
go: downloading github.com/gorilla/css v1.0.0
go: downloading github.com/dlclark/regexp2 v1.4.0
chezmoi version dev
From github.com:bbugyi200/dotfiles
   0765dd8e..9ee5fd2a  master     -> origin/master
Updating 0765dd8e..9ee5fd2a
Fast-forward
 home/.chezmoiignore                                |   4 +
 home/.chezmoiremove                                |   1 +
 ...hange_after_enable_bob_ref_intake_timer.sh.tmpl |   9 +
 home/bin/executable_bob_xlib_pull                  | 282 -------
 home/bin/executable_maybe_bob_highlights_sync      |  47 +-
 home/dot_config/bob/config.yml                     |   2 +-
 .../dot_config/systemd/user/bob-ref-intake.service |  12 +
 home/dot_config/systemd/user/bob-ref-intake.timer  |  11 +
 tests/bash/bob_xlib_pull_test.sh                   | 933 ---------------------
 tests/bash/maybe_bob_highlights_sync_test.sh       | 100 +++
 10 files changed, 165 insertions(+), 1236 deletions(-)
 create mode 100644 home/.chezmoiscripts/run_onchange_after_enable_bob_ref_intake_timer.sh.tmpl
 delete mode 100755 home/bin/executable_bob_xlib_pull
 create mode 100644 home/dot_config/systemd/user/bob-ref-intake.service
 create mode 100644 home/dot_config/systemd/user/bob-ref-intake.timer
 delete mode 100644 tests/bash/bob_xlib_pull_test.sh
 create mode 100644 tests/bash/maybe_bob_highlights_sync_test.sh

[38;5;5m>>> BUILD REPO EXISTS: /home/bryan/tmp/chezmoi_build/neovim. CHECKING OUT master BRANCH.[0m
Already on 'master'
Your branch is up to date with 'origin/master'.

[38;5;5m>>> UPDATING NEOVIM REPO.[0m
From https://github.com/neovim/neovim
   9b7ec59580..74eef1490b  master     -> origin/master
 + 080c248fa4...1f97db1a26 marvim/ci-version-update -> origin/marvim/ci-version-update  (forced update)
Updating 9b7ec59580..74eef1490b
Fast-forward
 runtime/doc/api-ui-events.txt                  |   4 +-
 runtime/doc/api.txt                            |  75 ++--
 runtime/doc/autocmd.txt                        | 553 +++++++++++++------------
 runtime/doc/change.txt                         | 412 +++++++++---------
 runtime/doc/channel.txt                        |   9 +-
 runtime/doc/cmdline.txt                        |  67 +--
 runtime/doc/credits.txt                        |   2 +-
 runtime/doc/deprecated.txt                     |   6 +-
 runtime/doc/dev.txt                            |   1 +
 runtime/doc/dev_arch.txt                       |   3 +-
 runtime/doc/dev_style.txt                      |   1 +
 runtime/doc/dev_test.txt                       |   1 +
 runtime/doc/dev_theme.txt                      |   1 +
 runtime/doc/dev_tools.txt                      |   1 +
 runtime/doc/dev_vimpatch.txt                   |   1 +
 runtime/doc/diagnostic.txt                     |  30 +-
 runtime/doc/diff.txt                           |  30 +-
 runtime/doc/digraph.txt                        |  13 +-
 runtime/doc/editing.txt                        | 245 +++++------
 runtime/doc/faq.txt                            |   1 +
 runtime/doc/filetype.txt                       |   1 +
 runtime/doc/fold.txt                           | 105 +++--
 runtime/doc/ft_ada.txt                         | 120 ++----
 runtime/doc/ft_hare.txt                        |   2 +-
 runtime/doc/ft_ps1.txt                         |   3 +
 runtime/doc/ft_raku.txt                        |   3 +-
 runtime/doc/ft_rust.txt                        |   2 +-
 runtime/doc/ft_sql.txt                         |   3 +
 runtime/doc/gui.txt                            |  13 +-
 runtime/doc/helphelp.txt                       |  61 +--
 runtime/doc/if_perl.txt                        |  68 ++-
 runtime/doc/if_pyth.txt                        |  20 +-
 runtime/doc/if_ruby.txt                        |  21 +-
 runtime/doc/indent.txt                         |   3 +
 runtime/doc/index.txt                          |   4 +-
 runtime/doc/insert.txt                         | 187 +++++----
 runtime/doc/intro.txt                          | 139 +++----
 runtime/doc/job_control.txt                    |   1 +
 runtime/doc/l10n-arabic.txt                    |   5 +-
 runtime/doc/l10n-hebrew.txt                    |   1 +
 runtime/doc/l10n-russian.txt                   |   1 +
 runtime/doc/l10n-vietnamese.txt                |   3 +
 runtime/doc/lsp.txt                            | 122 ++----
 runtime/doc/lua-async.txt                      |  11 +-
 runtime/doc/lua-bit.txt                        |   1 +
 runtime/doc/lua-guide.txt                      |   3 +-
 runtime/doc/lua-plugin.txt                     |   3 +-
 runtime/doc/lua.txt                            |  60 ++-
 runtime/doc/luaref.txt                         |   5 +-
 runtime/doc/luvref.txt                         |   4 +-
 runtime/doc/map.txt                            |  50 +--
 runtime/doc/mbyte.txt                          |   1 +
 runtime/doc/message.txt                        |   3 +
 runtime/doc/mlang.txt                          |   7 +-
 runtime/doc/motion.txt                         | 523 ++++++++++++-----------
 runtime/doc/news-0.10.txt                      |   1 +
 runtime/doc/news-0.11.txt                      |   1 +
 runtime/doc/news-0.12.txt                      |   1 +
 runtime/doc/news-0.9.txt                       |   1 +
 runtime/doc/news.txt                           |   7 +-
 runtime/doc/nvim.txt                           |   1 +
 runtime/doc/options.txt                        |  49 ++-
 runtime/doc/pack.txt                           |  66 ++-
 runtime/doc/pattern.txt                        | 172 ++++----
 runtime/doc/pi_gzip.txt                        |   1 +
 runtime/doc/pi_msgpack.txt                     |   3 +
 runtime/doc/pi_paren.txt                       |   1 +
 runtime/doc/pi_spec.txt                        |   3 +
 runtime/doc/pi_tar.txt                         |   5 +-
 runtime/doc/pi_tutor.txt                       |   4 +-
 runtime/doc/plugins.txt                        |  26 +-
 runtime/doc/provider.txt                       |   1 +
 runtime/doc/quickfix.txt                       | 332 ++++++++-------
 runtime/doc/recover.txt                        |  16 +-
 runtime/doc/remote.txt                         |   1 +
 runtime/doc/remote_plugin.txt                  |   1 +
 runtime/doc/repeat.txt                         |  81 ++--
 runtime/doc/rileft.txt                         |   4 +-
 runtime/doc/scroll.txt                         | 103 ++---
 runtime/doc/sign.txt                           |   7 +-
 runtime/doc/spell.txt                          |  75 ++--
 runtime/doc/starting.txt                       |  55 +--
 runtime/doc/support.txt                        |   1 +
 runtime/doc/syntax.txt                         |  25 +-
 runtime/doc/tabpage.txt                        |  49 ++-
 runtime/doc/tagsrch.txt                        | 230 +++++-----
 runtime/doc/terminal.txt                       |   1 +
 runtime/doc/tips.txt                           |   1 +
 runtime/doc/treesitter.txt                     | 288 ++++++-------
 runtime/doc/tui.txt                            |   1 +
 runtime/doc/uganda.txt                         |   3 +
 runtime/doc/undo.txt                           |  42 +-
 runtime/doc/userfunc.txt                       |  13 +-
 runtime/doc/usr_01.txt                         |   3 +-
 runtime/doc/usr_02.txt                         |   3 +-
 runtime/doc/usr_03.txt                         |   3 +-
 runtime/doc/usr_04.txt                         |   3 +-
 runtime/doc/usr_05.txt                         |   3 +-
 runtime/doc/usr_06.txt                         |   3 +-
 runtime/doc/usr_07.txt                         |   3 +-
 runtime/doc/usr_08.txt                         |   3 +-
 runtime/doc/usr_09.txt                         |   3 +-
 runtime/doc/usr_10.txt                         |   3 +-
 runtime/doc/usr_11.txt                         |   3 +-
 runtime/doc/usr_12.txt                         |   3 +-
 runtime/doc/usr_20.txt                         |   3 +-
 runtime/doc/usr_21.txt                         |   3 +-
 runtime/doc/usr_22.txt                         |   6 +-
 runtime/doc/usr_23.txt                         |   3 +-
 runtime/doc/usr_24.txt                         |   3 +-
 runtime/doc/usr_25.txt                         |   3 +-
 runtime/doc/usr_26.txt                         |   3 +-
 runtime/doc/usr_27.txt                         |   3 +-
 runtime/doc/usr_28.txt                         |   3 +-
 runtime/doc/usr_29.txt                         |   3 +-
 runtime/doc/usr_30.txt                         |   3 +-
 runtime/doc/usr_31.txt                         |   3 +-
 runtime/doc/usr_32.txt                         |   3 +-
 runtime/doc/usr_40.txt                         |   3 +-
 runtime/doc/usr_41.txt                         |   3 +-
 runtime/doc/usr_42.txt                         |   3 +-
 runtime/doc/usr_43.txt                         |   3 +-
 runtime/doc/usr_44.txt                         |   3 +-
 runtime/doc/usr_45.txt                         |   3 +-
 runtime/doc/usr_toc.txt                        |   3 +-
 runtime/doc/various.txt                        | 217 +++++-----
 runtime/doc/vi_diff.txt                        |   1 +
 runtime/doc/vim_diff.txt                       |   2 +-
 runtime/doc/vimeval.txt                        | 102 ++---
 runtime/doc/vimfn.txt                          |  21 +-
 runtime/doc/vimscript.txt                      |  31 +-
 runtime/doc/visual.txt                         |  53 +--
 runtime/doc/vvars.txt                          | 309 +++++---------
 runtime/doc/windows.txt                        | 261 ++++++------
 runtime/doc/zip.txt                            |   3 +-
 runtime/lua/nvim/dir.lua                       |   2 +-
 runtime/lua/vim/_meta/options.gen.lua          |   2 +-
 runtime/lua/vim/log.lua                        |   8 +-
 runtime/lua/vim/net.lua                        |   5 +-
 runtime/lua/vim/pack.lua                       |  29 +-
 runtime/lua/vim/pack/health.lua                | 132 ++++--
 runtime/lua/vim/tty.lua                        |   8 +-
 runtime/org.neovim.nvim.desktop                |   2 +-
 runtime/plugin/dir.lua                         |   4 -
 src/gen/gen_eval_files.lua                     |  59 +--
 src/gen/gen_help_html.lua                      | 463 +++++----------------
 src/gen/gen_vimdoc.lua                         |  35 +-
 src/nvim/bufwrite.c                            |  64 ++-
 src/nvim/change.c                              |   4 +
 src/nvim/dialog.c                              |   1 +
 src/nvim/fileio.c                              |  11 +-
 src/nvim/indent.c                              |   4 +-
 src/nvim/insexpand.c                           |  12 +-
 src/nvim/message.c                             |  26 +-
 src/nvim/options.lua                           |   2 +-
 src/nvim/version.c                             |  36 +-
 test/functional/api/ui_spec.lua                |   9 +
 test/functional/editor/completion_spec.lua     |  22 +-
 test/functional/lua/log_spec.lua               |   8 +-
 test/functional/lua/net_spec.lua               |  13 +-
 test/functional/plugin/dir_spec.lua            |  55 ++-
 test/functional/plugin/lsp/completion_spec.lua |   9 +-
 test/functional/terminal/tui_spec.lua          |  10 +
 test/functional/ui/messages2_spec.lua          |  10 +-
 test/functional/ui/messages_spec.lua           |  96 +++--
 test/old/testdir/test_visual.vim               |   4 +-
 166 files changed, 3406 insertions(+), 3525 deletions(-)

[38;5;5m>>> NEOVIM VERSION UPDATE:  NONE -> v0.12.6[0m
Note: switching to 'v0.12.6'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 779c36969e NVIM v0.12.6
mkdir -p ".deps"
/usr/bin/cmake -S /home/bryan/tmp/chezmoi_build/neovim//cmake.deps -B ".deps" -G "Unix Makefiles" 
-- Found GNU Make at /usr/bin/gmake
-- CMAKE_BUILD_TYPE=Release
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bryan/tmp/chezmoi_build/neovim/.deps
mkdir -p build
touch "build/.ran-deps-cmake"
/usr/bin/cmake --build ".deps"
gmake[1]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[2]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 13%] Built target treesitter_markdown
[ 14%] Built target treesitter_lua
[ 21%] Built target treesitter
[ 41%] Built target unibilium
[ 43%] Built target treesitter_query
[ 43%] Built target treesitter_c
[ 53%] Built target luajit
[ 59%] Built target libuv
[ 71%] Built target treesitter_vim
[ 71%] Built target lua_compat53
[ 79%] Built target utf8proc
[ 86%] Built target treesitter_vimdoc
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 96%] Built target lpeg
[100%] Built target luv
gmake[2]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[1]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
/usr/bin/cmake --build build
gmake[1]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
-- Found GNU Make at /usr/bin/gmake
-- CMAKE_INSTALL_PREFIX=/home/bryan/.local
-- CMAKE_BUILD_TYPE=Release
-- Using Lua interpreter: /home/bryan/tmp/chezmoi_build/neovim/.deps/usr/bin/luajit
-- Using Lua interpreter for code generation: /home/bryan/tmp/chezmoi_build/neovim/.deps/usr/bin/luajit
-- main_lib props '/home/bryan/tmp/chezmoi_build/neovim/.deps/usr/include/luajit-2.1;/home/bryan/tmp/chezmoi_build/neovim/.deps/usr/include;/home/bryan/tmp/chezmoi_build/neovim/build/src/nvim/auto;/home/bryan/tmp/chezmoi_build/neovim/build/include;/home/bryan/tmp/chezmoi_build/neovim/build/cmake.config;/home/bryan/tmp/chezmoi_build/neovim/src'
-- nlua0 props '/home/bryan/tmp/chezmoi_build/neovim/.deps/usr/include/luajit-2.1;/home/bryan/tmp/chezmoi_build/neovim/src;/home/bryan/tmp/chezmoi_build/neovim/build/cmake.config;/home/bryan/tmp/chezmoi_build/neovim/build/include'
-- iconv props '/usr/include'
-- libuv props '/home/bryan/tmp/chezmoi_build/neovim/.deps/usr/include'
-- treesitter props '/home/bryan/tmp/chezmoi_build/neovim/.deps/usr/include'
-- utf8proc props '/home/bryan/tmp/chezmoi_build/neovim/.deps/usr/include'
-- libintl props '/usr/include'
-- unibilium props '/home/bryan/tmp/chezmoi_build/neovim/.deps/usr/include'
-- Configuring done (2.9s)
-- Generating done (0.6s)
-- Build files have been written to: /home/bryan/tmp/chezmoi_build/neovim/build
gmake[2]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  0%] Building C object src/tee/CMakeFiles/tee.dir/tee.c.o
[  0%] Building C object src/nvim/CMakeFiles/nlua0.dir/__/mpack/conv.c.o
[  0%] Building C object src/nvim/CMakeFiles/nlua0.dir/__/mpack/mpack_core.c.o
[  4%] Built target xxd
[  4%] Building C object src/nvim/CMakeFiles/nlua0.dir/__/mpack/object.c.o
[  4%] Building C object src/nvim/CMakeFiles/nlua0.dir/__/mpack/lmpack.c.o
[  4%] Building C object src/nvim/CMakeFiles/nlua0.dir/__/mpack/rpc.c.o
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  4%] Built target nvim_runtime_deps
[  4%] Linking C executable ../../bin/tee
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  4%] Built target tee
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  4%] Built target update_version_stamp
[  4%] Linking C shared module ../../lib/libnlua0.so
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  4%] Built target nlua0
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  4%] Generating auto/api/extmark.c.generated.h, ../../include/api/extmark.h.generated.h
[  4%] Generating auto/api/tabpage.c.generated.h, ../../include/api/tabpage.h.generated.h
[  4%] Generating auto/api/deprecated.c.generated.h, ../../include/api/deprecated.h.generated.h
[  9%] Generating auto/api/ui.c.generated.h, ../../include/api/ui.h.generated.h
[  9%] Generating auto/api/events.c.generated.h, ../../include/api/events.h.generated.h
[  4%] Generating auto/api/options.c.generated.h, ../../include/api/options.h.generated.h
[  9%] Generating auto/api/command.c.generated.h, ../../include/api/command.h.generated.h
[  9%] Generating auto/ui_events_call.generated.h, auto/ui_events_remote.generated.h, ../../ui_metadata.mpack, auto/ui_events_client.generated.h
[  9%] Generating auto/api/vim.c.generated.h, ../../include/api/vim.h.generated.h
[  9%] Generating auto/api/buffer.c.generated.h, ../../include/api/buffer.h.generated.h
[  9%] Generating auto/api/autocmd.c.generated.h, ../../include/api/autocmd.h.generated.h
[  9%] Generating ../../include/api/events.h.inline.generated.h
[  9%] Generating ../../include/api/autocmd.h.inline.generated.h
[  9%] Generating ../../include/api/deprecated.h.inline.generated.h
[  9%] Generating auto/api/window.c.generated.h, ../../include/api/window.h.generated.h
[  9%] Generating ../../include/api/command.h.inline.generated.h
[  9%] Generating auto/api/vimscript.c.generated.h, ../../include/api/vimscript.h.generated.h
[  9%] Generating ../../include/api/extmark.h.inline.generated.h
[  9%] Generating auto/api/win_config.c.generated.h, ../../include/api/win_config.h.generated.h
[  9%] Generating ../../include/api/buffer.h.inline.generated.h
[  9%] Generating ../../include/api/options.h.inline.generated.h
[  9%] Generating ../../include/api/private/converter.h.inline.generated.h
[  9%] Generating ../../include/api/keysets_defs.h.inline.generated.h
[  9%] Generating ../../include/api/private/defs.h.inline.generated.h
[  9%] Generating auto/api/private/helpers.c.generated.h, ../../include/api/private/helpers.h.generated.h
[  9%] Generating auto/api/private/dispatch.c.generated.h, ../../include/api/private/dispatch.h.generated.h
[  9%] Generating ../../include/api/private/dispatch.h.inline.generated.h
[  9%] Generating auto/api/private/converter.c.generated.h, ../../include/api/private/converter.h.generated.h
[  9%] Generating ../../include/api/private/helpers.h.inline.generated.h
[  9%] Generating ../../include/api/private/validate.h.inline.generated.h
[  9%] Generating auto/api/private/validate.c.generated.h, ../../include/api/private/validate.h.generated.h
[  9%] Generating ../../include/api/ui_events.h.inline.generated.h
[  9%] Generating ../../include/api/vim.h.inline.generated.h
[  9%] Generating ../../include/api/tabpage.h.inline.generated.h
[  9%] Generating ../../include/api/vimscript.h.inline.generated.h
[  9%] Generating ../../include/api/ui.h.inline.generated.h
[  9%] Generating ../../include/api/window.h.inline.generated.h
[  9%] Generating ../../include/api/win_config.h.inline.generated.h
[  9%] Generating ../../include/ascii_defs.h.inline.generated.h
[  9%] Generating auto/arabic.c.generated.h, ../../include/arabic.h.generated.h
[  9%] Generating ../../include/arabic.h.inline.generated.h
[  9%] Generating ../../include/arglist.h.inline.generated.h
[  9%] Generating ../../include/arglist_defs.h.inline.generated.h
[  9%] Generating ../../include/autocmd_defs.h.inline.generated.h
[  9%] Generating ../../include/buffer.h.inline.generated.h
[  9%] Generating ../../include/auevents_enum.generated.h, auto/auevents_name_map.generated.h
[  9%] Generating auto/autocmd.c.generated.h, ../../include/autocmd.h.generated.h
[ 14%] Generating ../../include/buffer_updates.h.inline.generated.h
[ 14%] Generating ../../include/assert_defs.h.inline.generated.h
[ 14%] Generating auto/base64.c.generated.h, ../../include/base64.h.generated.h
[ 14%] Generating ../../include/buffer_defs.h.inline.generated.h
[ 14%] Generating ../../include/autocmd.h.inline.generated.h
[ 14%] Generating auto/buffer_updates.c.generated.h, ../../include/buffer_updates.h.generated.h
[ 14%] Generating auto/arglist.c.generated.h, ../../include/arglist.h.generated.h
[ 14%] Generating auto/buffer.c.generated.h, ../../include/buffer.h.generated.h
[ 14%] Generating ../../include/base64.h.inline.generated.h
[ 14%] Generating auto/bufwrite.c.generated.h, ../../include/bufwrite.h.generated.h
[ 14%] Generating auto/change.c.generated.h, ../../include/change.h.generated.h
[ 14%] Generating ../../include/bufwrite.h.inline.generated.h
[ 14%] Generating ../../include/change.h.inline.generated.h
[ 14%] Generating ../../include/charset.h.inline.generated.h
[ 14%] Generating auto/channel.c.generated.h, ../../include/channel.h.generated.h
[ 14%] Generating ../../include/channel.h.inline.generated.h
[ 14%] Generating auto/clipboard.c.generated.h, ../../include/clipboard.h.generated.h
[ 14%] Generating auto/cmdhist.c.generated.h, ../../include/cmdhist.h.generated.h
[ 14%] Generating ../../include/cmdexpand_defs.h.inline.generated.h
[ 14%] Generating ../../include/cmdexpand.h.inline.generated.h
[ 14%] Generating ../../include/clipboard.h.inline.generated.h
[ 14%] Generating ../../include/context.h.inline.generated.h
[ 14%] Generating ../../include/cursor_shape.h.inline.generated.h
[ 14%] Generating auto/cmdexpand.c.generated.h, ../../include/cmdexpand.h.generated.h
[ 14%] Generating auto/cursor.c.generated.h, ../../include/cursor.h.generated.h
[ 14%] Generating ../../include/channel_defs.h.inline.generated.h
[ 14%] Generating auto/context.c.generated.h, ../../include/context.h.generated.h
[ 14%] Generating auto/cursor_shape.c.generated.h, ../../include/cursor_shape.h.generated.h
[ 14%] Generating ../../include/cmdhist.h.inline.generated.h
[ 14%] Generating ../../include/debugger.h.inline.generated.h
[ 14%] Generating auto/debugger.c.generated.h, ../../include/debugger.h.generated.h
[ 14%] Generating auto/decoration_provider.c.generated.h, ../../include/decoration_provider.h.generated.h
[ 14%] Generating ../../include/cursor.h.inline.generated.h
[ 14%] Generating ../../include/decoration_defs.h.inline.generated.h
[ 14%] Generating auto/charset.c.generated.h, ../../include/charset.h.generated.h
[ 14%] Generating ../../include/decoration_provider.h.inline.generated.h
[ 14%] Generating ../../include/diff.h.inline.generated.h
[ 14%] Generating auto/diff.c.generated.h, ../../include/diff.h.generated.h
[ 14%] Generating auto/digraph.c.generated.h, ../../include/digraph.h.generated.h
[ 14%] Generating auto/decoration.c.generated.h, ../../include/decoration.h.generated.h
[ 14%] Generating ../../include/drawline.h.inline.generated.h
[ 14%] Generating ../../include/drawscreen.h.inline.generated.h
[ 14%] Generating ../../include/decoration.h.inline.generated.h
[ 14%] Generating auto/eval.c.generated.h, ../../include/eval.h.generated.h
[ 14%] Generating auto/edit.c.generated.h, ../../include/edit.h.generated.h
[ 14%] Generating ../../include/errors.h.inline.generated.h
[ 14%] Generating ../../include/eval.h.inline.generated.h
[ 14%] Generating auto/eval/decode.c.generated.h, ../../include/eval/decode.h.generated.h
[ 14%] Generating auto/drawscreen.c.generated.h, ../../include/drawscreen.h.generated.h
[ 14%] Generating ../../include/digraph.h.inline.generated.h
[ 14%] Generating ../../include/edit.h.inline.generated.h
[ 14%] Generating auto/eval/buffer.c.generated.h, ../../include/eval/buffer.h.generated.h
[ 14%] Generating auto/drawline.c.generated.h, ../../include/drawline.h.generated.h
[ 14%] Generating auto/eval/encode.c.generated.h, ../../include/eval/encode.h.generated.h
[ 14%] Generating ../../include/eval/decode.h.inline.generated.h
[ 14%] Generating ../../include/eval/buffer.h.inline.generated.h
[ 14%] Generating ../../include/eval/deprecated.h.inline.generated.h
[ 19%] Generating auto/eval/executor.c.generated.h, ../../include/eval/executor.h.generated.h
[ 19%] Generating ../../include/eval/encode.h.inline.generated.h
[ 19%] Generating ../../include/eval/executor.h.inline.generated.h
[ 19%] Generating auto/eval/fs.c.generated.h, ../../include/eval/fs.h.generated.h
[ 19%] Generating ../../include/eval/funcs.h.inline.generated.h
[ 19%] Generating auto/eval/funcs.c.generated.h, ../../include/eval/funcs.h.generated.h
[ 19%] Generating auto/eval/gc.c.generated.h, ../../include/eval/gc.h.generated.h
[ 19%] Generating ../../include/eval/typval.h.inline.generated.h
[ 19%] Generating auto/eval/deprecated.c.generated.h, ../../include/eval/deprecated.h.generated.h
[ 19%] Generating ../../include/eval/fs.h.inline.generated.h
[ 19%] Generating auto/eval/typval.c.generated.h, ../../include/eval/typval.h.generated.h
[ 23%] Generating ../../include/eval/typval_defs.h.inline.generated.h
[ 23%] Generating auto/eval/vars.c.generated.h, ../../include/eval/vars.h.generated.h
[ 23%] Generating ../../include/eval/list.h.inline.generated.h
[ 23%] Generating ../../include/eval/userfunc.h.inline.generated.h
[ 23%] Generating auto/eval/userfunc.c.generated.h, ../../include/eval/userfunc.h.generated.h
[ 23%] Generating ../../include/eval/vars.h.inline.generated.h
[ 23%] Generating ../../include/event/libuv_proc.h.inline.generated.h
[ 23%] Generating auto/event/multiqueue.c.generated.h, ../../include/event/multiqueue.h.generated.h
[ 23%] Generating auto/eval/window.c.generated.h, ../../include/eval/window.h.generated.h
[ 23%] Generating ../../include/event/multiqueue.h.inline.generated.h
[ 23%] Generating ../../include/eval/window.h.inline.generated.h
[ 23%] Generating ../../include/event/loop.h.inline.generated.h
[ 23%] Generating ../../include/eval_defs.h.inline.generated.h
[ 23%] Generating ../../include/event/defs.h.inline.generated.h
[ 23%] Generating auto/event/proc.c.generated.h, ../../include/event/proc.h.generated.h
[ 23%] Generating ../../include/eval/typval_encode.h.inline.generated.h
[ 23%] Generating auto/event/libuv_proc.c.generated.h, ../../include/event/libuv_proc.h.generated.h
[ 23%] Generating ../../include/eval/gc.h.inline.generated.h
[ 23%] Generating auto/event/loop.c.generated.h, ../../include/event/loop.h.generated.h
[ 23%] Generating ../../include/event/proc.h.inline.generated.h
[ 23%] Generating auto/eval/list.c.generated.h, ../../include/eval/list.h.generated.h
[ 23%] Generating auto/event/rstream.c.generated.h, ../../include/event/rstream.h.generated.h
[ 23%] Generating ../../include/event/rstream.h.inline.generated.h
[ 23%] Generating ../../include/event/signal.h.inline.generated.h
[ 23%] Generating ../../include/event/socket.h.inline.generated.h
[ 23%] Generating auto/event/socket.c.generated.h, ../../include/event/socket.h.generated.h
[ 23%] Generating auto/event/signal.c.generated.h, ../../include/event/signal.h.generated.h
[ 23%] Generating auto/event/stream.c.generated.h, ../../include/event/stream.h.generated.h
[ 23%] Generating ../../include/event/stream.h.inline.generated.h
[ 23%] Generating auto/event/time.c.generated.h, ../../include/event/time.h.generated.h
[ 23%] Generating auto/ex_cmds.c.generated.h, ../../include/ex_cmds.h.generated.h
[ 23%] Generating ../../include/ex_cmds.h.inline.generated.h
[ 23%] Generating auto/ex_cmds2.c.generated.h, ../../include/ex_cmds2.h.generated.h
[ 23%] Generating ../../include/event/time.h.inline.generated.h
[ 23%] Generating ../../include/event/wstream.h.inline.generated.h
[ 23%] Generating auto/event/wstream.c.generated.h, ../../include/event/wstream.h.generated.h
[ 23%] Generating ../../include/ex_docmd.h.inline.generated.h
[ 23%] Generating auto/ex_docmd.c.generated.h, ../../include/ex_docmd.h.generated.h
[ 23%] Generating ../../include/ex_cmds2.h.inline.generated.h
[ 23%] Generating ../../include/ex_cmds_defs.h.inline.generated.h
[ 23%] Generating ../../include/ex_cmds_enum.generated.h, auto/ex_cmds_defs.generated.h
[ 23%] Generating auto/ex_eval.c.generated.h, ../../include/ex_eval.h.generated.h
[ 23%] Generating auto/ex_getln.c.generated.h, ../../include/ex_getln.h.generated.h
[ 23%] Generating ../../include/ex_getln_defs.h.inline.generated.h
[ 23%] Generating ../../include/ex_getln.h.inline.generated.h
[ 23%] Generating ../../include/ex_eval_defs.h.inline.generated.h
[ 23%] Generating auto/ex_session.c.generated.h, ../../include/ex_session.h.generated.h
[ 23%] Generating ../../include/ex_eval.h.inline.generated.h
[ 23%] Generating ../../include/fileio.h.inline.generated.h
[ 23%] Generating ../../include/extmark.h.inline.generated.h
[ 23%] Generating auto/file_search.c.generated.h, ../../include/file_search.h.generated.h
[ 23%] Generating auto/fileio.c.generated.h, ../../include/fileio.h.generated.h
[ 23%] Generating ../../include/ex_session.h.inline.generated.h
[ 23%] Generating ../../include/extmark_defs.h.inline.generated.h
[ 23%] Generating auto/extmark.c.generated.h, ../../include/extmark.h.generated.h
[ 23%] Generating ../../include/file_search.h.inline.generated.h
[ 23%] Generating ../../include/fold.h.inline.generated.h
[ 23%] Generating ../../include/func_attr.h.inline.generated.h
[ 23%] Generating ../../include/fuzzy.h.inline.generated.h
[ 23%] Generating auto/fold.c.generated.h, ../../include/fold.h.generated.h
[ 23%] Generating ../../include/fold_defs.h.inline.generated.h
[ 28%] Generating ../../include/garray.h.inline.generated.h
[ 28%] Generating ../../include/garray_defs.h.inline.generated.h
[ 28%] Generating auto/garray.c.generated.h, ../../include/garray.h.generated.h
[ 28%] Generating auto/fuzzy.c.generated.h, ../../include/fuzzy.h.generated.h
[ 28%] Generating auto/getchar.c.generated.h, ../../include/getchar.h.generated.h
[ 28%] Generating ../../include/getchar_defs.h.inline.generated.h
[ 28%] Generating ../../include/getchar.h.inline.generated.h
[ 28%] Generating ../../include/globals.h.inline.generated.h
[ 28%] Generating ../../include/gettext_defs.h.inline.generated.h
[ 28%] Generating ../../include/grid_defs.h.inline.generated.h
[ 28%] Generating auto/hashtab.c.generated.h, ../../include/hashtab.h.generated.h
[ 28%] Generating auto/grid.c.generated.h, ../../include/grid.h.generated.h
[ 33%] Generating auto/help.c.generated.h, ../../include/help.h.generated.h
[ 33%] Generating ../../include/hashtab.h.inline.generated.h
[ 33%] Generating ../../include/hashtab_defs.h.inline.generated.h
[ 33%] Generating ../../include/help.h.inline.generated.h
[ 33%] Generating ../../include/grid.h.inline.generated.h
[ 33%] Generating auto/highlight_group.c.generated.h, ../../include/highlight_group.h.generated.h
[ 33%] Generating ../../include/highlight.h.inline.generated.h
[ 33%] Generating auto/highlight.c.generated.h, ../../include/highlight.h.generated.h
[ 33%] Generating ../../include/highlight_group.h.inline.generated.h
[ 33%] Generating ../../include/highlight_defs.h.inline.generated.h
[ 33%] Generating auto/indent.c.generated.h, ../../include/indent.h.generated.h
[ 33%] Generating ../../include/iconv_defs.h.inline.generated.h
[ 33%] Generating ../../include/indent.h.inline.generated.h
[ 33%] Generating auto/indent_c.c.generated.h, ../../include/indent_c.h.generated.h
[ 33%] Generating ../../include/insexpand.h.inline.generated.h
[ 33%] Generating ../../include/indent_c.h.inline.generated.h
[ 33%] Generating auto/input.c.generated.h, ../../include/input.h.generated.h
[ 33%] Generating auto/insexpand.c.generated.h, ../../include/insexpand.h.generated.h
[ 33%] Generating ../../include/input.h.inline.generated.h
[ 33%] Generating auto/keycodes.c.generated.h, ../../include/keycodes.h.generated.h
[ 33%] Generating ../../include/keycodes.h.inline.generated.h
[ 33%] Generating ../../include/lib/queue_defs.h.inline.generated.h
[ 33%] Generating auto/lua/api_wrappers.c.generated.h, ../../include/lua/api_wrappers.h.generated.h
[ 33%] Generating auto/lua/converter.c.generated.h, ../../include/lua/converter.h.generated.h
[ 33%] Generating auto/linematch.c.generated.h, ../../include/linematch.h.generated.h
[ 33%] Generating ../../include/log.h.inline.generated.h
[ 33%] Generating auto/lua/executor.c.generated.h, ../../include/lua/executor.h.generated.h
[ 33%] Generating auto/lua/spell.c.generated.h, ../../include/lua/spell.h.generated.h
[ 33%] Generating ../../include/lua/spell.h.inline.generated.h
[ 33%] Generating ../../include/lua/secure.h.inline.generated.h
[ 33%] Generating auto/lua/secure.c.generated.h, ../../include/lua/secure.h.generated.h
[ 33%] Generating ../../include/lua/executor.h.inline.generated.h
[ 33%] Generating ../../include/lua/stdlib.h.inline.generated.h
[ 33%] Generating auto/lua/stdlib.c.generated.h, ../../include/lua/stdlib.h.generated.h
[ 33%] Generating ../../include/lua/base64.h.inline.generated.h
[ 33%] Generating auto/lua/treesitter.c.generated.h, ../../include/lua/treesitter.h.generated.h
[ 33%] Generating auto/lua/xdiff.c.generated.h, ../../include/lua/xdiff.h.generated.h
[ 33%] Generating ../../include/lua/treesitter.h.inline.generated.h
[ 33%] Generating ../../include/macros_defs.h.inline.generated.h
[ 33%] Generating ../../include/lua/xdiff.h.inline.generated.h
[ 33%] Generating auto/main.c.generated.h, ../../include/main.h.generated.h
[ 33%] Generating auto/map_glyph_cache.c.generated.h, ../../include/map_glyph_cache.h.generated.h
[ 33%] Generating auto/map.c.generated.h, ../../include/map.h.generated.h
[ 33%] Generating ../../include/main.h.inline.generated.h
[ 33%] Generating ../../include/map_defs.h.inline.generated.h
[ 33%] Generating ../../include/linematch.h.inline.generated.h
[ 33%] Generating auto/log.c.generated.h, ../../include/log.h.generated.h
[ 33%] Generating auto/lua/base64.c.generated.h, ../../include/lua/base64.h.generated.h
[ 33%] Generating auto/mapping.c.generated.h, ../../include/mapping.h.generated.h
[ 33%] Generating auto/mark.c.generated.h, ../../include/mark.h.generated.h
[ 33%] Generating ../../include/lua/converter.h.inline.generated.h
[ 33%] Generating ../../include/mapping_defs.h.inline.generated.h
[ 38%] Generating ../../include/marktree_defs.h.inline.generated.h
[ 38%] Generating ../../include/mapping.h.inline.generated.h
[ 38%] Generating ../../include/mark_defs.h.inline.generated.h
[ 38%] Generating ../../include/mark.h.inline.generated.h
[ 38%] Generating ../../include/marktree.h.inline.generated.h
[ 38%] Generating auto/match.c.generated.h, ../../include/match.h.generated.h
[ 38%] Generating auto/marktree.c.generated.h, ../../include/marktree.h.generated.h
[ 38%] Generating ../../include/mbyte.h.inline.generated.h
[ 38%] Generating auto/math.c.generated.h, ../../include/math.h.generated.h
[ 38%] Generating auto/mbyte.c.generated.h, ../../include/mbyte.h.generated.h
[ 38%] Generating ../../include/mbyte_defs.h.inline.generated.h
[ 38%] Generating ../../include/memfile.h.inline.generated.h
[ 38%] Generating ../../include/math.h.inline.generated.h
[ 38%] Generating auto/memfile.c.generated.h, ../../include/memfile.h.generated.h
[ 38%] Generating ../../include/match.h.inline.generated.h
[ 38%] Generating ../../include/memline.h.inline.generated.h
[ 38%] Generating ../../include/memfile_defs.h.inline.generated.h
[ 38%] Generating auto/memline.c.generated.h, ../../include/memline.h.generated.h
[ 38%] Generating ../../include/memline_defs.h.inline.generated.h
[ 38%] Generating auto/memory.c.generated.h, ../../include/memory.h.generated.h
[ 38%] Generating ../../include/memory_defs.h.inline.generated.h
[ 38%] Generating ../../include/memory.h.inline.generated.h
[ 38%] Generating ../../include/message.h.inline.generated.h
[ 38%] Generating auto/message.c.generated.h, ../../include/message.h.generated.h
[ 38%] Generating auto/mouse.c.generated.h, ../../include/mouse.h.generated.h
[ 38%] Generating auto/menu.c.generated.h, ../../include/menu.h.generated.h
[ 38%] Generating ../../include/menu_defs.h.inline.generated.h
[ 38%] Generating ../../include/message_defs.h.inline.generated.h
[ 38%] Generating ../../include/menu.h.inline.generated.h
[ 42%] Generating auto/move.c.generated.h, ../../include/move.h.generated.h
[ 38%] Generating ../../include/mouse.h.inline.generated.h
[ 42%] Generating auto/msgpack_rpc/channel.c.generated.h, ../../include/msgpack_rpc/channel.h.generated.h
[ 42%] Generating auto/msgpack_rpc/packer.c.generated.h, ../../include/msgpack_rpc/packer.h.generated.h
[ 42%] Generating ../../include/msgpack_rpc/packer.h.inline.generated.h
[ 42%] Generating ../../include/move.h.inline.generated.h
[ 42%] Generating auto/msgpack_rpc/unpacker.c.generated.h, ../../include/msgpack_rpc/unpacker.h.generated.h
[ 42%] Generating ../../include/msgpack_rpc/server.h.inline.generated.h
[ 42%] Generating ../../include/msgpack_rpc/unpacker.h.inline.generated.h
[ 42%] Generating ../../include/msgpack_rpc/channel.h.inline.generated.h
[ 42%] Generating ../../include/msgpack_rpc/packer_defs.h.inline.generated.h
[ 42%] Generating auto/msgpack_rpc/server.c.generated.h, ../../include/msgpack_rpc/server.h.generated.h
[ 42%] Generating ../../include/msgpack_rpc/channel_defs.h.inline.generated.h
[ 42%] Generating auto/normal.c.generated.h, ../../include/normal.h.generated.h
[ 42%] Generating ../../include/normal.h.inline.generated.h
[ 42%] Generating auto/ops.c.generated.h, ../../include/ops.h.generated.h
[ 42%] Generating ../../include/ops.h.inline.generated.h
[ 42%] Generating ../../include/normal_defs.h.inline.generated.h
[ 42%] Generating auto/os/fileio.c.generated.h, ../../include/os/fileio.h.generated.h
[ 42%] Generating auto/optionstr.c.generated.h, ../../include/optionstr.h.generated.h
[ 42%] Generating ../../include/option.h.inline.generated.h
[ 42%] Generating auto/option.c.generated.h, ../../include/option.h.generated.h
[ 42%] Generating ../../include/os/dl.h.inline.generated.h
[ 42%] Generating ../../include/option_vars.h.inline.generated.h
[ 42%] Generating auto/os/dl.c.generated.h, ../../include/os/dl.h.generated.h
[ 42%] Generating ../../include/option_defs.h.inline.generated.h
[ 42%] Generating auto/os/env.c.generated.h, ../../include/os/env.h.generated.h
[ 47%] Generating auto/os/fs.c.generated.h, ../../include/os/fs.h.generated.h
[ 47%] Generating ../../include/os/fileio_defs.h.inline.generated.h
[ 47%] Generating ../../include/optionstr.h.inline.generated.h
[ 47%] Generating ../../include/os/fs.h.inline.generated.h
[ 47%] Generating ../../include/os/fileio.h.inline.generated.h
[ 47%] Generating ../../include/os/fs_defs.h.inline.generated.h
[ 47%] Generating auto/os/input.c.generated.h, ../../include/os/input.h.generated.h
[ 47%] Generating ../../include/os/os.h.inline.generated.h
[ 47%] Generating ../../include/os/lang.h.inline.generated.h
[ 47%] Generating auto/os/lang.c.generated.h, ../../include/os/lang.h.generated.h
[ 47%] Generating ../../include/os/os_defs.h.inline.generated.h
[ 47%] Generating ../../include/os/input.h.inline.generated.h
[ 47%] Generating ../../include/os/proc.h.inline.generated.h
[ 47%] Generating ../../include/os/pty_conpty_win.h.inline.generated.h
[ 47%] Generating auto/os/pty_proc_unix.c.generated.h, ../../include/os/pty_proc_unix.h.generated.h
[ 47%] Generating auto/os/proc.c.generated.h, ../../include/os/proc.h.generated.h
[ 47%] Generating auto/os/mem.c.generated.h, ../../include/os/mem.h.generated.h
[ 47%] Generating ../../include/os/pty_proc_unix.h.inline.generated.h
[ 47%] Generating ../../include/os/shell.h.inline.generated.h
[ 47%] Generating ../../include/os/pty_proc.h.inline.generated.h
[ 47%] Generating ../../include/os/os_win_console.h.inline.generated.h
[ 47%] Generating ../../include/os/pty_proc_win.h.inline.generated.h
[ 47%] Generating auto/os/shell.c.generated.h, ../../include/os/shell.h.generated.h
[ 47%] Generating auto/os/signal.c.generated.h, ../../include/os/signal.h.generated.h
[ 47%] Generating ../../include/os/signal.h.inline.generated.h
[ 47%] Generating auto/os/stdpaths.c.generated.h, ../../include/os/stdpaths.h.generated.h
[ 47%] Generating ../../include/os/stdpaths_defs.h.inline.generated.h
[ 47%] Generating ../../include/os/time.h.inline.generated.h
[ 47%] Generating ../../include/os/unix_defs.h.inline.generated.h
[ 47%] Generating auto/os/time.c.generated.h, ../../include/os/time.h.generated.h
[ 47%] Generating ../../include/os/time_defs.h.inline.generated.h
[ 47%] Generating ../../include/plines.h.inline.generated.h
[ 47%] Generating auto/path.c.generated.h, ../../include/path.h.generated.h
[ 47%] Generating auto/os/users.c.generated.h, ../../include/os/users.h.generated.h
[ 47%] Generating auto/profile.c.generated.h, ../../include/profile.h.generated.h
[ 47%] Generating ../../include/pos_defs.h.inline.generated.h
[ 47%] Generating ../../include/popupmenu.h.inline.generated.h
[ 47%] Generating auto/popupmenu.c.generated.h, ../../include/popupmenu.h.generated.h
[ 47%] Generating ../../include/path.h.inline.generated.h
[ 47%] Generating ../../include/profile.h.inline.generated.h
[ 47%] Generating auto/quickfix.c.generated.h, ../../include/quickfix.h.generated.h
[ 47%] Generating auto/plines.c.generated.h, ../../include/plines.h.generated.h
[ 47%] Generating ../../include/quickfix.h.inline.generated.h
[ 47%] Generating auto/regexp.c.generated.h, ../../include/regexp.h.generated.h
[ 47%] Generating ../../include/regexp_defs.h.inline.generated.h
[ 47%] Generating auto/runtime.c.generated.h, ../../include/runtime.h.generated.h
[ 47%] Generating ../../include/register.h.inline.generated.h
[ 47%] Generating ../../include/regexp.h.inline.generated.h
[ 47%] Generating ../../include/register_defs.h.inline.generated.h
[ 52%] Generating ../../include/search.h.inline.generated.h
[ 52%] Generating auto/register.c.generated.h, ../../include/register.h.generated.h
[ 52%] Generating auto/shada.c.generated.h, ../../include/shada.h.generated.h
[ 52%] Generating ../../include/runtime.h.inline.generated.h
[ 52%] Generating ../../include/runtime_defs.h.inline.generated.h
[ 52%] Generating auto/sha256.c.generated.h, ../../include/sha256.h.generated.h
[ 52%] Generating auto/search.c.generated.h, ../../include/search.h.generated.h
[ 52%] Generating auto/spell.c.generated.h, ../../include/spell.h.generated.h
[ 57%] Generating auto/sign.c.generated.h, ../../include/sign.h.generated.h
[ 57%] Generating ../../include/sign_defs.h.inline.generated.h
[ 57%] Generating ../../include/sha256.h.inline.generated.h
[ 57%] Generating ../../include/shada.h.inline.generated.h
[ 57%] Generating ../../include/spell.h.inline.generated.h
[ 57%] Generating ../../include/sign.h.inline.generated.h
[ 57%] Generating ../../include/spell_defs.h.inline.generated.h
[ 57%] Generating auto/spellfile.c.generated.h, ../../include/spellfile.h.generated.h
[ 57%] Generating ../../include/spellfile.h.inline.generated.h
[ 57%] Generating auto/spellsuggest.c.generated.h, ../../include/spellsuggest.h.generated.h
[ 57%] Generating auto/state.c.generated.h, ../../include/state.h.generated.h
[ 57%] Generating ../../include/state_defs.h.inline.generated.h
[ 57%] Generating ../../include/spellsuggest.h.inline.generated.h
[ 57%] Generating auto/statusline.c.generated.h, ../../include/statusline.h.generated.h
[ 57%] Generating ../../include/statusline.h.inline.generated.h
[ 57%] Generating ../../include/state.h.inline.generated.h
[ 57%] Generating auto/syntax.c.generated.h, ../../include/syntax.h.generated.h
[ 57%] Generating ../../include/syntax.h.inline.generated.h
[ 57%] Generating ../../include/statusline_defs.h.inline.generated.h
[ 57%] Generating auto/strings.c.generated.h, ../../include/strings.h.generated.h
[ 57%] Generating ../../include/tag.h.inline.generated.h
[ 57%] Generating auto/textformat.c.generated.h, ../../include/textformat.h.generated.h
[ 57%] Generating auto/tag.c.generated.h, ../../include/tag.h.generated.h
[ 57%] Generating ../../include/terminal.h.inline.generated.h
[ 57%] Generating ../../include/syntax_defs.h.inline.generated.h
[ 57%] Generating ../../include/strings.h.inline.generated.h
[ 57%] Generating auto/terminal.c.generated.h, ../../include/terminal.h.generated.h
[ 57%] Generating ../../include/testing.h.inline.generated.h
[ 57%] Generating auto/testing.c.generated.h, ../../include/testing.h.generated.h
[ 57%] Generating auto/tui/input.c.generated.h, ../../include/tui/input.h.generated.h
[ 57%] Generating auto/textobject.c.generated.h, ../../include/textobject.h.generated.h
[ 57%] Generating ../../include/textobject.h.inline.generated.h
[ 57%] Generating ../../include/textformat.h.inline.generated.h
[ 57%] Generating ../../include/tui/input.h.inline.generated.h
[ 57%] Generating ../../include/tui/input_defs.h.inline.generated.h
[ 57%] Generating auto/tui/terminfo.c.generated.h, ../../include/tui/terminfo.h.generated.h
[ 57%] Generating ../../include/tui/terminfo.h.inline.generated.h
[ 57%] Generating ../../include/tui/terminfo_builtin.h.inline.generated.h
[ 57%] Generating ../../include/tui/terminfo_enum_defs.h.inline.generated.h
[ 57%] Generating ../../include/tui/terminfo_defs.h.inline.generated.h
[ 57%] Generating auto/tui/termkey/driver-ti.c.generated.h, ../../include/tui/termkey/driver-ti.h.generated.h
[ 57%] Generating auto/tui/tui.c.generated.h, ../../include/tui/tui.h.generated.h
[ 57%] Generating ../../include/tui/termkey/driver-ti.h.inline.generated.h
[ 57%] Generating auto/tui/termkey/driver-csi.c.generated.h, ../../include/tui/termkey/driver-csi.h.generated.h
[ 57%] Generating auto/tui/termkey/termkey.c.generated.h, ../../include/tui/termkey/termkey.h.generated.h
[ 57%] Generating ../../include/tui/termkey/termkey.h.inline.generated.h
[ 57%] Generating ../../include/tui/termkey/driver-csi.h.inline.generated.h
[ 61%] Generating ../../include/tui/tui_defs.h.inline.generated.h
[ 61%] Generating ../../include/tui/ugrid.h.inline.generated.h
[ 61%] Generating ../../include/tui/termkey/termkey_defs.h.inline.generated.h
[ 61%] Generating auto/ui_client.c.generated.h, ../../include/ui_client.h.generated.h
[ 61%] Generating ../../include/tui/tui.h.inline.generated.h
[ 61%] Generating ../../include/tui/termkey/termkey-internal.h.inline.generated.h
[ 61%] Generating auto/ui.c.generated.h, ../../include/ui.h.generated.h
[ 61%] Generating auto/tui/ugrid.c.generated.h, ../../include/tui/ugrid.h.generated.h
[ 61%] Generating ../../include/types_defs.h.inline.generated.h
[ 61%] Generating auto/ui_events_client.c.generated.h, ../../include/ui_events_client.h.generated.h
[ 61%] Generating ../../include/ui.h.inline.generated.h
[ 61%] Generating ../../include/ui_client.h.inline.generated.h
[ 61%] Generating ../../include/undo.h.inline.generated.h
[ 61%] Generating auto/ui_compositor.c.generated.h, ../../include/ui_compositor.h.generated.h
[ 61%] Generating ../../include/ui_compositor.h.inline.generated.h
[ 61%] Generating ../../include/ui_defs.h.inline.generated.h
[ 61%] Generating auto/ui_events_call.c.generated.h, ../../include/ui_events_call.h.generated.h
[ 61%] Generating auto/undo.c.generated.h, ../../include/undo.h.generated.h
[ 61%] Generating auto/ui_events_remote.c.generated.h, ../../include/ui_events_remote.h.generated.h
[ 61%] Generating auto/usercmd.c.generated.h, ../../include/usercmd.h.generated.h
[ 61%] Generating ../../include/undo_defs.h.inline.generated.h
[ 61%] Generating ../../include/version.h.inline.generated.h
[ 61%] Generating auto/version.c.generated.h, ../../include/version.h.generated.h
[ 61%] Generating ../../include/usercmd.h.inline.generated.h
[ 61%] Generating ../../include/viml/parser/expressions.h.inline.generated.h
[ 61%] Generating ../../include/viml/parser/parser_defs.h.inline.generated.h
[ 61%] Generating auto/viml/parser/parser.c.generated.h, ../../include/viml/parser/parser.h.generated.h
[ 61%] Generating auto/viml/parser/expressions.c.generated.h, ../../include/viml/parser/expressions.h.generated.h
[ 61%] Generating ../../include/viml/parser/parser.h.inline.generated.h
[ 61%] Generating auto/vterm/keyboard.c.generated.h, ../../include/vterm/keyboard.h.generated.h
[ 61%] Generating auto/vterm/encoding.c.generated.h, ../../include/vterm/encoding.h.generated.h
[ 61%] Generating ../../include/vterm/keyboard.h.inline.generated.h
[ 61%] Generating ../../include/vterm/encoding.h.inline.generated.h
[ 61%] Generating ../../include/vterm/parser.h.inline.generated.h
[ 61%] Generating auto/vterm/pen.c.generated.h, ../../include/vterm/pen.h.generated.h
[ 61%] Generating ../../include/vterm/mouse.h.inline.generated.h
[ 61%] Generating auto/vterm/mouse.c.generated.h, ../../include/vterm/mouse.h.generated.h
[ 61%] Generating ../../include/vterm/pen.h.inline.generated.h
[ 61%] Generating auto/vterm/parser.c.generated.h, ../../include/vterm/parser.h.generated.h
[ 61%] Generating ../../include/vim_defs.h.inline.generated.h
[ 61%] Generating auto/vterm/vterm.c.generated.h, ../../include/vterm/vterm.h.generated.h
[ 66%] Generating auto/vterm/state.c.generated.h, ../../include/vterm/state.h.generated.h
[ 66%] Generating auto/vterm/screen.c.generated.h, ../../include/vterm/screen.h.generated.h
[ 66%] Generating ../../include/vterm/screen.h.inline.generated.h
[ 66%] Generating ../../include/vterm/state.h.inline.generated.h
[ 66%] Generating ../../include/vterm/vterm_keycodes_defs.h.inline.generated.h
[ 66%] Generating ../../include/vterm/vterm_internal_defs.h.inline.generated.h
[ 66%] Generating ../../include/vterm/vterm.h.inline.generated.h
[ 66%] Generating auto/winfloat.c.generated.h, ../../include/winfloat.h.generated.h
[ 66%] Generating ../../include/window.h.inline.generated.h
[ 66%] Generating ../../include/winfloat.h.inline.generated.h
[ 66%] Generating ../../include/vterm/vterm_defs.h.inline.generated.h
[ 66%] Generating auto/window.c.generated.h, ../../include/window.h.generated.h
[ 66%] Generating auto/keycode_names.generated.h
[ 66%] Generating auto/options.generated.h, auto/options_enum.generated.h, auto/options_map.generated.h, auto/option_vars.generated.h
[ 66%] Generating auto/lua/vim_module.generated.h
[ 66%] Generating auto/api/private/dispatch_wrappers.generated.h, ../../exported_funcs_metadata.mpack, ../../eval_funcs_metadata.mpack, auto/lua_api_c_bindings.generated.h, auto/keysets_defs.generated.h
[ 66%] Generating auto/api/private/dispatch_wrappers.c.generated.h, ../../include/api/private/dispatch_wrappers.h.generated.h
[ 71%] Generating auto/funcs.generated.h, ../../funcs_data.mpack
[ 71%] Generating auto/api/private/api_metadata.generated.h
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[ 71%] Generating auto/os/time.c.generated.h, ../../include/os/time.h.generated.h
[ 71%] Generating auto/log.c.generated.h, ../../include/log.h.generated.h
[ 71%] Generating auto/grid.c.generated.h, ../../include/grid.h.generated.h
[ 71%] Generating ../../include/api/private/defs.h.inline.generated.h
[ 71%] Generating ../../include/mark_defs.h.inline.generated.h
[ 71%] Generating ../../include/mbyte.h.inline.generated.h
[ 71%] Generating auto/mbyte.c.generated.h, ../../include/mbyte.h.generated.h
[ 71%] Generating auto/vterm/vterm.c.generated.h, ../../include/vterm/vterm.h.generated.h
[ 71%] Generating ../../include/lib/queue_defs.h.inline.generated.h
[ 71%] Generating auto/memory.c.generated.h, ../../include/memory.h.generated.h
[ 71%] Generating auto/event/multiqueue.c.generated.h, ../../include/event/multiqueue.h.generated.h
[ 71%] Generating auto/vterm/screen.c.generated.h, ../../include/vterm/screen.h.generated.h
[ 71%] Generating auto/api/deprecated.c.generated.h, ../../include/api/deprecated.h.generated.h
[ 71%] Generating auto/api/events.c.generated.h, ../../include/api/events.h.generated.h
[ 71%] Generating auto/vterm/pen.c.generated.h, ../../include/vterm/pen.h.generated.h
[ 71%] Generating auto/api/command.c.generated.h, ../../include/api/command.h.generated.h
[ 71%] Generating auto/api/private/dispatch.c.generated.h, ../../include/api/private/dispatch.h.generated.h
[ 71%] Generating auto/api/autocmd.c.generated.h, ../../include/api/autocmd.h.generated.h
[ 71%] Generating auto/api/buffer.c.generated.h, ../../include/api/buffer.h.generated.h
[ 71%] Generating auto/api/extmark.c.generated.h, ../../include/api/extmark.h.generated.h
[ 71%] Generating auto/api/options.c.generated.h, ../../include/api/options.h.generated.h
[ 71%] Generating auto/api/ui.c.generated.h, ../../include/api/ui.h.generated.h
[ 71%] Generating auto/api/tabpage.c.generated.h, ../../include/api/tabpage.h.generated.h
[ 71%] Generating auto/api/window.c.generated.h, ../../include/api/window.h.generated.h
[ 71%] Generating auto/api/win_config.c.generated.h, ../../include/api/win_config.h.generated.h
[ 71%] Generating auto/api/vim.c.generated.h, ../../include/api/vim.h.generated.h
[ 71%] Generating auto/api/vimscript.c.generated.h, ../../include/api/vimscript.h.generated.h
[ 71%] Generating auto/buffer.c.generated.h, ../../include/buffer.h.generated.h
[ 71%] Generating ../../include/buffer.h.inline.generated.h
[ 71%] Generating auto/api/private/validate.c.generated.h, ../../include/api/private/validate.h.generated.h
[ 71%] Generating auto/api/private/helpers.c.generated.h, ../../include/api/private/helpers.h.generated.h
[ 71%] Generating ../../include/ascii_defs.h.inline.generated.h
[ 71%] Generating auto/autocmd.c.generated.h, ../../include/autocmd.h.generated.h
[ 71%] Generating ../../include/eval/typval.h.inline.generated.h
[ 71%] Generating auto/eval/typval.c.generated.h, ../../include/eval/typval.h.generated.h
[ 71%] Generating auto/event/loop.c.generated.h, ../../include/event/loop.h.generated.h
[ 71%] Generating auto/hashtab.c.generated.h, ../../include/hashtab.h.generated.h
[ 71%] Generating auto/message.c.generated.h, ../../include/message.h.generated.h
[ 71%] Generating auto/buffer_updates.c.generated.h, ../../include/buffer_updates.h.generated.h
[ 71%] Generating auto/strings.c.generated.h, ../../include/strings.h.generated.h
[ 71%] Generating auto/lua/executor.c.generated.h, ../../include/lua/executor.h.generated.h
[ 71%] Generating auto/usercmd.c.generated.h, ../../include/usercmd.h.generated.h
[ 71%] Generating auto/change.c.generated.h, ../../include/change.h.generated.h
[ 71%] Generating ../../include/strings.h.inline.generated.h
[ 71%] Generating auto/ex_cmds.c.generated.h, ../../include/ex_cmds.h.generated.h
[ 71%] Generating auto/extmark.c.generated.h, ../../include/extmark.h.generated.h
[ 71%] Generating auto/cursor.c.generated.h, ../../include/cursor.h.generated.h
[ 71%] Generating auto/mapping.c.generated.h, ../../include/mapping.h.generated.h
[ 71%] Generating auto/mark.c.generated.h, ../../include/mark.h.generated.h
[ 71%] Generating ../../include/mark.h.inline.generated.h
[ 71%] Generating auto/undo.c.generated.h, ../../include/undo.h.generated.h
[ 71%] Generating auto/memline.c.generated.h, ../../include/memline.h.generated.h
[ 71%] Generating ../../include/ops.h.inline.generated.h
[ 71%] Generating auto/ops.c.generated.h, ../../include/ops.h.generated.h
[ 71%] Generating auto/move.c.generated.h, ../../include/move.h.generated.h
[ 71%] Generating ../../include/register.h.inline.generated.h
[ 71%] Generating auto/ex_docmd.c.generated.h, ../../include/ex_docmd.h.generated.h
[ 71%] Generating auto/ex_eval.c.generated.h, ../../include/ex_eval.h.generated.h
[ 71%] Generating ../../include/charset.h.inline.generated.h
[ 71%] Generating auto/charset.c.generated.h, ../../include/charset.h.generated.h
[ 71%] Generating auto/register.c.generated.h, ../../include/register.h.generated.h
[ 71%] Generating auto/regexp.c.generated.h, ../../include/regexp.h.generated.h
[ 71%] Generating auto/decoration.c.generated.h, ../../include/decoration.h.generated.h
[ 71%] Generating auto/garray.c.generated.h, ../../include/garray.h.generated.h
[ 71%] Generating auto/window.c.generated.h, ../../include/window.h.generated.h
[ 71%] Generating ../../include/decoration.h.inline.generated.h
[ 71%] Generating auto/eval/vars.c.generated.h, ../../include/eval/vars.h.generated.h
[ 71%] Generating auto/highlight.c.generated.h, ../../include/highlight.h.generated.h
[ 71%] Generating auto/api/private/converter.c.generated.h, ../../include/api/private/converter.h.generated.h
[ 71%] Generating auto/marktree.c.generated.h, ../../include/marktree.h.generated.h
[ 71%] Generating auto/highlight_group.c.generated.h, ../../include/highlight_group.h.generated.h
[ 71%] Generating auto/option.c.generated.h, ../../include/option.h.generated.h
[ 71%] Generating auto/channel.c.generated.h, ../../include/channel.h.generated.h
[ 71%] Generating ../../include/channel.h.inline.generated.h
[ 71%] Generating auto/main.c.generated.h, ../../include/main.h.generated.h
[ 71%] Generating auto/msgpack_rpc/packer.c.generated.h, ../../include/msgpack_rpc/packer.h.generated.h
[ 71%] Generating auto/ui_events_call.c.generated.h, ../../include/ui_events_call.h.generated.h
[ 71%] Generating auto/event/libuv_proc.c.generated.h, ../../include/event/libuv_proc.h.generated.h
[ 71%] Generating auto/msgpack_rpc/channel.c.generated.h, ../../include/msgpack_rpc/channel.h.generated.h
[ 71%] Generating auto/ui.c.generated.h, ../../include/ui.h.generated.h
[ 71%] Generating auto/ui_events_remote.c.generated.h, ../../include/ui_events_remote.h.generated.h
[ 71%] Generating auto/os/pty_proc_unix.c.generated.h, ../../include/os/pty_proc_unix.h.generated.h
[ 71%] Generating auto/eval.c.generated.h, ../../include/eval.h.generated.h
[ 71%] Generating auto/drawscreen.c.generated.h, ../../include/drawscreen.h.generated.h
[ 71%] Generating auto/decoration_provider.c.generated.h, ../../include/decoration_provider.h.generated.h
[ 71%] Generating auto/sign.c.generated.h, ../../include/sign.h.generated.h
[ 71%] Generating auto/eval/decode.c.generated.h, ../../include/eval/decode.h.generated.h
[ 71%] Generating auto/eval/encode.c.generated.h, ../../include/eval/encode.h.generated.h
[ 71%] Generating auto/eval/userfunc.c.generated.h, ../../include/eval/userfunc.h.generated.h
[ 71%] Generating auto/ex_getln.c.generated.h, ../../include/ex_getln.h.generated.h
[ 71%] Generating ../../include/eval/typval_encode.h.inline.generated.h
[ 71%] Generating auto/msgpack_rpc/unpacker.c.generated.h, ../../include/msgpack_rpc/unpacker.h.generated.h
[ 71%] Generating auto/runtime.c.generated.h, ../../include/runtime.h.generated.h
[ 71%] Generating auto/context.c.generated.h, ../../include/context.h.generated.h
[ 71%] Generating auto/ui_client.c.generated.h, ../../include/ui_client.h.generated.h
[ 71%] Generating ../../include/os/fileio_defs.h.inline.generated.h
[ 71%] Generating auto/ui_events_client.c.generated.h, ../../include/ui_events_client.h.generated.h
[ 71%] Generating auto/fold.c.generated.h, ../../include/fold.h.generated.h
[ 71%] Generating auto/event/wstream.c.generated.h, ../../include/event/wstream.h.generated.h
[ 71%] Generating auto/drawline.c.generated.h, ../../include/drawline.h.generated.h
[ 71%] Generating auto/keycodes.c.generated.h, ../../include/keycodes.h.generated.h
[ 71%] Generating auto/getchar.c.generated.h, ../../include/getchar.h.generated.h
[ 71%] Generating auto/math.c.generated.h, ../../include/math.h.generated.h
[ 71%] Generating auto/insexpand.c.generated.h, ../../include/insexpand.h.generated.h
[ 71%] Generating auto/lua/treesitter.c.generated.h, ../../include/lua/treesitter.h.generated.h
[ 71%] Generating auto/normal.c.generated.h, ../../include/normal.h.generated.h
[ 71%] Generating auto/optionstr.c.generated.h, ../../include/optionstr.h.generated.h
[ 71%] Generating auto/os/proc.c.generated.h, ../../include/os/proc.h.generated.h
[ 71%] Generating auto/popupmenu.c.generated.h, ../../include/popupmenu.h.generated.h
[ 71%] Generating auto/os/input.c.generated.h, ../../include/os/input.h.generated.h
[ 71%] Generating auto/statusline.c.generated.h, ../../include/statusline.h.generated.h
[ 71%] Generating auto/viml/parser/expressions.c.generated.h, ../../include/viml/parser/expressions.h.generated.h
[ 71%] Generating auto/state.c.generated.h, ../../include/state.h.generated.h
[ 71%] Generating auto/terminal.c.generated.h, ../../include/terminal.h.generated.h
[ 71%] Generating auto/winfloat.c.generated.h, ../../include/winfloat.h.generated.h
[ 71%] Generating auto/viml/parser/parser.c.generated.h, ../../include/viml/parser/parser.h.generated.h
[ 71%] Generating auto/syntax.c.generated.h, ../../include/syntax.h.generated.h
[ 71%] Generating auto/plines.c.generated.h, ../../include/plines.h.generated.h
[ 71%] Generating ../../include/plines.h.inline.generated.h
[ 71%] Generating auto/eval/window.c.generated.h, ../../include/eval/window.h.generated.h
[ 71%] Generating ../../include/viml/parser/parser.h.inline.generated.h
[ 71%] Generating auto/ui_compositor.c.generated.h, ../../include/ui_compositor.h.generated.h
[ 71%] Generating auto/arglist.c.generated.h, ../../include/arglist.h.generated.h
[ 71%] Generating auto/ex_cmds2.c.generated.h, ../../include/ex_cmds2.h.generated.h
[ 71%] Generating auto/os/stdpaths.c.generated.h, ../../include/os/stdpaths.h.generated.h
[ 71%] Generating auto/os/env.c.generated.h, ../../include/os/env.h.generated.h
[ 71%] Generating auto/fileio.c.generated.h, ../../include/fileio.h.generated.h
[ 71%] Generating auto/arabic.c.generated.h, ../../include/arabic.h.generated.h
[ 71%] Generating auto/path.c.generated.h, ../../include/path.h.generated.h
[ 71%] Generating auto/os/mem.c.generated.h, ../../include/os/mem.h.generated.h
[ 71%] Generating auto/version.c.generated.h, ../../include/version.h.generated.h
[ 71%] Generating auto/os/users.c.generated.h, ../../include/os/users.h.generated.h
[ 71%] Generating auto/base64.c.generated.h, ../../include/base64.h.generated.h
[ 71%] Generating auto/profile.c.generated.h, ../../include/profile.h.generated.h
[ 71%] Generating auto/diff.c.generated.h, ../../include/diff.h.generated.h
[ 71%] Generating auto/search.c.generated.h, ../../include/search.h.generated.h
[ 71%] Generating auto/cmdexpand.c.generated.h, ../../include/cmdexpand.h.generated.h
[ 71%] Generating auto/digraph.c.generated.h, ../../include/digraph.h.generated.h
[ 71%] Generating auto/file_search.c.generated.h, ../../include/file_search.h.generated.h
[ 71%] Generating auto/help.c.generated.h, ../../include/help.h.generated.h
[ 71%] Generating auto/quickfix.c.generated.h, ../../include/quickfix.h.generated.h
[ 71%] Generating auto/fuzzy.c.generated.h, ../../include/fuzzy.h.generated.h
[ 71%] Generating auto/spell.c.generated.h, ../../include/spell.h.generated.h
[ 71%] Generating auto/os/fs.c.generated.h, ../../include/os/fs.h.generated.h
[ 71%] Generating auto/sha256.c.generated.h, ../../include/sha256.h.generated.h
[ 71%] Generating auto/input.c.generated.h, ../../include/input.h.generated.h
[ 71%] Generating auto/indent.c.generated.h, ../../include/indent.h.generated.h
[ 71%] Generating auto/edit.c.generated.h, ../../include/edit.h.generated.h
[ 71%] Generating auto/indent_c.c.generated.h, ../../include/indent_c.h.generated.h
[ 71%] Generating auto/bufwrite.c.generated.h, ../../include/bufwrite.h.generated.h
[ 71%] Generating auto/textformat.c.generated.h, ../../include/textformat.h.generated.h
[ 71%] Generating auto/event/proc.c.generated.h, ../../include/event/proc.h.generated.h
[ 71%] Generating auto/event/stream.c.generated.h, ../../include/event/stream.h.generated.h
[ 71%] Generating auto/event/socket.c.generated.h, ../../include/event/socket.h.generated.h
[ 71%] Generating auto/menu.c.generated.h, ../../include/menu.h.generated.h
[ 71%] Generating auto/event/rstream.c.generated.h, ../../include/event/rstream.h.generated.h
[ 71%] Generating auto/os/shell.c.generated.h, ../../include/os/shell.h.generated.h
[ 71%] Generating auto/msgpack_rpc/server.c.generated.h, ../../include/msgpack_rpc/server.h.generated.h
[ 71%] Generating auto/eval/funcs.c.generated.h, ../../include/eval/funcs.h.generated.h
[ 71%] Generating auto/clipboard.c.generated.h, ../../include/clipboard.h.generated.h
[ 71%] Generating auto/shada.c.generated.h, ../../include/shada.h.generated.h
[ 71%] Generating auto/cmdhist.c.generated.h, ../../include/cmdhist.h.generated.h
[ 71%] Generating auto/tag.c.generated.h, ../../include/tag.h.generated.h
[ 71%] Generating auto/os/lang.c.generated.h, ../../include/os/lang.h.generated.h
[ 71%] Generating auto/debugger.c.generated.h, ../../include/debugger.h.generated.h
[ 71%] Generating auto/linematch.c.generated.h, ../../include/linematch.h.generated.h
[ 71%] Generating auto/cursor_shape.c.generated.h, ../../include/cursor_shape.h.generated.h
[ 71%] Generating auto/match.c.generated.h, ../../include/match.h.generated.h
[ 71%] Generating auto/mouse.c.generated.h, ../../include/mouse.h.generated.h
[ 71%] Generating auto/eval/gc.c.generated.h, ../../include/eval/gc.h.generated.h
[ 71%] Generating auto/textobject.c.generated.h, ../../include/textobject.h.generated.h
[ 71%] Generating auto/eval/executor.c.generated.h, ../../include/eval/executor.h.generated.h
[ 71%] Generating auto/event/time.c.generated.h, ../../include/event/time.h.generated.h
[ 71%] Generating auto/eval/buffer.c.generated.h, ../../include/eval/buffer.h.generated.h
[ 71%] Generating auto/eval/fs.c.generated.h, ../../include/eval/fs.h.generated.h
[ 71%] Generating auto/eval/deprecated.c.generated.h, ../../include/eval/deprecated.h.generated.h
[ 71%] Generating auto/os/fileio.c.generated.h, ../../include/os/fileio.h.generated.h
[ 71%] Generating auto/eval/list.c.generated.h, ../../include/eval/list.h.generated.h
[ 71%] Generating auto/testing.c.generated.h, ../../include/testing.h.generated.h
[ 71%] Generating auto/ex_session.c.generated.h, ../../include/ex_session.h.generated.h
[ 71%] Generating auto/spellsuggest.c.generated.h, ../../include/spellsuggest.h.generated.h
[ 71%] Generating auto/event/signal.c.generated.h, ../../include/event/signal.h.generated.h
[ 71%] Generating auto/lua/secure.c.generated.h, ../../include/lua/secure.h.generated.h
[ 71%] Generating auto/lua/converter.c.generated.h, ../../include/lua/converter.h.generated.h
[ 71%] Generating auto/os/dl.c.generated.h, ../../include/os/dl.h.generated.h
[ 71%] Generating auto/lua/spell.c.generated.h, ../../include/lua/spell.h.generated.h
[ 71%] Generating auto/lua/base64.c.generated.h, ../../include/lua/base64.h.generated.h
[ 71%] Generating auto/spellfile.c.generated.h, ../../include/spellfile.h.generated.h
[ 71%] Generating auto/lua/xdiff.c.generated.h, ../../include/lua/xdiff.h.generated.h
[ 71%] Generating auto/os/signal.c.generated.h, ../../include/os/signal.h.generated.h
[ 71%] Generating auto/memfile.c.generated.h, ../../include/memfile.h.generated.h
[ 71%] Generating auto/lua/stdlib.c.generated.h, ../../include/lua/stdlib.h.generated.h
[ 71%] Generating auto/vterm/state.c.generated.h, ../../include/vterm/state.h.generated.h
[ 71%] Generating auto/vterm/keyboard.c.generated.h, ../../include/vterm/keyboard.h.generated.h
[ 71%] Generating auto/vterm/mouse.c.generated.h, ../../include/vterm/mouse.h.generated.h
[ 71%] Generating auto/vterm/parser.c.generated.h, ../../include/vterm/parser.h.generated.h
[ 71%] Generating auto/tui/input.c.generated.h, ../../include/tui/input.h.generated.h
[ 71%] Generating auto/tui/termkey/driver-ti.c.generated.h, ../../include/tui/termkey/driver-ti.h.generated.h
[ 71%] Generating auto/tui/termkey/driver-csi.c.generated.h, ../../include/tui/termkey/driver-csi.h.generated.h
[ 71%] Generating auto/tui/termkey/termkey.c.generated.h, ../../include/tui/termkey/termkey.h.generated.h
[ 71%] Generating auto/tui/tui.c.generated.h, ../../include/tui/tui.h.generated.h
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/mpack/mpack_core.c.o
[ 71%] Generating auto/tui/ugrid.c.generated.h, ../../include/tui/ugrid.h.generated.h
[ 71%] Generating auto/tui/terminfo.c.generated.h, ../../include/tui/terminfo.h.generated.h
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/__/test/unit/fixtures/multiqueue.c.o
[ 71%] Generating auto/vterm/encoding.c.generated.h, ../../include/vterm/encoding.h.generated.h
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/mpack/rpc.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/mpack/object.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/mpack/lmpack.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/__/test/unit/fixtures/vterm_test.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/mpack/conv.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/private/validate.c.o
[ 71%] Generating auto/api/private/dispatch_wrappers.c.generated.h, ../../include/api/private/dispatch_wrappers.h.generated.h
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/bufwrite.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/arabic.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/arglist.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/base64.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/change.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/charset.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/decoration.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/context.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/cursor_shape.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/cmdhist.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/decoration_provider.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/cursor.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/diff.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/drawline.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/gc.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/drawscreen.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/window.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/libuv_proc.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/multiqueue.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/proc.c.o
[ 71%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/loop.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/rstream.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/socket.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/signal.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/extmark.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/grid.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/time.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/stream.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/event/wstream.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/hashtab.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/indent_c.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/help.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/keycodes.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/garray.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/input.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/linematch.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/base64.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/spell.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/log.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/secure.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/treesitter.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/stdlib.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/map.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/map_glyph_cache.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/marktree.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/mark.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/math.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/memfile.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/memline.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/match.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/mbyte.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/move.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/menu.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/optionstr.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/dl.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/msgpack_rpc/packer.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/fileio.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/pty_proc_unix.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/fs.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/lang.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/mem.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/users.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/shell.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/proc.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/stdpaths.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/time.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/signal.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/plines.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/profile.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/spellfile.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/spellsuggest.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/popupmenu.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/sha256.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/search.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/strings.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/sign.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/textobject.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/spell.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/syntax.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tui/termkey/driver-csi.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tui/terminfo.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/viml/parser/parser.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tui/termkey/termkey.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tui/termkey/driver-ti.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tui/ugrid.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/undo.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ui.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/encoding.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ui_compositor.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/version.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/keyboard.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/mouse.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/vterm.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/state.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/parser.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/pen.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/vterm/screen.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/winfloat.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/xdiff/xdiffi.c.o
[ 76%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/cjson/lua_cjson.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/xdiff/xemit.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/xdiff/xutils.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/xdiff/xpatience.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/xdiff/xprepare.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/__/xdiff/xhistogram.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/command.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/deprecated.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/autocmd.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/events.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/buffer.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/extmark.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/options.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/private/converter.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/private/dispatch.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/vimscript.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/tabpage.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/private/helpers.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/ui.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/autocmd.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/window.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/vim.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/buffer.c.o
[ 80%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/clipboard.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/msgpack_rpc/server.c.o
[ 90%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/executor.c.o
[ 95%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/input.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/register.c.o
[100%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/channel.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/statusline.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/buffer.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/highlight.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/fuzzy.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/vars.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/msgpack_rpc/channel.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/fold.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/digraph.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/api/win_config.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/msgpack_rpc/unpacker.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/edit.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/path.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ex_docmd.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/state.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/mapping.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/encode.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/getchar.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/quickfix.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ex_cmds2.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/runtime.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/mouse.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/buffer_updates.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/debugger.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/indent.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/userfunc.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/regexp.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/fs.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/highlight_group.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/shada.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/message.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tag.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/viml/parser/expressions.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/typval.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/funcs.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/testing.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/cmdexpand.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/xdiff.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/terminal.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ex_session.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tui/tui.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/memory.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/os/env.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/option.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/insexpand.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ui_client.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/usercmd.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/api_wrappers.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/file_search.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/textformat.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/executor.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ops.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/deprecated.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/decode.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ex_eval.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ex_cmds.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/lua/converter.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/normal.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/main.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/ex_getln.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/fileio.c.o
[ 85%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/eval/list.c.o
[100%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/tui/input.c.o
[100%] Building C object src/nvim/CMakeFiles/nvim_bin.dir/window.c.o
[100%] Linking C executable ../../bin/nvim
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[100%] Built target nvim_bin
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[100%] Generating pack/dist/opt/matchit/doc/tags
[100%] Generating syntax/vim/generated.vim
[100%] Generating doc/tags
[100%] Generating pack/dist/opt/netrw/doc/tags
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[100%] Built target nvim_runtime
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[100%] Built target nvim
gmake[2]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[1]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
mkdir -p ".deps"
/usr/bin/cmake -S /home/bryan/tmp/chezmoi_build/neovim//cmake.deps -B ".deps" -G "Unix Makefiles" 
-- Found GNU Make at /usr/bin/gmake
-- CMAKE_BUILD_TYPE=Release
-- Configuring done (0.3s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bryan/tmp/chezmoi_build/neovim/.deps
mkdir -p build
touch "build/.ran-deps-cmake"
/usr/bin/cmake --build ".deps"
gmake[1]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[2]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[  7%] Built target unibilium
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 14%] Built target libuv
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 21%] Built target luajit
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 28%] Built target lua_compat53
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 35%] Built target luv
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 42%] Built target lpeg
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 50%] Built target treesitter_c
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 57%] Built target treesitter_lua
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 64%] Built target treesitter_vim
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 71%] Built target treesitter_vimdoc
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 78%] Built target treesitter_query
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 85%] Built target treesitter_markdown
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[ 92%] Built target treesitter
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
[100%] Built target utf8proc
gmake[2]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
gmake[1]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/.deps'
/usr/bin/cmake --build build
gmake[1]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[2]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  0%] Built target nvim_runtime_deps
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  0%] Built target update_version_stamp
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  0%] Built target nlua0
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[  0%] Generating auto/api/autocmd.c.generated.h, ../../include/api/autocmd.h.generated.h
[  0%] Generating auto/api/buffer.c.generated.h, ../../include/api/buffer.h.generated.h
[  0%] Generating auto/api/command.c.generated.h, ../../include/api/command.h.generated.h
[  0%] Generating auto/api/deprecated.c.generated.h, ../../include/api/deprecated.h.generated.h
[  0%] Generating auto/api/events.c.generated.h, ../../include/api/events.h.generated.h
[  0%] Generating auto/api/extmark.c.generated.h, ../../include/api/extmark.h.generated.h
[  0%] Generating auto/api/options.c.generated.h, ../../include/api/options.h.generated.h
[  0%] Generating auto/api/tabpage.c.generated.h, ../../include/api/tabpage.h.generated.h
[  4%] Generating auto/api/ui.c.generated.h, ../../include/api/ui.h.generated.h
[  4%] Generating auto/api/vim.c.generated.h, ../../include/api/vim.h.generated.h
[  4%] Generating auto/api/vimscript.c.generated.h, ../../include/api/vimscript.h.generated.h
[  4%] Generating auto/api/win_config.c.generated.h, ../../include/api/win_config.h.generated.h
[  4%] Generating auto/api/window.c.generated.h, ../../include/api/window.h.generated.h
[  4%] Generating ../../include/api/autocmd.h.inline.generated.h
[  4%] Generating ../../include/api/buffer.h.inline.generated.h
[  4%] Generating ../../include/api/command.h.inline.generated.h
[  4%] Generating ../../include/api/deprecated.h.inline.generated.h
[  4%] Generating ../../include/api/events.h.inline.generated.h
[  4%] Generating ../../include/api/extmark.h.inline.generated.h
[  4%] Generating ../../include/api/keysets_defs.h.inline.generated.h
[  4%] Generating ../../include/api/options.h.inline.generated.h
[  4%] Generating auto/api/private/converter.c.generated.h, ../../include/api/private/converter.h.generated.h
[  4%] Generating ../../include/api/private/converter.h.inline.generated.h
[  4%] Generating ../../include/api/private/defs.h.inline.generated.h
[  4%] Generating auto/api/private/dispatch.c.generated.h, ../../include/api/private/dispatch.h.generated.h
[  4%] Generating ../../include/api/private/dispatch.h.inline.generated.h
[  4%] Generating auto/api/private/dispatch_wrappers.c.generated.h, ../../include/api/private/dispatch_wrappers.h.generated.h
[  4%] Generating auto/api/private/helpers.c.generated.h, ../../include/api/private/helpers.h.generated.h
[  4%] Generating ../../include/api/private/helpers.h.inline.generated.h
[  4%] Generating auto/api/private/validate.c.generated.h, ../../include/api/private/validate.h.generated.h
[  4%] Generating ../../include/api/private/validate.h.inline.generated.h
[  4%] Generating ../../include/api/tabpage.h.inline.generated.h
[  4%] Generating ../../include/api/ui.h.inline.generated.h
[  4%] Generating ../../include/api/ui_events.h.inline.generated.h
[  4%] Generating ../../include/api/vim.h.inline.generated.h
[  4%] Generating ../../include/api/vimscript.h.inline.generated.h
[  4%] Generating ../../include/api/win_config.h.inline.generated.h
[  4%] Generating ../../include/api/window.h.inline.generated.h
[  4%] Generating auto/arabic.c.generated.h, ../../include/arabic.h.generated.h
[  4%] Generating ../../include/arabic.h.inline.generated.h
[  4%] Generating auto/arglist.c.generated.h, ../../include/arglist.h.generated.h
[  4%] Generating ../../include/arglist.h.inline.generated.h
[  4%] Generating ../../include/arglist_defs.h.inline.generated.h
[  4%] Generating ../../include/ascii_defs.h.inline.generated.h
[  4%] Generating ../../include/assert_defs.h.inline.generated.h
[  4%] Generating auto/autocmd.c.generated.h, ../../include/autocmd.h.generated.h
[  4%] Generating ../../include/autocmd.h.inline.generated.h
[  4%] Generating ../../include/autocmd_defs.h.inline.generated.h
[  4%] Generating auto/base64.c.generated.h, ../../include/base64.h.generated.h
[  4%] Generating ../../include/base64.h.inline.generated.h
[  4%] Generating auto/buffer.c.generated.h, ../../include/buffer.h.generated.h
[  4%] Generating ../../include/buffer.h.inline.generated.h
[  4%] Generating ../../include/buffer_defs.h.inline.generated.h
[  4%] Generating auto/buffer_updates.c.generated.h, ../../include/buffer_updates.h.generated.h
[  9%] Generating ../../include/buffer_updates.h.inline.generated.h
[  9%] Generating auto/bufwrite.c.generated.h, ../../include/bufwrite.h.generated.h
[  9%] Generating ../../include/bufwrite.h.inline.generated.h
[  9%] Generating auto/change.c.generated.h, ../../include/change.h.generated.h
[  9%] Generating ../../include/change.h.inline.generated.h
[  9%] Generating auto/channel.c.generated.h, ../../include/channel.h.generated.h
[  9%] Generating ../../include/channel.h.inline.generated.h
[  9%] Generating ../../include/channel_defs.h.inline.generated.h
[  9%] Generating auto/charset.c.generated.h, ../../include/charset.h.generated.h
[  9%] Generating ../../include/charset.h.inline.generated.h
[  9%] Generating auto/clipboard.c.generated.h, ../../include/clipboard.h.generated.h
[  9%] Generating ../../include/clipboard.h.inline.generated.h
[  9%] Generating auto/cmdexpand.c.generated.h, ../../include/cmdexpand.h.generated.h
[  9%] Generating ../../include/cmdexpand.h.inline.generated.h
[  9%] Generating ../../include/cmdexpand_defs.h.inline.generated.h
[  9%] Generating auto/cmdhist.c.generated.h, ../../include/cmdhist.h.generated.h
[  9%] Generating ../../include/cmdhist.h.inline.generated.h
[  9%] Generating auto/context.c.generated.h, ../../include/context.h.generated.h
[  9%] Generating ../../include/context.h.inline.generated.h
[  9%] Generating auto/cursor.c.generated.h, ../../include/cursor.h.generated.h
[  9%] Generating ../../include/cursor.h.inline.generated.h
[  9%] Generating auto/cursor_shape.c.generated.h, ../../include/cursor_shape.h.generated.h
[  9%] Generating ../../include/cursor_shape.h.inline.generated.h
[  9%] Generating auto/debugger.c.generated.h, ../../include/debugger.h.generated.h
[  9%] Generating ../../include/debugger.h.inline.generated.h
[  9%] Generating auto/decoration.c.generated.h, ../../include/decoration.h.generated.h
[  9%] Generating ../../include/decoration.h.inline.generated.h
[  9%] Generating ../../include/decoration_defs.h.inline.generated.h
[  9%] Generating auto/decoration_provider.c.generated.h, ../../include/decoration_provider.h.generated.h
[  9%] Generating ../../include/decoration_provider.h.inline.generated.h
[  9%] Generating auto/diff.c.generated.h, ../../include/diff.h.generated.h
[  9%] Generating ../../include/diff.h.inline.generated.h
[  9%] Generating auto/digraph.c.generated.h, ../../include/digraph.h.generated.h
[  9%] Generating ../../include/digraph.h.inline.generated.h
[  9%] Generating auto/drawline.c.generated.h, ../../include/drawline.h.generated.h
[  9%] Generating ../../include/drawline.h.inline.generated.h
[  9%] Generating auto/drawscreen.c.generated.h, ../../include/drawscreen.h.generated.h
[  9%] Generating ../../include/drawscreen.h.inline.generated.h
[  9%] Generating auto/edit.c.generated.h, ../../include/edit.h.generated.h
[  9%] Generating ../../include/edit.h.inline.generated.h
[  9%] Generating ../../include/errors.h.inline.generated.h
[  9%] Generating auto/eval.c.generated.h, ../../include/eval.h.generated.h
[  9%] Generating ../../include/eval.h.inline.generated.h
[  9%] Generating auto/eval/buffer.c.generated.h, ../../include/eval/buffer.h.generated.h
[  9%] Generating ../../include/eval/buffer.h.inline.generated.h
[  9%] Generating auto/eval/decode.c.generated.h, ../../include/eval/decode.h.generated.h
[  9%] Generating ../../include/eval/decode.h.inline.generated.h
[  9%] Generating auto/eval/deprecated.c.generated.h, ../../include/eval/deprecated.h.generated.h
[  9%] Generating ../../include/eval/deprecated.h.inline.generated.h
[  9%] Generating auto/eval/encode.c.generated.h, ../../include/eval/encode.h.generated.h
[  9%] Generating ../../include/eval/encode.h.inline.generated.h
[ 14%] Generating auto/eval/executor.c.generated.h, ../../include/eval/executor.h.generated.h
[ 14%] Generating ../../include/eval/executor.h.inline.generated.h
[ 14%] Generating auto/eval/fs.c.generated.h, ../../include/eval/fs.h.generated.h
[ 14%] Generating ../../include/eval/fs.h.inline.generated.h
[ 14%] Generating auto/eval/funcs.c.generated.h, ../../include/eval/funcs.h.generated.h
[ 14%] Generating ../../include/eval/funcs.h.inline.generated.h
[ 14%] Generating auto/eval/gc.c.generated.h, ../../include/eval/gc.h.generated.h
[ 14%] Generating ../../include/eval/gc.h.inline.generated.h
[ 14%] Generating auto/eval/list.c.generated.h, ../../include/eval/list.h.generated.h
[ 14%] Generating ../../include/eval/list.h.inline.generated.h
[ 14%] Generating auto/eval/typval.c.generated.h, ../../include/eval/typval.h.generated.h
[ 14%] Generating ../../include/eval/typval.h.inline.generated.h
[ 19%] Generating ../../include/eval/typval_defs.h.inline.generated.h
[ 19%] Generating ../../include/eval/typval_encode.h.inline.generated.h
[ 19%] Generating auto/eval/userfunc.c.generated.h, ../../include/eval/userfunc.h.generated.h
[ 19%] Generating ../../include/eval/userfunc.h.inline.generated.h
[ 19%] Generating auto/eval/vars.c.generated.h, ../../include/eval/vars.h.generated.h
[ 19%] Generating ../../include/eval/vars.h.inline.generated.h
[ 19%] Generating auto/eval/window.c.generated.h, ../../include/eval/window.h.generated.h
[ 19%] Generating ../../include/eval/window.h.inline.generated.h
[ 19%] Generating ../../include/eval_defs.h.inline.generated.h
[ 19%] Generating ../../include/event/defs.h.inline.generated.h
[ 19%] Generating auto/event/libuv_proc.c.generated.h, ../../include/event/libuv_proc.h.generated.h
[ 19%] Generating ../../include/event/libuv_proc.h.inline.generated.h
[ 19%] Generating auto/event/loop.c.generated.h, ../../include/event/loop.h.generated.h
[ 19%] Generating ../../include/event/loop.h.inline.generated.h
[ 19%] Generating auto/event/multiqueue.c.generated.h, ../../include/event/multiqueue.h.generated.h
[ 19%] Generating ../../include/event/multiqueue.h.inline.generated.h
[ 19%] Generating auto/event/proc.c.generated.h, ../../include/event/proc.h.generated.h
[ 19%] Generating ../../include/event/proc.h.inline.generated.h
[ 19%] Generating auto/event/rstream.c.generated.h, ../../include/event/rstream.h.generated.h
[ 19%] Generating ../../include/event/rstream.h.inline.generated.h
[ 19%] Generating auto/event/signal.c.generated.h, ../../include/event/signal.h.generated.h
[ 19%] Generating ../../include/event/signal.h.inline.generated.h
[ 19%] Generating auto/event/socket.c.generated.h, ../../include/event/socket.h.generated.h
[ 19%] Generating ../../include/event/socket.h.inline.generated.h
[ 19%] Generating auto/event/stream.c.generated.h, ../../include/event/stream.h.generated.h
[ 19%] Generating ../../include/event/stream.h.inline.generated.h
[ 19%] Generating auto/event/time.c.generated.h, ../../include/event/time.h.generated.h
[ 19%] Generating ../../include/event/time.h.inline.generated.h
[ 19%] Generating auto/event/wstream.c.generated.h, ../../include/event/wstream.h.generated.h
[ 19%] Generating ../../include/event/wstream.h.inline.generated.h
[ 19%] Generating auto/ex_cmds.c.generated.h, ../../include/ex_cmds.h.generated.h
[ 19%] Generating ../../include/ex_cmds.h.inline.generated.h
[ 19%] Generating auto/ex_cmds2.c.generated.h, ../../include/ex_cmds2.h.generated.h
[ 19%] Generating ../../include/ex_cmds2.h.inline.generated.h
[ 19%] Generating ../../include/ex_cmds_defs.h.inline.generated.h
[ 19%] Generating auto/ex_docmd.c.generated.h, ../../include/ex_docmd.h.generated.h
[ 19%] Generating ../../include/ex_docmd.h.inline.generated.h
[ 19%] Generating auto/ex_eval.c.generated.h, ../../include/ex_eval.h.generated.h
[ 19%] Generating ../../include/ex_eval.h.inline.generated.h
[ 19%] Generating ../../include/ex_eval_defs.h.inline.generated.h
[ 19%] Generating auto/ex_getln.c.generated.h, ../../include/ex_getln.h.generated.h
[ 19%] Generating ../../include/ex_getln.h.inline.generated.h
[ 19%] Generating ../../include/ex_getln_defs.h.inline.generated.h
[ 19%] Generating auto/ex_session.c.generated.h, ../../include/ex_session.h.generated.h
[ 19%] Generating ../../include/ex_session.h.inline.generated.h
[ 19%] Generating auto/extmark.c.generated.h, ../../include/extmark.h.generated.h
[ 19%] Generating ../../include/extmark.h.inline.generated.h
[ 19%] Generating ../../include/extmark_defs.h.inline.generated.h
[ 19%] Generating auto/file_search.c.generated.h, ../../include/file_search.h.generated.h
[ 19%] Generating ../../include/file_search.h.inline.generated.h
[ 19%] Generating auto/fileio.c.generated.h, ../../include/fileio.h.generated.h
[ 19%] Generating ../../include/fileio.h.inline.generated.h
[ 19%] Generating auto/fold.c.generated.h, ../../include/fold.h.generated.h
[ 19%] Generating ../../include/fold.h.inline.generated.h
[ 19%] Generating ../../include/fold_defs.h.inline.generated.h
[ 19%] Generating ../../include/func_attr.h.inline.generated.h
[ 19%] Generating auto/fuzzy.c.generated.h, ../../include/fuzzy.h.generated.h
[ 19%] Generating ../../include/fuzzy.h.inline.generated.h
[ 19%] Generating auto/garray.c.generated.h, ../../include/garray.h.generated.h
[ 23%] Generating ../../include/garray.h.inline.generated.h
[ 23%] Generating ../../include/garray_defs.h.inline.generated.h
[ 23%] Generating auto/getchar.c.generated.h, ../../include/getchar.h.generated.h
[ 23%] Generating ../../include/getchar.h.inline.generated.h
[ 23%] Generating ../../include/getchar_defs.h.inline.generated.h
[ 23%] Generating ../../include/gettext_defs.h.inline.generated.h
[ 23%] Generating ../../include/globals.h.inline.generated.h
[ 23%] Generating auto/grid.c.generated.h, ../../include/grid.h.generated.h
[ 23%] Generating ../../include/grid.h.inline.generated.h
[ 23%] Generating ../../include/grid_defs.h.inline.generated.h
[ 23%] Generating auto/hashtab.c.generated.h, ../../include/hashtab.h.generated.h
[ 23%] Generating ../../include/hashtab.h.inline.generated.h
[ 23%] Generating ../../include/hashtab_defs.h.inline.generated.h
[ 28%] Generating auto/help.c.generated.h, ../../include/help.h.generated.h
[ 28%] Generating ../../include/help.h.inline.generated.h
[ 28%] Generating auto/highlight.c.generated.h, ../../include/highlight.h.generated.h
[ 28%] Generating ../../include/highlight.h.inline.generated.h
[ 28%] Generating ../../include/highlight_defs.h.inline.generated.h
[ 28%] Generating auto/highlight_group.c.generated.h, ../../include/highlight_group.h.generated.h
[ 28%] Generating ../../include/highlight_group.h.inline.generated.h
[ 28%] Generating ../../include/iconv_defs.h.inline.generated.h
[ 28%] Generating auto/indent.c.generated.h, ../../include/indent.h.generated.h
[ 28%] Generating ../../include/indent.h.inline.generated.h
[ 28%] Generating auto/indent_c.c.generated.h, ../../include/indent_c.h.generated.h
[ 28%] Generating ../../include/indent_c.h.inline.generated.h
[ 28%] Generating auto/input.c.generated.h, ../../include/input.h.generated.h
[ 28%] Generating ../../include/input.h.inline.generated.h
[ 28%] Generating auto/insexpand.c.generated.h, ../../include/insexpand.h.generated.h
[ 28%] Generating ../../include/insexpand.h.inline.generated.h
[ 28%] Generating auto/keycodes.c.generated.h, ../../include/keycodes.h.generated.h
[ 28%] Generating ../../include/keycodes.h.inline.generated.h
[ 28%] Generating ../../include/lib/queue_defs.h.inline.generated.h
[ 28%] Generating auto/linematch.c.generated.h, ../../include/linematch.h.generated.h
[ 28%] Generating ../../include/linematch.h.inline.generated.h
[ 28%] Generating auto/log.c.generated.h, ../../include/log.h.generated.h
[ 28%] Generating ../../include/log.h.inline.generated.h
[ 28%] Generating auto/lua/api_wrappers.c.generated.h, ../../include/lua/api_wrappers.h.generated.h
[ 28%] Generating auto/lua/base64.c.generated.h, ../../include/lua/base64.h.generated.h
[ 28%] Generating ../../include/lua/base64.h.inline.generated.h
[ 28%] Generating auto/lua/converter.c.generated.h, ../../include/lua/converter.h.generated.h
[ 28%] Generating ../../include/lua/converter.h.inline.generated.h
[ 28%] Generating auto/lua/executor.c.generated.h, ../../include/lua/executor.h.generated.h
[ 28%] Generating ../../include/lua/executor.h.inline.generated.h
[ 28%] Generating auto/lua/secure.c.generated.h, ../../include/lua/secure.h.generated.h
[ 28%] Generating ../../include/lua/secure.h.inline.generated.h
[ 28%] Generating auto/lua/spell.c.generated.h, ../../include/lua/spell.h.generated.h
[ 28%] Generating ../../include/lua/spell.h.inline.generated.h
[ 28%] Generating auto/lua/stdlib.c.generated.h, ../../include/lua/stdlib.h.generated.h
[ 28%] Generating ../../include/lua/stdlib.h.inline.generated.h
[ 28%] Generating auto/lua/treesitter.c.generated.h, ../../include/lua/treesitter.h.generated.h
[ 28%] Generating ../../include/lua/treesitter.h.inline.generated.h
[ 28%] Generating auto/lua/xdiff.c.generated.h, ../../include/lua/xdiff.h.generated.h
[ 28%] Generating ../../include/lua/xdiff.h.inline.generated.h
[ 28%] Generating ../../include/macros_defs.h.inline.generated.h
[ 28%] Generating auto/main.c.generated.h, ../../include/main.h.generated.h
[ 28%] Generating ../../include/main.h.inline.generated.h
[ 28%] Generating auto/map.c.generated.h, ../../include/map.h.generated.h
[ 28%] Generating ../../include/map_defs.h.inline.generated.h
[ 28%] Generating auto/map_glyph_cache.c.generated.h, ../../include/map_glyph_cache.h.generated.h
[ 28%] Generating auto/mapping.c.generated.h, ../../include/mapping.h.generated.h
[ 33%] Generating ../../include/mapping.h.inline.generated.h
[ 33%] Generating ../../include/mapping_defs.h.inline.generated.h
[ 33%] Generating auto/mark.c.generated.h, ../../include/mark.h.generated.h
[ 33%] Generating ../../include/mark.h.inline.generated.h
[ 33%] Generating ../../include/mark_defs.h.inline.generated.h
[ 33%] Generating auto/marktree.c.generated.h, ../../include/marktree.h.generated.h
[ 33%] Generating ../../include/marktree.h.inline.generated.h
[ 33%] Generating ../../include/marktree_defs.h.inline.generated.h
[ 33%] Generating auto/match.c.generated.h, ../../include/match.h.generated.h
[ 33%] Generating ../../include/match.h.inline.generated.h
[ 33%] Generating auto/math.c.generated.h, ../../include/math.h.generated.h
[ 33%] Generating ../../include/math.h.inline.generated.h
[ 33%] Generating auto/mbyte.c.generated.h, ../../include/mbyte.h.generated.h
[ 33%] Generating ../../include/mbyte.h.inline.generated.h
[ 33%] Generating ../../include/mbyte_defs.h.inline.generated.h
[ 33%] Generating auto/memfile.c.generated.h, ../../include/memfile.h.generated.h
[ 33%] Generating ../../include/memfile.h.inline.generated.h
[ 33%] Generating ../../include/memfile_defs.h.inline.generated.h
[ 33%] Generating auto/memline.c.generated.h, ../../include/memline.h.generated.h
[ 33%] Generating ../../include/memline.h.inline.generated.h
[ 33%] Generating ../../include/memline_defs.h.inline.generated.h
[ 33%] Generating auto/memory.c.generated.h, ../../include/memory.h.generated.h
[ 33%] Generating ../../include/memory.h.inline.generated.h
[ 33%] Generating ../../include/memory_defs.h.inline.generated.h
[ 33%] Generating auto/menu.c.generated.h, ../../include/menu.h.generated.h
[ 33%] Generating ../../include/menu.h.inline.generated.h
[ 33%] Generating ../../include/menu_defs.h.inline.generated.h
[ 33%] Generating auto/message.c.generated.h, ../../include/message.h.generated.h
[ 33%] Generating ../../include/message.h.inline.generated.h
[ 33%] Generating ../../include/message_defs.h.inline.generated.h
[ 33%] Generating auto/mouse.c.generated.h, ../../include/mouse.h.generated.h
[ 33%] Generating ../../include/mouse.h.inline.generated.h
[ 38%] Generating auto/move.c.generated.h, ../../include/move.h.generated.h
[ 38%] Generating ../../include/move.h.inline.generated.h
[ 38%] Generating auto/msgpack_rpc/channel.c.generated.h, ../../include/msgpack_rpc/channel.h.generated.h
[ 38%] Generating ../../include/msgpack_rpc/channel.h.inline.generated.h
[ 38%] Generating ../../include/msgpack_rpc/channel_defs.h.inline.generated.h
[ 38%] Generating auto/msgpack_rpc/packer.c.generated.h, ../../include/msgpack_rpc/packer.h.generated.h
[ 38%] Generating ../../include/msgpack_rpc/packer.h.inline.generated.h
[ 38%] Generating ../../include/msgpack_rpc/packer_defs.h.inline.generated.h
[ 38%] Generating auto/msgpack_rpc/server.c.generated.h, ../../include/msgpack_rpc/server.h.generated.h
[ 38%] Generating ../../include/msgpack_rpc/server.h.inline.generated.h
[ 38%] Generating auto/msgpack_rpc/unpacker.c.generated.h, ../../include/msgpack_rpc/unpacker.h.generated.h
[ 38%] Generating ../../include/msgpack_rpc/unpacker.h.inline.generated.h
[ 38%] Generating auto/normal.c.generated.h, ../../include/normal.h.generated.h
[ 38%] Generating ../../include/normal.h.inline.generated.h
[ 38%] Generating ../../include/normal_defs.h.inline.generated.h
[ 38%] Generating auto/ops.c.generated.h, ../../include/ops.h.generated.h
[ 38%] Generating ../../include/ops.h.inline.generated.h
[ 38%] Generating auto/option.c.generated.h, ../../include/option.h.generated.h
[ 38%] Generating ../../include/option.h.inline.generated.h
[ 38%] Generating ../../include/option_defs.h.inline.generated.h
[ 38%] Generating ../../include/option_vars.h.inline.generated.h
[ 38%] Generating auto/optionstr.c.generated.h, ../../include/optionstr.h.generated.h
[ 42%] Generating ../../include/optionstr.h.inline.generated.h
[ 42%] Generating auto/os/dl.c.generated.h, ../../include/os/dl.h.generated.h
[ 42%] Generating ../../include/os/dl.h.inline.generated.h
[ 42%] Generating auto/os/env.c.generated.h, ../../include/os/env.h.generated.h
[ 42%] Generating auto/os/fileio.c.generated.h, ../../include/os/fileio.h.generated.h
[ 42%] Generating ../../include/os/fileio.h.inline.generated.h
[ 42%] Generating ../../include/os/fileio_defs.h.inline.generated.h
[ 42%] Generating auto/os/fs.c.generated.h, ../../include/os/fs.h.generated.h
[ 42%] Generating ../../include/os/fs.h.inline.generated.h
[ 42%] Generating ../../include/os/fs_defs.h.inline.generated.h
[ 42%] Generating auto/os/input.c.generated.h, ../../include/os/input.h.generated.h
[ 42%] Generating ../../include/os/input.h.inline.generated.h
[ 42%] Generating auto/os/lang.c.generated.h, ../../include/os/lang.h.generated.h
[ 42%] Generating ../../include/os/lang.h.inline.generated.h
[ 42%] Generating auto/os/mem.c.generated.h, ../../include/os/mem.h.generated.h
[ 42%] Generating ../../include/os/os.h.inline.generated.h
[ 42%] Generating ../../include/os/os_defs.h.inline.generated.h
[ 42%] Generating ../../include/os/os_win_console.h.inline.generated.h
[ 42%] Generating auto/os/proc.c.generated.h, ../../include/os/proc.h.generated.h
[ 42%] Generating ../../include/os/proc.h.inline.generated.h
[ 42%] Generating ../../include/os/pty_conpty_win.h.inline.generated.h
[ 42%] Generating ../../include/os/pty_proc.h.inline.generated.h
[ 42%] Generating auto/os/pty_proc_unix.c.generated.h, ../../include/os/pty_proc_unix.h.generated.h
[ 42%] Generating ../../include/os/pty_proc_unix.h.inline.generated.h
[ 42%] Generating ../../include/os/pty_proc_win.h.inline.generated.h
[ 42%] Generating auto/os/shell.c.generated.h, ../../include/os/shell.h.generated.h
[ 42%] Generating ../../include/os/shell.h.inline.generated.h
[ 42%] Generating auto/os/signal.c.generated.h, ../../include/os/signal.h.generated.h
[ 42%] Generating ../../include/os/signal.h.inline.generated.h
[ 42%] Generating auto/os/stdpaths.c.generated.h, ../../include/os/stdpaths.h.generated.h
[ 42%] Generating ../../include/os/stdpaths_defs.h.inline.generated.h
[ 42%] Generating auto/os/time.c.generated.h, ../../include/os/time.h.generated.h
[ 42%] Generating ../../include/os/time.h.inline.generated.h
[ 42%] Generating ../../include/os/time_defs.h.inline.generated.h
[ 42%] Generating ../../include/os/unix_defs.h.inline.generated.h
[ 42%] Generating auto/os/users.c.generated.h, ../../include/os/users.h.generated.h
[ 42%] Generating auto/path.c.generated.h, ../../include/path.h.generated.h
[ 42%] Generating ../../include/path.h.inline.generated.h
[ 42%] Generating auto/plines.c.generated.h, ../../include/plines.h.generated.h
[ 42%] Generating ../../include/plines.h.inline.generated.h
[ 42%] Generating auto/popupmenu.c.generated.h, ../../include/popupmenu.h.generated.h
[ 42%] Generating ../../include/popupmenu.h.inline.generated.h
[ 42%] Generating ../../include/pos_defs.h.inline.generated.h
[ 42%] Generating auto/profile.c.generated.h, ../../include/profile.h.generated.h
[ 42%] Generating ../../include/profile.h.inline.generated.h
[ 42%] Generating auto/quickfix.c.generated.h, ../../include/quickfix.h.generated.h
[ 42%] Generating ../../include/quickfix.h.inline.generated.h
[ 42%] Generating auto/regexp.c.generated.h, ../../include/regexp.h.generated.h
[ 42%] Generating ../../include/regexp.h.inline.generated.h
[ 42%] Generating ../../include/regexp_defs.h.inline.generated.h
[ 42%] Generating auto/register.c.generated.h, ../../include/register.h.generated.h
[ 42%] Generating ../../include/register.h.inline.generated.h
[ 42%] Generating ../../include/register_defs.h.inline.generated.h
[ 42%] Generating auto/runtime.c.generated.h, ../../include/runtime.h.generated.h
[ 42%] Generating ../../include/runtime.h.inline.generated.h
[ 42%] Generating ../../include/runtime_defs.h.inline.generated.h
[ 42%] Generating auto/search.c.generated.h, ../../include/search.h.generated.h
[ 47%] Generating ../../include/search.h.inline.generated.h
[ 47%] Generating auto/sha256.c.generated.h, ../../include/sha256.h.generated.h
[ 47%] Generating ../../include/sha256.h.inline.generated.h
[ 47%] Generating auto/shada.c.generated.h, ../../include/shada.h.generated.h
[ 47%] Generating ../../include/shada.h.inline.generated.h
[ 52%] Generating auto/sign.c.generated.h, ../../include/sign.h.generated.h
[ 52%] Generating ../../include/sign.h.inline.generated.h
[ 52%] Generating ../../include/sign_defs.h.inline.generated.h
[ 52%] Generating auto/spell.c.generated.h, ../../include/spell.h.generated.h
[ 52%] Generating ../../include/spell.h.inline.generated.h
[ 52%] Generating ../../include/spell_defs.h.inline.generated.h
[ 52%] Generating auto/spellfile.c.generated.h, ../../include/spellfile.h.generated.h
[ 52%] Generating ../../include/spellfile.h.inline.generated.h
[ 52%] Generating auto/spellsuggest.c.generated.h, ../../include/spellsuggest.h.generated.h
[ 52%] Generating ../../include/spellsuggest.h.inline.generated.h
[ 52%] Generating auto/state.c.generated.h, ../../include/state.h.generated.h
[ 52%] Generating ../../include/state.h.inline.generated.h
[ 52%] Generating ../../include/state_defs.h.inline.generated.h
[ 52%] Generating auto/statusline.c.generated.h, ../../include/statusline.h.generated.h
[ 52%] Generating ../../include/statusline.h.inline.generated.h
[ 52%] Generating ../../include/statusline_defs.h.inline.generated.h
[ 52%] Generating auto/strings.c.generated.h, ../../include/strings.h.generated.h
[ 52%] Generating ../../include/strings.h.inline.generated.h
[ 52%] Generating auto/syntax.c.generated.h, ../../include/syntax.h.generated.h
[ 52%] Generating ../../include/syntax.h.inline.generated.h
[ 52%] Generating ../../include/syntax_defs.h.inline.generated.h
[ 52%] Generating auto/tag.c.generated.h, ../../include/tag.h.generated.h
[ 52%] Generating ../../include/tag.h.inline.generated.h
[ 52%] Generating auto/terminal.c.generated.h, ../../include/terminal.h.generated.h
[ 52%] Generating ../../include/terminal.h.inline.generated.h
[ 52%] Generating auto/testing.c.generated.h, ../../include/testing.h.generated.h
[ 52%] Generating ../../include/testing.h.inline.generated.h
[ 52%] Generating auto/textformat.c.generated.h, ../../include/textformat.h.generated.h
[ 52%] Generating ../../include/textformat.h.inline.generated.h
[ 52%] Generating auto/textobject.c.generated.h, ../../include/textobject.h.generated.h
[ 52%] Generating ../../include/textobject.h.inline.generated.h
[ 52%] Generating auto/tui/input.c.generated.h, ../../include/tui/input.h.generated.h
[ 52%] Generating ../../include/tui/input.h.inline.generated.h
[ 52%] Generating ../../include/tui/input_defs.h.inline.generated.h
[ 52%] Generating auto/tui/terminfo.c.generated.h, ../../include/tui/terminfo.h.generated.h
[ 52%] Generating ../../include/tui/terminfo.h.inline.generated.h
[ 52%] Generating ../../include/tui/terminfo_builtin.h.inline.generated.h
[ 52%] Generating ../../include/tui/terminfo_defs.h.inline.generated.h
[ 52%] Generating ../../include/tui/terminfo_enum_defs.h.inline.generated.h
[ 52%] Generating auto/tui/termkey/driver-csi.c.generated.h, ../../include/tui/termkey/driver-csi.h.generated.h
[ 52%] Generating ../../include/tui/termkey/driver-csi.h.inline.generated.h
[ 52%] Generating auto/tui/termkey/driver-ti.c.generated.h, ../../include/tui/termkey/driver-ti.h.generated.h
[ 52%] Generating ../../include/tui/termkey/driver-ti.h.inline.generated.h
[ 52%] Generating ../../include/tui/termkey/termkey-internal.h.inline.generated.h
[ 52%] Generating auto/tui/termkey/termkey.c.generated.h, ../../include/tui/termkey/termkey.h.generated.h
[ 52%] Generating ../../include/tui/termkey/termkey.h.inline.generated.h
[ 52%] Generating ../../include/tui/termkey/termkey_defs.h.inline.generated.h
[ 52%] Generating auto/tui/tui.c.generated.h, ../../include/tui/tui.h.generated.h
[ 52%] Generating ../../include/tui/tui.h.inline.generated.h
[ 52%] Generating ../../include/tui/tui_defs.h.inline.generated.h
[ 52%] Generating auto/tui/ugrid.c.generated.h, ../../include/tui/ugrid.h.generated.h
[ 57%] Generating ../../include/tui/ugrid.h.inline.generated.h
[ 57%] Generating ../../include/types_defs.h.inline.generated.h
[ 57%] Generating auto/ui.c.generated.h, ../../include/ui.h.generated.h
[ 57%] Generating ../../include/ui.h.inline.generated.h
[ 57%] Generating auto/ui_client.c.generated.h, ../../include/ui_client.h.generated.h
[ 57%] Generating ../../include/ui_client.h.inline.generated.h
[ 57%] Generating auto/ui_compositor.c.generated.h, ../../include/ui_compositor.h.generated.h
[ 57%] Generating ../../include/ui_compositor.h.inline.generated.h
[ 57%] Generating ../../include/ui_defs.h.inline.generated.h
[ 57%] Generating auto/ui_events_call.c.generated.h, ../../include/ui_events_call.h.generated.h
[ 57%] Generating auto/ui_events_client.c.generated.h, ../../include/ui_events_client.h.generated.h
[ 57%] Generating auto/ui_events_remote.c.generated.h, ../../include/ui_events_remote.h.generated.h
[ 57%] Generating auto/undo.c.generated.h, ../../include/undo.h.generated.h
[ 57%] Generating ../../include/undo.h.inline.generated.h
[ 57%] Generating ../../include/undo_defs.h.inline.generated.h
[ 57%] Generating auto/usercmd.c.generated.h, ../../include/usercmd.h.generated.h
[ 57%] Generating ../../include/usercmd.h.inline.generated.h
[ 57%] Generating auto/version.c.generated.h, ../../include/version.h.generated.h
[ 57%] Generating ../../include/version.h.inline.generated.h
[ 57%] Generating ../../include/vim_defs.h.inline.generated.h
[ 57%] Generating auto/viml/parser/expressions.c.generated.h, ../../include/viml/parser/expressions.h.generated.h
[ 57%] Generating ../../include/viml/parser/expressions.h.inline.generated.h
[ 57%] Generating auto/viml/parser/parser.c.generated.h, ../../include/viml/parser/parser.h.generated.h
[ 57%] Generating ../../include/viml/parser/parser.h.inline.generated.h
[ 57%] Generating ../../include/viml/parser/parser_defs.h.inline.generated.h
[ 57%] Generating auto/vterm/encoding.c.generated.h, ../../include/vterm/encoding.h.generated.h
[ 57%] Generating ../../include/vterm/encoding.h.inline.generated.h
[ 57%] Generating auto/vterm/keyboard.c.generated.h, ../../include/vterm/keyboard.h.generated.h
[ 57%] Generating ../../include/vterm/keyboard.h.inline.generated.h
[ 57%] Generating auto/vterm/mouse.c.generated.h, ../../include/vterm/mouse.h.generated.h
[ 57%] Generating ../../include/vterm/mouse.h.inline.generated.h
[ 57%] Generating auto/vterm/parser.c.generated.h, ../../include/vterm/parser.h.generated.h
[ 57%] Generating ../../include/vterm/parser.h.inline.generated.h
[ 57%] Generating auto/vterm/pen.c.generated.h, ../../include/vterm/pen.h.generated.h
[ 57%] Generating ../../include/vterm/pen.h.inline.generated.h
[ 57%] Generating auto/vterm/screen.c.generated.h, ../../include/vterm/screen.h.generated.h
[ 57%] Generating ../../include/vterm/screen.h.inline.generated.h
[ 61%] Generating auto/vterm/state.c.generated.h, ../../include/vterm/state.h.generated.h
[ 61%] Generating ../../include/vterm/state.h.inline.generated.h
[ 61%] Generating auto/vterm/vterm.c.generated.h, ../../include/vterm/vterm.h.generated.h
[ 61%] Generating ../../include/vterm/vterm.h.inline.generated.h
[ 61%] Generating ../../include/vterm/vterm_defs.h.inline.generated.h
[ 61%] Generating ../../include/vterm/vterm_internal_defs.h.inline.generated.h
[ 61%] Generating ../../include/vterm/vterm_keycodes_defs.h.inline.generated.h
[ 61%] Generating auto/window.c.generated.h, ../../include/window.h.generated.h
[ 61%] Generating ../../include/window.h.inline.generated.h
[ 61%] Generating auto/winfloat.c.generated.h, ../../include/winfloat.h.generated.h
[ 61%] Generating ../../include/winfloat.h.inline.generated.h
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[ 61%] Generating auto/event/multiqueue.c.generated.h, ../../include/event/multiqueue.h.generated.h
[ 61%] Generating ../../include/lib/queue_defs.h.inline.generated.h
[ 61%] Generating auto/memory.c.generated.h, ../../include/memory.h.generated.h
[ 61%] Generating auto/os/time.c.generated.h, ../../include/os/time.h.generated.h
[ 61%] Generating ../../include/api/private/defs.h.inline.generated.h
[ 61%] Generating auto/grid.c.generated.h, ../../include/grid.h.generated.h
[ 61%] Generating auto/log.c.generated.h, ../../include/log.h.generated.h
[ 61%] Generating ../../include/mark_defs.h.inline.generated.h
[ 61%] Generating auto/mbyte.c.generated.h, ../../include/mbyte.h.generated.h
[ 61%] Generating ../../include/mbyte.h.inline.generated.h
[ 61%] Generating auto/vterm/pen.c.generated.h, ../../include/vterm/pen.h.generated.h
[ 61%] Generating auto/vterm/screen.c.generated.h, ../../include/vterm/screen.h.generated.h
[ 61%] Generating auto/vterm/vterm.c.generated.h, ../../include/vterm/vterm.h.generated.h
[ 61%] Generating auto/api/autocmd.c.generated.h, ../../include/api/autocmd.h.generated.h
[ 61%] Generating auto/api/private/dispatch.c.generated.h, ../../include/api/private/dispatch.h.generated.h
[ 61%] Generating auto/api/buffer.c.generated.h, ../../include/api/buffer.h.generated.h
[ 61%] Generating auto/api/command.c.generated.h, ../../include/api/command.h.generated.h
[ 61%] Generating auto/api/deprecated.c.generated.h, ../../include/api/deprecated.h.generated.h
[ 61%] Generating auto/api/events.c.generated.h, ../../include/api/events.h.generated.h
[ 61%] Generating auto/api/extmark.c.generated.h, ../../include/api/extmark.h.generated.h
[ 61%] Generating auto/api/options.c.generated.h, ../../include/api/options.h.generated.h
[ 61%] Generating auto/api/tabpage.c.generated.h, ../../include/api/tabpage.h.generated.h
[ 61%] Generating auto/api/ui.c.generated.h, ../../include/api/ui.h.generated.h
[ 61%] Generating auto/api/vim.c.generated.h, ../../include/api/vim.h.generated.h
[ 61%] Generating auto/api/vimscript.c.generated.h, ../../include/api/vimscript.h.generated.h
[ 61%] Generating auto/api/win_config.c.generated.h, ../../include/api/win_config.h.generated.h
[ 61%] Generating auto/api/window.c.generated.h, ../../include/api/window.h.generated.h
[ 61%] Generating auto/api/private/dispatch_wrappers.c.generated.h, ../../include/api/private/dispatch_wrappers.h.generated.h
[ 61%] Generating auto/api/private/helpers.c.generated.h, ../../include/api/private/helpers.h.generated.h
[ 61%] Generating auto/api/private/validate.c.generated.h, ../../include/api/private/validate.h.generated.h
[ 61%] Generating ../../include/ascii_defs.h.inline.generated.h
[ 61%] Generating auto/autocmd.c.generated.h, ../../include/autocmd.h.generated.h
[ 61%] Generating auto/buffer.c.generated.h, ../../include/buffer.h.generated.h
[ 61%] Generating ../../include/buffer.h.inline.generated.h
[ 61%] Generating auto/eval/typval.c.generated.h, ../../include/eval/typval.h.generated.h
[ 61%] Generating ../../include/eval/typval.h.inline.generated.h
[ 61%] Generating auto/event/loop.c.generated.h, ../../include/event/loop.h.generated.h
[ 61%] Generating auto/hashtab.c.generated.h, ../../include/hashtab.h.generated.h
[ 61%] Generating auto/lua/executor.c.generated.h, ../../include/lua/executor.h.generated.h
[ 61%] Generating auto/message.c.generated.h, ../../include/message.h.generated.h
[ 61%] Generating auto/strings.c.generated.h, ../../include/strings.h.generated.h
[ 61%] Generating ../../include/strings.h.inline.generated.h
[ 61%] Generating auto/usercmd.c.generated.h, ../../include/usercmd.h.generated.h
[ 61%] Generating auto/buffer_updates.c.generated.h, ../../include/buffer_updates.h.generated.h
[ 61%] Generating auto/change.c.generated.h, ../../include/change.h.generated.h
[ 61%] Generating auto/cursor.c.generated.h, ../../include/cursor.h.generated.h
[ 61%] Generating auto/ex_cmds.c.generated.h, ../../include/ex_cmds.h.generated.h
[ 61%] Generating auto/extmark.c.generated.h, ../../include/extmark.h.generated.h
[ 61%] Generating auto/mapping.c.generated.h, ../../include/mapping.h.generated.h
[ 61%] Generating auto/mark.c.generated.h, ../../include/mark.h.generated.h
[ 61%] Generating ../../include/mark.h.inline.generated.h
[ 61%] Generating auto/memline.c.generated.h, ../../include/memline.h.generated.h
[ 61%] Generating auto/move.c.generated.h, ../../include/move.h.generated.h
[ 61%] Generating auto/ops.c.generated.h, ../../include/ops.h.generated.h
[ 61%] Generating ../../include/ops.h.inline.generated.h
[ 61%] Generating auto/undo.c.generated.h, ../../include/undo.h.generated.h
[ 61%] Generating auto/charset.c.generated.h, ../../include/charset.h.generated.h
[ 61%] Generating ../../include/charset.h.inline.generated.h
[ 61%] Generating auto/ex_docmd.c.generated.h, ../../include/ex_docmd.h.generated.h
[ 61%] Generating auto/ex_eval.c.generated.h, ../../include/ex_eval.h.generated.h
[ 61%] Generating auto/garray.c.generated.h, ../../include/garray.h.generated.h
[ 61%] Generating auto/regexp.c.generated.h, ../../include/regexp.h.generated.h
[ 61%] Generating auto/register.c.generated.h, ../../include/register.h.generated.h
[ 61%] Generating ../../include/register.h.inline.generated.h
[ 61%] Generating auto/window.c.generated.h, ../../include/window.h.generated.h
[ 61%] Generating auto/decoration.c.generated.h, ../../include/decoration.h.generated.h
[ 61%] Generating ../../include/decoration.h.inline.generated.h
[ 61%] Generating auto/eval/vars.c.generated.h, ../../include/eval/vars.h.generated.h
[ 61%] Generating auto/highlight.c.generated.h, ../../include/highlight.h.generated.h
[ 61%] Generating auto/highlight_group.c.generated.h, ../../include/highlight_group.h.generated.h
[ 61%] Generating auto/marktree.c.generated.h, ../../include/marktree.h.generated.h
[ 61%] Generating auto/option.c.generated.h, ../../include/option.h.generated.h
[ 61%] Generating auto/api/private/converter.c.generated.h, ../../include/api/private/converter.h.generated.h
[ 61%] Generating auto/channel.c.generated.h, ../../include/channel.h.generated.h
[ 61%] Generating ../../include/channel.h.inline.generated.h
[ 61%] Generating auto/event/libuv_proc.c.generated.h, ../../include/event/libuv_proc.h.generated.h
[ 61%] Generating auto/main.c.generated.h, ../../include/main.h.generated.h
[ 61%] Generating auto/msgpack_rpc/channel.c.generated.h, ../../include/msgpack_rpc/channel.h.generated.h
[ 61%] Generating auto/msgpack_rpc/packer.c.generated.h, ../../include/msgpack_rpc/packer.h.generated.h
[ 61%] Generating auto/os/pty_proc_unix.c.generated.h, ../../include/os/pty_proc_unix.h.generated.h
[ 61%] Generating auto/ui.c.generated.h, ../../include/ui.h.generated.h
[ 61%] Generating auto/ui_events_call.c.generated.h, ../../include/ui_events_call.h.generated.h
[ 61%] Generating auto/ui_events_remote.c.generated.h, ../../include/ui_events_remote.h.generated.h
[ 61%] Generating auto/decoration_provider.c.generated.h, ../../include/decoration_provider.h.generated.h
[ 61%] Generating auto/drawscreen.c.generated.h, ../../include/drawscreen.h.generated.h
[ 61%] Generating auto/sign.c.generated.h, ../../include/sign.h.generated.h
[ 61%] Generating auto/eval.c.generated.h, ../../include/eval.h.generated.h
[ 61%] Generating auto/eval/decode.c.generated.h, ../../include/eval/decode.h.generated.h
[ 61%] Generating auto/eval/encode.c.generated.h, ../../include/eval/encode.h.generated.h
[ 61%] Generating ../../include/eval/typval_encode.h.inline.generated.h
[ 61%] Generating auto/eval/userfunc.c.generated.h, ../../include/eval/userfunc.h.generated.h
[ 61%] Generating ../../include/os/fileio_defs.h.inline.generated.h
[ 61%] Generating auto/ex_getln.c.generated.h, ../../include/ex_getln.h.generated.h
[ 61%] Generating auto/ui_client.c.generated.h, ../../include/ui_client.h.generated.h
[ 61%] Generating auto/ui_events_client.c.generated.h, ../../include/ui_events_client.h.generated.h
[ 61%] Generating auto/msgpack_rpc/unpacker.c.generated.h, ../../include/msgpack_rpc/unpacker.h.generated.h
[ 61%] Generating auto/runtime.c.generated.h, ../../include/runtime.h.generated.h
[ 61%] Generating auto/event/wstream.c.generated.h, ../../include/event/wstream.h.generated.h
[ 61%] Generating auto/context.c.generated.h, ../../include/context.h.generated.h
[ 61%] Generating auto/drawline.c.generated.h, ../../include/drawline.h.generated.h
[ 61%] Generating auto/fold.c.generated.h, ../../include/fold.h.generated.h
[ 61%] Generating auto/getchar.c.generated.h, ../../include/getchar.h.generated.h
[ 61%] Generating auto/insexpand.c.generated.h, ../../include/insexpand.h.generated.h
[ 61%] Generating auto/keycodes.c.generated.h, ../../include/keycodes.h.generated.h
[ 61%] Generating auto/lua/treesitter.c.generated.h, ../../include/lua/treesitter.h.generated.h
[ 61%] Generating auto/math.c.generated.h, ../../include/math.h.generated.h
[ 61%] Generating auto/normal.c.generated.h, ../../include/normal.h.generated.h
[ 61%] Generating auto/optionstr.c.generated.h, ../../include/optionstr.h.generated.h
[ 61%] Generating auto/os/input.c.generated.h, ../../include/os/input.h.generated.h
[ 61%] Generating auto/os/proc.c.generated.h, ../../include/os/proc.h.generated.h
[ 61%] Generating auto/popupmenu.c.generated.h, ../../include/popupmenu.h.generated.h
[ 61%] Generating auto/state.c.generated.h, ../../include/state.h.generated.h
[ 61%] Generating auto/statusline.c.generated.h, ../../include/statusline.h.generated.h
[ 61%] Generating auto/terminal.c.generated.h, ../../include/terminal.h.generated.h
[ 61%] Generating auto/viml/parser/expressions.c.generated.h, ../../include/viml/parser/expressions.h.generated.h
[ 61%] Generating auto/viml/parser/parser.c.generated.h, ../../include/viml/parser/parser.h.generated.h
[ 61%] Generating ../../include/viml/parser/parser.h.inline.generated.h
[ 61%] Generating auto/eval/window.c.generated.h, ../../include/eval/window.h.generated.h
[ 61%] Generating auto/syntax.c.generated.h, ../../include/syntax.h.generated.h
[ 61%] Generating auto/ui_compositor.c.generated.h, ../../include/ui_compositor.h.generated.h
[ 61%] Generating auto/winfloat.c.generated.h, ../../include/winfloat.h.generated.h
[ 61%] Generating auto/plines.c.generated.h, ../../include/plines.h.generated.h
[ 61%] Generating ../../include/plines.h.inline.generated.h
[ 61%] Generating auto/arabic.c.generated.h, ../../include/arabic.h.generated.h
[ 61%] Generating auto/arglist.c.generated.h, ../../include/arglist.h.generated.h
[ 61%] Generating auto/ex_cmds2.c.generated.h, ../../include/ex_cmds2.h.generated.h
[ 61%] Generating auto/fileio.c.generated.h, ../../include/fileio.h.generated.h
[ 61%] Generating auto/path.c.generated.h, ../../include/path.h.generated.h
[ 61%] Generating auto/version.c.generated.h, ../../include/version.h.generated.h
[ 61%] Generating auto/os/env.c.generated.h, ../../include/os/env.h.generated.h
[ 61%] Generating auto/os/mem.c.generated.h, ../../include/os/mem.h.generated.h
[ 61%] Generating auto/os/stdpaths.c.generated.h, ../../include/os/stdpaths.h.generated.h
[ 61%] Generating auto/os/users.c.generated.h, ../../include/os/users.h.generated.h
[ 61%] Generating auto/profile.c.generated.h, ../../include/profile.h.generated.h
[ 61%] Generating auto/search.c.generated.h, ../../include/search.h.generated.h
[ 61%] Generating auto/base64.c.generated.h, ../../include/base64.h.generated.h
[ 61%] Generating auto/cmdexpand.c.generated.h, ../../include/cmdexpand.h.generated.h
[ 61%] Generating auto/diff.c.generated.h, ../../include/diff.h.generated.h
[ 61%] Generating auto/digraph.c.generated.h, ../../include/digraph.h.generated.h
[ 61%] Generating auto/file_search.c.generated.h, ../../include/file_search.h.generated.h
[ 61%] Generating auto/fuzzy.c.generated.h, ../../include/fuzzy.h.generated.h
[ 61%] Generating auto/help.c.generated.h, ../../include/help.h.generated.h
[ 61%] Generating auto/indent.c.generated.h, ../../include/indent.h.generated.h
[ 61%] Generating auto/indent_c.c.generated.h, ../../include/indent_c.h.generated.h
[ 61%] Generating auto/os/fs.c.generated.h, ../../include/os/fs.h.generated.h
[ 61%] Generating auto/quickfix.c.generated.h, ../../include/quickfix.h.generated.h
[ 61%] Generating auto/spell.c.generated.h, ../../include/spell.h.generated.h
[ 61%] Generating auto/bufwrite.c.generated.h, ../../include/bufwrite.h.generated.h
[ 61%] Generating auto/input.c.generated.h, ../../include/input.h.generated.h
[ 61%] Generating auto/sha256.c.generated.h, ../../include/sha256.h.generated.h
[ 61%] Generating auto/edit.c.generated.h, ../../include/edit.h.generated.h
[ 61%] Generating auto/textformat.c.generated.h, ../../include/textformat.h.generated.h
[ 61%] Generating auto/event/proc.c.generated.h, ../../include/event/proc.h.generated.h
[ 61%] Generating auto/event/rstream.c.generated.h, ../../include/event/rstream.h.generated.h
[ 61%] Generating auto/event/socket.c.generated.h, ../../include/event/socket.h.generated.h
[ 61%] Generating auto/event/stream.c.generated.h, ../../include/event/stream.h.generated.h
[ 61%] Generating auto/msgpack_rpc/server.c.generated.h, ../../include/msgpack_rpc/server.h.generated.h
[ 61%] Generating auto/os/shell.c.generated.h, ../../include/os/shell.h.generated.h
[ 61%] Generating auto/clipboard.c.generated.h, ../../include/clipboard.h.generated.h
[ 61%] Generating auto/cmdhist.c.generated.h, ../../include/cmdhist.h.generated.h
[ 61%] Generating auto/eval/funcs.c.generated.h, ../../include/eval/funcs.h.generated.h
[ 61%] Generating auto/menu.c.generated.h, ../../include/menu.h.generated.h
[ 61%] Generating auto/os/lang.c.generated.h, ../../include/os/lang.h.generated.h
[ 61%] Generating auto/tag.c.generated.h, ../../include/tag.h.generated.h
[ 61%] Generating auto/shada.c.generated.h, ../../include/shada.h.generated.h
[ 61%] Generating auto/cursor_shape.c.generated.h, ../../include/cursor_shape.h.generated.h
[ 61%] Generating auto/debugger.c.generated.h, ../../include/debugger.h.generated.h
[ 61%] Generating auto/linematch.c.generated.h, ../../include/linematch.h.generated.h
[ 61%] Generating auto/match.c.generated.h, ../../include/match.h.generated.h
[ 61%] Generating auto/mouse.c.generated.h, ../../include/mouse.h.generated.h
[ 61%] Generating auto/textobject.c.generated.h, ../../include/textobject.h.generated.h
[ 61%] Generating auto/eval/executor.c.generated.h, ../../include/eval/executor.h.generated.h
[ 61%] Generating auto/eval/gc.c.generated.h, ../../include/eval/gc.h.generated.h
[ 61%] Generating auto/event/time.c.generated.h, ../../include/event/time.h.generated.h
[ 61%] Generating auto/eval/buffer.c.generated.h, ../../include/eval/buffer.h.generated.h
[ 61%] Generating auto/eval/deprecated.c.generated.h, ../../include/eval/deprecated.h.generated.h
[ 61%] Generating auto/eval/fs.c.generated.h, ../../include/eval/fs.h.generated.h
[ 61%] Generating auto/os/fileio.c.generated.h, ../../include/os/fileio.h.generated.h
[ 61%] Generating auto/eval/list.c.generated.h, ../../include/eval/list.h.generated.h
[ 61%] Generating auto/os/dl.c.generated.h, ../../include/os/dl.h.generated.h
[ 61%] Generating auto/spellsuggest.c.generated.h, ../../include/spellsuggest.h.generated.h
[ 61%] Generating auto/testing.c.generated.h, ../../include/testing.h.generated.h
[ 61%] Generating auto/event/signal.c.generated.h, ../../include/event/signal.h.generated.h
[ 61%] Generating auto/ex_session.c.generated.h, ../../include/ex_session.h.generated.h
[ 61%] Generating auto/lua/secure.c.generated.h, ../../include/lua/secure.h.generated.h
[ 61%] Generating auto/spellfile.c.generated.h, ../../include/spellfile.h.generated.h
[ 61%] Generating auto/memfile.c.generated.h, ../../include/memfile.h.generated.h
[ 61%] Generating auto/lua/converter.c.generated.h, ../../include/lua/converter.h.generated.h
[ 61%] Generating auto/lua/base64.c.generated.h, ../../include/lua/base64.h.generated.h
[ 61%] Generating auto/lua/stdlib.c.generated.h, ../../include/lua/stdlib.h.generated.h
[ 61%] Generating auto/lua/spell.c.generated.h, ../../include/lua/spell.h.generated.h
[ 61%] Generating auto/lua/xdiff.c.generated.h, ../../include/lua/xdiff.h.generated.h
[ 61%] Generating auto/os/signal.c.generated.h, ../../include/os/signal.h.generated.h
[ 61%] Generating auto/vterm/keyboard.c.generated.h, ../../include/vterm/keyboard.h.generated.h
[ 61%] Generating auto/vterm/mouse.c.generated.h, ../../include/vterm/mouse.h.generated.h
[ 61%] Generating auto/vterm/parser.c.generated.h, ../../include/vterm/parser.h.generated.h
[ 61%] Generating auto/vterm/state.c.generated.h, ../../include/vterm/state.h.generated.h
[ 61%] Generating auto/tui/input.c.generated.h, ../../include/tui/input.h.generated.h
[ 61%] Generating auto/tui/termkey/driver-csi.c.generated.h, ../../include/tui/termkey/driver-csi.h.generated.h
[ 61%] Generating auto/tui/termkey/termkey.c.generated.h, ../../include/tui/termkey/termkey.h.generated.h
[ 61%] Generating auto/tui/tui.c.generated.h, ../../include/tui/tui.h.generated.h
[ 61%] Generating auto/tui/terminfo.c.generated.h, ../../include/tui/terminfo.h.generated.h
[ 61%] Generating auto/tui/termkey/driver-ti.c.generated.h, ../../include/tui/termkey/driver-ti.h.generated.h
[ 61%] Generating auto/tui/ugrid.c.generated.h, ../../include/tui/ugrid.h.generated.h
[ 61%] Generating auto/vterm/encoding.c.generated.h, ../../include/vterm/encoding.h.generated.h
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[ 95%] Built target nvim_bin
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[ 95%] Built target nvim_runtime
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[ 95%] Built target nvim
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[ 95%] Built target tee
gmake[3]: Entering directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[3]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
[100%] Built target xxd
gmake[2]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
gmake[1]: Leaving directory '/home/bryan/tmp/chezmoi_build/neovim/build'
/usr/bin/cmake --install build
-- Install configuration: "Release"
Created symlink /home/bryan/.config/systemd/user/timers.target.wants/bob-ref-intake.timer → /home/bryan/.config/systemd/user/bob-ref-intake.timer.

