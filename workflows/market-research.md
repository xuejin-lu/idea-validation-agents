---
name: market-research
trigger: "User wants to understand a market, industry, workflow category, or buyer segment"
exit_output: "memory/market_insights/<slug>-market-report.md"
---

# Workflow: Source-Backed Market Research

## Startup Announcement

> **Starting: Market Research**
> I will map buyers, recurring problems, substitutes, competitors, spending signals, distribution channels, and market structure. I will separate sourced facts from estimates.

## Research order

1. Define the market by **buyer + job/problem**, not by a vague technology label.
2. Find recurring workflows and pain using `problem-evidence-miner`.
3. Map competitors and substitutes using `competitor-research`.
4. Identify price anchors and evidence of existing spend.
5. Identify distribution and purchasing channels.
6. Find regulatory, procurement, integration, or trust constraints if relevant.
7. Estimate market size only when bottom-up inputs can be sourced.
8. Run `evidence-quality-gate`.

## Required report sections

Write `memory/market_insights/<slug>-market-report.md`:

# Market Research: <market>

## Definition
- Buyer:
- User:
- Job/problem:
- Geography:
- Scope exclusions:

## Evidence-backed pains
For each pain: source type, recurrence, severity, workaround, current spend/labor, confidence.

## Competitive structure
Direct competitors, substitutes, internal/manual alternatives, price anchors, switching friction.

## Demand and spending signals
Separate Tier A/B evidence from Tier C attention signals.

## Distribution / purchasing
How buyers discover, evaluate, approve, purchase, and renew.

## Market size
Only if defensible. Show formula, source for every input, assumptions, and sensitivity range.

## Contradictory evidence
What suggests the market may be weaker or harder than it first appears.

## Opportunity gaps
Only gaps that are supported by evidence.

## Unknowns
Critical facts not yet established.

## Recommended next research/test
The single cheapest action that would reduce the most uncertainty.

Do not output a giant TAM number without a bottom-up chain of evidence.
