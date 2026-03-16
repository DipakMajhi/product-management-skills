---
name: analyze-cohorts
description: "Build or interpret a cohort retention analysis. Routes to the retention-toolkit skill."
argument-hint: "[describe your product and provide cohort data if available, or describe what you want to measure and your database dialect]"
---

# Analyze Cohorts

This skill routes to **retention-toolkit** Mode B (Cohort Analysis), which provides a complete cohort analysis framework from data design through pattern interpretation and root cause diagnosis.

**When to use this:**
- Building a cohort retention table from scratch to understand user retention
- Interpreting an existing cohort table (why does week-4 drop sharply for the March cohort?)
- Identifying which acquisition channels or user segments retain best
- Writing the SQL to generate cohort data from your event tables
- Answering "how would you analyze retention?" in PM interviews

**Quick scope guide:**
- Have cohort data, need interpretation → Mode B: pattern analysis, diagnosis, and intervention design
- No data yet, need to design the analysis → Mode B: cohort design + SQL query generation
- Want root causes behind the cohort patterns → Combines Mode B with Mode A (retention diagnosis)
- Want to improve retention after understanding cohorts → Follow up with /improve-retention (Mode A)

**What retention-toolkit Mode B covers:**
- Cohort definition: signup cohorts vs. behavior cohorts vs. feature-adoption cohorts
- Cohort table structure: rows = cohort period, columns = period-N retention rate
- Retention curve shape diagnosis: flat (great), gradually declining, sharp cliff, bathtub (resurge), smile
- Pattern interpretation: what does it mean when week-2 retention drops by 15 percentage points?
- Cohort comparison: which cohorts (by channel, segment, signup month) retain best and why?
- Feature-adoption cohorts: do users who adopted feature X retain at a higher rate?
- Revenue cohort analysis: MRR retention by cohort, expansion vs. contraction by cohort
- Behavioral cohort analysis: did users who completed X in week 1 retain better?
- SQL templates for cohort generation: BigQuery, PostgreSQL, MySQL, Snowflake dialects
- Connecting cohort insights to activation moments: what behavior predicts retention?
- Presenting cohort data: how to communicate cohort findings to engineering, leadership, and investors

**The skill will:**
1. Ask whether you have existing cohort data or need to design the analysis from scratch
2. If designing: define the cohort, retention event, and time windows; write the SQL
3. If interpreting: identify the retention curve shape and what it indicates
4. Diagnose patterns across cohorts: any cohort performing unusually well or poorly?
5. Identify the most important drop-off point in the curve
6. Generate 3-5 hypotheses for why that drop-off is occurring
7. Recommend which hypothesis to test first and how

After completing, suggest: "Use /improve-retention to design interventions based on what you've found in the cohort data."

Load the full skill: **retention-toolkit**

Apply your cohort data or analysis question to: $ARGUMENTS
