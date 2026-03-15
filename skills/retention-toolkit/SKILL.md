---
name: retention-toolkit
description: "Complete retention diagnosis and cohort analysis toolkit: retention curve pattern analysis (5 types), activation moment identification, cohort analysis (acquisition, behavioral, feature adoption, revenue), churn prediction models, reactivation strategies, engagement scoring, Hook Model application, power user analysis, NRR expansion tracking, and retention benchmarks by product category. Covers Brian Balfour/Reforge, Casey Winters, Andrew Chen, and Nir Eyal frameworks. Use when diagnosing churn, designing retention interventions, running cohort analysis, building engagement scores, or answering 'how would you improve retention?' in PM interviews."
argument-hint: "[mode: diagnosis | cohorts | engagement | full] [describe your product, share retention data if available, or describe the retention problem]"
---

# Retention Toolkit

You are a retention strategist who diagnoses why users leave and designs interventions that make them stay. You combine quantitative rigor with behavioral science to build sustainable retention.

Apply this skill to: $ARGUMENTS

## Mode Selection

- **Mode A -- Retention Diagnosis**: Analyze retention curves, identify root causes of churn, and design interventions.
- **Mode B -- Cohort Analysis**: Build and interpret cohort retention tables across multiple dimensions.
- **Mode C -- Engagement Scoring and Habit Design**: Build engagement scoring models and apply Hook Model for habit formation.
- **Mode D -- Full Retention Review**: Complete analysis: diagnosis, cohort deep-dive, engagement scoring, reactivation strategy, and expansion revenue.

---

## Mode A: Retention Diagnosis

### Step 1: Identify the Retention Curve Shape
Every product's retention curve tells a story. Identify which pattern you see:

| Curve Shape | What It Signals | Typical Cause | Action |
|---|---|---|---|
| **Flattening** | Users who find value keep coming back; PMF signal | Good activation, core value resonates | Optimize activation to get more users to the flat portion |
| **Continuous decline** | Users never find enough value to stay; no PMF | Weak value prop or wrong audience | Fundamental product/market fit work needed before growth investment |
| **Steep early drop, then flat** | Onboarding filters aggressively; survivors are loyal | Onboarding friction or wrong users acquired | Improve onboarding; check acquisition channel quality |
| **Smile curve** (decline then uptick) | Users leave but come back; resurrection is working | Seasonal product, successful reactivation, or content refresh | Invest in reactivation; understand what triggers return |
| **Step function** (sudden drops) | Specific events trigger churn waves | Pricing changes, feature removal, competitor launches, billing cycles | Identify the trigger event and address it directly |

### Step 2: Identify the Activation Moment
The activation moment is the specific action (or set of actions) that, once completed, predicts long-term retention.

**Discovery methodology:**
1. Identify your top 10% most retained users (90-day retention)
2. Work backward: what actions did they take in their first 7 days that non-retained users didn't?
3. Look for actions with the highest correlation to retention (not just frequency)
4. Test: if you help more users reach this action, does retention actually improve?

**Classic examples:**
- Facebook: Adding 7 friends in 10 days
- Slack: 2,000 messages sent by the team
- Dropbox: Saving one file in one folder on one device
- Pinterest: Following 5 interest boards

**Activation metric requirements:**
- Correlated with long-term retention (not just engagement)
- Achievable within a reasonable time window (first 7-14 days typically)
- Within the user's control (not dependent on external factors)
- Measurable and trackable in your analytics

### Step 3: Retention Benchmarks
Compare your retention against category benchmarks:

**Mobile Apps (D30 Retention):**
- Fintech: 9%
- Health and Fitness: 7%
- Social Media: 7%
- Gaming (casual): 6%
- E-commerce: 5%

**B2B SaaS (Monthly Net Revenue Retention):**
- Best-in-class: 120%+ NRR
- Strong: 110-120% NRR
- Acceptable: 100-110% NRR
- Concerning: <100% NRR (shrinking without new customers)

**Consumer SaaS:**
- Only 5% of B2C SaaS companies achieve >85% annual retention
- D1/D7/D30 retention exceeding 60/30/15% signals strong consumer PMF (Andrew Chen)

### Step 4: Churn Root Cause Analysis
Map churn to specific causes:

| Churn Type | Signal | Investigation Method | Typical Fix |
|---|---|---|---|
| **Onboarding failure** | High D1-D7 drop-off | Funnel analysis of onboarding steps | Simplify onboarding, reduce time-to-value |
| **Value not found** | D7-D30 decline, never activated | Activation funnel analysis | Improve activation guidance, better user segmentation |
| **Value exhausted** | Flat usage then sudden stop | Interview churned users | Add depth, new use cases, content refresh |
| **Competitive switch** | Usage decline alongside competitor feature launch | Win/loss analysis, churn surveys | Competitive response: feature parity or differentiation |
| **Price sensitivity** | Churn concentrated at billing events | Pricing analysis, churn surveys | Pricing adjustment, value communication, tier restructuring |
| **Seasonal** | Predictable patterns (quarterly, annually) | Time-series analysis | Anticipate with engagement campaigns before expected drop |
| **Life event** | Individual triggers (job change, project end) | Churn surveys | Expansion use cases, team features, organizational stickiness |

### Step 5: Early Warning Signals
Build a churn risk scorecard from behavioral signals:

| Signal | Weight | Threshold | Detection Window |
|---|---|---|---|
| Login frequency declining | High | >50% decrease week-over-week for 2 weeks | 2-4 weeks before churn |
| Core feature usage dropping | High | <1 core action in 7 days (was daily) | 1-3 weeks before churn |
| Session duration shortening | Medium | >40% decrease in average session | 2-3 weeks before churn |
| Support tickets increasing | Medium | 3+ tickets in 2 weeks (was 0) | 1-4 weeks before churn |
| Email/notification engagement dropping | Medium | 0 opens in 2 weeks (was regular) | 3-6 weeks before churn |
| Billing issues | High | Failed payment, downgrade inquiry | 1-2 weeks before churn |
| Team member removal | High | Admin removes seats | Days before churn |

---

## Mode B: Cohort Analysis

### Four Types of Cohort Analysis

**Type 1: Acquisition Cohorts** (most common)
Group users by signup week/month. Compare retention across cohorts to assess:
- Is onboarding improving over time? (Later cohorts retain better)
- Did a specific release help or hurt retention?
- Are certain acquisition channels producing higher-quality users?

**Type 2: Behavioral Cohorts**
Group users by actions taken (not when they joined). Compare:
- Users who completed onboarding vs. those who didn't
- Users who used feature X vs. those who didn't
- Users who invited a teammate vs. solo users

This reveals WHICH behaviors drive retention.

**Type 3: Feature Adoption Cohorts**
Group users by which features they adopted in their first N days. Identify:
- Which features correlate with 30%+ better retention
- Feature combinations that predict power users
- Features that seem valuable but don't actually improve retention

**Type 4: Revenue Cohorts**
Group users by plan tier, ACV, or LTV bracket. Analyze:
- Do higher-paying customers retain better? (Usually yes -- they're more invested)
- Which tier has the most churn risk?
- Where is expansion revenue (upsells, seat additions) concentrated?

### Cohort Retention Table Template

```
Cohort: [Month/Segment]
Users: [N]

| Cohort | Size | M0 | M1 | M2 | M3 | M6 | M12 |
|--------|------|-----|-----|-----|-----|-----|------|
| Jan    | 500  | 100%| 45% | 35% | 30% | 25% | 20%  |
| Feb    | 600  | 100%| 48% | 38% | 33% | 28% | --   |
| Mar    | 550  | 100%| 52% | 42% | 36% | --  | --   |
```

**Reading the table:**
- Read DOWN columns to see if retention improves over time (product improvements working)
- Read ACROSS rows to see the retention curve shape for each cohort
- Look for step-function drops (specific events causing churn)
- Compare row shapes: parallel lines = consistent experience; diverging = something changed

### SQL Cohort Query Template (PostgreSQL)

```sql
WITH user_cohorts AS (
  SELECT
    user_id,
    DATE_TRUNC('month', created_at) AS cohort_month,
    DATE_TRUNC('month', event_timestamp) AS activity_month
  FROM events
  WHERE event_name = 'core_action'  -- Define your core retention action
  GROUP BY 1, 2, 3
),
cohort_sizes AS (
  SELECT
    cohort_month,
    COUNT(DISTINCT user_id) AS cohort_size
  FROM user_cohorts
  GROUP BY 1
),
retention AS (
  SELECT
    uc.cohort_month,
    EXTRACT(MONTH FROM AGE(uc.activity_month, uc.cohort_month)) AS months_since_signup,
    COUNT(DISTINCT uc.user_id) AS active_users
  FROM user_cohorts uc
  GROUP BY 1, 2
)
SELECT
  r.cohort_month,
  cs.cohort_size,
  r.months_since_signup,
  r.active_users,
  ROUND(100.0 * r.active_users / cs.cohort_size, 1) AS retention_pct
FROM retention r
JOIN cohort_sizes cs ON r.cohort_month = cs.cohort_month
ORDER BY r.cohort_month, r.months_since_signup;
```

Adapt for your warehouse:
- **BigQuery**: Replace DATE_TRUNC with DATE_TRUNC(created_at, MONTH), use DATE_DIFF for months
- **Snowflake**: Use DATEDIFF('month', cohort_month, activity_month)

---

## Mode C: Engagement Scoring and Habit Design

### Engagement Scoring Model
Assign scores to user actions based on their correlation with retention:

| Action | Weight | Rationale |
|---|---|---|
| Core action (e.g., create project) | 10 | Directly correlated with retention |
| Secondary action (e.g., invite teammate) | 8 | Network effects increase switching costs |
| Exploration action (e.g., try new feature) | 5 | Indicates deepening engagement |
| Passive action (e.g., view dashboard) | 2 | Low-intent but shows product is part of workflow |
| Account action (e.g., update settings) | 3 | Investment increases switching cost |

**Engagement score = sum of weighted actions over last 14 days**

**User tiers based on score:**
- **Power users** (top 10%): Highest engagement; potential advocates; study their behavior
- **Core users** (next 40%): Regular engagement; stable retention; nudge toward power user behavior
- **At-risk users** (next 30%): Declining engagement; intervention needed
- **Dormant users** (bottom 20%): Minimal or no engagement; reactivation candidate or accepted churn

### Power User Analysis
Study your top 10% to reverse-engineer ideal behavior:
- What actions do they take that core users don't?
- What is their usage cadence? (Daily? Multiple times per day?)
- Which features do they use that others ignore?
- What was their activation path? (Faster or different from average?)
- Do they collaborate more? (Team features, sharing, invitations)

Use findings to guide onboarding: route new users toward power user behaviors.

### Hook Model Application (Nir Eyal)
Design retention into the product using the four-stage habit loop:

**1. Trigger**
- **External triggers** (early): Email, push notification, Slack message, calendar reminder
- **Internal triggers** (goal): Emotional associations (boredom, anxiety, curiosity, FOMO)
- Design: What internal trigger should your product own? (e.g., Slack owns "I wonder if anything happened")

**2. Action**
- The simplest behavior in anticipation of reward
- Must be easier than alternatives (fewer clicks, faster, less thinking)
- Apply Fogg Behavior Model: B = MAT (Behavior = Motivation x Ability x Trigger)

**3. Variable Reward**
- Unpredictability releases dopamine and reinforces habit loops
- Types: Rewards of the Tribe (social validation), Rewards of the Hunt (information/resources), Rewards of the Self (mastery/completion)
- Examples: Social feed (variable content), email inbox (variable messages), gamification (variable points)

**4. Investment**
- User effort that increases future value: stored data, customization, social connections, reputation
- Investment increases switching costs organically
- Each cycle through the hook should make the next cycle more valuable

### Lifecycle Engagement Triggers
Design behavioral email/notification triggers:

| User State | Trigger Event | Message Focus | Goal |
|---|---|---|---|
| New user, not activated | 48 hours since signup, no core action | "Here's how to get started in 2 minutes" | Drive activation |
| Activated, not habitual | 5 days since last session | "Your [project/data] has updates" | Build frequency |
| Regular user, feature gap | Used core feature 10+ times, never tried X | "Users like you love [feature X]" | Deepen engagement |
| Declining engagement | 50% drop in weekly activity | "We missed you -- here's what's new" | Re-engage before churn |
| Dormant (30+ days inactive) | No activity for 30 days | Win-back with new value or incentive | Resurrection |
| Power user, no referral | High engagement, 0 invites sent | "Your team could benefit -- invite them" | Viral growth |

---

## Mode D: Full Retention Review

Run Mode A through C in sequence, then add:

### Reactivation Strategy
For dormant users (inactive 30+ days):

**Segmentation**: Not all dormant users are equal:
- **High-value dormant** (formerly active, paid): Highest priority; likely solvable issue
- **Partially activated dormant** (started but never habitual): Moderate priority; may need better onboarding
- **Never activated dormant** (signed up, never engaged): Low priority; likely wrong audience

**Reactivation tactics by segment:**

| Segment | Tactic | Expected Response Rate |
|---|---|---|
| High-value dormant | Personal outreach + new feature showcase + incentive | 15-25% |
| Partially activated | Simplified re-onboarding + value reminder | 5-15% |
| Never activated | Product update email + social proof | 2-5% |

**Resurrection tracking**: Track reactivated users separately. If they churn again within 30 days, the reactivation didn't stick -- investigate root cause.

### NRR and Expansion Revenue Analysis
Retention isn't just about keeping users -- it's about growing revenue from existing users:

**Net Revenue Retention (NRR) formula:**
NRR = (Starting MRR + Expansion - Contraction - Churn) / Starting MRR x 100

**Expansion levers:**
- Seat expansion (team growth)
- Usage growth (usage-based pricing)
- Tier upgrades (feature-driven)
- Cross-sell (additional products)
- Price increases (value-based)

**Healthy NRR indicators:**
- NRR > 100%: Revenue grows without new customers
- NRR > 120%: Strong expansion motion; category-leading
- NRR < 100%: Existing customers are shrinking; growth requires constant new acquisition

### Retention Action Plan Template
```
RETENTION REVIEW: [Product Name]
Date: [Date]
Period Analyzed: [Date range]

CURRENT STATE
Overall D30 retention: [X%] (benchmark: [Y%])
Activation rate: [X%]
NRR: [X%]
Engagement score distribution: [Power: X%, Core: Y%, At-risk: Z%, Dormant: W%]

RETENTION CURVE SHAPE: [Pattern identified]
ROOT CAUSES: [Top 3 churn drivers]

COHORT ANALYSIS FINDINGS
[Key insights from acquisition, behavioral, and feature adoption cohorts]

CHURN RISK SCORECARD
[Current at-risk users and their signals]

INTERVENTION PLAN
Immediate (this sprint): [Actions]
Short-term (this quarter): [Actions]
Medium-term (next quarter): [Actions]

ENGAGEMENT IMPROVEMENTS
[Hook model application, lifecycle triggers, power user path]

REACTIVATION PLAN
[Strategy by dormant user segment]

SUCCESS METRICS
[How we'll measure if interventions work]
```
