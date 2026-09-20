---
name: opportunity-discovery
trigger: "User wants startup/business opportunities and does not need to begin from a fixed idea"
exit_output: "memory/opportunity_shortlist.md"
---

# Workflow: Evidence-Led Opportunity Discovery

## Goal

Find problems worth testing before inventing products. This workflow replaces the upstream app-first idea-generation path.

## Startup Announcement

> **Starting: Opportunity Discovery**
> I will look for recurring problems, current workarounds, evidence of spend or labor, and only then turn the strongest problems into business concepts.

## Step 0 — Constraints, without interrogation

Use constraints already known from the conversation and `memory/user_profile.md` if available. Do **not** require the 10-question interview.

If essential constraints are absent, use conservative defaults:
- 1–3 person team
- low initial capital
- prototype or concierge test before full build
- no assumption that the answer must be an app

Record assumptions explicitly.

## Step 1 — Build a problem search space

Select 3–6 problem spaces using one or more of:
- industries the user can access,
- workflows with high administrative labor,
- compliance/reporting burdens,
- revenue leakage or errors,
- repetitive quoting/order-entry/reconciliation,
- coordination across email/chat/spreadsheets/PDFs,
- expensive expert services with repeatable sub-tasks,
- consumer categories where people already pay repeatedly.

Do not generate products yet.

## Step 2 — Run `problem-evidence-miner`

For each problem space, gather evidence of:
- repeated pain,
- frequency,
- severity/urgency,
- current workaround,
- existing spend or labor,
- economic buyer,
- switching friction,
- recentness,
- contradictory evidence.

Save one evidence record per problem.

Reject problems supported only by generic trend articles or a single anecdote.

## Step 3 — Convert evidence into opportunity hypotheses

For the strongest evidence clusters, create 5–8 opportunity hypotheses.

Each hypothesis must contain:
- target user,
- economic buyer,
- exact job/workflow,
- observed pain,
- current substitute,
- measurable value created,
- smallest testable offer,
- evidence references,
- largest unknown.

Do not add a feature just because AI can implement it.

## Step 4 — Run `competitor-research` on the best candidates

For the 3–5 strongest hypotheses:
- direct competitors,
- substitutes/manual process,
- internal build/do-nothing alternative,
- price anchors,
- complaint patterns,
- switching cost,
- evidence that buyers already pay.

## Step 5 — Run `evidence-quality-gate`

Audit every candidate. A candidate may advance only if:
- buyer is identified,
- pain evidence is repeated or Tier A,
- current workaround is known,
- value mechanism is measurable,
- at least one acquisition route is plausible.

Unknowns must remain visible.

## Step 6 — Design a cheap behavioral test

For the top 2–3 candidates, design the cheapest experiment that can falsify the riskiest assumption.

Prefer:
- manual concierge service,
- paid pilot offer,
- landing page with price,
- outbound to a narrow buyer list,
- workflow mockup + commitment request,
- deposit / LOI / trial request when appropriate.

Avoid surveys as the primary validation signal.

## Output

Write `memory/opportunity_shortlist.md`.

Use this structure:

# Opportunity Shortlist

## Research constraints
- ...

## Candidate A — <name>
- Target user:
- Economic buyer:
- Problem:
- Current workaround:
- Strongest evidence:
- Evidence quality: A/B/C/D mix
- Value mechanism:
- Why now:
- Main contradiction:
- Biggest unknown:
- Cheapest behavioral test:
- Kill criterion:

Repeat for each candidate.

## Not recommended now
Include discarded problem spaces and the specific missing gate/evidence. This prevents recycling weak ideas later.

## Final note
If a prioritization score is produced, put it in an appendix and label it a heuristic. The main shortlist must be justified by source-backed evidence, not score alone.
