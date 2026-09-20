# Current Control Spec

## Phase

**WAITING_FOR_EXTERNAL_BEHAVIOR**

Do not run broad discovery.
Do not repeat focused validation.
Do not regenerate launch assets.
Do not build software.

Selected candidate:

> Taiwan multi-channel e-commerce month-close / reconciliation preparation

Current state:

- posting_state: `READY_TO_POST`
- delivery_state: `DELIVERY_BLOCKED_PENDING_PRO_REVIEW`
- exact-wedge payment: unproven
- next gate: real buyer behavior

Read and obey:
- `FOUNDER_CONSTRAINTS.md`
- `RESEARCH_GATES.md`
- `PROJECT_STATE.md`
- `memory/launch_handoff.md`
- `memory/measurement_log.csv`

## On every 「開始」

First inspect whether new external evidence exists.

New external evidence means at least one real, non-header row in `memory/measurement_log.csv`, or a clearly identified new evidence file under `memory/external_behavior/`.

### If NO new external evidence exists

Do not research.
Do not regenerate files.
Do not invent prospects.
Do not change conclusions.

Return only a short Traditional-Chinese status:

> WAITING_FOR_EXTERNAL_BEHAVIOR：目前尚無新的真實買方行為可分析。刊登資產已準備好；正式交付仍需專業邊界審查。

Do not create a new RUN commit merely for repeating the waiting state.

### If new external evidence DOES exist

Analyze only the new real-world evidence.

For each observed prospect/action classify:
- segment match
- channel
- commercial stage: interest | buyer_request | commitment | paid_transaction
- redacted sample provided: yes/no
- fixed-scope quote accepted: yes/no
- scheduled start: yes/no
- paid commitment: yes/no
- professional review required: yes/no
- stop/rejection reason
- month-two continuation: yes/no/unknown

Then decide one of:

- `CONTINUE_TEST`
- `ADVANCE_TO_DELIVERY_REVIEW`
- `PIVOT_SCOPE`
- `KILL_TEST`

Do not infer payment from inquiries or posted budgets.

## Delivery gate

Even if a buyer commits:

- do not start real buyer-data delivery while `delivery_state = DELIVERY_BLOCKED_PENDING_PRO_REVIEW`;
- require completed professional boundary review before changing delivery state;
- never fabricate professional approval.

## Output when evidence exists

Update:
- `memory/measurement_log.csv` only with real observed facts
- `memory/behavioral_test_review.md`
- `memory/RUN_MANIFEST.md`

Commit and push as a `RUN:` commit, then verify remote SHA.

## External action boundary

Repository/Codex can analyze evidence after it is recorded.

Actual posting, marketplace login, buyer messaging, quote acceptance, file receipt, payment, and professional review require authorized external action. Never claim these occurred unless evidence is actually present.
