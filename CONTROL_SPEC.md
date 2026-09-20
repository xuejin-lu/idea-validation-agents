# Current Control Spec

## Task

Run a **fresh Taiwan-first opportunity discovery** from scratch.

Use:
- `FOUNDER_CONSTRAINTS.md`
- `workflows/opportunity-discovery.md`
- `skills/problem-evidence-miner/SKILL.md`
- `skills/competitor-research/SKILL.md`
- `skills/evidence-quality-gate/SKILL.md`

Do not reuse the conclusions from earlier US-focused discovery runs.

## Taiwan Evidence Gate — Mandatory

A candidate may appear in **Top Opportunities** only if all of the following are true:

1. The target user or economic buyer exists in Taiwan.
2. The problem/workflow is demonstrated with **Taiwan-specific evidence**.
3. There are at least **two independent Taiwan-specific sources that directly support the pain, workaround, paid labor, or actual buyer behavior**.
4. At least one of those two sources must be a **demand-side or paid-labor signal**: e.g. customer reviews/requests, recurring job duties, documented manual workflow, service transactions, buyer-side case evidence, or actual conversion/usage behavior.
5. **Regulation, official process complexity, vendor feature pages, and vendor pricing are context/competition evidence only. They cannot by themselves satisfy the pain-evidence requirement.**
6. The candidate can plausibly reach its first 10 Taiwanese prospects online without making cold calling/cold email the primary channel.
7. A meaningful behavioral validation can be attempted within NT$5,000 and three months.

Foreign sources may:
- inspire a search hypothesis,
- explain a business model,
- provide comparison context.

Foreign sources may **not** by themselves:
- qualify a candidate for the shortlist,
- prove Taiwan demand,
- prove Taiwan willingness to pay,
- prove Taiwan regulatory applicability.

If an idea has strong foreign evidence but insufficient Taiwan evidence, put it under:

`Foreign inspiration — Taiwan unvalidated`

It must not appear in the Top Opportunities.

## Source preference for this run

Search Taiwan-specific evidence first. Examples:
- Taiwan government / laws / official statistics
- Taiwan industry associations
- 104 / local job listings when they reveal paid workflow labor
- Taiwan vendor/service pricing
- Taiwanese company documentation and case studies
- local marketplaces/directories
- PTT, Dcard, Mobile01, Facebook/LINE/community discussions when relevant
- Traditional-Chinese complaints, workflow discussions, templates, or service requests

Community anecdotes alone are not enough; use them to find stronger corroboration.

## Opportunity shape

Do not force AI, SaaS, or an app.

Prefer problems where:
- a small/niche Taiwan market is acceptable,
- manual service can be the first version,
- value can be measured in time, money, error/risk, or revenue,
- technical skill creates leverage but is not the reason the business exists.

## Output

Produce:
- `memory/opportunity_shortlist.md`
- `memory/opportunity_hypotheses.md`
- `memory/opportunity_competitor_map.md`
- `memory/evidence_audit.json`
- supporting evidence files as needed
- `memory/RUN_MANIFEST.md`

Do **not** recommend building software yet.
Do **not** recommend a paid pilot yet.
The purpose of this run is to find Taiwan-grounded candidates for ChatGPT review.


## Evidence Role Gate — Mandatory

For every evidence item, assign exactly one primary role:

- `pain` — directly shows the target user experiences the problem/workaround.
- `paid_labor` — shows people are paid to perform the workflow.
- `transaction` — shows customers actually purchase a solution/service.
- `competition` — proves an alternative/vendor exists.
- `regulatory_context` — proves a legal/process requirement.
- `market_context` — shows market size/infrastructure/attention, but not pain.

A candidate may enter Top Opportunities only if it has:
- at least two independent Taiwan-specific items across `pain`, `paid_labor`, or `transaction`;
- and at least one of those is `paid_labor` or `transaction`, or an unusually strong buyer-side `pain` signal.

Do not count a regulation plus two vendor pricing pages as three confirmations of customer pain.

If this gate fails, place the idea under:
`Interesting but pain not yet demonstrated`.

## This run's review correction

The previous run over-credited some evidence:
- official rules prove obligations, not unresolved pain;
- vendor pricing proves supply/price anchors, not demand volume;
- vendor blog posts may describe a workflow but can have sales bias.

Re-research prior candidates under the stricter Evidence Role Gate. Preserve any candidate that still passes; demote candidates that do not. Search for new Taiwan candidates if needed.
