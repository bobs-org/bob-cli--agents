- **AGENTS:**
  - [bbugyi200.apollo.research.2x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2x.linker.w0.md)

%auto #gh:gh_bobs-org__bob-cli I would like to make some changes to clean up some of the
capture syntax we support currently to make it more consistent and easier to understand.
Can you help me implement this?

- The `@file+id#type` syntax shoould be retired in favor the `@file+id#drawer` syntax,
  where `#drawer` should match the name of an all capitialized task bullet, which would
  be converted to an H2 section if the task were ever converted into a project note.
  - Changing the type of a task we are targeting would then need to be done using a
    separate `#type` token when using the `@file+id` syntax.
  - For example, the `Some note goes here. @foo+bar#requirements #fix` capture should be
    able to be used to add a new `Some note goes here.` bullet to the `REQUIREMENTS`
    drawer of the `^bar` task in the ~/bob/foo.md file.
- When `#` is typed after `@file+id` we should trigger a great completion menu for any
  existing drawers on that task and (prioritized lower in the list) any recent drawers
  that have been used on other tasks or in other project notes (these drawers take the
  form of H2 sections when in project notes).
- If the targeted drawer does not exist when using the `@file+id#drawer` capture syntax,
  we should create it.
- As a part of this change, let's add a new "task drawer" (aka "drawer") glossary term.
- I also want to migrate the trailing `#` functionality (specifies that a bullet should
  be added to the current pomodoro), the `%` syntax, and the `@@template` syntax to a
  new `%<C>` directive syntax.
  - `<C>` should be one of the following single characters: "c" (clip), "n" (note), "t"
    (template).
  - `%c`: This should work just like the current `%` syntax (though I would love if this
    syntax supported previews better in the bob-mac-capture app).
  - `%n`: This should work just like the current trailing `#` functionality.
  - `%t`: This should work almost just like the `@@template` syntax, but we shouldn't
    re-write the capture to put `%t` on the top line (just leave it where it was typed).
  - Make sure that when the character `%` is pressed we display a good description of
    each of these directives to the user in the bob-mac-capture app.
  - This change will allow us to start displaying the task type completion menu in the
    bob-mac-capture app immediately after `#` is pressed (when not after `@file+id`--we
    should show completion drawers in that case), instead of waiting for a character to
    be pressed after `#`.
- We should also remove support for the `@@file+id` syntax as a part of this change,
  which I haven't used in a while since its use-case has been obsoleted by the
  `@@template` syntax (which is moving to `%t`).
- Make sure that we clean up all related legacy syntax by completely removing all
  reference to it (we don't want any backward compatibility for functionality that was
  added recently).
- See the bob-cli-ep epic bead for more context on the recent `#type` capture syntax
  changes.
- Review the capture_drawer_and_directive_grammar.md file in the research sidecar repo
  for context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).
- #beau

#plan %m:@xlarge %w:research.2x.linker
