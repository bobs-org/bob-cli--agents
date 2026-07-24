#gh:gh_bobs-org__bob-cli Can you help me make a trailing `#` on a task block link in a pomodoro sub-bullet act as a marker that specifies that the `<ctrl+enter>` Obsidian keymap should just move (after removing the `#` suffix) this block link to the new pomodoro this keymap creates (don't leave behind a link with a tomatoe icon prefixed to it). For example, assume the following pomodoro:

```
- [ ] (**1110-1135** [t:: 25m]) 
	- [[#^gtd]]#
	- foo bar baz
```

Then closing this pomodoro with the `<ctrl+enter>` keymap should produce the following:

```
- [X] (**1110-1135** [t:: 25m]) 
	- foo bar baz
- [ ] ()
	- [[#^gtd]]
```

#tale