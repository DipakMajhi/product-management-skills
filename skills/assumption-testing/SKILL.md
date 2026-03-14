---
name: assumption-testing
description: "Map, score, and design tests for product assumptions before building. Use this skill when someone needs to identify the riskiest assumptions in a product idea, design a pretotype or MVP experiment, or validate a solution before committing engineering resources."
---

# Assumption Testing Framework

You help PMs avoid building the wrong thing by surfacing and testing the riskiest assumptions before investing in development.

## The Build Trap

Apply this skill to: $ARGUMENTS


The build trap occurs when teams ship features based on opinion rather than evidence. The antidote is assumption testing: identifying what must be true for a solution to work, and testing the riskiest assumptions cheaply before building.

Most products fail not because of poor execution but because the underlying assumptions were wrong. McKinsey research indicates roughly 70% of features fail to deliver expected value. Assumption testing is the discipline that prevents wasted effort.

## Step 1: Assumption Extraction

For any product idea or solution, extract assumptions across four categories:

**Desirability Assumptions** (Do customers want this?)
- Users have the problem we think they have
- Users experience this problem frequently enough to seek a solution
- Users are willing to change their current behavior or switch from their existing solution
- The problem is painful enough that users will pay for a solution
- Our target segment is large enough to build a business around

**Usability Assumptions** (Can customers use this?)
- Users can discover and understand the feature without assistance
- Users can complete the key action without confusion or errors
- The solution fits into their existing workflow and tools
- The learning curve is acceptable for the target user sophistication level
- Users understand the value they are getting from the solution

**Viability Assumptions** (Does this work for the business?)
- This can be built within budget and timeline constraints
- The pricing users will accept generates sufficient margin
- We can acquire customers at a sustainable CAC
- LTV:CAC ratio is at least 3:1 at projected scale
- This does not cannibalize existing revenue streams in a net-negative way
- Regulatory and compliance requirements can be met

**Feasibility Assumptions** (Can we build this?)
- We have (or can acquire) the technical capability
- We can build this within the required timeline
- Key dependencies (APIs, partners, data sources) are accessible and reliable
- The solution can scale to the required user load
- We can maintain and iterate on this solution with available resources

## Step 2: Assumption Scoring

Score each assumption on two dimensions (1-5 each):

| Dimension | 1 | 3 | 5 |
|---|---|---|---|
| Impact if wrong | Solution still works, minor adjustment needed | Significant rework required | Entire solution fails, total write-off |
| Certainty (Evidence) | Strong data or direct evidence | Indirect evidence or analogy | Pure guess, no supporting evidence |

Risk Score = Impact x (6 - Certainty)

Highest risk scores get tested first. Plot assumptions on a 2x2 matrix:

- High Impact, Low Certainty: TEST IMMEDIATELY (these are leap-of-faith assumptions)
- High Impact, High Certainty: MONITOR (important but validated)
- Low Impact, Low Certainty: DEFER (test later or accept the risk)
- Low Impact, High Certainty: IGNORE (low risk, well understood)

## Step 3: Experiment Design

For each high-priority assumption, design the cheapest test that provides sufficient signal. Use the Riskiest Assumption Test (RAT) principle: test the assumption, not the full solution.

### Experiment Types (Ordered by Cost and Fidelity)

| Method | Cost | Time | Best For | Signal Strength |
|---|---|---|---|---|
| **Data mining** | Free | Hours | Checking if existing data already answers the question | Medium-High |
| **Desk research** | Free | Hours | Validating market size, competitive landscape, regulatory requirements | Low-Medium |
| **Customer interviews** (5-10 users) | Low | Days | Desirability assumptions, understanding motivations and behaviors | Medium |
| **Survey** (50+ responses) | Low | Days | Quantifying demand, willingness to pay, feature preferences | Medium |
| **Smoke test / Fake door** | Low | Days | Measuring real demand by showing a feature that does not exist and tracking clicks or signups | High |
| **Landing page test** | Low | Days-Week | Measuring conversion intent with ad spend driving traffic to a value proposition page | High |
| **Wizard of Oz** | Medium | Weeks | Simulating the product experience manually behind the scenes while users interact normally | High |
| **Concierge MVP** | Medium | Weeks | Delivering the solution manually to 1-5 customers to validate value and willingness to pay | High |
| **Prototype test** | Medium | Weeks | Usability assumptions with a clickable prototype and real user sessions | High |
| **Technical spike** | High | Weeks | Feasibility assumptions requiring actual code to validate performance or integration | High |
| **Beta / Pilot** | High | Months | Full solution validation with a limited user group before broad rollout | Very High |

### Strategyzer Test Card Method

For each experiment, document:
1. **Hypothesis**: We believe [assumption].
2. **Test**: To verify, we will [describe the experiment].
3. **Metric**: We will measure [specific metric].
4. **Criteria**: We are right if [success threshold]. We are wrong if [failure threshold].
5. **Timeline**: This test will take [duration] and cost [resources].

### Strategyzer Learning Card Method

After each experiment, document:
1. **Hypothesis tested**: [What we set out to validate]
2. **Observation**: We observed [what actually happened, with data].
3. **Learnings**: From this we learned [specific insight].
4. **Decision**: Therefore we will [pivot / persevere / stop / run follow-up test].

## Step 4: Pretotyping (Before Prototyping)

Pretotyping answers "Should we build this?" before prototyping answers "Can we build this?" (Alberto Savoia methodology)

### Pretotype Techniques
- **The Mechanical Turk**: Replace complex back-end automation with humans doing the work manually. Users do not know the difference.
- **The Pinocchio**: Create a non-functional physical or visual representation and gauge user reaction and intent.
- **The Fake Door**: Add a button, menu item, or link for a feature that does not exist. Measure how many users click it.
- **The One-Night Stand**: Set up a temporary, bare-minimum version of the experience (pop-up shop, one-day event, manual email sequence) and measure real behavior.
- **The Re-Label**: Take an existing product or feature and re-label or repackage it to test whether the new positioning resonates.

### Pretotyping Success Metrics
- Do not rely on stated intent ("Would you use this?"). Measure actual behavior.
- Click-through rates on fake doors (benchmark: 2-5% indicates real interest)
- Email signup rates for waitlists (benchmark: 5-10% of landing page visitors)
- Willingness to prepay or put down a deposit (strongest signal of demand)

## Step 5: Decision Framework

After running experiments, make an explicit decision:

| Evidence Pattern | Decision | Next Step |
|---|---|---|
| Core desirability assumption validated, feasibility confirmed | **Build** | Move to full product development |
| Desirability validated but usability concerns surfaced | **Iterate on design** | Run prototype tests before building |
| Desirability strong, viability uncertain | **Test pricing** | Conduct willingness-to-pay research or pricing experiment |
| Core desirability assumption invalidated | **Pivot** | Return to opportunity discovery. Reframe the problem. |
| Multiple assumptions invalidated | **Kill** | Stop investing. Document learnings for future reference. |
| Mixed signals, insufficient data | **Run follow-up test** | Design a higher-fidelity experiment targeting the ambiguous assumption |

## Integration with Continuous Discovery

Assumption testing is most effective when embedded in a continuous discovery cadence:

1. **Weekly customer interviews** surface new assumptions and validate existing ones.
2. **Opportunity Solution Trees** (Teresa Torres) connect assumptions to specific opportunities and solutions.
3. **Assumption backlogs** are maintained and groomed alongside the product backlog.
4. **Test velocity** becomes a team metric: how many assumptions are we validating per sprint?

## Output Template

---
**ASSUMPTION MAP**
**Solution/Idea:** [Description]
**Desired Outcome:** [What business goal this supports]
**Date:** [When this analysis was created]

**Assumption Inventory**

| ID | Assumption | Category | Impact (1-5) | Certainty (1-5) | Risk Score | Priority |
|---|---|---|---|---|---|---|
| A1 | [Assumption text] | Desirability | X | X | X | Test Now / Monitor / Defer / Ignore |
| A2 | ... | | | | | |

**Leap-of-Faith Assumptions** (Top 3 to Test)

**A[N]: [Assumption]**
- Category: [Desirability / Usability / Viability / Feasibility]
- Why it is risky: [Explanation of impact and lack of evidence]
- Cheapest valid test: [Test type + detailed description]
- Test Card:
  - Hypothesis: We believe [statement]
  - Test: To verify, we will [method]
  - Metric: We will measure [specific metric]
  - Success criteria: [Threshold that means proceed]
  - Failure criteria: [Threshold that means pivot]
  - Timeline: [Duration]
  - Cost: [Resources needed]

**Recommended Testing Sequence**
[Ordered list: which assumptions to test in what order and why, considering dependencies between assumptions]

**Kill Criteria**
[What combined evidence pattern would cause us to abandon this idea entirely]

**"Build" Trigger**
[What combined evidence across desirability, usability, viability, and feasibility would give us confidence to commit to full development]

**Learning Log** (updated after each experiment)
| Date | Assumption Tested | Method | Result | Decision |
|---|---|---|---|---|
| [Date] | [A1] | [Interview] | [Finding] | [Proceed / Pivot / Kill] |
---
