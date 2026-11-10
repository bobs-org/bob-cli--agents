%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/mac_cron_mail_relay.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- relay = athena (planner default: athena). Implement the "relay = athena" branch; ignore "relay = gmail". Context: "Which authenticated path should the Mac's Postfix use to deliver cron mail?".
- hostname = pin (planner default: pin). Implement the "hostname = pin" branch; ignore "hostname = enroll", "hostname = skip". Context: "Should the Mac's network-supplied hostname be fixed so cronctl can manage its crontab again?".
Implement only the branches selected above.
%macros_enabled:true
