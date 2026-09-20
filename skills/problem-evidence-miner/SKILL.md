---
name: problem-evidence-miner
description: Finds source-backed evidence that a problem is recurring, costly, urgent, or already paid for. Separates observations from inference and model estimates.
---

# Skill: Problem Evidence Miner

## Purpose

Research the **problem before the product**. Determine whether a specific workflow/pain is real enough to justify further startup work.

## Inputs

- Problem space, industry, buyer segment, or idea slug
- Optional geography
- Optional `memory/user_profile.md`
- Existing files under `memory/market_insights/` and `memory/ideas/<slug>/`

## What to look for

Collect evidence across multiple independent source types when possible:

### Strong signals
- public pricing for a product/service already solving the problem,
- procurement/tender records,
- job postings showing paid labor devoted to the workflow,
- documented implementation/case-study costs,
- repeated paid consultants/agencies,
- public filings or official data showing costs/volume,
- actual user behavior or conversion tests.

### Useful pain signals
- repeated reviews with the same complaint,
- independent forum/community threads describing the same workflow,
- support tickets/feature requests visible publicly,
- templates/spreadsheets/checklists used as workarounds,
- "how do you handle X?" discussions revealing manual steps,
- documented errors, delays, compliance burden, or rework.

### Weak signals
- generic market reports with no transparent method,
- social views/likes,
- one viral post,
- an LLM's own estimate.

Weak signals can guide search but cannot validate the problem.

## Evidence record

For every evidence item capture:

- source / URL or file reference,
- source type,
- publication/update date,
- target user/buyer represented,
- exact claim supported,
- `evidence_role`: pain | paid_labor | transaction | competition | regulatory_context | market_context,
- `claim_type`: observed | inferred | estimated,
- `tier`: A | B | C | D,
- independence from other evidence,
- geography,
- freshness,
- limitations.

Do not count syndicated copies of the same underlying source as independent evidence.

## Problem synthesis

For each problem, derive:

- **user**
- **economic buyer**
- **job/workflow**
- **trigger**
- **frequency** — only quantify if sourced
- **severity**
- **current workaround**
- **current spend/labor** — source-backed or unknown
- **consequence of failure/delay**
- **switching friction**
- **evidence of willingness to pay**
- **contradictory evidence**
- **unknowns**

## Evidence-role rule

Do not treat all strong-looking sources as proof of the same thing.

- Government regulations/process documents usually prove `regulatory_context`, not buyer pain.
- Vendor pricing/features usually prove `competition` or a price anchor, not demand.
- Job postings can prove `paid_labor` when the exact workflow appears in recurring duties.
- Customer requests/reviews, workflow discussions, case evidence, and actual submissions can prove `pain`.
- Documented purchases, service transactions, or conversion behavior can prove `transaction`.

To qualify as a real problem opportunity, require at least two independent Taiwan-specific items whose primary roles are among `pain`, `paid_labor`, or `transaction`. At least one should be `paid_labor` or `transaction`, unless the buyer-side pain evidence is exceptionally direct and repeated.

Do not let regulatory complexity + vendor pricing pass as demand validation.

## Validation rules

Mark `problem_evidence_status`:

- **strong** — at least one Tier A signal plus independent supporting evidence, or several independent Tier B signals with clear spend/labor and buyer.
- **moderate** — repeated independent pain evidence, but spend/urgency/buyer is incomplete.
- **weak** — mostly attention/trend signals or isolated anecdotes.
- **unsupported** — no credible independent evidence.

Never upgrade weak evidence merely because many search results repeat the same claim.

## Output

Write to `memory/problem_evidence/<slug>.json` (or `memory/ideas/<slug>/problem_evidence.json` for a fixed idea).

Include:

```json
{
  "problem": "",
  "user": "",
  "economic_buyer": "",
  "problem_evidence_status": "strong | moderate | weak | unsupported",
  "evidence_items": [
    {
      "source": "",
      "evidence_role": "pain | paid_labor | transaction | competition | regulatory_context | market_context",
      "claim_type": "observed | inferred | estimated",
      "tier": "A | B | C | D"
    }
  ],
  "current_workaround": [],
  "spend_or_labor_evidence": [],
  "willingness_to_pay_evidence": [],
  "contradictory_evidence": [],
  "unknowns": [],
  "research_gaps": []
}
```
