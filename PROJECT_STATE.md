# Project State

- phase: WAITING_FOR_EXTERNAL_BEHAVIOR
- selected_candidate: Taiwan multi-channel e-commerce month-close / reconciliation
- discovery_status: complete
- focused_validation_status: READY_FOR_REAL_WORLD_TEST
- launch_asset_status: complete
- posting_state: READY_TO_POST
- delivery_state: DELIVERY_BLOCKED_PENDING_PRO_REVIEW
- exact_wedge_payment: unproven
- next_gate: real buyer behavior
- software_build_allowed: false
- broad_discovery_allowed: false

## Ready assets

- `memory/marketplace_listing_copy.md`
- `memory/intake_form.md`
- `memory/data_handling_notice.md`
- `memory/demo/`
- `memory/measurement_log.csv`
- `memory/professional_review_brief.md`
- `memory/launch_handoff.md`

## Current decision

The project has reached research saturation.

Further desk research is not the next step.

The next useful evidence must come from real buyer behavior:
- redacted sample sharing,
- fixed-scope acceptance,
- concrete commitment,
- payment,
- repeat/month-two behavior,
- comparable input/output structure across buyers.

## Automation boundary

Codex must not regenerate the same launch assets while waiting.

If `memory/measurement_log.csv` contains only its header and there is no new evidence under `memory/external_behavior/`, the correct state is:

`WAITING_FOR_EXTERNAL_BEHAVIOR`

Actual posting, buyer communication, payment, file receipt and professional review require authorized external action and must never be fabricated.

## Delivery boundary

Posting/lead collection may proceed.

Real buyer-data delivery remains blocked until a Taiwan-qualified accounting/bookkeeping/tax professional reviews the proposed service boundary.

Use `memory/professional_review_brief.md` for that review.
