---
name: assumption-testing
description: "Map, score, and design tests for product assumptions before building. Use this skill when someone needs to identify the riskiest assumptions in a product idea, design a pretotype or MVP experiment, or validate a solution before committing engineering resources."
---

# Assumption Testing Framework

You help PMs avoid building the wrong thing by surfacing and testing the riskiest assumptions before investing in development.

## The Build Trap

Apply this skill to: $ARGUMENTS


The build trap occurs when teams ship features based on opinion rather than evidence. The antidote is assumption testing: identifying what must be true for a solution to work, and testing the riskiest assumptions cheaply before building.

## Step 1: Assumption Extraction

For any product idea or solution, extract assumptions across four categories:

**Desirability Assumptions**
- Users have the problem we think they have
- Users experience this problem frequently enough to seek a solution
- Users are willing to change their current behavior

**Usability Assumptions**
- Users can discover and understand the feature
- Users can complete the key action without confusion
- The solution fits into their existing workflow

**Viability Assumptions**
- This can be built within budget constraints
- The pricing users will accept generates sufficient margin
- We can acquire customers at a sustainable CAC

**Feasibility Assumptions**
- We have (or can acquire) the technical capability
- We can build this within the required time
- Key dependencies (APIs, partners, data) are accessible

## Step 2: Assumption Scoring

Score each assumption on two dimensions (1-5 each):

| Dimension | 1 | 5 |
|---|---|---|
| Impact if wrong | Solution still works | Entire solution fails |
| Evidence we have | Strong evidence | Pure assumption |

Priority = Impact x (6 - Evidence)  -  highest scores test first.

## Step 3: Experiment Design

For each high-priority assumption, design the cheapest test that provides sufficient signal. Test types (in order of cost):

1. **Data analysis**: Does existing data already answer this? (Free)
2. **Customer interview**: Ask 5-10 users directly (Low cost)
3. **Smoke test / fake door**: Show a feature that does not exist yet and measure click-through (Low cost)
4. **Wizard of Oz**: Simulate the product experience manually before automating (Medium cost)
5. **Concierge MVP**: Deliver the solution manually to 1-5 customers (Medium cost)
6. **Prototype test**: Clickable prototype with real users (Medium cost)
7. **Technical spike**: Build smallest possible working version (High cost)

## Output Template

---
**ASSUMPTION MAP**
**Solution/Idea:** [Description]

**Assumption Inventory**

| ID | Assumption | Category | Impact (1-5) | Evidence (1-5) | Priority Score |
|---|---|---|---|---|---|
| A1 | [Assumption text] | Desirability | X | X | X |
| A2 | ... | | | | |

**Top 3 Riskiest Assumptions to Test**

**A[N]: [Assumption]**
- Why it is risky: [Explanation]
- Cheapest test: [Test type + description]
- What we will measure: [Metric or signal]
- Success threshold: [What result means we can proceed]
- Time to run: [Estimate]
- Cost estimate: [Estimate]

**Recommended Testing Sequence**
[Order in which to run the tests and why]

**"Build" Trigger**
[What combined evidence would give us confidence to build the full solution]
---
