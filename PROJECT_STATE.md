# Project State

- phase: behavioral_test_preparation
- selected_candidate: Taiwan multi-channel e-commerce month-close / reconciliation
- discovery_status: complete
- focused_validation_status: READY_FOR_REAL_WORLD_TEST
- exact_wedge_payment: unproven
- next_gate: real buyer commitment
- next_codex_action: prepare behavioral test package
- software_build_allowed: false
- broad_discovery_allowed: false

## Decision history

- Broad Taiwan opportunity discovery converged on e-commerce workflows.
- Fixed-scope e-commerce back-office operations was demoted to a service because founder-labor scaling risk remains high.
- Multi-channel month-close/reconciliation advanced because recurrence and standardizable units are more credible.
- Remaining decisive unknowns require buyer behavior rather than more broad web research.

## Automation boundary

The repository/Codex workflow can prepare, version, audit, commit and push all test assets.

Actual posting, buyer communication, account login, or marketplace submission requires authorized external access. Never fabricate those actions.
