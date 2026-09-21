---
name: competitor-research
description: Maps competitors, substitutes, internal/manual alternatives, price anchors, switching costs, and positioning gaps for any business category without assuming a mobile-app market.
---

# Skill: Competitor Research

## Purpose

Understand what the buyer uses **instead of the proposed solution**. The strongest competitor is often a spreadsheet, employee, agency, existing bundled tool, internal process, or doing nothing.

## Categories

1. **Direct** — same buyer + same problem + similar solution.
2. **Indirect** — same problem, different solution.
3. **Manual/internal substitute** — labor, spreadsheets, email/chat, scripts, in-house tools.
4. **Service substitute** — consultant, agency, freelancer, managed service.
5. **Do nothing / tolerate the pain**.
6. **Emerging** — new entrant or incumbent feature that could collapse the opportunity.

## Research fields

For each important alternative record:
- buyer/user,
- geography,
- pricing or labor cost if publicly supported,
- core workflow,
- strengths,
- repeated complaints,
- switching cost,
- integrations/data lock-in,
- evidence source and date,
- confidence.

Do not estimate revenue/user counts from review counts unless explicitly labeled as a rough model assumption.

## Source order

Choose sources appropriate to the market:
- vendor pricing/docs,
- customer reviews and community discussions,
- implementation case studies,
- job postings/manual workflow evidence,
- procurement/tenders,
- official filings/statistics,
- app stores only when the product really is an app.

## Gap test

A "gap" is valid only if:
1. multiple users/buyers show the pain, and
2. incumbents do not already solve it adequately, and
3. the gap matters enough to affect time, money, risk, revenue, or switching behavior.

"Competitor has bad UI" is not a meaningful gap by itself.

## Output

For a fixed idea write `memory/ideas/<slug>/competitors.json`.

Include:
- direct_competitors
- indirect_competitors
- manual_internal_substitutes
- service_substitutes
- do_nothing_baseline
- emerging_threats
- price_anchors
- repeated_complaints
- validated_gaps
- switching_costs
- evidence_limitations
