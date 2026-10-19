%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/ref_create_mac_latency.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- arrivals = join (planner default: join). Implement the "arrivals = join" branch; ignore "arrivals = hint". Context: "Should references that arrive while the Refs panel is open join the visible list on their own?".
- intake_cadence = two_min (planner default: two_min). Implement the "intake_cadence = two_min" branch; ignore "intake_cadence = keep". Context: "Should athena and apollo drain their xlib/ intake queue every 2 minutes instead of every 10?".
Implement only the branches selected above.
