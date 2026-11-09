# Chat History - ace-run (bob-cli-j6.2--mon)

- **TIMESTAMP:** 2026-11-09 12:16:51 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-j6.2--mon

## Prompt

sase monitor start --command 'bash -lc \'\nset -euo pipefail\nrepo="$(pwd)"\nscratch="$(ssh mac "mktemp -d /tmp/bob-mac-capture-j6.2.XXXXXX")"\ncleanup() { ssh mac "rm -rf -- \\"$scratch\\"" || true; }\ntrap cleanup EXIT\nrsync -a --exclude=.git --exclude=.build "$repo/" "mac:$scratch/"\nssh mac "cd \\"$scratch\\" && ./Scripts/bundle.sh"\nssh mac "cd \\"$scratch\\" && just typecheck-tests"\nssh mac "cd \\"$scratch\\" && just format-lint"\n\'' --reason 'Compile and type-check the Bob Mac Capture alias changes on macOS'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
X11 forwarding request failed on channel 0
X11 forwarding request failed on channel 0
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureMergeInPresentation.swift:64:53: warning: string interpolation produces a debug description for an optional value; did you mean to make this explicit?
 62 |         let hasEnrichedMerge = merges.contains { $0.statusName != nil }
 63 |         sourceRows = merges.map { merge in
 64 |             let stableID = "\(merge.source.path)#^\(merge.source.blockID)"
    |                                                     |            |- note: provide a default value to avoid this warning
    |                                                     |            `- note: use 'String(describing:)' to silence this warning
    |                                                     `- warning: string interpolation produces a debug description for an optional value; did you mean to make this explicit?
 65 |             if hasEnrichedMerge, merge.statusName != nil {
 66 |                 let movedText: String

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10050:13: warning: no calls to throwing functions occur within 'try' expression
10048 |         let container = try decoder.singleValueContainer()
10049 |         // Explicit null has no value; treat it as absent.
10050 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
10051 |             throw DecodingError.valueNotFound(
10052 |                 CaptureThemeSuggestion.self,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/ParentTaskPickerPresentation.swift:656:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
654 | 
655 | private struct ParentTaskPickerIndexEntry: Sendable {
656 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
657 |     let bobIndex: Int
658 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/CaptureCore/CaptureModels.swift:10251:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10249 | }
10250 | 
10251 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
10252 |     public let replacement: String
10253 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[6/8] Compiling RefsCore HighlightsSaveScan.swift
/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |     private let fileURL: URL
 43 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |     private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |     private let fileURL: URL
184 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |     private let onError: @Sendable (String) -> Void
186 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |     private let fileURL: URL
378 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |     private let onError: @Sendable (String) -> Void
380 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[7/9] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelController.swift:1844:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1842 |         }
1843 | 
1844 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1845 |         return true
1846 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelController.swift:3147:17: error: argument 'pickerChipVisible' must precede argument 'modifierAliasOpenerOwnPickerIsEmpty'
3145 |                 pickerFilterIsEmpty: model.pickerFilterIsEmpty,
3146 |                 modifierAliasOpenerOwnPickerIsEmpty: model.modifierAliasOpenerOwnPickerIsEmpty,
3147 |                 pickerChipVisible: model.pickerChipVisible,
     |                 `- error: argument 'pickerChipVisible' must precede argument 'modifierAliasOpenerOwnPickerIsEmpty'
3148 |                 pickerOperatorContinuationKeys: model.pickerOperatorContinuationKeys,
3149 |                 pickerOperatorContinuationAliases: model.pickerOperatorContinuationAliases,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelController.swift:3481:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
3479 |         }
3480 |         if let textView = firstResponder as? NSTextView,
3481 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
3482 |            field.accessibilityIdentifier() == identifier
3483 |         {

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:3871:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3869 |                         requireInboxRouteChoice: true,
 3870 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3871 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil,
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3872 |                         expectPastWindows: expectPastWindows
 3873 |                     )

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:3871:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3869 |                         requireInboxRouteChoice: true,
 3870 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3871 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil,
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3872 |                         expectPastWindows: expectPastWindows
 3873 |                     )

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:4449:13: warning: initialization of immutable value 'requestID' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
 4447 |         statusText = "Refreshing successor offers…"
 4448 |         let generation = analysisGeneration
 4449 |         let requestID = UUID()
      |             `- warning: initialization of immutable value 'requestID' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
 4450 |         Task { [weak self, processClient] in
 4451 |             do {

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:4879:20: warning: result of call to 'armEscDiscard()' is unused [#no-usage]
 4877 |         // Two-step Esc while verdicts are staged.
 4878 |         if choice.closeCount > 0, !choice.outcomes.isEscArmed {
 4879 |             choice.armEscDiscard()
      |                    `- warning: result of call to 'armEscDiscard()' is unused [#no-usage]
 4880 |             pullInChoice = choice
 4881 |             let text = choice.outcomes.escArmedText ?? "Esc again to discard closes"

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:12823:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
12821 |         newName: String
12822 |     ) {
12823 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
12824 |               let rename = current.rename,
12825 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:16730:23: warning: no 'async' operations occur within 'await' expression
16728 |                 }
16729 | 
16730 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
16731 |                     return
16732 |                 }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:16743:35: warning: no 'async' operations occur within 'await' expression
16741 |                         CaptureGrammarGate.isCompatible(parse.grammar)
16742 |                         && parse.reportsClipDirective
16743 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
16744 |                         draft: draft,
16745 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:16758:27: warning: no 'async' operations occur within 'await' expression
16756 |                     await completionGate.value
16757 |                     try Task.checkCancellation()
16758 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
16759 |                         return
16760 |                     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:16768:47: warning: no 'async' operations occur within 'await' expression
16766 |                     shouldRequestCompletion = true
16767 |                 } else if let cursorUTF8Offset, requestCompletion {
16768 |                     shouldRequestCompletion = await self?.shouldRequestCompletion(
      |                                               `- warning: no 'async' operations occur within 'await' expression
16769 |                         parse: parse,
16770 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelModel.swift:16792:37: warning: no 'async' operations occur within 'await' expression
16790 |                         return
16791 |                     }
16792 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
16793 |                         parse: parse,
16794 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelView.swift:2931:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2929 |         return Text(String(label[..<range.lowerBound]))
2930 |             + Text(String(label[range])).bold()
2931 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2932 |     }
2933 | 

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelView.swift:2930:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2928 |         }
2929 |         return Text(String(label[..<range.lowerBound]))
2930 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2931 |             + Text(String(label[range.upperBound...]))
2932 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelView.swift:3732:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3730 |                     + Text("●").foregroundStyle(
3731 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3732 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3733 |                     .font(.caption)
3734 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePanelView.swift:3730:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3728 |             if parts.count == 2 {
3729 |                 (Text(parts[0]).foregroundStyle(.secondary)
3730 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3731 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3732 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePullInChoiceView.swift:837:19: warning: immutable value 'key' was never used; consider replacing with '_' or removing it [#no-usage]
 835 | 
 836 |     private var cancelDetailText: (text: String, faint: Bool)? {
 837 |         guard let key = offerKey, case .cancel(let reason) = verdict else {
     |                   `- warning: immutable value 'key' was never used; consider replacing with '_' or removing it [#no-usage]
 838 |             return nil
 839 |         }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CapturePullInChoiceView.swift:904:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 902 |             let chunk = Text("\(separator)\(entry.element.text)")
 903 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 904 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 905 |         }
 906 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |     public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                       `- note: static property declared here
182 | 
183 |     private let byteLimit: Int
    :
186 |     public private(set) var byteCost = 0
187 | 
188 |     public init(byteLimit: Int = defaultByteLimit) {
    |                                  `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |         self.byteLimit = max(byteLimit, 1)
190 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,

/private/tmp/bob-mac-capture-j6.2.CMAd7m/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
X11 forwarding request failed on channel 0

