#gh:gh_bobs-org__bob-cli The `just install` command is failing for the bob-mac-capture repo. See the command output below for context. Can you help me diagnose the root cause of this issue and fix it? #plan %m:@xlarge 
```
error: recipe `install` failed on line 42 with exit code 1
  ✗ build failed after 2:53 · exit 1
      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelController.swift:3355:21: error: argument 'moveChoiceVisible' must precede argument 'mailCloseVisible'
      3353 |                     pickerSourceIsRelation: model.pickerSourceIsRelation,
      3354 |                     mailCloseVisible: model.mailCloseVisible,
      3355 |                     moveChoiceVisible: model.moveChoiceVisible,
           |                     `- error: argument 'moveChoiceVisible' must precede argument 'mailCloseVisible'
      3356 |                     moveChoiceFilterFocused: model.moveChoiceVisible
      3357 |                         && (Self.findPickerFilterField(

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelController.swift:4029:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
      4027 |         }
      4028 |         if let textView = firstResponder as? NSTextView,
      4029 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
           |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
      4030 |            field.accessibilityIdentifier() == identifier
      4031 |         {

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:4541:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
       4539 |                         requireInboxRouteChoice: true,
       4540 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
       4541 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil,
            |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
       4542 |                         expectPastWindows: expectPastWindows,
       4543 |                         mailCloseDigest: mailCloseDigest

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:4541:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
       4539 |                         requireInboxRouteChoice: true,
       4540 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
       4541 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil,
            |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
       4542 |                         expectPastWindows: expectPastWindows,
       4543 |                         mailCloseDigest: mailCloseDigest

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:5707:20: warning: result of call to 'armEscDiscard()' is unused [#no-usage]
       5705 |         // are staged. Default Met never arms.
       5706 |         if choice.totalCloseCount > 0, !choice.outcomes.isEscArmed {
       5707 |             choice.armEscDiscard()
            |                    `- warning: result of call to 'armEscDiscard()' is unused [#no-usage]
       5708 |             pullInChoice = choice
       5709 |             let text = choice.outcomes.escArmedText ?? "Esc again to discard closes"

      full log  ~/.local/state/bob-cli/install-all/logs/20261124-153046-95626-bob-mac-capture.log
      rerun with  just install-all -v  to stream build output
  ✗ 1 new commit · 0b441d3 → c2a4426 · install failed (exit 1)

```