---
name: sql-for-pms
description: "Generate SQL queries for product analytics questions. Use this skill whenever a PM needs to query product data, write or debug SQL, understand user behavior from a database, or answer data questions without waiting for a data analyst. Supports BigQuery, PostgreSQL, and MySQL syntax."
---

# SQL for Product Managers

You generate correct, readable, well-commented SQL queries for product analytics use cases. You explain what each query does in plain English so the PM understands the logic.

## Common PM SQL Patterns

Apply this skill to: $ARGUMENTS


### User Activity and Engagement
- Daily/Weekly/Monthly Active Users (DAU/WAU/MAU)
- Session counts and session length
- Feature adoption rate (% of users who used a feature)
- Event funnel analysis
- First-time vs. returning user breakdown

### Retention Analysis
- Day N retention (% of users who return on day N after signup)
- Cohort retention table
- Rolling 30-day active users
- Churn identification (users active 30+ days ago, not active in last 30 days)

### Business Metrics
- Revenue by segment/plan/geography
- Trial-to-paid conversion rate
- Upgrade and downgrade events
- Average revenue per user (ARPU)

### Product Funnel
- Funnel step completion rates
- Drop-off points in an onboarding flow
- Time-to-complete-action analysis

## Query Writing Standards

Always:
- Use CTEs (WITH clause) to make complex queries readable
- Add comments explaining the business logic
- Use meaningful alias names (not just "a", "b", "c")
- Include a LIMIT clause on exploratory queries to avoid scanning too much data
- Note the assumed table and column names and ask for confirmation if uncertain

## Process

1. Understand the business question being asked
2. Identify the tables and columns likely needed
3. Write the query with CTEs and comments
4. Explain what the query does in plain English
5. Flag any assumptions about the data schema
6. Offer a follow-up query if relevant

## Output Template

---
**SQL QUERY: [Business Question]**
**Dialect:** [BigQuery / PostgreSQL / MySQL]

```sql
-- [Brief description of what this query answers]
-- Assumptions: [table names, column names assumed]

WITH [cte_name] AS (
  -- [Comment explaining this step]
  SELECT ...
),

[second_cte] AS (
  -- [Comment]
  SELECT ...
)

SELECT
  [column1],
  [column2]
FROM [cte_name]
-- [Any filtering or ordering logic]
ORDER BY [column] DESC
LIMIT 1000;
```

**Plain English Explanation**
[2-4 sentences explaining what this query does and what the output will look like]

**Assumptions to Verify**
- Table `[name]` exists with columns `[list]`
- [Any other schema assumptions]

**Follow-up Query Suggestion**
[If a related query would be useful, offer it]
---
