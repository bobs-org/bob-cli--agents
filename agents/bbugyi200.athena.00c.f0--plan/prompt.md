#gh:gh_bobs-org__bob-cli #fork:00c The `just install` command is failing on my macbook (see the command output below for context). Can you help me diagnose the root cause of this issue and fix it? #plan 
```
❯ just install
./Scripts/install.sh --target "~/Applications" --identity "-"
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/.build/install-bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/.build/install-bundle/Bob Mac Capture.app: replacing existing signature
cp: Building for production...
[0/5] Write sources
[2/5] Write swift-version--1AB21518FC5DEDBE.txt
[4/6] Compiling CaptureCore BobEnvironment.swift
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/CaptureCore/CaptureTargetsCache.swift:39:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
37 |     public func refresh(
38 |         using client: BobProcessClient,
39 |         now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
40 |     ) async -> CaptureTargetsSnapshot {
41 |         do {
[5/7] Compiling BobMacCapture AppDelegate.swift
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:452:23: warning: no 'async' operations occur within 'await' expression
450 |                 }
451 |
452 |                 guard await self?.isCurrentAnalysis(generation) == true else {
    |                       `- warning: no 'async' operations occur within 'await' expression
453 |                     return
454 |                 }

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:456:20: warning: no 'async' operations occur within 'await' expression
454 |                 }
455 |
456 |                 if await self?.shouldRequestCompletion(parse: parse, cursor: cursorUTF8Offset) == true {
    |                    `- warning: no 'async' operations occur within 'await' expression
457 |                     if let cached = await self?.cachedRouteCompletion(
458 |                         parse: parse,

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:457:37: warning: no 'async' operations occur within 'await' expression
455 |
456 |                 if await self?.shouldRequestCompletion(parse: parse, cursor: cursorUTF8Offset) == true {
457 |                     if let cached = await self?.cachedRouteCompletion(
    |                                     `- warning: no 'async' operations occur within 'await' expression
458 |                         parse: parse,
459 |                         cursor: cursorUTF8Offset,

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:502:28: warning: no 'async' operations occur within 'await' expression
500 |                 }
501 |
502 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
    |                            `- warning: no 'async' operations occur within 'await' expression
503 |                 let preview = try await CaptureSignpost.measure("preview") {
504 |                     try await processClient.captureLivePreview(

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:120:38: warning: main actor-isolated static property 'captureCategoryIdentifier' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 36 | final class NotificationService: NSObject, ObservableObject {
 37 |     static let openNoteActionIdentifier = "org.bobs.bob-mac-capture.open-note"
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
    |                `- note: static property declared here
 39 |     static let targetPathKey = "targetPath"
 40 |     static let foregroundPresentationOptions: UNNotificationPresentationOptions = [
    :
118 |         content.subtitle = routeLabel
119 |         content.sound = .default
120 |         content.categoryIdentifier = captureCategoryIdentifier
    |                                      `- warning: main actor-isolated static property 'captureCategoryIdentifier' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
121 |         if let targetPath {
122 |             content.userInfo = [targetPathKey: targetPath]

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:122:33: warning: main actor-isolated static property 'targetPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 37 |     static let openNoteActionIdentifier = "org.bobs.bob-mac-capture.open-note"
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
 39 |     static let targetPathKey = "targetPath"
    |                `- note: static property declared here
 40 |     static let foregroundPresentationOptions: UNNotificationPresentationOptions = [
 41 |         .banner, .sound, .list,
    :
120 |         content.categoryIdentifier = captureCategoryIdentifier
121 |         if let targetPath {
122 |             content.userInfo = [targetPathKey: targetPath]
    |                                 `- warning: main actor-isolated static property 'targetPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
123 |         }
124 |         return content

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:145:25: warning: main actor-isolated static property 'openNoteActionIdentifier' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 35 | @MainActor
 36 | final class NotificationService: NSObject, ObservableObject {
 37 |     static let openNoteActionIdentifier = "org.bobs.bob-mac-capture.open-note"
    |                `- note: static property declared here
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
 39 |     static let targetPathKey = "targetPath"
    :
143 |     nonisolated static func captureCategory() -> UNNotificationCategory {
144 |         let openNote = UNNotificationAction(
145 |             identifier: openNoteActionIdentifier,
    |                         `- warning: main actor-isolated static property 'openNoteActionIdentifier' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
146 |             title: "Open Note",
147 |             options: [.foreground]

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:150:25: warning: main actor-isolated static property 'captureCategoryIdentifier' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 36 | final class NotificationService: NSObject, ObservableObject {
 37 |     static let openNoteActionIdentifier = "org.bobs.bob-mac-capture.open-note"
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
    |                `- note: static property declared here
 39 |     static let targetPathKey = "targetPath"
 40 |     static let foregroundPresentationOptions: UNNotificationPresentationOptions = [
    :
148 |         )
149 |         return UNNotificationCategory(
150 |             identifier: captureCategoryIdentifier,
    |                         `- warning: main actor-isolated static property 'captureCategoryIdentifier' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
151 |             actions: [openNote],
152 |             intentIdentifiers: [],

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:167:40: warning: main actor-isolated static property 'openNoteActionIdentifier' can not be referenced from a nonisolated autoclosure; this is an error in the Swift 6 language mode
 35 | @MainActor
 36 | final class NotificationService: NSObject, ObservableObject {
 37 |     static let openNoteActionIdentifier = "org.bobs.bob-mac-capture.open-note"
    |                `- note: static property declared here
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
 39 |     static let targetPathKey = "targetPath"
    :
165 |         guard
166 |             actionIdentifier == UNNotificationDefaultActionIdentifier
167 |                 || actionIdentifier == openNoteActionIdentifier
    |                                        `- warning: main actor-isolated static property 'openNoteActionIdentifier' can not be referenced from a nonisolated autoclosure; this is an error in the Swift 6 language mode
168 |         else {
169 |             return nil

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:171:41: warning: main actor-isolated static property 'targetPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 37 |     static let openNoteActionIdentifier = "org.bobs.bob-mac-capture.open-note"
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
 39 |     static let targetPathKey = "targetPath"
    |                `- note: static property declared here
 40 |     static let foregroundPresentationOptions: UNNotificationPresentationOptions = [
 41 |         .banner, .sound, .list,
    :
169 |             return nil
170 |         }
171 |         guard let targetPath = userInfo[targetPathKey] as? String else {
    |                                         `- warning: main actor-isolated static property 'targetPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
172 |             return nil
173 |         }

/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:184:32: warning: main actor-isolated static property 'foregroundPresentationOptions' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 38 |     static let captureCategoryIdentifier = "org.bobs.bob-mac-capture.capture"
 39 |     static let targetPathKey = "targetPath"
 40 |     static let foregroundPresentationOptions: UNNotificationPresentationOptions = [
    |                `- note: static property declared here
 41 |         .banner, .sound, .list,
 42 |     ]
    :
182 |         withCompletionHandler completionHandler: @escaping (UNNotificationPresentationOptions) -> Void
183 |     ) {
184 |         completionHandler(Self.foregroundPresentationOptions)
    |                                `- warning: main actor-isolated static property 'foregroundPresentationOptions' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
185 |     }
186 |
[5/7] Write Objects.LinkFileList
[6/7] Linking BobMacCapture
Build of product 'BobMacCapture' complete! (58.36s)
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/.build/install-bundle/Bob Mac Capture.app: File name too long
error: recipe `install` failed on line 22 with exit code 1
```