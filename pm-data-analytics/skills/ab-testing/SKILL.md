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
2. **Primary metric**: The one metric this test is designed to move.
3. **Secondary metrics**: Metrics to monitor for unintended effects.
4. **Guardrail metrics**: Metrics that should NOT decline.
5. **Sample unit**: What is being randomized? (User, session, device, account)
6. **Population**: Which users will be in the test? (All users? New users only? Paid users?)
7. **Traffic split**: 50/50 is standard; justify any other split.
8. **Minimum detectable effect (MDE)**: The smallest improvement that is worth deploying.
9. **Required sample size**: Calculate before starting.
10. **Test duration**: Run for at least one full weekly cycle; account for novelty effects.

## Sample Size Calculation

Formula:
Required N per variant = (16 x baseline_conversion x (1 - baseline_conversion)) / (MDE)^2

Where MDE is expressed as an absolute difference (not relative).

Example: Baseline conversion = 5%, MDE = 1 percentage point (20% relative lift)
N = (16 x 0.05 x 0.95) / (0.01)^2 = (0.76) / 0.0001 = 7,600 users per variant

Standard parameters: 95% confidence, 80% statistical power.

## Statistical Significance Interpretation

A result is statistically significant (p < 0.05) when:
- The observed difference is unlikely to be due to random variation
- You have reached the required sample size
- The test has run for the planned duration

Do NOT stop a test early because it looks positive - this is called "peeking" and inflates false positive rates.

## Decision Framework

| Result | Interpretation | Action |
|---|---|---|
| Statistically significant positive | The change works | Ship it |
| Statistically significant negative | The change hurts | Revert, investigate |
| No significant result (adequate sample) | No detectable effect | Iterate on the hypothesis |
| No significant result (insufficient sample) | Underpowered test | Run longer or increase traffic |
| Significant on primary, negative on guardrail | Mixed result | Do not ship; rethink the approach |

## Common A/B Testing Mistakes

- Testing too many variants at once (increases false positive risk)
- Stopping the test as soon as it reaches significance
- Not accounting for seasonality in test duration
- Using page views as the sample unit when users are the right unit
- Testing a change that affects only 5% of users with a 5% conversion lift - you will never reach significance

## Output Template

---
**A/B TEST DESIGN / ANALYSIS**

**Test Name:** [Name]
**Hypothesis:** [Full hypothesis statement]

**Design**
Primary metric: [Metric + definition]
Secondary metrics: [List]
Guardrail metrics: [List]
Sample unit: [User / Session / Account]
Population: [Which users]
Traffic split: [Variant A / Variant B %]

**Sample Size Calculation**
Baseline rate: [X%]
Minimum detectable effect: [X percentage points (X% relative)]
Required N per variant: [Calculated value]
Expected daily traffic: [N users per day]
Required test duration: [N days]

**Results** (if analyzing an existing test)
| Metric | Control | Treatment | Lift | p-value | Significant? |
|---|---|---|---|---|---|
| [Primary metric] | X% | Y% | +Z% | 0.0X | Yes/No |
| [Guardrail metric] | | | | | |

**Decision**
[Ship / Iterate / Stop + clear reasoning]

**What We Learned**
[1-2 sentences on the insight from this test, regardless of outcome]
---
