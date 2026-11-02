#gh:gh_bobs-org__bob-cli The `just install` command is failing for the bob-mac-capture app (see the partial command output below for context). Can you help me diagnose the root cause of this issue and fix it? #plan %m:@xlarge 
```
/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift:3639:9: error: closure containing control flow statement cannot be used with result builder 'ViewBuilder'
3637 |             )
3638 |         }
3639 |         for relationComplete in success.relationCompletes {
     |         `- error: closure containing control flow statement cannot be used with result builder 'ViewBuilder'
3640 |             guard let complete = relationComplete.taskComplete else {
3641 |                 continue

SwiftUI.ViewBuilder:2:30: note: struct 'ViewBuilder' declared here
1 | @available(iOS 13.0, macOS 10.15, tvOS 13.0, watchOS 6.0, *)
2 | @resultBuilder public struct ViewBuilder {
  |                              `- note: struct 'ViewBuilder' declared here
3 |     public static func buildExpression<Content>(_ content: Content) -> Content where Content : View
4 |     public static func buildBlock() -> EmptyView

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift:4950:10: warning: result of call to 'accessibilityLabel' is unused [#no-usage]
4948 |         )
4949 |         .accessibilityElement(children: .combine)
4950 |         .accessibilityLabel(accessibilityText)
     |          `- warning: result of call to 'accessibilityLabel' is unused [#no-usage]
4951 |     }
4952 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift:4890:18: error: function declares an opaque return type, but has no return statements in its body from which to infer an underlying type [#OpaqueTypeInference]
4888 |     }
4889 |
4890 |     private func eventWarningBanner(
     |                  `- error: function declares an opaque return type, but has no return statements in its body from which to infer an underlying type [#OpaqueTypeInference]
4891 |         headline: String,
4892 |         detail: String?,
     :
4906 |             displayHeadline = Text(headline)
4907 |         }
4908 |         VStack(alignment: .leading, spacing: 4) {
     |         `- note: did you mean to return the last expression?
4909 |             HStack(alignment: .firstTextBaseline, spacing: 6) {
4910 |                 Image(systemName: "exclamationmark.triangle.fill")

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 |
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 |
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 |
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 |
 174 |     private var fetcher: RefsFetching?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 |
11 |     /// Returns true when the refresh should run, recording the start.

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift:854:30: error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 852 |         }
 853 |         guard count > 0 else { return "" }
 854 |         let keepMovingRows = captures.flatMap { capture in
     |                              `- error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 855 |             (capture.taskComplete?.keepMoving ?? [])
 856 |                 + (capture.pomodoroClose?.keepMoving ?? [])

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 |
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#OpaqueTypeInference]: <https://docs.swift.org/compiler/documentation/diagnostics/opaque-type-inference>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>

error: recipe `install` failed on line 42 with exit code 1
  ✗ 9 new commits · 01c753b → 0f2f46f · install failed (exit 1)
```