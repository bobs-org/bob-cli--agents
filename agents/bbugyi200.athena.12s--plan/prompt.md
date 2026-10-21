#gh:gh_bobs-org__bob-cli When the `<cmd+t>` keymap is used in the Highlights app, all previous state
that was persisted for the bob-mac-capture app's ref panel should be cleared (as if the
user used the `<ctrl+z>` keymap on that panel). See the
~/tmp/screenshots/20261021_073902.png screenshot for an example of a problem we
experience because we don't currently do this. Can you help me fix this?

#plan %m:@xlarge %auto