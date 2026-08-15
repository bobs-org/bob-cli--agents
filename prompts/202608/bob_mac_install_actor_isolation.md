- **PLAN:**
  [202608/bob_mac_install_actor_isolation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_install_actor_isolation.md)
- **AGENTS:**
  - [bbugyi200.athena.02b--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.02b.md)

Installing the bob-mac-capture app on my macbook with the `just install` command fails
(see the partial command output below for context). Can you help me diagnose the root
cause of this issue and fix it? Review the bob-cli-u and bob-cli-t epic beads first,
which may be related. If this issue relates to either of those epic beads or any of the
corresponding phase beads, make sure to add appropriate notes to those beads. Think this
through thoroughly and create a plan using your `/sase_plan` skill. Choose and author
the appropriate tier, validate and revalidate until it passes, then submit it with
`sase plan propose` (as the skill instructs) before making any file changes.

```
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:189:41: warning: main actor-isolated static property 'targetPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 37 |     static let openNoteActionIdentifier = "org.bobs.bob-mac-capture.open-note"
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
 39 |     static let targetPathKey = "targetPath"
    |                `- note: static property declared here
 40 |     static let foregroundPresentationOptions: UNNotificationPresentationOptions = [
 41 |         .banner, .sound, .list,
    :
187 |             return nil
188 |         }
189 |         guard let targetPath = userInfo[targetPathKey] as? String else {
    |                                         `- warning: main actor-isolated static property 'targetPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
190 |             return nil
191 |         }

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:202:32: warning: main actor-isolated static property 'foregroundPresentationOptions' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
 39 |     static let targetPathKey = "targetPath"
 40 |     static let foregroundPresentationOptions: UNNotificationPresentationOptions = [
    |                `- note: static property declared here
 41 |         .banner, .sound, .list,
 42 |     ]
    :
200 |         withCompletionHandler completionHandler: @escaping (UNNotificationPresentationOptions) -> Void
201 |     ) {
202 |         completionHandler(Self.foregroundPresentationOptions)
    |                                `- warning: main actor-isolated static property 'foregroundPresentationOptions' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
203 |     }
204 |

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>

error: recipe `install` failed on line 22 with exit code 1
```
