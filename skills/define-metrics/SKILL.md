---
name: define-metrics
description: "Define a North Star Metric, supporting input metrics, and guardrail metrics for a product or feature. Routes to the metrics-and-okrs skill."
argument-hint: "[describe your product, how it delivers value to users, and what business model it supports]"
---

# Define Metrics

This skill routes to **metrics-and-okrs** Mode B (Full Metrics Framework), which provides a complete metrics hierarchy from North Star to guardrails.

**When to use this:**
- Defining metrics for a new product or major feature from scratch
- Discovering your team is measuring vanity metrics that don't reflect real value
- Building a metrics tree to show what moves the North Star
- Aligning the team on a single most-important metric to optimize for
- Preparing for a PM interview question about metrics or success measurement

**Quick scope guide:**
- Want just the North Star Metric → Use /north-star instead (Mode A, focused)
- Want the full hierarchy (NSM + input metrics + guardrails + AARRR) → This command (Mode B)
- Want to build OKRs from these metrics → Follow up with /plan-okrs (Mode C)
- Want to write SQL to measure these → Follow up with /write-query

**What metrics-and-okrs Mode B covers:**
- North Star Metric definition: the single metric that best captures delivered customer value
- Business game classification: attention (daily engagement), transaction (volume × value), productivity (time-to-outcome), transformation (behavior change)
- 5-point NSM quality test: does it capture value, predict retention, guide trade-offs, is it measurable, is it actionable?
- Input metrics: 3-5 leading indicators that drive the NSM (the levers your team controls)
- Guardrail metrics: what must NOT degrade when optimizing the NSM (revenue, latency, NPS, churn)
- AARRR (Pirate Metrics) overlay: mapping Acquisition, Activation, Retention, Referral, Revenue to your hierarchy
- HEART framework (Google): Happiness, Engagement, Adoption, Retention, Task Success — for UX-heavy products
- Metric tree visualization: showing how input metrics roll up to the NSM
- Common metric anti-patterns: vanity metrics, lagging-only metrics, too many metrics, metrics divorced from user value

**The skill will:**
1. Ask about your product's core value exchange and business model
2. Classify the business game to guide metric selection
3. Define a candidate North Star Metric and test it against the 5-point quality test
4. Identify 3-5 input metrics that are the levers to move the NSM
5. Define guardrail metrics to prevent local optimizations that harm the whole
6. Build the metric tree showing the full hierarchy

Load the full skill: **metrics-and-okrs**

Apply your product context to: $ARGUMENTS
