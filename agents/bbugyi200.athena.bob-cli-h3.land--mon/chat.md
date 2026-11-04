# Chat History - ace-run (bob-cli-h3.land--mon)

- **TIMESTAMP:** 2026-11-04 13:46:30 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-h3.land--mon

## Prompt

sase monitor start --command 'scratch_dir=/tmp/bob-mac-capture-goto-closeout-20261104131437\nstatus=0\nssh -o BatchMode=yes -o ConnectTimeout=5 mac mkdir "$scratch_dir" || status=$?\nif [ "$status" -eq 0 ]; then\n  rsync -az --exclude=.git --exclude=.build /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-mac-capture/ "mac:$scratch_dir/" || status=$?\nfi\nif [ "$status" -eq 0 ]; then\n  ssh -o BatchMode=yes -o ConnectTimeout=5 mac "cd $scratch_dir && Scripts/bundle.sh --configuration debug --identity - --output $scratch_dir/bundle && just typecheck-tests" || status=$?\nfi\nssh -o BatchMode=yes -o ConnectTimeout=5 mac rm -rf "$scratch_dir" || true\nexit "$status"' --reason 'Compile the approved Go To scope repair in a scratch copy on macOS'

## Response

sase tool run ac02b61f0751e3d22b5d6c5cd610aef6
X11 forwarding request failed on channel 0
X11 forwarding request failed on channel 0
Building for debugging...
[0/8] Write sources
[3/8] Write BobMacCapture-entitlement.plist
[4/8] Write swift-version--1AB21518FC5DEDBE.txt
[6/90] Compiling CaptureCore CaptureTaskThemePresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[7/90] Compiling CaptureCore CaptureTaskTypeMenuPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[8/90] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[9/90] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[10/90] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[11/90] Compiling CaptureCore CaptureTransferPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[12/90] Compiling CaptureCore CaptureUnconfiguredThemePresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[13/90] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[14/90] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[15/90] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[16/90] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[17/90] Compiling CaptureCore CaptureOpenPlan.swift
[18/90] Compiling CaptureCore CapturePanelPlacement.swift
[19/90] Compiling CaptureCore CapturePickerHelpers.swift
[20/90] Compiling CaptureCore CapturePickerPresentation.swift
[21/90] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[22/90] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[23/90] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[24/90] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[25/90] Compiling CaptureCore CapturePomodoroLineTokens.swift
[26/90] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[27/90] Compiling CaptureCore CapturePomodoroMergePresentation.swift
[28/90] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[29/90] Compiling CaptureCore CaptureCompletionMenu.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[30/90] Compiling CaptureCore CaptureDrawerMenuPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[31/90] Compiling CaptureCore CaptureEditWrite.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[32/90] Compiling CaptureCore CaptureGrammarGate.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[33/90] Compiling CaptureCore CaptureInboxRoutePresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[34/90] Compiling CaptureCore CaptureLineCaseToggle.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[35/90] Compiling CaptureCore CaptureLinkGuardPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[36/90] Compiling CaptureCore CaptureList.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[37/90] Compiling CaptureCore CaptureModels.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[38/90] Compiling CaptureCore CaptureMoveChoicePresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[39/90] Compiling CaptureCore CaptureNotePullPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[40/90] Compiling CaptureCore CaptureOpenHintPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:8882:13: warning: no calls to throwing functions occur within 'try' expression
 8880 |         let container = try decoder.singleValueContainer()
 8881 |         // Explicit null has no value; treat it as absent.
 8882 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8883 |             throw DecodingError.valueNotFound(
 8884 |                 CaptureThemeSuggestion.self,
[41/90] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[42/90] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[43/90] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[44/90] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[45/90] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[46/90] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[47/90] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[48/90] Compiling CaptureCore CaptureBlockDiffRow.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[49/90] Compiling CaptureCore CaptureBlockIDSplice.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[50/90] Compiling CaptureCore CaptureClipPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[51/90] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[52/90] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[53/90] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[54/90] Compiling CaptureCore CapturePomodoroSplitPresentation.swift
[55/90] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[56/90] Compiling CaptureCore CaptureProjectNotePresentation.swift
[57/90] Compiling CaptureCore CaptureRefFileUnder.swift
[58/90] Compiling CaptureCore CaptureRefPresentation.swift
[59/90] Compiling CaptureCore CaptureRelatedModels.swift
[60/90] Compiling CaptureCore CaptureRelationCancelPresentation.swift
[61/90] Compiling CaptureCore CaptureRelationCloseEffect.swift
[62/90] Compiling CaptureCore CaptureRelationCompletePresentation.swift
[63/90] Compiling CaptureCore CaptureRelationHeldPresentation.swift
[64/90] Emitting module CaptureCore
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[65/90] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[66/90] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[67/90] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[68/90] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[69/90] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[70/90] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[71/90] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[72/90] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[73/90] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[74/90] Compiling CaptureCore CaptureAgendaBoundaryRefresh.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[75/90] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[76/90] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[77/90] Compiling CaptureCore CaptureRelationSuccessorModels.swift
[78/90] Compiling CaptureCore CaptureRelationshipCopy.swift
[79/90] Compiling CaptureCore CaptureRelationshipPresentation.swift
[80/90] Compiling CaptureCore CaptureSavedTemplates.swift
[81/90] Compiling CaptureCore CaptureSubBulletPresentation.swift
[82/90] Compiling CaptureCore CaptureSuccessorOfferRows.swift
[83/90] Compiling CaptureCore CaptureSuccessorPresentation.swift
[84/90] Compiling CaptureCore CaptureTargetsCache.swift
[85/90] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[86/90] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[87/90] Compiling CaptureCore CaptureTaskGotoScopeState.swift
[88/101] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[89/101] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[90/101] Compiling CaptureCore ProjectTaskMovePickerPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[91/101] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[92/101] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[93/101] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[94/101] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[95/101] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[96/101] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[97/101] Compiling CaptureCore WikilinkTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[98/101] Compiling CaptureCore WorkBadgeTone.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/CaptureCore/CaptureModels.swift:9083:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9081 | }
 9082 | 
 9083 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9084 |     public let replacement: String
 9085 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[99/132] Compiling RefsCore RefsDecoding.swift
[100/132] Compiling RefsCore RefsFetching.swift
[101/132] Compiling RefsCore RefsHighlightPicker.swift
[102/132] Compiling RefsCore RefsHighlightsTabs.swift
[103/132] Compiling RefsCore RefsInspector.swift
[104/132] Compiling RefsCore RefsPickerScope.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[105/132] Compiling RefsCore RefsQuoteUnderline.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[106/132] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[107/132] Compiling RefsCore RefsRename.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[108/132] Compiling RefsCore RefsInspectorImages.swift
[109/132] Compiling RefsCore RefsLinks.swift
[110/132] Compiling RefsCore RefsListScroll.swift
[111/132] Compiling RefsCore RefsModel.swift
[112/132] Compiling RefsCore RefsScan.swift
[113/132] Compiling RefsCore RefsScanReceipt.swift
[114/132] Compiling RefsCore RefsSectionedWindow.swift
[115/132] Compiling RefsCore RefsSelection.swift
[116/132] Emitting module RefsCore
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[117/132] Compiling RefsCore HighlightsSaveScan.swift
[118/132] Compiling RefsCore RefsArrivals.swift
[119/132] Compiling RefsCore RefsCaption.swift
[120/132] Compiling RefsCore RefsCode.swift
[121/132] Compiling RefsCore RefsCopy.swift
[122/132] Compiling RefsCore RefsNew.swift
[123/132] Compiling RefsCore RefsNewest.swift
[124/132] Compiling RefsCore RefsPDFUpdates.swift
[125/132] Compiling RefsCore RefsPanelGeometry.swift
[126/132] Compiling RefsCore RefsStores.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[127/132] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[128/132] Compiling RefsCore RefsTabsRanking.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[129/132] Compiling RefsCore RefsToday.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[130/136] Compiling RefsCore RefsTodayLinkCard.swift
[131/136] Compiling RefsCore RefsTodayLinkModels.swift
[132/136] Compiling RefsCore RefsTodayLinkPresentation.swift
[133/136] Compiling RefsCore RefsWatcherRelevance.swift
[134/217] Compiling BobMacCapture RefsSearchBar.swift
[135/217] Compiling BobMacCapture RefsTabsViews.swift
[136/217] Compiling BobMacCapture RefsTodayLinkCardView.swift
[137/217] Compiling BobMacCapture RefsUnderlineRenderer.swift
[138/217] Compiling BobMacCapture RefsVisualTokens.swift
[139/217] Compiling BobMacCapture RefsAliasHotkeyRegistration.swift
[140/217] Compiling BobMacCapture RefsHighlightsCodeKey.swift
[141/217] Compiling BobMacCapture RefsHighlightsCopyKey.swift
[142/217] Compiling BobMacCapture RefsHighlightsLinkKey.swift
[143/217] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[144/217] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[145/228] Compiling BobMacCapture RefsHotkeyRegistration.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[146/228] Compiling BobMacCapture RelationLabelField.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[147/228] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[148/228] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[149/228] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[150/228] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[151/228] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[152/228] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[153/228] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[154/228] Compiling BobMacCapture TodayBadge.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[155/228] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[156/228] Compiling BobMacCapture RefsLinkPreviewWell.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[157/228] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[158/228] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[159/228] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[160/228] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[161/228] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[162/228] Compiling BobMacCapture RefsPickerScopeViews.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[163/228] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[164/228] Compiling BobMacCapture RefsRenameCardView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[165/228] Compiling BobMacCapture RefsRowView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[166/228] Compiling BobMacCapture RefsScanReceiptObserver.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[167/228] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[168/228] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[169/228] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[170/228] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[171/228] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[172/228] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[173/228] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[174/228] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[175/228] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[176/228] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[177/228] Compiling BobMacCapture CaptureTaskTypeMenuView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[178/228] Compiling BobMacCapture ClipCardView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[179/228] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[180/228] Compiling BobMacCapture RefsCodePreviewWell.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[181/228] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[182/228] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[183/228] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[184/228] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[185/228] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[186/228] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[187/228] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[188/228] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[189/228] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[190/228] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[191/228] Compiling BobMacCapture CaptureAliasHotkeyRegistration.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[192/228] Compiling BobMacCapture CaptureDrawerMenuView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[193/228] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[194/228] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[195/228] Compiling BobMacCapture CaptureInboxRouteChoiceView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[196/228] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[197/228] Compiling BobMacCapture CaptureListGroupCapsule.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[198/228] Compiling BobMacCapture CaptureMoveChoiceView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[199/228] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[200/228] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[201/228] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:1622:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1620 |         }
1621 | 
1622 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1623 |         return true
1624 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelController.swift:2337:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2335 |         }
2336 |         if let textView = firstResponder as? NSTextView,
2337 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2338 |            field.accessibilityIdentifier() == identifier
2339 |         {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:2774:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2772 |                         requireInboxRouteChoice: true,
 2773 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2774 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2775 |                     )
 2776 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:10178:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10176 |         newName: String
10177 |     ) {
10178 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10179 |               let rename = current.rename,
10180 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13526:23: warning: no 'async' operations occur within 'await' expression
13524 |                 }
13525 | 
13526 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
13527 |                     return
13528 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13539:35: warning: no 'async' operations occur within 'await' expression
13537 |                         CaptureGrammarGate.isCompatible(parse.grammar)
13538 |                         && parse.reportsClipDirective
13539 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
13540 |                         draft: draft,
13541 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13554:27: warning: no 'async' operations occur within 'await' expression
13552 |                     await completionGate.value
13553 |                     try Task.checkCancellation()
13554 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
13555 |                         return
13556 |                     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13561:20: warning: no 'async' operations occur within 'await' expression
13559 |                 if let cursorUTF8Offset,
13560 |                    requestCompletion,
13561 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
13562 |                        parse: parse,
13563 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelModel.swift:13567:37: warning: no 'async' operations occur within 'await' expression
13565 |                    ) == true
13566 |                 {
13567 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
13568 |                         parse: parse,
13569 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2783:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
2783 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2784 |     }
2785 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:2782:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2780 |         }
2781 |         return Text(String(label[..<range.lowerBound]))
2782 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2783 |             + Text(String(label[range.upperBound...]))
2784 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3575:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3573 |                     + Text("●").foregroundStyle(
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3576 |                     .font(.caption)
3577 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CapturePanelView.swift:3573:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3571 |             if parts.count == 2 {
3572 |                 (Text(parts[0]).foregroundStyle(.secondary)
3573 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3574 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3575 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[202/228] Emitting module BobMacCapture
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[203/228] Compiling BobMacCapture HighlightsSaveKeyMonitor.swift
[204/228] Compiling BobMacCapture HighlightsTakeover.swift
[205/228] Compiling BobMacCapture HotKeyRegistry.swift
[206/228] Compiling BobMacCapture NotificationService.swift
[207/228] Compiling BobMacCapture PlainTextPaste.swift
[208/228] Compiling BobMacCapture PomodoroBlockView.swift
[209/228] Compiling BobMacCapture PomodoroHomeColor.swift
[210/228] Compiling BobMacCapture PomodoroNameField.swift
[211/228] Compiling BobMacCapture PomodoroThemeViews.swift
[212/228] Compiling BobMacCapture AXHighlightsTabsReader.swift
[213/228] Compiling BobMacCapture RefsActionsMenu.swift
[214/228] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[215/228] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[216/228] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[217/228] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[218/228] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[219/228] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[220/228] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[221/228] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[222/228] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[223/228] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[224/228] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[225/228] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-goto-closeout-20261104131437/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[225/228] Write Objects.LinkFileList
[226/228] Linking BobMacCapture
[227/228] Applying BobMacCapture
Build of product 'BobMacCapture' complete! (105.48s)
/tmp/bob-mac-capture-goto-closeout-20261104131437/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-goto-closeout-20261104131437/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-goto-closeout-20261104131437/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
[0/1] Planning build
Building for debugging...
[0/11] Write sources
[2/13] Write BobMacCaptureInstallHelper-entitlement.plist
[3/13] Write refs-rank-entitlement.plist
[4/13] Write swift-version--1AB21518FC5DEDBE.txt
[6/18] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[7/18] Compiling refs_rank main.swift
[8/18] Emitting module refs_rank
[9/18] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[10/18] Emitting module BobMacCaptureInstallHelper
[11/18] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[12/18] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[12/18] Write Objects.LinkFileList
[14/18] Linking BobMacCaptureInstallHelper
[15/18] Linking refs-rank
[16/18] Applying refs-rank
[16/18] Applying BobMacCaptureInstallHelper
Build complete! (2.33s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
X11 forwarding request failed on channel 0
succeeded  exit=0  duration=141600ms

