- **AGENTS:**
  - [bbugyi200.apollo.ct.f0.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ct.f0.f0.md)
- **ARTIFACTS:**
  - [mac_gog_file_keyring.md](https://github.com/bobs-org/bob-cli--plans/blob/bb59949df0c858908a049b09b41475bab78e152f/202611/mac_gog_file_keyring.md)

%model:@medium #gh:gh_bobs-org__bob-cli [@plan:202611/mac_gog_file_keyring.md][1]

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):

- agent_recipe = skill (planner default: skill). Implement the "agent_recipe = skill"
  branch; ignore "agent_recipe = none". Context: "Should the sase_gmail skill gain a
  narrow section teaching agents the Mac SSH draft recipe?".
- followup_drafts = draft (planner default: draft). Implement the "followup_drafts =
  draft" branch; ignore "followup_drafts = skip". Context: "After you approve the gate,
  should the follow-up agent create the Dan Dowd and Samuel Lam Gmail drafts?".
- keychain_cleanup = keep (planner default: keep). Implement the "keychain_cleanup =
  keep" branch; ignore "keychain_cleanup = delete". Context: "Should the script delete
  the six old gogcli macOS keychain items once the file keyring is verified?". Implement
  only the branches selected above.

[1]:
  https://github.com/bobs-org/bob-cli--plans/blob/bb59949df0c858908a049b09b41475bab78e152f/202611/mac_gog_file_keyring.md
