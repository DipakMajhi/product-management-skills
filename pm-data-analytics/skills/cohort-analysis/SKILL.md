---
name: cohort-analysis
description: "Design and interpret cohort analyses for product retention and engagement. Use this skill when someone needs to understand retention curves, compare user cohorts over time, analyze feature adoption by signup period, or identify when and why users churn."
---

# Cohort Analysis Guide

A cohort analysis tracks groups of users who share a common characteristic (usually signup date) and measures how their behavior evolves over time.

## Types of Cohort Analysis

Apply this skill to: $ARGUMENTS


### Retention Cohort
The most common type. Measures the % of users from a signup cohort who are still active N days/weeks/months later.

Output: A retention table where:
- Rows = signup cohorts (week or month)
- Columns = time periods (Day 1, Day 7, Day 14, Day 30...)
- Cells = % of users from that cohort still active at that period

Healthy SaaS retention benchmarks (Day 30): Consumer apps 20-40%, B2B SaaS 40-60%.

### Feature Adoption Cohort
Measures % of users from each cohort who have adopted a specific feature.
Use to understand: Is a new feature being adopted more by recent cohorts? (A sign of improving onboarding)

### Revenue Cohort
Measures revenue from each signup cohort over time.
Use to understand: Are newer cohorts more or less valuable than older ones? (Detects monetization changes)

## Reading a Retention Table

Look for:
- **Absolute retention level**: Is Day 30 retention at 20% or 40%? This is the headline number.
- **Improvement trend**: Are newer cohorts retaining better than older ones? (Product improving)
- **The "smile curve"**: Some products show decreasing then re-increasing retention (users who stay past a threshold become habitual users)
- **Step changes**: A cohort that retains significantly better may correspond to a product change you shipped. This is gold.

## Diagnosing Poor Retention

If Day 7 retention is low:
- Problem is in activation (users are not finding value in week 1)
- Investigate: onboarding completion rate, time to first value, day-1 confusion signals

If Day 30 retention is low but Day 7 is OK:
- Problem is in habit formation
- Investigate: feature depth, notification strategy, workflow integration

If long-term (90-day+) retention is low:
- Problem is in sustained value delivery
- Investigate: power user paths, expansion features, competitive alternatives

## Output Template

---
**COHORT ANALYSIS**
**Analysis Type:** Retention / Feature Adoption / Revenue
**Cohort Definition:** [e.g., users who signed up in [week/month]]
**Activity Definition:** [e.g., "active" = logged in and performed at least one core action]

**Retention Table**
| Cohort | Cohort Size | Day 1 | Day 7 | Day 14 | Day 30 | Day 60 | Day 90 |
|---|---|---|---|---|---|---|---|
| [Month 1] | N | X% | X% | X% | X% | X% | X% |
| [Month 2] | N | | | | | | |

**Trend Analysis**
[Are newer cohorts better or worse? What changed?]

**Benchmark Comparison**
Day 7 retention: [X%] vs. industry benchmark [Y%]
Day 30 retention: [X%] vs. industry benchmark [Y%]

**Diagnosis and Recommendations**
[Based on the pattern, what is the likely root cause and what should be investigated or changed?]
---
