#gh:gh_bobs-org__bob-cli Can you help me improve the `bob capture` command by recognizing bulleted lists and translating each of those bullets into its own Obsidian task sub-bullet? For example, consider the `bob capture 'foo bar baz @foo %'` command if the clipboard's current contents were as follows and the command were run on 2026-07-17:
```
- Use `@` symbol instead of `#` for tribe prefix. 
- Support expansion of families within clan.
- Family members must be launched sequentially. 
```

This would then result in the following task being added to the ~/bob/foo.md file:
```
- [ ] #task foo bar baz [created::2026-07-17]
  - Use `@` symbol instead of `#` for tribe prefix. 
  - Support expansion of families within clan.
  - Family members must be launched sequentially. 
```

#plan