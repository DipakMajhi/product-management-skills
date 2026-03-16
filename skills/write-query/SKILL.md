---
name: write-query
description: "Generate a SQL query for a product analytics question. Routes to the sql-for-pms skill."
argument-hint: "[describe what you want to measure and your database dialect: BigQuery, PostgreSQL, MySQL, or Snowflake]"
---

# Write Query

This skill routes to **sql-for-pms**, which generates production-ready SQL for 25+ common PM analytics query patterns across BigQuery, PostgreSQL, MySQL, and Snowflake.

**When to use this:**
- Pulling data to answer a specific product question without waiting for a data analyst
- Building a dashboard query for a product metric you own
- Checking whether an experiment moved a metric
- Answering "write a SQL query to find X" in PM technical interviews

**Quick query type guide:**
- Retention and cohort analysis → Week-N or month-N retention tables, cohort retention heatmaps
- Funnel analysis → Step-by-step conversion with drop-off rates between each step
- DAU / MAU / WAU → Rolling active user counts with configurable time windows
- Feature adoption → % of users who used feature X in their first N days
- Experiment results → Treatment vs. control comparison with significance proxies
- Power users → Defining and counting users above an activity threshold
- Churn signals → Users who were active 30 days ago but not in the last 7 days
- Revenue metrics → MRR, ARR, ARPU, expansion vs. contraction breakdown

**What sql-for-pms covers:**
- 25+ query templates across the most common PM analytics use cases
- Dialect-specific syntax: BigQuery, PostgreSQL, MySQL, Snowflake — including window functions, CTEs, date arithmetic
- Retention queries: cohort-based, event-based, feature-specific retention
- Funnel queries: ordered event sequence with per-step conversion and drop-off
- DAU/MAU/WAU queries: rolling windows, stickiness ratio (DAU/MAU)
- Cohort analysis: user cohorts by signup week, feature adoption cohorts
- A/B test analysis: treatment vs. control conversion rates, confidence intervals
- Power user queries: percentile-based segmentation
- Revenue queries: MRR movements (new, expansion, contraction, churn), LTV calculation
- Query explanation in plain English — always explains what the query does and what assumptions it makes
- Schema assumption documentation — flags column names and table structures assumed

**The skill will:**
1. Ask for the analytics question, database dialect, and any known schema details
2. Write the SQL query with clear comments explaining each section
3. Explain what the query does in plain English
4. Document schema assumptions explicitly
5. Offer alternative approaches if the query is complex
6. Flag performance considerations for large tables (indexing, partitioning hints)

Load the full skill: **sql-for-pms**

Apply your analytics question to: $ARGUMENTS
