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


## Externalizability Gate — Mandatory

A recurring paid workflow is not automatically a startup opportunity.

Evidence role `paid_labor` proves that the work exists and consumes payroll. It does **not** prove that the buyer wants an external vendor, software product, or new service.

To enter **Top Opportunities**, a candidate must now satisfy BOTH:

### A. Problem-existence evidence
At least two independent Taiwan-specific items across `pain`, `paid_labor`, or `transaction`.

### B. Externalizability / buying evidence
At least one **recent Taiwan-specific demand-side signal** showing one of:
- a buyer actively requests an external service or quote,
- a marketplace contains actual customer requests/reviews for that service category,
- a company publicly describes outsourcing the workflow,
- a customer pays for a comparable external service,
- repeated buyer-side discussions ask for a provider/tool rather than merely describing internal work.

A job posting alone cannot satisfy B.
A vendor pricing page alone cannot satisfy B.
A government requirement cannot satisfy B.

If A passes but B does not, classify the candidate as:

`Real workflow, external demand unproven`

not Top Opportunity.

## Recency Gate

For pain/externalizability evidence:
- prefer evidence from the last 24 months;
- evidence older than 24 months may support workflow continuity, but cannot be the sole direct pain signal;
- if the only buyer-side pain evidence is stale, the candidate must be `research-more` until refreshed.

## Review correction for next run

Re-check the current candidates:

- Construction quantity/billing: the Tasker request is useful buyer-side externalization evidence, but one request and an unconfirmed budget are not enough to call the opportunity strongest. Find additional independent recent buyer-side requests or demote.
- Tender readiness: PRO360 buyer requests/reviews are stronger externalization evidence; verify that the specific wedge is preflight/readiness rather than full proposal writing.
- E-commerce reconciliation: paid-labor evidence is strong, but the direct seller pain source is old. Find 2025–2026 buyer-side evidence for external help or demote.

Do not rank a candidate above another merely because the internal labor burden is larger. External buying behavior matters.


## Repeatability & Leverage Gate — Mandatory

A paid external service is not automatically a startup opportunity.

A candidate may be commercially real but still behave like one-off freelancing if every customer requires fully custom founder labor.

To appear in **Top Startup Opportunities**, a candidate must satisfy at least one of:

### A. Customer recurrence
There is evidence or a highly credible workflow reason that the same customer needs the service repeatedly:
- monthly,
- quarterly,
- per shipment,
- per tender,
- per project phase,
- or another recurring trigger.

### B. Cross-customer standardization
The workflow can plausibly reuse the same:
- input format,
- checklist,
- template,
- rules,
- QA process,
- or automation across multiple similar customers.

And the candidate must have a plausible **leverage path**:
- automation,
- reusable templates,
- delegation to trained operators,
- software-assisted processing,
- standardized intake/output,
- or another way to avoid founder-hours scaling 1:1 with revenue.

Do not require software from day one. Manual-first remains valid.
But if repeatability and leverage are both unproven, classify the candidate as:

`Real paid service, startup repeatability unproven`

not Top Startup Opportunity.

## Ranking rule

Separate these concepts:

1. **External demand strength** — will someone pay an outsider?
2. **Repeatability** — will the same workflow recur?
3. **Standardization** — can similar jobs share a process?
4. **Leverage** — can revenue grow without founder labor growing 1:1?

Do not rank a one-off freelance task above a recurring workflow solely because its marketplace evidence is newer or its visible budget is larger.

## Review correction for next run

Re-check current candidates:

- Vertical PDF/image conversion: external demand is real, but repeat purchase and reusable schema are not yet proven. Demote unless a narrow document family shows recurring volume and shared structure.
- E-commerce reconciliation: monthly recurrence is structurally stronger; verify whether the same input/output pattern repeats and whether customers need month-two service.
- Tender preflight: per-tender recurrence may exist; measure how often the target vertical bids and whether reusable company-document profiles reduce marginal work.
- Construction preconstruction/estimation: project recurrence exists, but professional expertise and custom scope may keep labor linear; require evidence of a standardizable sub-workflow.

For each candidate, explicitly output:
- recurrence trigger,
- expected recurrence type: same-customer | cross-customer | none/unknown,
- standardizable unit,
- leverage path,
- founder-labor scaling risk: low | medium | high.
