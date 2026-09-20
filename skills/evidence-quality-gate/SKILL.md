---
name: evidence-quality-gate
description: Audits startup research claims for source strength, independence, freshness, contradiction, and unsupported precision before a decision is made.
---

# Skill: Evidence Quality Gate

## Purpose

Prevent polished research from outrunning its evidence.

## Audit every material claim

Classify each as:
- **Observed**
- **Inferred**
- **Estimated**
- **Unknown**

Assign evidence tier:
- **A** behavioral/transactional
- **B** repeated pain/workflow
- **C** attention/trend
- **D** model assumption

## Checks

1. **Source fit** — does the source represent the actual target buyer/geography?
2. **Independence** — are multiple sources genuinely independent?
3. **Freshness** — is the evidence recent enough for the claim?
4. **Directness** — does the source support the exact claim or only something adjacent?
5. **Contradiction** — is there credible counter-evidence?
6. **Precision** — are precise numbers backed by data, or created by a model?
7. **Selection bias** — are complaints/reviews being mistaken for population prevalence?
8. **Commercial signal** — is there evidence of spend/commitment, or only interest?
9. **Externalizability** — does the evidence show buyers will purchase/outsourced the workflow, or only that they hire employees to do it internally?
10. **Recency of buyer pain** — is there recent Taiwan buyer-side evidence, especially within the last 24 months?
11. **Repeatability** — does the workflow recur for the same customer or repeat across similar customers?
12. **Standardization** — is there a reusable unit of work, or is every job fully bespoke?
13. **Leverage** — can templates, delegation, automation, or software reduce founder-hours per unit of revenue?

## Hard-stop conditions

Return `research-more` or `insufficient` when:
- buyer is unclear,
- the candidate relies on job postings to infer external demand,
- the only direct buyer pain evidence is older than 24 months,
- no recent Taiwan-specific evidence shows outsourcing, vendor search, purchase, quote request, or comparable external buying behavior,
- the candidate is only a one-off paid service with no credible recurrence or cross-customer standardization,
- founder labor appears likely to scale 1:1 with revenue and no leverage path is identified,
- only Tier C/D evidence supports demand,
- willingness-to-pay is asserted without spend/behavioral evidence,
- TAM/CAC/LTV is mostly assumption-driven,
- one source is being counted as a market,
- contradictory evidence is ignored.

## Output

Write `evidence_audit.json` next to the research artifact being audited:

```json
{
  "status": "validated-enough-to-test | research-more | insufficient",
  "claim_audit": [],
  "strongest_evidence": [],
  "weakest_claims": [],
  "contradictions": [],
  "unsupported_precision": [],
  "critical_unknowns": [],
  "next_evidence_to_collect": ""
}
```

The status means:
- **validated-enough-to-test** — enough evidence to justify a cheap behavioral experiment, not a full build.
- **research-more** — promising, but a critical gate is still unknown.
- **insufficient** — evidence does not currently justify more founder time.


## Startup-vs-service classification

Every reviewed opportunity must receive one of:

- `startup-ready-to-test` — external demand + recurrence/standardization + plausible leverage path.
- `service-ready-to-test` — external demand exists, but repeatability/leverage is not yet strong enough for startup classification.
- `research-more` — one or more commercial gates remain unresolved.
- `insufficient` — evidence does not justify more time now.

A `service-ready-to-test` result is not a failure. It may be a useful cash-flow business or manual discovery vehicle, but do not label it a Top Startup Opportunity until repeatability/leverage improves.
