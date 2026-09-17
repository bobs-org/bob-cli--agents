#gh:gh_bobs-org__bob-cli #fork:08 This caused a failure on my macbook (see the command output below for context). Can you help me diagnose the root cause of this issue and fix it? %m:gpt-6-astra 
```
❯ bob highlights scan -w
pre_scan_command: run PATH="$HOME/bin:$PATH" bob_xlib_pull
bob_xlib_pull: athena probe failed (exit 1).
bob_xlib_pull: athena: find: paths must precede expression: `pending'
bob_xlib_pull: apollo probe failed (exit 1).
bob_xlib_pull: apollo: find: paths must precede expression: `pending'
bob highlights: pre-scan command failed with exit 1: PATH="$HOME/bin:$PATH" bob_xlib_pull
```