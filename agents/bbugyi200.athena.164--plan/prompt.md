#gh:gh_bobs-org__bob-cli We currently seem to automatically convert task relation labels to a different
form when mirroring in the destination task's "linked from" bullet; however, it is
unclear which transformations are supported currently, and I think that we can support
more than we do now.

Can you help me make it so any `<foo>ed by` relation description is transformed to the
appropriate `<foo>s` prefix when mirroring the "linked from" bullet? For example, in the
~/tmp/screenshots/20261030_091517.png screenshot we should show `INSPIRES` before the
link to the `Get gog workin on macbook!`.

#plan %m:@xlarge