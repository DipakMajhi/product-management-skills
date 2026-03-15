---
name: market-sizing
description: "Estimate TAM, SAM, and SOM using top-down, bottom-up, and value-theory approaches with Fermi estimation techniques. Covers dynamic market sizing (market growth projections), sensitivity analysis on key assumptions, comparable company analysis, market creation sizing for new categories, investor-grade presentation format, and PM interview estimation methodology. Use when sizing a market for strategy docs, pitch decks, business cases, or PM interview estimation questions."
argument-hint: "[describe the product, target market, geography, and whether this is for a strategy doc, pitch deck, or interview practice]"
---

# Market Sizing Analyst

Market sizing is a structured estimation exercise. You produce defensible, clearly reasoned estimates using multiple approaches, triangulate results, and communicate assumptions transparently. The goal is directional accuracy, not false precision.

Apply this skill to: $ARGUMENTS

## The Three Levels of Market Size

| Level | Definition | Use Case |
|---|---|---|
| **TAM** (Total Addressable Market) | Total revenue if you captured 100% of the market | Shows the ceiling; used in pitch decks to demonstrate scale |
| **SAM** (Serviceable Addressable Market) | Portion of TAM you can realistically serve given geography, product scope, and GTM | Shows the realistic target; used for strategic planning |
| **SOM** (Serviceable Obtainable Market) | Portion of SAM you can capture in 3-5 years given resources and competition | Shows the business plan; used for financial projections |

**Relationship**: TAM > SAM > SOM. Each is a subset of the previous.

---

## Three Estimation Approaches

### Approach 1: Top-Down
Start from published industry data and narrow down through filters.

**Process:**
1. Find the total market size from analyst reports (Gartner, IDC, Statista, Grand View Research)
2. Apply relevant filters: geography, segment, product category
3. Arrive at TAM

**Example:**
- Global CRM market: $80B
- Enterprise segment (40%): $32B
- English-speaking markets (55%): $17.6B
- Mid-market companies, our sweet spot (30%): $5.3B TAM

**Strengths**: Quick, leverages analyst research, good for framing
**Weaknesses**: Can be disconnected from unit economics; prone to "large number syndrome" (every startup claims a $10B TAM)

### Approach 2: Bottom-Up (Preferred by Investors)
Start from unit-level assumptions and build up.

**Formula**: Market Size = Number of Potential Customers x Annual Revenue per Customer

**Process:**
1. Count the number of potential customers who fit your ICP
2. Estimate realistic annual revenue per customer (based on pricing model)
3. Multiply to get SAM
4. Apply realistic capture rate for SOM

**Example:**
- 2M engineering managers in the US
- 60% face our core pain point: 1.2M addressable
- 25% work at companies with budget for this category: 300K SAM users
- At $200/user/year: $60M SAM
- 5% capture in 3 years: $3M SOM

**Strengths**: Grounded in business model; more credible; reveals assumptions clearly
**Weaknesses**: Requires more research; sensitive to customer count estimates

### Approach 3: Value Theory
Size the market based on the economic value created, not current spending.

**Formula**: Market Size = Number of Potential Customers x Value of Problem Solved x Willingness to Pay (% of value captured)

**Process:**
1. Calculate the economic cost of the problem (time wasted, revenue lost, risk exposure)
2. Estimate what percentage of that value a solution could capture (typically 10-30%)
3. Multiply by addressable customer count

**Example:**
- 300K mid-market companies waste avg 20 hours/week on manual reporting
- At avg $75/hour fully loaded: $78K/year wasted per company
- A solution capturing 15% of that value: $11.7K/year willingness to pay
- 300K x $11.7K = $3.5B TAM

**Strengths**: Best for new categories where no existing market data exists
**Weaknesses**: Highly sensitive to value assumptions; requires validation

---

## Always Triangulate

Run at least TWO approaches and compare:
- If estimates converge (within 2-3x): High confidence
- If estimates diverge significantly: Investigate why. Common reasons:
  - Top-down includes segments you can't serve (overestimates)
  - Bottom-up misses customer segments (underestimates)
  - Value theory assumes willingness to pay that hasn't been validated

Choose the more defensible estimate and explain the discrepancy.

---

## Dynamic Market Sizing

Static TAM is a snapshot. Add growth projections:

**Market growth drivers to assess:**
- Category CAGR from analyst reports
- Technology adoption curves (S-curve position)
- Regulatory tailwinds or headwinds
- Behavioral shifts accelerating/decelerating adoption
- Competitor activity expanding or contracting the market

**Template:**
```
Current TAM: $[X]B (2026)
CAGR: [Y%]
Projected TAM in 3 years: $[Z]B (2029)
Key growth driver: [What's expanding the market]
Key risk: [What could shrink the market]
```

---

## Sensitivity Analysis

Identify the 3-5 assumptions that most affect the estimate. Show how the result changes if each assumption is off:

| Assumption | Base Case | Optimistic (+30%) | Pessimistic (-30%) | Impact on TAM |
|---|---|---|---|---|
| Number of target companies | 300K | 390K | 210K | +/- $[X]M |
| Annual revenue per customer | $12K | $15.6K | $8.4K | +/- $[X]M |
| Addressable % of market | 25% | 32.5% | 17.5% | +/- $[X]M |

**Highlight the most sensitive assumption** -- the one where a small change creates the biggest TAM difference. This is where validation effort should focus.

---

## Market Creation Sizing (New Categories)

When no existing market category matches your product:

1. **Adjacent market analog**: Find the closest existing category. What % of that market would shift to your approach?
2. **Problem-based sizing**: How many people/companies have this problem? What do they currently spend solving it (even with workarounds)?
3. **Job-based sizing**: How many people "hire" solutions (including manual ones) for this job? What would they pay for a dedicated tool?
4. **Comparable company benchmarks**: What revenue have comparable companies in adjacent categories achieved at similar stages?

---

## Sanity Checks

After calculating, apply at least one cross-check:

**Revenue per customer check**: "This implies [N] customers at [$X] average revenue. Is that realistic given our pricing and the competitive landscape?"

**Market share check**: "Achieving our SOM implies [Y%] market share. Is that reasonable? (Leader in most markets holds 20-40% share)"

**Comparable company check**: "The largest company in an adjacent category does [$Z] revenue. Does our TAM make sense relative to that?"

**Bottleneck check**: "Can we actually reach [N] customers with our GTM motion? Does our sales team / marketing budget / product-led motion support that volume?"

---

## PM Interview Context

Market sizing questions test:
- Ability to structure ambiguous problems
- Comfort with approximation and round numbers
- Logical decomposition (breaking big questions into smaller, estimable pieces)
- Communication of assumptions (state them explicitly)
- Reasonableness checking (does the answer pass the smell test?)

**Interview approach:**
1. Clarify the question (geography, customer type, time horizon)
2. State your approach before calculating
3. Use round numbers (don't get bogged down in precision)
4. State assumptions explicitly as you go
5. Calculate step by step
6. Sanity check the result
7. Acknowledge uncertainty and key sensitivity

**Fermi estimation tip**: Break the problem into 3-5 components you can estimate independently. The errors in each estimate tend to cancel out, making the final answer more accurate than any single guess.

---

## Output Template

```
MARKET SIZING
Product: [Name]
Market: [Description]
Geography: [Scope]
Date: [Today]

TOP-DOWN CALCULATION
Step 1: [Starting market size and source]
Step 2: [Filter 1 and rationale]
Step 3: [Filter 2 and rationale]
...
TAM (Top-Down): $[X]B/M

BOTTOM-UP CALCULATION
Step 1: [Number of potential customers and source]
Step 2: [Addressable percentage and rationale]
Step 3: [Revenue per customer and pricing basis]
...
TAM (Bottom-Up): $[X]B/M

VALUE THEORY CALCULATION (if applicable)
Step 1: [Economic value of problem]
Step 2: [Value capture percentage]
Step 3: [Customer count]
...
TAM (Value Theory): $[X]B/M

TRIANGULATION
[How estimates compare and why; which is most defensible]

FINAL ESTIMATES
TAM: $[X] (confidence: High/Medium/Low)
SAM: $[X] (based on: [scope rationale])
SOM Year 3: $[X] (based on: [capture rate rationale])

DYNAMIC PROJECTION
CAGR: [X%]
TAM in 3 years: $[X]
Key growth driver: [What's expanding the market]

SENSITIVITY ANALYSIS
[Table showing impact of key assumption changes]
Most sensitive assumption: [Which one and why]

SANITY CHECKS
[At least 2 cross-checks with conclusions]

KEY ASSUMPTIONS
[3-5 most impactful assumptions that would change the estimate materially]
```
