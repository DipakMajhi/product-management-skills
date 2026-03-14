---
name: north-star-metric
description: "Define a North Star Metric and supporting input metrics for a product. Use this skill when someone needs to identify the right North Star for their product, understand the Business Game their product plays (attention, transaction, or productivity), or set up a metrics hierarchy. Pairs with the metrics-framework skill in pm-product-execution."
---

# North Star Metric Framework

A North Star Metric (NSM) is the single metric that best captures the core value your product delivers to users and that, when it grows, drives sustainable long-term business success.

## The Business Game Classification

Apply this skill to: $ARGUMENTS


Sean Ellis and Amplitude's research identified three "business games" products play:

**Attention Game**: Products that monetize time and engagement
- NSM tends to be: Time spent, content consumed, sessions per user
- Examples: Spotify, Netflix, YouTube, TikTok
- Risk: Optimizing attention at the expense of user wellbeing

**Transaction Game**: Products that monetize when a transaction occurs
- NSM tends to be: Transactions completed, GMV, bookings
- Examples: Airbnb, Uber, Amazon, Stripe
- Risk: Optimizing transaction volume at expense of transaction quality

**Productivity Game**: Products that monetize by making users more effective
- NSM tends to be: Tasks completed, time saved, goals achieved
- Examples: Slack, Notion, Figma, Salesforce
- Risk: Optimizing feature usage over actual outcomes

## NSM Quality Test

A good North Star Metric:
1. Measures value delivered to users, not just to the business
2. Is a leading indicator of long-term revenue (not revenue itself)
3. Is specific to your product (not generic like "DAU")
4. Can be improved by multiple teams across multiple levers
5. Is measurable and unambiguous

Bad NSM examples:
- Revenue (a business outcome, not a user value measure)
- DAU (measures presence, not value)
- "Number of features used" (activity, not value)

## NSM to Input Metrics Connection

An input metric is a metric the team can directly influence that, when improved, moves the North Star. The relationship should be causal, not just correlated.

Template: "If we increase [input metric] by improving [product area], the North Star will increase because [causal mechanism]."

## Output Template

---
**NORTH STAR METRIC DEFINITION**

**Product:** [Name]
**Business Game:** [Attention / Transaction / Productivity]
**Rationale:** [Why this game applies]

**Recommended North Star Metric**
Name: [Metric name]
Definition: [Precise definition - what counts, time window, what is excluded]
Current Baseline: [Value if known]
NSM Quality Test:
- Measures user value: Yes/No - [Reason]
- Leading indicator: Yes/No - [Reason]
- Product-specific: Yes/No - [Reason]
- Influenceable: Yes/No - [Reason]

**Input Metrics**
| Input Metric | Definition | How It Drives the NSM | Team Owner |
|---|---|---|---|
| [Metric 1] | | [Causal mechanism] | |
| [Metric 2] | | | |
| [Metric 3] | | | |

**Alternative NSM Candidates Considered**
| Candidate | Why Not Chosen |
|---|---|
| [Metric] | [Reason] |

**Alignment with Business Model**
[How this NSM, if grown sustainably, drives revenue for the business]
---
