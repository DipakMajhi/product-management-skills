---
name: product-iteration
description: "Design structured product iteration processes for existing features using Build-Measure-Learn (Lean Startup), PDCA/Deming Cycle, OODA Loop, feature audit methodology, impact mapping (Gojko Adzic), and post-launch monitoring playbooks. Covers the PM interview 'how would you improve X' framework, data-informed vs data-driven iteration, iteration cycle design (monitoring, diagnosis, quick wins, depth iteration), feature audit 2x2 (adoption vs frequency), iteration anti-patterns (vanity metrics, local optimization, premature optimization, analysis paralysis, bikeshedding), success metric definition, and multi-cycle iteration planning. Use when improving existing features, building iteration plans from data and feedback, running post-launch improvement cycles, or answering PM interview questions about product improvement."
argument-hint: "[describe the feature or product area, its current state (usage data, feedback), what 'improve' means (metric, user segment, experience), and any constraints]"
---

# Product Iteration Framework

Iteration is how products get from "launched" to "great." Most launched features need 2-3 iteration cycles before they work well. A structured iteration process turns feedback into improvements systematically rather than reactively.

Apply this skill to: $ARGUMENTS

## Core Iteration Models

### Model 1: Build-Measure-Learn (Lean Startup)

| Phase | Activity | Key Question |
|---|---|---|
| **Build** | Create the minimum change needed to test a hypothesis | What is the smallest thing we can ship to learn? |
| **Measure** | Gather data with actionable metrics (not vanity metrics) | Did the change produce the expected improvement? |
| **Learn** | Analyze results and decide: persevere, pivot, or stop | What did we learn that changes our next move? |

**Critical insight**: The loop runs counter-clockwise in planning. Start with what you want to learn, then figure out what to measure, then determine what to build.

### Model 2: PDCA / Deming Cycle

| Phase | Activity | Product Application |
|---|---|---|
| **Plan** | Identify the problem and hypothesize a solution | Define what metric to improve, how, and why |
| **Do** | Test the change at small scale | Ship to a beta group or feature flag |
| **Check/Study** | Review results against expectations | Compare actual vs. predicted impact |
| **Act** | Standardize what worked; adjust what did not | Roll out to all users or iterate further |

**Key difference from Build-Measure-Learn**: PDCA emphasizes the "Study" phase -- understanding WHY something worked or did not, not just whether it did. This prevents false positives and cargo-cult copying.

### Model 3: OODA Loop

| Phase | Activity | Product Application |
|---|---|---|
| **Observe** | Gather quantitative data, qualitative feedback, competitive signals | Monitor dashboards, read support tickets, watch session recordings |
| **Orient** | Update mental models based on observations | Challenge existing beliefs about why users behave this way |
| **Decide** | Choose the highest-leverage intervention | Prioritize using impact/effort/confidence |
| **Act** | Ship the change and begin observing again | Deploy and return to Observe |

**When to use OODA**: Fast-moving competitive situations where speed of iteration matters more than depth of analysis.

---

## The "How Would You Improve X" Interview Framework

Used in PM interviews when asked "How would you improve [existing product]?"

### Step 1: Clarify the Goal (30 seconds)
- What does "improve" mean? (Engagement, revenue, retention, satisfaction, new users)
- Improve for whom? (All users, a specific segment, new vs. existing)
- What constraints exist? (Timeline, resources, technical limitations)
- What is the current state? (Ask about metrics if not provided)

### Step 2: Define User Segments (1 minute)
- Who are the different types of users?
- What are their distinct needs and behaviors?
- Which segment should we focus on? (Largest, most strategic, most underserved)

### Step 3: Identify Pain Points (1-2 minutes)
For the target segment, surface their biggest frustrations:
- What causes confusion or friction?
- What takes too long?
- What are they trying to do that the product does not support?
- What causes them to leave or churn?

### Step 4: Prioritize Pain Points (30 seconds)
Select based on: most common, most severe, most aligned with the business goal.

### Step 5: Ideate Solutions (2 minutes)
For the top pain point, generate 3-5 solutions spanning different investment levels:

| Type | Description | Example |
|---|---|---|
| Quick fix | Small change, high confidence | Improve error message copy |
| Medium investment | Feature enhancement, moderate confidence | Redesign onboarding flow |
| Big bet | Major new capability, lower confidence | Build a new product surface |

### Step 6: Prioritize and Recommend (1 minute)
Select one solution. Explain why using impact, confidence, and effort. Describe how you would test it and what success looks like.

### Step 7: Define Success Metrics (30 seconds)
- Primary metric: The one number that tells you the improvement worked
- Guardrail metric: What should NOT get worse as a result
- Leading indicator: Early signal (before the primary metric moves)

---

## Feature Audit Methodology

Map existing features on two axes to identify iteration priorities:

| Axis | Measure | Source |
|---|---|---|
| Adoption | Percentage of users who use this feature at least once | Product analytics |
| Frequency | How often adopters use the feature | Product analytics |

### Feature Audit 2x2

| Quadrant | Adoption | Frequency | Diagnosis | Action |
|---|---|---|---|---|
| **Power features** | High | High | Core value drivers | Protect and enhance; do not break these |
| **Underperforming** | High | Low | Users try it but do not return | Improve the experience; investigate why usage drops |
| **Niche** | Low | High | Small passionate audience | Increase awareness; evaluate if the audience can grow |
| **Zombie** | Low | Low | Nobody uses it meaningfully | Consider removing; reallocate resources |

### Feature Audit Process

1. Pull adoption and frequency data for all features
2. Plot on the 2x2 matrix
3. Investigate underperforming and zombie features: why are they failing?
4. For underperforming features: is the problem awareness, onboarding, or value delivery?
5. For zombie features: interview the small number of users -- are they using it for something you did not expect?
6. Make explicit keep/kill/improve decisions

---

## Post-Launch Iteration Cycle

### Phase 1: Monitor (Week 1-2 Post-Launch)

| Signal | What to Watch | Red Flag |
|---|---|---|
| Discovery | Are users finding the feature? | Less than 30% of target segment has seen it |
| Activation | Are users completing the core action? | Activation rate below 20% |
| Errors | Are there bugs or error spikes? | Error rate above 1% of sessions |
| Support volume | Are users confused? | Spike in related support tickets |
| Qualitative | What does early feedback say? | Consistent negative themes |

### Phase 2: Diagnose (Week 3-4)

Compare actual usage to predicted usage:

| Scenario | Likely Cause | Investigation |
|---|---|---|
| Usage below expectations | Awareness problem or activation problem | Check funnel: are users seeing it but not engaging? Or not seeing it at all? |
| Usage at expectations but satisfaction low | Value delivery problem | Interview users: does it do what they expected? |
| Usage above expectations | Unmet need validated | Double down: what adjacent needs can you address? |
| Usage concentrated in unexpected segment | Positioning or feature fit surprise | Interview those users: why do they love it? |

### Phase 3: Quick Wins (Month 2)

Take the top 2-3 learnings from monitoring data and feedback:
- Fix confusion points (copy, layout, onboarding)
- Remove unnecessary friction (extra steps, required fields)
- Address the single biggest complaint
- Ship and measure within 1-2 sprints

### Phase 4: Depth Iteration (Month 3+)

- Build deeper capabilities for power users who adopted the core
- Address pain points causing churn from the feature
- Explore the most requested enhancements
- Run A/B tests on significant changes before full rollout

### Post-Launch Monitoring Dashboard

Track these metrics from day one:

| Metric | Cadence | Healthy Range |
|---|---|---|
| Feature discovery rate | Daily | 50%+ of target segment within 2 weeks |
| Activation rate | Daily | 20-40%+ depending on category |
| DAU/MAU ratio | Weekly | 20%+ indicates healthy engagement |
| Retention (D7, D30) | Weekly | Improving or stable |
| NPS or CSAT for the feature | Bi-weekly | NPS 30+ or CSAT 4.0+ |
| Support ticket volume (related) | Daily | Decreasing trend |

---

## Impact Mapping (Gojko Adzic)

Impact mapping connects iteration work to business objectives:

```
Goal (business objective)
    |
    Actors (who can help or hinder achieving the goal)
        |
        Impacts (what behavior changes would help or hinder)
            |
            Deliverables (what we can build to create those impacts)
```

### Application to Iteration

1. Start with the business goal the feature is supposed to serve
2. Identify which actors (user segments, internal teams, partners) affect the goal
3. Define what behavior changes in those actors would move the goal
4. Map your iteration backlog to specific behavior changes
5. If a backlog item does not connect to a behavior change that connects to the goal, question its priority

---

## Data-Informed vs. Data-Driven Iteration

| Approach | How It Works | Strengths | Weaknesses |
|---|---|---|---|
| **Data-driven** | Decisions based solely on data; A/B testing is fundamental | Defensible; reduces bias; good for optimization | Can limit innovation; misses qualitative nuance; optimizes locally |
| **Data-informed** | Data is one input alongside user research, intuition, and strategy | Allows nuance and innovation; considers context | Harder to justify; requires strong product judgment |

**Best practice**: Establish a data-driven foundation (measure everything, run experiments, kill what does not work), then layer data-informed judgment on top (use data to inform, not dictate, strategic bets).

### When to Use Each

| Situation | Approach |
|---|---|
| Optimizing an existing flow (checkout, onboarding) | Data-driven: A/B test variations |
| Exploring a new product direction | Data-informed: qualitative research + small experiments |
| Feature performing unexpectedly | Data-driven first (diagnose with data), then data-informed (understand why with research) |
| Competitive response needed quickly | Data-informed: make the best judgment call with available evidence |

---

## Iteration Anti-Patterns

| Anti-Pattern | What It Looks Like | Why It Fails | Fix |
|---|---|---|---|
| **Vanity metrics** | Tracking downloads, pageviews, or sign-ups without engagement | Numbers look good but do not reflect user value | Use actionable metrics: retention, activation, NPS |
| **Local optimization** | Improving a feature in isolation without considering the whole experience | Gains in one area cause losses in another | Always set guardrail metrics alongside primary metrics |
| **Premature optimization** | Optimizing performance or UX before validating the feature delivers value | Polishing something nobody wants | Validate value first, then optimize the experience |
| **Analysis paralysis** | Over-analyzing without taking action | Nothing ships; learning stalls | Timebox analysis to 1 sprint; ship the best hypothesis |
| **Bikeshedding** | Debating trivial details (button color) while ignoring strategic issues | Delays meaningful work | Use effort/impact matrix; defer low-impact decisions |
| **Iteration without measurement** | Shipping changes without measuring impact | No way to know if improvements actually improved anything | Define success metrics before every iteration cycle |
| **Feature creep** | Adding features in response to every request without pruning | Product becomes bloated and confusing | Use feature audit; kill underperforming features |
| **Ignoring qualitative data** | Only looking at numbers, never talking to users | Misses the "why" behind the "what" | Pair every quantitative diagnosis with 5 user conversations |

---

## Multi-Cycle Iteration Planning

### Iteration Backlog Structure

Organize iteration work into cycles with increasing investment:

| Cycle | Timing | Focus | Investment | Evidence Required |
|---|---|---|---|---|
| Cycle 0 | Pre-launch | Instrument analytics, set baselines | Minimal | None (preparation) |
| Cycle 1 | Week 2-4 | Quick wins from monitoring data | Low (1-2 sprints) | Usage data + qualitative themes |
| Cycle 2 | Month 2-3 | Medium investments from diagnosed gaps | Medium (2-4 sprints) | Diagnosed root causes + user interviews |
| Cycle 3 | Month 4+ | Depth improvements for power users | High (quarter initiative) | Validated hypotheses from Cycle 1-2 |

### Cycle Transition Criteria

Move to the next cycle only when:
- Current cycle changes have been shipped and measured
- Measurement confirms the expected direction (even if magnitude differs)
- New research questions have been identified
- The team has enough signal to justify increased investment

---

## Output Template

```
PRODUCT ITERATION PLAN
Feature / Product Area: [Name]
Launch Date: [Date]
Current Status: [Key metrics since launch]
Date: [Today]

ITERATION GOAL
Business objective: [What the feature should achieve]
Success metric: [Primary metric and target]
Guardrail metric: [What should not get worse]
Current baseline: [Where the metric stands today]

USER FEEDBACK SUMMARY
Source 1 ([Support tickets / NPS / Interviews]): [Key themes]
Source 2 ([Analytics / Session recordings]): [Key themes]
Source 3 ([Competitive feedback]): [Key themes]

FEATURE AUDIT
| Feature/Component | Adoption | Frequency | Quadrant | Action |
|-------------------|----------|-----------|----------|--------|
| [Component]       | [%]      | [Rate]    | [Type]   | [Keep/Kill/Improve] |

PAIN POINT PRIORITIZATION
| Pain Point | Frequency | Severity | Business Impact | Root Cause | Priority |
|-----------|-----------|----------|----------------|------------|----------|
| [Pain]    | H/M/L     | H/M/L    | [Impact]       | [Cause]    | 1/2/3    |

ITERATION BACKLOG

Cycle 1 (Quick wins -- Week 2-4):
| Change | Expected Impact | Evidence Basis | Effort | Metric to Track |
|--------|----------------|---------------|--------|-----------------|
| [Change] | [Impact] | [Evidence] | [S/M/L] | [Metric] |

Cycle 2 (Medium investments -- Month 2-3):
| Change | Expected Impact | Evidence Basis | Effort | Metric to Track |
|--------|----------------|---------------|--------|-----------------|
| [Change] | [Impact] | [Evidence] | [S/M/L] | [Metric] |

Cycle 3 (Depth improvements -- Month 4+):
| Change | Expected Impact | Evidence Basis | Effort | Metric to Track |
|--------|----------------|---------------|--------|-----------------|
| [Change] | [Impact] | [Evidence] | [S/M/L] | [Metric] |

SUCCESS METRICS
| Metric | Baseline | After Cycle 1 | After Cycle 2 | After Cycle 3 |
|--------|----------|--------------|--------------|--------------|
| [Primary] | [X] | [Target] | [Target] | [Target] |
| [Guardrail] | [X] | [Floor] | [Floor] | [Floor] |

IMPACT MAP
Goal: [Business objective]
  Actor: [User segment]
    Impact: [Behavior change]
      Deliverable: [Iteration item]

NEXT RESEARCH QUESTION
[The one thing we most need to learn to inform the next cycle]

KILL CRITERIA
[Under what conditions would we stop iterating and deprecate this feature]
```
