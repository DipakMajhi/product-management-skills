---
name: funnel-optimization
description: "Diagnose and optimize product funnels including acquisition, onboarding, upgrade, and checkout flows. Use this skill when someone needs to improve conversion rates, identify where users drop off, design funnel experiments, or answer "how would you improve this funnel?" in a PM interview."
---

# Funnel Optimization Framework

A funnel is a sequence of steps where users must complete each step to reach the goal. Every step has a conversion rate; improving any step improves the overall funnel.

## Funnel Optimization Process

Apply this skill to: $ARGUMENTS


### Step 1: Map the Funnel
Write out every step a user takes from entry to goal. Be specific - "signup" is not a step; "enter email, click verify link, set password, complete profile" are four steps.

### Step 2: Measure Each Step
For each step, calculate:
- Completion rate: % of users who enter this step and complete it
- Drop-off rate: % who abandon at this step
- Time at step: How long users spend before dropping off

### Step 3: Prioritize by Impact

Use the bottleneck method:
For each step, calculate: "If I improved this step by 20%, what would the overall funnel conversion become?"
The step with the highest impact is the bottleneck - fix it first.

### Step 4: Diagnose Drop-off

For each high-drop-off step, investigate:
- **Confusion**: Do users not understand what is being asked?
- **Friction**: Is the step unnecessarily difficult?
- **Motivation loss**: Have users lost confidence in the value by this point?
- **Distraction**: Are users navigating away rather than dropping out?
- **Technical failure**: Is there a bug or error causing drop-off?

Diagnostic methods:
- Session recordings (watch actual users navigating the step)
- Heatmaps (where are users clicking that they should not be?)
- Form analytics (which field causes the most abandonment?)
- Exit surveys (5-second pop-up: "What stopped you from completing X?")

### Step 5: Design Experiments

For each diagnosed problem:
- Confusion: Rewrite copy, add tooltip, simplify the ask
- Friction: Remove fields, pre-fill data, add social proof
- Motivation loss: Reorder steps to deliver value before asking for effort
- Technical failure: Fix the bug first, then optimize

## Funnel Math Reference

Overall funnel conversion = Step 1 CR x Step 2 CR x Step 3 CR x ... Step N CR

Example: 60% x 80% x 70% x 50% = 16.8% overall conversion

Improving the worst step (50%) to 65%: 60% x 80% x 70% x 65% = 21.8% (a 30% improvement in overall conversion)

## Output Template

---
**FUNNEL ANALYSIS: [Funnel Name]**
**Entry Point:** [Where users enter]
**Goal:** [What successful completion looks like]

**Funnel Map and Metrics**
| Step | Description | Entry N | Completion % | Drop-off % | Time at Step |
|---|---|---|---|---|---|
| 1 | [Step] | N | X% | X% | [Avg time] |
| 2 | | | | | |

**Overall Funnel Conversion:** [X%]
**Benchmark:** [Y% - state source]

**Bottleneck Analysis**
Primary bottleneck: Step [N] - [Name] (X% drop-off)
Impact of fixing: Overall conversion would improve from X% to ~Y% (+Z pp)

**Diagnosis: Why Users Drop at Step [N]**
[Confusion / Friction / Motivation / Technical - with evidence]

**Experiment Roadmap**
| Experiment | Hypothesis | Primary Metric | Success Threshold | Effort |
|---|---|---|---|---|
| [Experiment 1] | "By [change], [metric] will improve by [X%] because [reason]" | [Metric] | [Target] | H/M/L |

**Quick Wins**
[Any changes that can be made without A/B testing and that have high confidence of improving conversion]
---
