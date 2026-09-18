#gh:gh_bobs-org__bob-cli Can you help me fix these failures I'm seeing when running the `chezmoi update -av` command? #plan

```
>>> INSTALLING ROCK: busted

Error: Could not find Lua 5.1 in PATH.
Please set your Lua interpreter with:

   luarocks --lua-version=5.1 --local config variables.LUA </path/lua>

LuaRocks install failed for busted (exit status 1).

>>> INSTALLING ROCK: nlua

Error: Could not find Lua 5.1 in PATH.
Please set your Lua interpreter with:

   luarocks --lua-version=5.1 --local config variables.LUA </path/lua>

LuaRocks install failed for nlua (exit status 1).

>>> INSTALLING ROCK: llscheck

Error: Could not find Lua 5.1 in PATH.
Please set your Lua interpreter with:

   luarocks --lua-version=5.1 --local config variables.LUA </path/lua>

LuaRocks install failed for llscheck (exit status 1).

>>> INSTALLING ROCK: luacheck

Error: Could not find Lua 5.1 in PATH.
Please set your Lua interpreter with:

   luarocks --lua-version=5.1 --local config variables.LUA </path/lua>

LuaRocks install failed for luacheck (exit status 1).

>>> INSTALLING ROCK: luacov

Error: Could not find Lua 5.1 in PATH.
Please set your Lua interpreter with:

   luarocks --lua-version=5.1 --local config variables.LUA </path/lua>

LuaRocks install failed for luacov (exit status 1).

LuaRocks failed to install required rocks in /Users/bbugyi/.luarocks:
  - busted (exit status 1). Retry: luarocks --lua-version=5.1 install --local busted
  - nlua (exit status 1). Retry: luarocks --lua-version=5.1 install --local nlua
  - llscheck (exit status 1). Retry: luarocks --lua-version=5.1 install --local llscheck
  - luacheck (exit status 1). Retry: luarocks --lua-version=5.1 install --local luacheck
  - luacov (exit status 1). Retry: luarocks --lua-version=5.1 install --local luacov
chezmoi: .chezmoiscripts/install_luarocks: exit status 1
```