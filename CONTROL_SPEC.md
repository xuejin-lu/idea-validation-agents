# Current Control Spec

## Phase

**Launch Asset Finalization — Candidate A**

Do not reopen broad discovery.
Do not build software.
Do not claim the market test has launched.

Selected candidate:

> Taiwan multi-channel e-commerce month-close / reconciliation preparation

Current status:

- research: complete enough for behavioral testing
- exact-wedge payment: unproven
- posting/lead-generation assets: mostly prepared
- actual delivery boundary: not yet professionally confirmed
- next objective: make the test package executable without fabricating external actions

Read and obey:
- `FOUNDER_CONSTRAINTS.md`
- `RESEARCH_GATES.md`
- `PROJECT_STATE.md`
- latest behavioral-test package files under `memory/`

## Important state split

Do not use one generic `READY_TO_LAUNCH` state.

Separate:

1. `READY_TO_POST`
   - listing copy, intake, privacy notice, demo and measurement log are ready;
   - founder may publish the offer to collect real buyer behavior.

2. `READY_TO_DELIVER`
   - actual buyer-data handling and service delivery are allowed only after the professional/accounting boundary has been reviewed and the data-handling process is acceptable.

3. `DELIVERY_BLOCKED_PENDING_PRO_REVIEW`
   - posting/commitment-seeking may proceed, but real delivery must not start yet.

The goal of this run is to finish Stage 1 assets and make the Stage 2 blocker explicit.

## Required outputs

Create/update all of the following in Traditional Chinese.

### 1. Direct-use intake asset

Create:

`memory/intake_form.md`

It must be directly copyable into a form tool or sent to a prospect.

Include:
- minimum qualification questions,
- explicit request for redacted sample only,
- no password/OTP/backend login,
- privacy/data-handling notice,
- professional-boundary disclaimer,
- request for a fixed-scope quote/commitment.

Do not merely describe what a form should contain.

### 2. Actual synthetic demo package

Create a small demo directory using only synthetic data:

`memory/demo/`

At minimum:
- `normalized_demo.csv`
- `exceptions_demo.csv`
- `accountant_handoff_demo.md`
- `README.md`

The data must be invented/demo-only and clearly labeled as such.

The demo must demonstrate:
- traceability back to source IDs,
- at least one matched item,
- at least one missing/refund/fee exception,
- unresolved items,
- accountant-review flags,
- no tax/accounting conclusion.

### 3. Measurement log

Create:

`memory/measurement_log.csv`

Columns must cover:
- timestamp
- channel
- listing/version
- inbound case ID
- segment match
- commercial stage
- redacted sample offered
- fixed-scope quote accepted
- scheduled start
- paid commitment
- exception categories
- operator hours
- professional review required
- stop/rejection reason
- month-two continuation

Seed with header only. Do not fabricate prospects.

### 4. Privacy/data-handling notice

Create:

`memory/data_handling_notice.md`

It must state:
- what data is requested,
- what must be redacted,
- what must never be sent,
- temporary storage expectations,
- access limitation,
- deletion/retention procedure,
- no reuse for model training/public portfolio,
- what happens if regulated/professional accounting judgment is required.

Do not claim compliance certifications that do not exist.

### 5. Professional-boundary review brief

Create:

`memory/professional_review_brief.md`

This is a short question list that can be handed to a Taiwan-qualified accountant/bookkeeping/tax professional.

Ask them to review:
- whether the proposed data-preparation/reconciliation scope crosses into regulated bookkeeping/accounting/tax representation,
- which wording should be removed,
- which output fields require professional review,
- whether accepting a paid fixed-scope data-preparation engagement is acceptable before formal bookkeeping/tax work,
- minimum contract/disclaimer/data-handling precautions.

Do not answer these questions yourself unless directly supported by authoritative Taiwan law.

### 6. Launch handoff

Create:

`memory/launch_handoff.md`

It must contain exactly:
- which listing copy to use,
- which demo files to attach/show,
- which intake asset to send,
- what counts as commitment,
- what NOT to promise,
- where human/external account action is required,
- how to record responses in `measurement_log.csv`.

## State decision

At the end, set both states separately:

- `posting_state: READY_TO_POST | NOT_READY_TO_POST`
- `delivery_state: READY_TO_DELIVER | DELIVERY_BLOCKED_PENDING_PRO_REVIEW | NOT_READY_TO_DELIVER`

Expected default if assets are complete but no professional review has occurred:

- `posting_state: READY_TO_POST`
- `delivery_state: DELIVERY_BLOCKED_PENDING_PRO_REVIEW`

Do not label the whole project simply `READY_TO_LAUNCH`.

## External action rule

If Codex does not have authorized external marketplace/account access:
- do not attempt to fabricate posting;
- do not claim a buyer was contacted;
- mark `EXTERNAL_ACTION_REQUIRED`.

This run ends after assets are created, committed, pushed, and remote delivery is verified.

## Next phase

After this run, further `開始` commands must **not** regenerate the same assets.

If no real buyer behavior has been imported into the repository yet, stop with:

`WAITING_FOR_EXTERNAL_BEHAVIOR`

and identify the missing external evidence rather than repeating research or preparation.
