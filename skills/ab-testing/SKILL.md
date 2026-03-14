---
name: ab-testing
description: "Design, size, and analyze A/B tests for product features. Use this skill when someone needs to design an experiment, calculate sample size, check if a test has reached statistical significance, interpret A/B test results, or understand when to ship, iterate, or stop a test. This is commonly tested in PM analytics interviews."
---

# A/B Testing Framework

A/B testing is how product teams make decisions with data instead of opinions. You help PMs design rigorous tests and interpret results correctly.

## Test Design Checklist

Apply this skill to: $ARGUMENTS


Before running any A/B test:

1. **Hypothesis**: "By changing [X], we expect [Y] to increase/decrease by [Z%] because [reasoning]."
2. **Primary metric (OEC)**: The single Overall Evaluation Criterion this test is designed to move.
3. **Secondary metrics**: Metrics to monitor for unintended effects or to explain the "why" behind results.
4. **Guardrail metrics**: Metrics that must NOT decline (e.g., latency, crash rate, revenue per user).
5. **Sample unit**: What is being randomized? (User, session, device, account, geographic cluster)
6. **Population**: Which users will be in the test? (All users? New users only? Paid users? Specific segments?)
7. **Traffic split**: 50/50 is standard and maximizes statistical power; justify any other split (e.g., risk mitigation with 90/10 for high-risk changes).
8. **Minimum detectable effect (MDE)**: The smallest improvement worth deploying, informed by business impact analysis.
9. **Required sample size**: Calculate before starting using the formula below.
10. **Test duration**: Run for at least one full weekly cycle to account for day-of-week effects; consider novelty and primacy effects.
11. **Interaction check**: Identify any other concurrent experiments that could interact with this one.
12. **Pre-launch validation**: Run A/A test or verify assignment mechanism distributes traffic evenly.

## Sample Size Calculation

### Frequentist Approach (Standard)

Formula for proportions:
Required N per variant = (16 x baseline_rate x (1 - baseline_rate)) / (MDE)^2

Where MDE is expressed as an absolute difference (not relative).

Example: Baseline conversion = 5%, MDE = 1 percentage point (20% relative lift)
N = (16 x 0.05 x 0.95) / (0.01)^2 = (0.76) / 0.0001 = 7,600 users per variant

Standard parameters: 95% confidence (alpha = 0.05), 80% statistical power (beta = 0.20).

For continuous metrics (e.g., revenue per user):
N per variant = (16 x variance) / (MDE)^2

### Adjustments to Sample Size

- **Multiple variants**: Apply Bonferroni correction. For K variants, use alpha/K as the significance threshold, which increases required N.
- **Multiple metrics**: If testing 5 metrics, expect 1 false positive at p < 0.05 by chance. Apply corrections or pre-designate one primary metric.
- **Cluster randomization**: Multiply N by the design effect factor: DE = 1 + (cluster_size - 1) x ICC, where ICC is the intra-cluster correlation.
- **CUPED variance reduction**: If using pre-experiment covariates, required N decreases by roughly 10-50% depending on covariate correlation.

### Duration Estimation

Required days = (Required N per variant x number of variants) / daily eligible traffic
Minimum duration: 7 days (one full weekly cycle). Recommended: 14 days for most tests.

## Statistical Approaches

### Frequentist Testing (Standard)
- Compute p-value: probability of observing the result if there were truly no difference.
- Statistically significant at p < 0.05 means less than 5% chance this is a false positive.
- Report confidence intervals alongside p-values for practical significance assessment.
- Important: p-values assume you commit to a sample size in advance and do not peek.

### Bayesian Testing
- Expresses results as "probability that variant B outperforms control" (e.g., "94% chance B is better").
- More intuitive for stakeholders. Does not require fixed sample sizes.
- Requires specifying priors (use weakly informative priors based on historical experiment data).
- Best for: early-stage products with limited traffic, continuous monitoring needs, or when incorporating prior experiment results.
- Decision rule: Ship if P(B > A) exceeds your threshold (e.g., 95%) AND expected lift exceeds minimum worthwhile effect.

### Sequential Testing (Always-Valid Inference)
- Allows continuous monitoring without inflating false positive rates.
- Uses always-valid p-values or confidence sequences that remain valid at any stopping time.
- Methods: mixture Sequential Probability Ratio Test (mSPRT), alpha-spending functions.
- Best for: high-velocity teams monitoring tests daily, situations where early stopping saves significant cost.
- Tradeoff: Slightly less power than fixed-horizon tests for equivalent sample size.

## Advanced Techniques

### CUPED (Controlled-experiment Using Pre-Experiment Data)
- Uses pre-experiment user behavior data to reduce variance in experiment metrics.
- Adjusts the metric: Y_adjusted = Y - theta x (X_pre - mean(X_pre)), where X_pre is the pre-experiment covariate.
- Typically improves sensitivity by 10-50%, equivalent to running the test with 20-100% more users.
- Requirements: A stable pre-experiment metric that correlates with the experiment metric.
- Used by Microsoft, Netflix, Airbnb, and most mature experimentation platforms.

### Stratified Sampling and Post-Stratification
- Divide users into homogeneous strata (e.g., by platform, country, activity level) before or after assignment.
- Reduces variance by removing between-stratum differences from the treatment effect estimate.
- Complementary to CUPED and can be stacked with it for additional power gains.

### Multi-Armed Bandit (Adaptive Allocation)
- Dynamically shifts traffic toward better-performing variants during the experiment.
- Lower regret (fewer users exposed to inferior variants) compared to fixed 50/50 split.
- Best for: short-lived optimizations (headlines, ad copy, UI variants) where speed matters more than precise measurement.
- Not suitable for: tests requiring precise effect size estimates or long-term impact measurement.
- Methods: Thompson Sampling, Upper Confidence Bound (UCB), Epsilon-Greedy.

### Handling Network Effects and Interference
When users influence each other (social products, marketplaces, messaging):
- **Cluster-randomized trials**: Randomize at the geographic region, team, or marketplace level instead of the individual user.
- **Switchback experiments**: Alternate treatment and control across time windows (e.g., hours or days). Useful for marketplace algorithms and pricing experiments.
- **Interleaving experiments**: For ranking/search tests, interleave results from both variants in the same session. Achieves up to 50x faster iteration on search ranking (used by Airbnb, Netflix).
- Always check for spillover effects between treatment and control groups.

### Heterogeneous Treatment Effects (HTE)
- Analyze whether the treatment effect differs across user segments (new vs. returning, mobile vs. desktop, geography).
- Pre-register subgroup analyses to avoid data-dredging.
- Methods: Conditional Average Treatment Effect (CATE) estimation using causal forests, S-learner, T-learner.
- Useful for personalization decisions: "Ship this change only for segments where it helps."

## Common A/B Testing Mistakes

1. **Peeking and early stopping**: Checking results daily and stopping when significant inflates false positive rates from 5% to 20-30%. Use sequential testing or commit to a fixed sample size.
2. **Too many variants**: Testing 5+ variants simultaneously requires much larger samples due to multiple comparison corrections.
3. **Wrong randomization unit**: Using page views when the correct unit is users leads to correlated observations and invalid inference.
4. **Ignoring seasonality**: A test running only on weekdays may not generalize to weekends. Run at least 1-2 full weekly cycles.
5. **Underpowered tests**: Testing a change affecting 5% of users with a 5% expected lift on a metric with high variance will never reach significance with reasonable traffic.
6. **Ignoring practical significance**: A result can be statistically significant but too small to matter. Always assess whether the effect size justifies the implementation cost.
7. **No pre-registration**: Deciding hypotheses and metrics after seeing data enables cherry-picking. Document the test plan before launching.
8. **Ignoring novelty and primacy effects**: New features may show inflated initial engagement (novelty) or suppressed engagement (resistance to change). Wait for effects to stabilize.
9. **Running concurrent experiments without interaction detection**: Overlapping experiments can interact, producing misleading results. Use experiment namespaces or check for interactions.
10. **Confusing correlation with causation in post-hoc analysis**: Subgroup findings from a single experiment are hypotheses, not conclusions. Validate with follow-up experiments.

## Quasi-Experimental Methods (When A/B Tests Are Not Feasible)

When you cannot randomize (pricing changes, policy changes, partner rollouts):
- **Difference-in-Differences (DiD)**: Compare pre/post changes between treatment and control groups. Requires parallel trends assumption.
- **Regression Discontinuity Design (RDD)**: Exploit sharp eligibility cutoffs (e.g., users above/below a threshold) to estimate causal effects.
- **Interrupted Time Series (ITS)**: Analyze metric trends before and after an intervention when no control group exists.
- **Propensity Score Matching**: Match treated users with similar untreated users based on observable characteristics.
- Always acknowledge these are weaker than true randomized experiments and flag the assumptions.

## Decision Framework

| Result | Interpretation | Action |
|---|---|---|
| Statistically significant positive on primary, guardrails stable | The change works as intended | Ship it |
| Statistically significant positive on primary, guardrail degraded | Mixed result with tradeoff | Do not ship. Rethink the approach or accept tradeoff only with explicit stakeholder sign-off |
| Statistically significant negative on primary | The change hurts | Revert, investigate why, extract learning |
| Not significant, adequate sample reached | No detectable effect at this MDE | Iterate on hypothesis. Consider: Was the MDE realistic? Was the change impactful enough? |
| Not significant, insufficient sample | Underpowered test | Run longer, increase traffic, or apply variance reduction (CUPED) |
| Significant on secondary but not primary | Interesting signal, not actionable alone | Do not ship based on secondary metrics alone. Design follow-up test targeting the secondary finding |
| HTE analysis shows segment-specific wins | Works for some users, not all | Consider targeted rollout or personalization strategy |

## Experimentation Maturity and Velocity

### Level 1 - Ad Hoc Testing
- Individual tests run occasionally. No shared infrastructure.
- Action: Standardize hypothesis templates and metric definitions.

### Level 2 - Systematic Testing
- Regular experimentation with a shared tool (GrowthBook, Statsig, Eppo, LaunchDarkly).
- Action: Build a test review process and centralized experiment log.

### Level 3 - Scaled Experimentation
- Most features launched behind feature flags. Experiment reviews before shipping.
- Action: Implement CUPED, sequential testing, and automated experiment diagnostics.

### Level 4 - Experimentation Culture
- Hundreds of experiments per quarter. Experimentation is the default, not the exception.
- Action: Build experiment portfolios, detect interactions, measure experiment velocity as a team metric.

## Output Template

---
**A/B TEST DESIGN / ANALYSIS**

**Test Name:** [Name]
**Hypothesis:** [Full hypothesis statement: By changing X, we expect Y to change by Z% because reasoning]
**Statistical Approach:** [Frequentist / Bayesian / Sequential]

**Design**
Primary metric (OEC): [Metric + definition]
Secondary metrics: [List with definitions]
Guardrail metrics: [List with acceptable degradation thresholds]
Sample unit: [User / Session / Account / Cluster]
Population: [Which users, any exclusions]
Traffic split: [Variant A / Variant B % + justification if not 50/50]
Concurrent experiments to check for interaction: [List or "None identified"]

**Sample Size Calculation**
Baseline rate: [X%]
Minimum detectable effect: [X percentage points (X% relative)]
Confidence level: [95%] | Power: [80%]
Variance reduction method: [None / CUPED / Stratification]
Required N per variant: [Calculated value]
Expected daily eligible traffic: [N users per day]
Required test duration: [N days, minimum 7]

**Pre-Launch Checklist**
- [ ] Hypothesis and metrics documented and reviewed
- [ ] Sample size calculated and achievable within traffic
- [ ] Randomization unit confirmed
- [ ] Logging and metric collection verified
- [ ] A/A validation or traffic split check planned
- [ ] Interaction with concurrent experiments assessed
- [ ] Success criteria and decision rules agreed upon in advance

**Results** (if analyzing an existing test)
| Metric | Control | Treatment | Absolute Lift | Relative Lift | p-value / P(B>A) | CI (95%) | Significant? |
|---|---|---|---|---|---|---|---|
| [Primary metric] | X% | Y% | +Z pp | +W% | 0.0X | [L, U] | Yes/No |
| [Secondary metric] | | | | | | | |
| [Guardrail metric] | | | | | | | |

**Segment Analysis** (if applicable)
| Segment | Control | Treatment | Lift | Significant? |
|---|---|---|---|---|
| [New users] | | | | |
| [Returning users] | | | | |
| [Mobile] | | | | |

**Decision**
[Ship / Ship to segment / Iterate / Stop + clear reasoning tied to pre-registered criteria]

**What We Learned**
[2-3 sentences on insights from this test, including implications for future experiments, regardless of outcome]

**Follow-Up Actions**
[Next experiment to run, features to investigate, or changes to test design]
---
