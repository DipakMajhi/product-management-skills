---
name: assumption-testing
description: "Map, score, and design tests for product assumptions before building. Covers assumption extraction across desirability/usability/viability/feasibility, Strategyzer Test Card and Learning Card, Riskiest Assumption Test (RAT), David Bland's Testing Business Ideas methodology, Alberto Savoia pretotyping (XYZ hypothesis, YODA vs OPD), evidence hierarchy (5 levels from opinion to controlled experiment), experiment type decision tree (12 methods ordered by cost and fidelity), sample size guidance for qualitative vs quantitative, learning velocity metrics, experiment portfolio management, common validation mistakes (confirmation bias, survivorship bias, false positives), and kill criteria design. Use when identifying riskiest assumptions, designing pretotypes or MVPs, validating solutions before engineering investment, or building an evidence-based product development practice."
argument-hint: "[describe the product idea or solution, the desired outcome it supports, what you already know vs. what you are guessing, and any constraints on testing]"
---

# Assumption Testing Framework

You help PMs avoid building the wrong thing by surfacing and testing the riskiest assumptions before investing in development. Most products fail not because of poor execution but because the underlying assumptions were wrong.

Apply this skill to: $ARGUMENTS

## The Build Trap

The build trap occurs when teams ship features based on opinion rather than evidence. The antidote is assumption testing: identifying what must be true for a solution to work, and testing the riskiest assumptions cheaply before building.

Research indicates roughly 70% of features fail to deliver expected value. Assumption testing is the discipline that prevents wasted effort.

---

## Step 1: Assumption Extraction

For any product idea or solution, extract assumptions across four categories:

### Desirability Assumptions (Do customers want this?)

- Users have the problem we think they have
- Users experience this problem frequently enough to seek a solution
- Users are willing to change their current behavior or switch from existing solutions
- The problem is painful enough that users will pay for a solution
- Our target segment is large enough to build a business around
- Users perceive our solution as addressing their problem (not a different one)

### Usability Assumptions (Can customers use this?)

- Users can discover and understand the feature without assistance
- Users can complete the key action without confusion or errors
- The solution fits into their existing workflow and tools
- The learning curve is acceptable for the target user sophistication level
- Users understand the value they are getting from the solution
- Error recovery is intuitive (users can fix mistakes without support)

### Viability Assumptions (Does this work for the business?)

- This can be built within budget and timeline constraints
- The pricing users will accept generates sufficient margin
- We can acquire customers at a sustainable CAC
- LTV:CAC ratio is at least 3:1 at projected scale
- This does not cannibalize existing revenue streams in a net-negative way
- Regulatory and compliance requirements can be met
- The solution strengthens (or at least does not weaken) our competitive position

### Feasibility Assumptions (Can we build this?)

- We have (or can acquire) the technical capability
- We can build this within the required timeline
- Key dependencies (APIs, partners, data sources) are accessible and reliable
- The solution can scale to the required user load
- We can maintain and iterate on this solution with available resources
- Data quality and availability support the solution's core logic

### Extraction from Lean Canvas

Every cell on the Lean Canvas contains testable assumptions:

| Canvas Cell | Example Assumptions |
|---|---|
| Problem | Users actually face this problem frequently |
| Customer Segments | This segment is large enough and reachable |
| Unique Value Proposition | Users perceive this as differentiated |
| Solution | This approach solves the problem better than alternatives |
| Channels | We can reach customers through these channels at acceptable cost |
| Revenue Streams | Users will pay this price at this frequency |
| Cost Structure | Unit economics work at scale |
| Key Metrics | These metrics actually indicate product health |
| Unfair Advantage | This advantage is durable and hard to replicate |

---

## Step 2: Assumption Scoring

Score each assumption on two dimensions (1-5 each):

| Dimension | 1 | 3 | 5 |
|---|---|---|---|
| Impact if wrong | Solution still works, minor adjustment | Significant rework required | Entire solution fails, total write-off |
| Certainty (Evidence) | Strong data or direct evidence | Indirect evidence or analogy | Pure guess, no supporting evidence |

**Risk Score = Impact x (6 - Certainty)**

Highest risk scores get tested first. Plot assumptions on a 2x2 matrix:

| Quadrant | Impact | Certainty | Action |
|---|---|---|---|
| Leap of Faith | High | Low | TEST IMMEDIATELY -- these determine success or failure |
| Known Risk | High | High | MONITOR -- important but currently validated |
| Unknown | Low | Low | DEFER -- test later or accept the risk |
| Safe | Low | High | IGNORE -- low risk, well understood |

### Assumption Mapping Workshop

To facilitate assumption mapping with a team:

1. Use "We believe that..." format for each assumption
2. Color-code by category (green = desirability, blue = usability, yellow = viability, red = feasibility)
3. Each participant writes assumptions individually (3 minutes)
4. Share and cluster as a group (10 minutes)
5. Vote on impact and certainty using dot stickers
6. Plot on the 2x2 matrix
7. Select top 3 leap-of-faith assumptions for immediate testing

---

## Step 3: Evidence Hierarchy

Not all evidence is equal. Know the strength of what you have:

| Level | Evidence Type | Strength | Example |
|---|---|---|---|
| 1 | Opinion and intuition | Weakest | "I think users want this" |
| 2 | Secondary research (OPD) | Low-Medium | Market reports, competitor analysis, published studies |
| 3 | Qualitative primary research | Medium | Customer interviews (5-15 users), observation |
| 4 | Quantitative behavioral data | Medium-High | Analytics, A/B tests, smoke tests measuring real behavior |
| 5 | Controlled experiments | Strongest | Randomized controlled tests, longitudinal studies |

**Key principle (Alberto Savoia)**: Your Own Data (YODA) is always more valuable than Other People's Data (OPD). OPD may be biased, outdated, or collected from a different context. Pretotyping and direct experiments generate YODA.

**Progression rule**: Start with the cheapest evidence level that provides a useful signal. Only invest in higher-fidelity evidence when lower-cost methods are inconclusive or when the stakes justify it.

---

## Step 4: Experiment Design

For each high-priority assumption, design the cheapest test that provides sufficient signal. Use the Riskiest Assumption Test (RAT) principle: test the assumption, not the full solution.

### Experiment Types (Ordered by Cost and Fidelity)

| Method | Cost | Time | Best For | Signal Strength |
|---|---|---|---|---|
| **Data mining** | Free | Hours | Checking if existing data already answers the question | Medium-High |
| **Desk research** | Free | Hours | Market size, competitive landscape, regulatory requirements | Low-Medium |
| **Customer interviews** (5-15) | Low | Days | Desirability assumptions, understanding motivations | Medium |
| **Survey** (50+ responses) | Low | Days | Quantifying demand, willingness to pay, preferences | Medium |
| **Smoke test / Fake door** | Low | Days | Measuring real demand for a feature that does not yet exist | High |
| **Landing page test** | Low | Days-Week | Conversion intent with ad spend driving traffic | High |
| **Concierge MVP** | Medium | Weeks | Delivering the solution manually to validate value and WTP | High |
| **Wizard of Oz** | Medium | Weeks | Simulating automation with humans behind the scenes | High |
| **Prototype test** | Medium | Weeks | Usability assumptions with clickable prototype and real users | High |
| **Technical spike** | High | Weeks | Feasibility requiring actual code to validate | High |
| **Pilot / Beta** | High | Months | Full solution validation with limited user group | Very High |
| **A/B test (production)** | High | Weeks-Months | Measuring causal impact of a change at scale | Very High |

### Experiment Selection Decision Tree

1. Can existing data answer this? If yes, mine the data first.
2. Is this a desirability question? Start with interviews (5-8 users), then validate with a smoke test.
3. Is this a usability question? Build a prototype and test with 5 users.
4. Is this a viability question? Test pricing with a landing page or concierge MVP.
5. Is this a feasibility question? Run a technical spike.
6. Is the risk high enough to justify investment? If not, accept the assumption and monitor.

### Sample Size Guidance

| Method | Minimum Sample | Why |
|---|---|---|
| Qualitative interviews | 5-8 per segment | Saturation reached at 12-13; 5 users reveal ~85% of usability issues (Nielsen) |
| Surveys | 50-200 responses | Needed for statistical confidence on proportions |
| Smoke tests | 100-500 exposures | Need enough traffic for meaningful click-through signal |
| A/B tests | Calculate per MDE | Use power calculation based on baseline rate and minimum detectable effect |

---

## Step 5: Strategyzer Test Card and Learning Card

### Test Card (Before the Experiment)

Document before running any experiment:

| Field | Content |
|---|---|
| **Hypothesis** | We believe [assumption] |
| **Test** | To verify, we will [describe the experiment] |
| **Metric** | We will measure [specific metric] |
| **Success criteria** | We are right if [threshold] |
| **Failure criteria** | We are wrong if [threshold] |
| **Timeline** | This test will take [duration] |
| **Cost** | [Resources, budget, people needed] |

**Critical**: Define success and failure criteria BEFORE running the test. This prevents post-hoc rationalization.

### Learning Card (After the Experiment)

Document after each experiment:

| Field | Content |
|---|---|
| **Hypothesis tested** | What we set out to validate |
| **Observation** | What actually happened, with data |
| **Learnings** | Specific insight gained |
| **Decision** | Pivot / Persevere / Stop / Run follow-up test |
| **Confidence change** | How much did our certainty increase? |

---

## Step 6: Pretotyping (Alberto Savoia)

Pretotyping answers "Should we build this?" before prototyping answers "Can we build this?"

### XYZ Hypothesis Format

"At least [X percent] of [Y target segment] will [Z measurable action]."

Example: "At least 20% of packaged sushi buyers will buy second-day sushi if it is half the price of fresh sushi."

This format forces specificity: who, how many, what behavior. No vague "users will like it."

### Pretotype Techniques

| Technique | How It Works | Example |
|---|---|---|
| **Mechanical Turk** | Replace complex automation with humans doing the work manually; users do not know | Zappos founders manually buying and shipping shoes before building e-commerce |
| **Pinocchio** | Non-functional physical or visual representation to gauge reaction | Jeff Hawkins carrying a wooden block sized like a Palm Pilot |
| **Fake Door** | Button, menu item, or link for a feature that does not exist; measure clicks | "Coming soon" feature in navigation; track click-through rate |
| **One-Night Stand** | Temporary, bare-minimum version of the experience | Pop-up shop, one-day event, manual email sequence |
| **Re-Label** | Take an existing product and repackage/reposition it | Rename an existing feature and test if new framing increases adoption |
| **Infiltrator** | Place your product idea inside an existing platform to test demand | List a product on a marketplace before building it |

### Pretotype Success Metrics

Do not rely on stated intent ("Would you use this?"). Measure actual behavior:

| Signal | Benchmark | Strength |
|---|---|---|
| Click-through on fake door | 2-5% indicates real interest | Medium |
| Email signup for waitlist | 5-10% of landing page visitors | Medium-High |
| Pre-order or deposit | Any meaningful conversion | Very High (strongest signal) |
| Time spent engaging | Above baseline for similar content | Medium |
| Repeat behavior | Users return without prompting | High |

---

## Step 7: Common Validation Mistakes

| Mistake | What Goes Wrong | Prevention |
|---|---|---|
| **Confirmation bias** | Testing to validate rather than to learn; cherry-picking positive results | Pre-commit to success/failure criteria; have a skeptic review the test design |
| **Leading questions** | Interview questions that suggest the desired answer | Use open-ended, neutral questions; have someone else review your script |
| **Survivorship bias** | Only interviewing current users (not churned or non-adopters) | Include churned users and people who evaluated but did not adopt |
| **False positives from smoke tests** | Curiosity clicks mistaken for purchase intent | Measure depth of engagement, not just clicks; require multi-step commitment |
| **Stated vs. revealed preference** | People say they would use it but behavior says otherwise | Always measure behavior over stated intent |
| **Testing safe assumptions** | Validating what you already know instead of what is risky | Use the assumption scoring matrix; test high-impact, low-certainty first |
| **Insufficient sample** | Drawing conclusions from 2-3 data points | Follow sample size guidance per method |
| **Frankenstein MVP** | Assembling bits from various sources without coherent experience | Ensure the test artifact delivers a coherent value proposition, even if minimal |
| **Moving goalposts** | Changing success criteria after seeing results | Write Test Cards before experiments; do not change criteria post-hoc |

---

## Step 8: Learning Velocity and Experiment Portfolio

### Learning Velocity

Learning velocity measures how fast the team converts uncertainty into validated knowledge.

| Metric | What It Measures | Healthy Range |
|---|---|---|
| Assumptions tested per sprint | Rate of learning | 1-2 per sprint |
| Learning-to-experiment ratio | Quality of experiments | 1:1 (each experiment produces a usable learning) |
| Time from hypothesis to decision | Cycle time | Days to weeks, not months |
| Percentage of solutions discarded based on evidence | Willingness to learn vs. confirm | 30-50% (teams that never discard are not testing risky assumptions) |

### Portfolio Approach to Experiments

Run a portfolio of experiments simultaneously across different risk levels:

| Risk Level | Experiment Investment | Expected Outcome |
|---|---|---|
| High risk, high reward | 20% of experiment budget | Some will fail; the ones that succeed create breakthrough value |
| Medium risk | 50% of experiment budget | Most will produce useful learning |
| Low risk (optimization) | 30% of experiment budget | Incremental improvements on validated features |

**Key insight**: Learning velocity (converting R&D into validated knowledge) matters more than experiment velocity (number of experiments run). A team running 10 inconclusive experiments per sprint is less effective than a team running 2 decisive ones.

---

## Step 9: Decision Framework

After running experiments, make an explicit decision:

| Evidence Pattern | Decision | Next Step |
|---|---|---|
| Core desirability validated, feasibility confirmed | **Build** | Move to full product development |
| Desirability validated but usability concerns | **Iterate on design** | Run prototype tests before building |
| Desirability strong, viability uncertain | **Test pricing** | Conduct willingness-to-pay research |
| Core desirability assumption invalidated | **Pivot** | Return to opportunity discovery; reframe the problem |
| Multiple assumptions invalidated | **Kill** | Stop investing; document learnings for future reference |
| Mixed signals, insufficient data | **Run follow-up test** | Design higher-fidelity experiment targeting the ambiguous assumption |

### Kill Criteria

Define kill criteria before starting experiments:

"We will abandon this idea if ANY of the following are true after testing:
- Fewer than [X%] of target users express the problem
- Willingness to pay is below [$Y]
- Technical feasibility requires more than [Z months] of engineering
- [Specific competitive barrier] cannot be overcome"

### Build Trigger

"We will commit to full development when ALL of the following are validated:
- Desirability: [Specific evidence threshold]
- Usability: [Specific evidence threshold]
- Viability: [Specific evidence threshold]
- Feasibility: [Specific evidence threshold]"

---

## Step 10: Integration with Continuous Discovery

Assumption testing is most effective embedded in a continuous discovery cadence:

1. **Weekly customer interviews** surface new assumptions and validate existing ones
2. **Opportunity Solution Trees** connect assumptions to specific opportunities and solutions
3. **Assumption backlogs** are maintained and groomed alongside the product backlog
4. **Test velocity** becomes a team metric: how many assumptions are we validating per sprint?
5. **Learning logs** accumulate institutional knowledge about what works and what does not

---

## Output Template

```
ASSUMPTION MAP
Solution/Idea: [Description]
Desired Outcome: [What business goal this supports]
Date: [When this analysis was created]

ASSUMPTION INVENTORY

| ID | Assumption | Category | Impact (1-5) | Certainty (1-5) | Risk Score | Priority |
|----|-----------|----------|-------------|-----------------|------------|----------|
| A1 | [Text]    | [D/U/V/F]| X           | X               | X          | Test Now / Monitor / Defer / Ignore |
| A2 | ...       |          |             |                 |            |          |

EVIDENCE INVENTORY
| Assumption | Current Evidence | Evidence Level (1-5) | Gaps |
|-----------|-----------------|---------------------|------|
| A1        | [What we know]  | [Level]             | [What we need] |

LEAP-OF-FAITH ASSUMPTIONS (Top 3 to Test)

A[N]: [Assumption]
- Category: [Desirability / Usability / Viability / Feasibility]
- Why it is risky: [Impact explanation + lack of evidence]
- Cheapest valid test: [Test type + detailed description]
- Test Card:
  - Hypothesis: We believe [statement]
  - Test: To verify, we will [method]
  - Metric: We will measure [specific metric]
  - Success criteria: [Threshold that means proceed]
  - Failure criteria: [Threshold that means pivot]
  - Timeline: [Duration]
  - Cost: [Resources needed]
  - Sample size: [N and rationale]

RECOMMENDED TESTING SEQUENCE
[Ordered list: which assumptions to test first and why, including dependencies]

KILL CRITERIA
[What combined evidence pattern would cause us to abandon this idea entirely]

BUILD TRIGGER
[What combined evidence across D/U/V/F would give confidence to commit to full development]

LEARNING LOG (updated after each experiment)
| Date | Assumption | Method | Result | Confidence Change | Decision |
|------|-----------|--------|--------|-------------------|----------|
| [Date] | [A1] | [Method] | [Finding] | [+/-] | [Proceed / Pivot / Kill] |
```
