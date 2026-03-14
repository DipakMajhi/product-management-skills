---
name: metrics-framework
description: "Define a metrics framework for a product including North Star Metric, input metrics, guardrail metrics, and a measurement plan. Use this skill when someone needs to define success metrics for a product or feature, set up a metrics dashboard, understand the difference between leading and lagging indicators, or answer "how would you measure success?" in a PM interview."
---

# Product Metrics Framework

Metrics are how a team navigates. Without the right metrics, a team is optimizing for the wrong outcomes or flying blind.

## Metric Hierarchy

Apply this skill to: $ARGUMENTS


### Layer 1: North Star Metric
One metric that best captures the core value the product delivers to users and that, if it grows sustainably, drives long-term business success.

Properties of a good North Star Metric:
- It measures user value, not just business value (DAU is not a North Star; it is an output)
- It is sensitive enough to move meaningfully week over week
- The whole team can influence it
- It is specific to this product (not generic like "revenue")

Examples:
- Spotify: "Time spent listening per user per week"
- Airbnb: "Nights booked"
- Slack: "Messages sent per active team per day"
- LinkedIn: "Monthly active professional interactions"

### Layer 2: Input Metrics (Leading Indicators)
3-5 metrics that the team can directly influence and that, when improved, predictably move the North Star Metric. These are the levers.

### Layer 3: Guardrail Metrics
Metrics that must NOT decline while the team improves the North Star. They protect against optimization that creates collateral damage.

Examples: If North Star is "sessions per user", guardrails might include "session satisfaction score" and "unsubscribe rate."

### Layer 4: Operational Metrics
Day-to-day health metrics: uptime, latency, error rates, support ticket volume. Important but not strategic.

## AARRR Metrics Framework (for growth products)

- **Acquisition**: How do users find and sign up?
- **Activation**: Do users have a meaningful first experience?
- **Retention**: Do users come back?
- **Referral**: Do users bring others?
- **Revenue**: Do users pay or generate revenue?

For most products, Retention is the most important lever. Fixing acquisition without fixing retention is filling a leaky bucket.

## Defining a Measurement Plan

For any feature or initiative, define:
1. **Primary metric**: The one metric this initiative is designed to move
2. **Direction and target**: Increase DAU by X%, Decrease churn by Y%
3. **Baseline**: Current value (without a baseline, you cannot measure improvement)
4. **Measurement method**: How will you track this? (product analytics, SQL query, A/B test)
5. **Time horizon**: When do you expect to see movement?
6. **Minimum detectable effect**: What change is meaningful vs. noise?

## Output Template

---
**METRICS FRAMEWORK: [Product Name]**

**North Star Metric**
Metric: [Name]
Definition: [Precise definition - what counts, what does not]
Current Baseline: [Value]
12-Month Target: [Value]
Rationale: [Why this metric captures the core value we deliver]

**Input Metrics**
| Metric | Definition | Current Baseline | Target | How It Drives North Star |
|---|---|---|---|---|
| [Metric 1] | [Definition] | [Value] | [Value] | [Mechanism] |
| [Metric 2] | | | | |
| [Metric 3] | | | | |

**Guardrail Metrics**
| Metric | Definition | Acceptable Floor |
|---|---|---|
| [Metric] | [Definition] | [Minimum acceptable value] |

**AARRR Snapshot** (where relevant)
| Stage | Key Metric | Current Value | Benchmark / Target |
|---|---|---|---|
| Acquisition | | | |
| Activation | | | |
| Retention | | | |
| Referral | | | |
| Revenue | | | |

**Data Infrastructure Notes**
[How these metrics are currently tracked, and any gaps in instrumentation]
---
