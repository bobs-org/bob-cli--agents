%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/emoji_colon_completion.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- bare_colon = open (planner default: open). Implement the "bare_colon = open" branch; ignore "bare_colon = first_char". Context: "Should a bare ':' (no query letters typed yet) already open the menu?".
- closing_colon = inert (planner default: inert). Implement the "closing_colon = inert" branch; ignore "closing_colon = autocommit". Context: "Should typing a full ':name:' shortcode auto-replace it with the emoji without a menu selection?".
- enablement = auto (planner default: auto). Implement the "enablement = auto" branch; ignore "enablement = manual". Context: "After deploy, should the agent enable the plugin by adding bob-emoji to community-plugins.json?".
Implement only the branches selected above.
%macros_enabled:true
