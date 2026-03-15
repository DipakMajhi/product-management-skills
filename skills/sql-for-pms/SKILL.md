---
name: sql-for-pms
description: "Generate correct, readable, well-commented SQL queries for product analytics. Covers 25+ PM query patterns including DAU/WAU/MAU, retention (D1/D7/D30), cohort analysis, funnel analysis, feature adoption, revenue metrics (MRR, ARR, ARPU, churn rate), user segmentation, and A/B test analysis. Includes window functions (ROW_NUMBER, LAG, LEAD, running totals, moving averages), CTE-based query structure, dialect differences (BigQuery, PostgreSQL, Snowflake, MySQL), SQL optimization tips (partitioning, avoiding full scans), common PM SQL mistakes, and self-serve analytics patterns. Use when querying product data, writing or debugging SQL, understanding user behavior from a database, or building analytics queries without waiting for a data analyst."
argument-hint: "[describe the business question you want to answer, the database dialect (BigQuery/PostgreSQL/Snowflake/MySQL), and any known table or column names]"
---

# SQL for Product Managers

You generate correct, readable, well-commented SQL queries for product analytics use cases. You explain what each query does in plain English so the PM understands the logic and can modify it confidently.

Apply this skill to: $ARGUMENTS

## Query Writing Standards

### Always Follow These Rules

1. Use CTEs (WITH clause) to make complex queries readable -- one logical step per CTE
2. Add comments explaining the business logic, not the SQL syntax
3. Use meaningful alias names (not "a", "b", "c" -- use "active_users", "first_sessions", etc.)
4. Include a LIMIT clause on exploratory queries to avoid scanning too much data
5. Note assumed table and column names and ask for confirmation if uncertain
6. Specify the dialect and note any syntax that differs across platforms

### Query Structure Template

```sql
-- QUESTION: [Business question in plain English]
-- DIALECT: [BigQuery / PostgreSQL / Snowflake / MySQL]
-- ASSUMPTIONS: [Table names, column names, date formats assumed]

WITH step_one AS (
  -- [Business logic explanation]
  SELECT ...
),

step_two AS (
  -- [Business logic explanation]
  SELECT ...
)

SELECT
  [columns with clear aliases]
FROM step_two
ORDER BY [meaningful ordering]
LIMIT 1000;
```

---

## PM SQL Pattern Library

### Category 1: User Activity and Engagement

**Daily/Weekly/Monthly Active Users (DAU/WAU/MAU)**

```sql
-- DAU/WAU/MAU calculation
-- Assumes: events table with user_id, event_timestamp
WITH daily_active AS (
  SELECT
    DATE(event_timestamp) AS activity_date,
    COUNT(DISTINCT user_id) AS dau
  FROM events
  WHERE event_timestamp >= CURRENT_DATE - INTERVAL '30 days'
  GROUP BY DATE(event_timestamp)
),

weekly_active AS (
  SELECT
    DATE_TRUNC('week', event_timestamp) AS week_start,
    COUNT(DISTINCT user_id) AS wau
  FROM events
  WHERE event_timestamp >= CURRENT_DATE - INTERVAL '90 days'
  GROUP BY DATE_TRUNC('week', event_timestamp)
)

SELECT * FROM daily_active ORDER BY activity_date DESC;
```

**DAU/MAU Ratio (Stickiness)**

```sql
-- Stickiness ratio: DAU/MAU
-- A ratio above 20% indicates healthy engagement
WITH monthly_active AS (
  SELECT COUNT(DISTINCT user_id) AS mau
  FROM events
  WHERE event_timestamp >= CURRENT_DATE - INTERVAL '30 days'
),

daily_avg AS (
  SELECT AVG(dau) AS avg_dau
  FROM (
    SELECT DATE(event_timestamp) AS d, COUNT(DISTINCT user_id) AS dau
    FROM events
    WHERE event_timestamp >= CURRENT_DATE - INTERVAL '30 days'
    GROUP BY DATE(event_timestamp)
  ) daily
)

SELECT
  daily_avg.avg_dau,
  monthly_active.mau,
  ROUND(daily_avg.avg_dau * 100.0 / monthly_active.mau, 1) AS stickiness_pct
FROM daily_avg, monthly_active;
```

**Feature Adoption Rate**

```sql
-- What percentage of active users used feature X this month?
WITH active_users AS (
  SELECT COUNT(DISTINCT user_id) AS total_active
  FROM events
  WHERE event_timestamp >= CURRENT_DATE - INTERVAL '30 days'
),

feature_users AS (
  SELECT COUNT(DISTINCT user_id) AS feature_active
  FROM events
  WHERE event_name = 'feature_x_used'
    AND event_timestamp >= CURRENT_DATE - INTERVAL '30 days'
)

SELECT
  feature_users.feature_active,
  active_users.total_active,
  ROUND(feature_users.feature_active * 100.0 / active_users.total_active, 1) AS adoption_pct
FROM feature_users, active_users;
```

### Category 2: Retention Analysis

**Day-N Retention (D1, D7, D30)**

```sql
-- D1, D7, D30 retention by signup cohort
-- Assumes: users table (user_id, signup_date), events table (user_id, event_timestamp)
WITH cohort AS (
  SELECT
    user_id,
    DATE(signup_date) AS cohort_date
  FROM users
  WHERE signup_date >= CURRENT_DATE - INTERVAL '90 days'
),

user_activity AS (
  SELECT
    c.user_id,
    c.cohort_date,
    DATE(e.event_timestamp) AS activity_date,
    DATE(e.event_timestamp) - c.cohort_date AS days_since_signup
  FROM cohort c
  JOIN events e ON c.user_id = e.user_id
)

SELECT
  cohort_date,
  COUNT(DISTINCT user_id) AS cohort_size,
  COUNT(DISTINCT CASE WHEN days_since_signup = 1 THEN user_id END) AS d1_retained,
  COUNT(DISTINCT CASE WHEN days_since_signup = 7 THEN user_id END) AS d7_retained,
  COUNT(DISTINCT CASE WHEN days_since_signup = 30 THEN user_id END) AS d30_retained,
  ROUND(COUNT(DISTINCT CASE WHEN days_since_signup = 1 THEN user_id END) * 100.0
    / COUNT(DISTINCT user_id), 1) AS d1_pct,
  ROUND(COUNT(DISTINCT CASE WHEN days_since_signup = 7 THEN user_id END) * 100.0
    / COUNT(DISTINCT user_id), 1) AS d7_pct,
  ROUND(COUNT(DISTINCT CASE WHEN days_since_signup = 30 THEN user_id END) * 100.0
    / COUNT(DISTINCT user_id), 1) AS d30_pct
FROM user_activity
GROUP BY cohort_date
ORDER BY cohort_date;
```

**Cohort Retention Table**

```sql
-- Full cohort retention grid (week-over-week)
WITH cohort AS (
  SELECT
    user_id,
    DATE_TRUNC('week', signup_date) AS cohort_week
  FROM users
),

activity AS (
  SELECT
    c.user_id,
    c.cohort_week,
    DATE_TRUNC('week', e.event_timestamp) AS activity_week
  FROM cohort c
  JOIN events e ON c.user_id = e.user_id
),

retention AS (
  SELECT
    cohort_week,
    (DATE_PART('day', activity_week - cohort_week) / 7)::INT AS week_number,
    COUNT(DISTINCT user_id) AS active_users
  FROM activity
  GROUP BY cohort_week, week_number
)

SELECT
  cohort_week,
  MAX(CASE WHEN week_number = 0 THEN active_users END) AS week_0,
  MAX(CASE WHEN week_number = 1 THEN active_users END) AS week_1,
  MAX(CASE WHEN week_number = 2 THEN active_users END) AS week_2,
  MAX(CASE WHEN week_number = 3 THEN active_users END) AS week_3,
  MAX(CASE WHEN week_number = 4 THEN active_users END) AS week_4
FROM retention
GROUP BY cohort_week
ORDER BY cohort_week;
```

### Category 3: Funnel Analysis

**Step-by-Step Funnel Conversion**

```sql
-- Onboarding funnel: signup -> profile -> first action -> activation
WITH funnel AS (
  SELECT
    user_id,
    MIN(CASE WHEN event_name = 'signup_complete' THEN event_timestamp END) AS step_1,
    MIN(CASE WHEN event_name = 'profile_complete' THEN event_timestamp END) AS step_2,
    MIN(CASE WHEN event_name = 'first_core_action' THEN event_timestamp END) AS step_3,
    MIN(CASE WHEN event_name = 'activation_milestone' THEN event_timestamp END) AS step_4
  FROM events
  WHERE event_timestamp >= CURRENT_DATE - INTERVAL '30 days'
  GROUP BY user_id
)

SELECT
  COUNT(step_1) AS step_1_signup,
  COUNT(step_2) AS step_2_profile,
  COUNT(step_3) AS step_3_first_action,
  COUNT(step_4) AS step_4_activated,
  ROUND(COUNT(step_2) * 100.0 / NULLIF(COUNT(step_1), 0), 1) AS step_1_to_2_pct,
  ROUND(COUNT(step_3) * 100.0 / NULLIF(COUNT(step_2), 0), 1) AS step_2_to_3_pct,
  ROUND(COUNT(step_4) * 100.0 / NULLIF(COUNT(step_3), 0), 1) AS step_3_to_4_pct,
  ROUND(COUNT(step_4) * 100.0 / NULLIF(COUNT(step_1), 0), 1) AS overall_conversion_pct
FROM funnel;
```

### Category 4: Revenue Metrics

**MRR and Growth Decomposition**

```sql
-- MRR decomposition: new, expansion, contraction, churn
WITH monthly_revenue AS (
  SELECT
    user_id,
    DATE_TRUNC('month', payment_date) AS month,
    SUM(amount) AS mrr
  FROM payments
  GROUP BY user_id, DATE_TRUNC('month', payment_date)
),

mrr_changes AS (
  SELECT
    curr.month,
    curr.user_id,
    curr.mrr AS current_mrr,
    prev.mrr AS previous_mrr
  FROM monthly_revenue curr
  LEFT JOIN monthly_revenue prev
    ON curr.user_id = prev.user_id
    AND curr.month = prev.month + INTERVAL '1 month'
)

SELECT
  month,
  SUM(CASE WHEN previous_mrr IS NULL THEN current_mrr ELSE 0 END) AS new_mrr,
  SUM(CASE WHEN current_mrr > previous_mrr AND previous_mrr IS NOT NULL
    THEN current_mrr - previous_mrr ELSE 0 END) AS expansion_mrr,
  SUM(CASE WHEN current_mrr < previous_mrr
    THEN previous_mrr - current_mrr ELSE 0 END) AS contraction_mrr,
  SUM(current_mrr) AS total_mrr
FROM mrr_changes
GROUP BY month
ORDER BY month;
```

**ARPU by Segment**

```sql
-- Average revenue per user by plan type
SELECT
  u.plan_type,
  COUNT(DISTINCT u.user_id) AS users,
  SUM(p.amount) AS total_revenue,
  ROUND(SUM(p.amount) / COUNT(DISTINCT u.user_id), 2) AS arpu
FROM users u
JOIN payments p ON u.user_id = p.user_id
WHERE p.payment_date >= CURRENT_DATE - INTERVAL '30 days'
GROUP BY u.plan_type
ORDER BY arpu DESC;
```

### Category 5: Window Functions for Product Analytics

**Running Total**

```sql
-- Cumulative signups over time
SELECT
  DATE(signup_date) AS day,
  COUNT(*) AS daily_signups,
  SUM(COUNT(*)) OVER (ORDER BY DATE(signup_date)) AS cumulative_signups
FROM users
GROUP BY DATE(signup_date)
ORDER BY day;
```

**7-Day Rolling Average DAU**

```sql
-- Smoothed DAU trend (7-day moving average)
WITH daily AS (
  SELECT
    DATE(event_timestamp) AS day,
    COUNT(DISTINCT user_id) AS dau
  FROM events
  GROUP BY DATE(event_timestamp)
)

SELECT
  day,
  dau,
  ROUND(AVG(dau) OVER (
    ORDER BY day
    ROWS BETWEEN 6 PRECEDING AND CURRENT ROW
  ), 0) AS rolling_7day_avg
FROM daily
ORDER BY day;
```

**Previous Period Comparison (LAG)**

```sql
-- Week-over-week comparison of active users
WITH weekly AS (
  SELECT
    DATE_TRUNC('week', event_timestamp) AS week,
    COUNT(DISTINCT user_id) AS wau
  FROM events
  GROUP BY DATE_TRUNC('week', event_timestamp)
)

SELECT
  week,
  wau,
  LAG(wau) OVER (ORDER BY week) AS prev_week_wau,
  ROUND((wau - LAG(wau) OVER (ORDER BY week)) * 100.0
    / NULLIF(LAG(wau) OVER (ORDER BY week), 0), 1) AS wow_change_pct
FROM weekly
ORDER BY week DESC;
```

**Top N per Group (ROW_NUMBER)**

```sql
-- Top 3 most-used features per user segment
WITH feature_usage AS (
  SELECT
    u.segment,
    e.event_name AS feature,
    COUNT(*) AS usage_count,
    ROW_NUMBER() OVER (
      PARTITION BY u.segment
      ORDER BY COUNT(*) DESC
    ) AS rank
  FROM events e
  JOIN users u ON e.user_id = u.user_id
  GROUP BY u.segment, e.event_name
)

SELECT segment, feature, usage_count
FROM feature_usage
WHERE rank <= 3
ORDER BY segment, rank;
```

### Category 6: A/B Test Analysis

```sql
-- A/B test results: conversion rate by variant with confidence
WITH test_results AS (
  SELECT
    variant,
    COUNT(DISTINCT user_id) AS users,
    COUNT(DISTINCT CASE WHEN converted = true THEN user_id END) AS conversions
  FROM ab_test_assignments
  WHERE test_name = 'onboarding_v2'
  GROUP BY variant
)

SELECT
  variant,
  users,
  conversions,
  ROUND(conversions * 100.0 / users, 2) AS conversion_rate_pct,
  ROUND(conversions * 100.0 / users
    - (SELECT conversions * 100.0 / users FROM test_results WHERE variant = 'control'), 2)
    AS lift_vs_control_pp
FROM test_results
ORDER BY variant;
```

---

## Dialect Differences

| Feature | PostgreSQL | BigQuery | Snowflake | MySQL |
|---|---|---|---|---|
| Date truncation | DATE_TRUNC('month', col) | DATE_TRUNC(col, MONTH) | DATE_TRUNC('MONTH', col) | DATE_FORMAT(col, '%Y-%m-01') |
| Date arithmetic | col + INTERVAL '30 days' | DATE_ADD(col, INTERVAL 30 DAY) | DATEADD('day', 30, col) | DATE_ADD(col, INTERVAL 30 DAY) |
| Integer division | col::INT or CAST | CAST(col AS INT64) | col::INTEGER | CAST(col AS SIGNED) |
| String concatenation | col1 \|\| col2 | CONCAT(col1, col2) | col1 \|\| col2 | CONCAT(col1, col2) |
| NULLIF | NULLIF(x, 0) | NULLIF(x, 0) | NULLIF(x, 0) | NULLIF(x, 0) |
| Array functions | ARRAY_AGG | ARRAY_AGG | ARRAY_AGG | GROUP_CONCAT |
| Temp functions | Not native | CREATE TEMP FUNCTION | Not supported | Not native |

**General rule**: Write in PostgreSQL syntax as the most portable, then adapt for BigQuery or Snowflake as needed.

---

## SQL Optimization Tips for PMs

| Problem | Solution |
|---|---|
| Query scans entire table | Add WHERE clause on partitioned column (usually date); use LIMIT for exploration |
| Query takes minutes to run | Use approximate functions (APPROX_COUNT_DISTINCT in BigQuery); reduce date range |
| Joining large tables is slow | Filter each table in CTEs before joining; join on indexed columns |
| NULL handling errors | Use COALESCE(column, 0) for calculations; remember NULL != NULL (use IS NULL) |
| Division by zero | Wrap divisors in NULLIF(column, 0) |
| Date filtering off-by-one | BETWEEN is inclusive on both ends; use >= and < for precise ranges |
| Results look wrong | Check for duplicate rows from JOINs; use COUNT(DISTINCT) instead of COUNT |

---

## Common PM SQL Mistakes

| Mistake | Example | Fix |
|---|---|---|
| Counting duplicates | COUNT(user_id) on joined table | Use COUNT(DISTINCT user_id) |
| NULL comparison | WHERE status = NULL | Use WHERE status IS NULL |
| Date range error | BETWEEN '2026-01-01' AND '2026-01-31' misses Jan 31 timestamps | Use >= '2026-01-01' AND < '2026-02-01' |
| Not handling NULLs in NOT IN | WHERE id NOT IN (SELECT id FROM ...) fails if subquery returns NULL | Use NOT EXISTS or add WHERE id IS NOT NULL |
| Over-fetching data | SELECT * FROM events (billions of rows) | Always filter by date and add LIMIT for exploration |
| Using functions on indexed columns | WHERE DATE(created_at) = '2026-01-01' | Use WHERE created_at >= '2026-01-01' AND created_at < '2026-01-02' |
| Ambiguous column names | Joining tables with same column name without alias | Always use table_alias.column_name |

---

## Process for Answering a PM's Data Question

1. **Understand the business question**: Restate it in your own words to confirm understanding
2. **Identify tables and columns**: What data is needed? What schema is assumed?
3. **Write the query**: Use CTEs, comments, and meaningful aliases
4. **Explain in plain English**: What the query does and what the output will look like
5. **Flag assumptions**: Table names, column names, date ranges, data quality assumptions
6. **Offer follow-ups**: What related question might the PM want to answer next?
7. **Note dialect**: Specify BigQuery/PostgreSQL/Snowflake and flag any dialect-specific syntax

---

## Output Template

```
SQL QUERY: [Business Question]
Dialect: [BigQuery / PostgreSQL / Snowflake / MySQL]

[SQL query with CTEs and comments]

PLAIN ENGLISH EXPLANATION
[2-4 sentences: what this query does, what the output columns mean, what to look for]

ASSUMPTIONS TO VERIFY
- Table [name] exists with columns [list]
- [Date column] is in [timezone/format]
- [Any data quality assumptions]

FOLLOW-UP QUERY SUGGESTION
[Related question the PM might want to answer next, with a brief description of the query]

DIALECT NOTES
[Any syntax that would need to change for a different database]
```
