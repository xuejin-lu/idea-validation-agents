# Project State

- phase: launch_asset_finalization
- selected_candidate: Taiwan multi-channel e-commerce month-close / reconciliation
- discovery_status: complete
- focused_validation_status: READY_FOR_REAL_WORLD_TEST
- exact_wedge_payment: unproven
- posting_state: assets_not_finalized
- delivery_state: DELIVERY_BLOCKED_PENDING_PRO_REVIEW
- next_gate: real buyer commitment
- next_codex_action: finalize direct-use launch assets
- software_build_allowed: false
- broad_discovery_allowed: false

## Decision history

- Broad Taiwan opportunity discovery converged on e-commerce workflows.
- Fixed-scope e-commerce back-office operations was demoted to a service because founder-labor scaling risk remains high.
- Multi-channel month-close/reconciliation advanced because recurrence and standardizable units are more credible.
- Focused validation reached `READY_FOR_REAL_WORLD_TEST`.
- Behavioral-test preparation produced listing/intake/deliverable specifications.
- Review found that posting readiness and delivery readiness must be separated.
- Real buyer-data delivery remains blocked until the professional/accounting boundary is reviewed.

## Automation boundary

The repository/Codex workflow can:
- prepare and version test assets,
- generate synthetic demo data,
- prepare forms/notices/logs,
- commit and push,
- audit incoming evidence once it exists in the repository.

It cannot, without separate authorized external access:
- log into Tasker/PRO360/community accounts,
- publish listings,
- message buyers,
- receive marketplace responses,
- obtain real commitment/payment.

Never fabricate these actions.

## Stop condition

Once launch assets are finalized, if no real external buyer behavior is available in the repository, Codex must return:

`WAITING_FOR_EXTERNAL_BEHAVIOR`

instead of repeating research or regenerating assets.
