---
name: evidence-validation
trigger: "User has a concrete startup/business idea and wants to know whether it is worth testing"
exit_output: "memory/ideas/<slug>/decision_memo.md"
---

# Workflow: Evidence-Led Idea Validation

## Startup Announcement

> **Starting: Evidence Validation**
> I will test whether the problem, buyer, workaround, willingness-to-pay signals, competition, and distribution path are real before recommending implementation.

## Step 1 — Capture the hypothesis

Create `memory/ideas/<slug>/idea.md` with:
- proposed customer/user,
- proposed buyer,
- problem,
- proposed solution,
- expected value,
- key assumptions,
- what is currently unknown.

Do not rewrite assumptions as facts.

## Step 2 — Problem evidence

Run `problem-evidence-miner`.

The validation should fail early if there is no credible evidence that the problem is recurring, costly, urgent, or already paid for.

## Step 3 — Competitors and substitutes

Run `competitor-research`.

The baseline is not merely another startup. Include:
- manual labor,
- spreadsheets,
- generic tools,
- consultants/agencies,
- internal development,
- doing nothing.

Record actual public pricing when available.

## Step 4 — Monetization and distribution evidence

Research:
- who controls budget,
- existing price anchors,
- purchasing friction,
- sales cycle if B2B,
- plausible first acquisition channel,
- whether founder has direct access to potential buyers.

Use upstream pricing/distribution skills only when their assumptions fit the business category.

## Step 5 — Market size only if defensible

Use `tam-sam-som-builder` only when the inputs are source-backed and the method fits the category.

If market size depends mostly on generic multipliers or unsourced conversion assumptions, label it **LOW CONFIDENCE** and do not let it drive the decision.

## Step 6 — Evidence audit

Run `evidence-quality-gate`.

Explicitly list:
- confirmed observations,
- inferences,
- estimates,
- contradictory evidence,
- unanswered critical questions.

## Step 7 — Riskiest assumption and behavioral experiment

Choose the assumption with the highest combination of criticality and uncertainty.

Design a test that is:
- cheaper than building the full product,
- time-bounded,
- behavioral rather than opinion-only,
- binary enough to support a decision.

Examples:
- ask 20 qualified businesses for a paid pilot,
- landing page with a real price and booking/payment intent,
- deliver the outcome manually to 5 customers,
- offer a paid setup/concierge version before automation.

## Step 8 — Decision memo

Write `memory/ideas/<slug>/decision_memo.md` with:

1. **Evidence status:** VALIDATED ENOUGH TO TEST / RESEARCH MORE / DROP FOR NOW
2. Buyer + problem in one sentence
3. Strongest observed evidence
4. Strongest contradictory evidence
5. Existing workaround + spend/labor
6. Competition/substitutes
7. Distribution path
8. Biggest unknown
9. Riskiest-assumption test
10. Pass threshold
11. Kill criterion
12. Next action

A legacy 0–100 score may be appended, but it must be labeled "heuristic" and may not override the evidence status.
