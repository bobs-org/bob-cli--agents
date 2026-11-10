#gh:gh_bobs-org__bob-cli The `.` to `&` capture alias isn't working as expected in the bob-mac-capture
app. Namely, when typing `.` after a space in the app and a `@foo[:^+]bar` reference
already exists, the `.` alias should expand to `&` instead of `@`. Even though another
`@baz[:^+]buz` reference is supported it is not common for me to use this type of bulk
capture and the `.` alias is meant to always expand to the most intuitive/desirable
character based on the context.

#plan %m:@xlarge