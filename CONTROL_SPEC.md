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
3. There are at least **two independent Taiwan-specific sources** supporting the problem or workaround.
4. At least one of those Taiwan sources is Tier A or Tier B under AGENTS.md.
5. The candidate can plausibly reach its first 10 Taiwanese prospects online without making cold calling/cold email the primary channel.
6. A meaningful behavioral validation can be attempted within NT$5,000 and three months.

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
