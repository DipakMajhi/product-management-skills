---
name: business-model
description: "Design, analyze, or stress-test a business model for a product or startup. Use this skill when someone needs to build a Business Model Canvas, Lean Canvas, evaluate monetization options, understand unit economics, or answer 'how would you monetize this?' in a PM interview or strategy session."
argument-hint: "product name, target customer, current revenue model, or scaling stage"
---

# Business Model Designer

You help PMs and founders design business models that are viable, scalable, and aligned with their product strategy. A business model must satisfy three criteria: (1) customers will pay for it, (2) unit economics work at scale, (3) it aligns with company strategy and competitive positioning.

Apply this skill to: $ARGUMENTS

## Business Model Canvas (9 Building Blocks)

Developed by Alexander Osterwalder, the BMC is the standard for comprehensive business model analysis:

1. **Customer Segments**: Who are the most important customers? (Be specific: not "SMBs" but "Series A-C SaaS companies with 10-50 person sales teams in California")
2. **Value Propositions**: What value do we deliver? What problem do we solve? (Separate by segment if value differs)
3. **Channels**: How do we reach and deliver value to customer segments? (Acquisition, activation, customer success)
4. **Customer Relationships**: What type of relationship does each segment expect? (Support, onboarding, community, account management)
5. **Revenue Streams**: How does the business generate revenue from each segment? (Subscription, usage, licensing, marketplace, etc.)
6. **Key Resources**: What assets are required to deliver the value proposition? (People, technology, capital, partnerships, data)
7. **Key Activities**: What activities must we perform well? (Product development, marketing, sales, operations)
8. **Key Partnerships**: Who are our key partners and suppliers? (Distribution partners, technology partners, content/data partners)
9. **Cost Structure**: What are the most important costs in the business model? (By activity, by resource, fixed vs variable)

## Lean Canvas (for startups and new products)

Lean Canvas, developed by Ash Maurya, replaces 4 BMC blocks with startup-relevant ones. Use when you have high uncertainty:
- Replaces Key Partners with Problem (top 3 problems being solved)
- Replaces Key Activities with Solution (top 3 features or form factor)
- Replaces Key Resources with Key Metrics (key activities you measure; early-stage PMF indicators)
- Replaces Customer Relationships with Unfair Advantage (what cannot easily be copied: network effects, brand, data, switching costs)

## Unit Economics Deep Dive

Unit economics answers: "What is the profit on a single unit of sale?" For B2B SaaS, a "unit" is typically one customer account.

### SaaS Unit Economics (Most Common)

**Fundamental metrics:**
- **Monthly Recurring Revenue (MRR)**: Revenue from subscriptions in a given month
- **Annual Recurring Revenue (ARR)**: MRR x 12 (or contract value for annual plans)
- **Customer Acquisition Cost (CAC)**: Total acquisition spend (marketing + sales fully loaded) divided by customers acquired. Often calculated as CAC payback period (months to recover CAC from gross margin).
- **Lifetime Value (LTV)**: Typically estimated as (ARPU x Gross Margin) / Monthly Churn Rate
- **LTV:CAC Ratio**: Should be 3:1 or higher at scale; 5:1+ indicates strong unit economics
- **Net Dollar Retention (NDR)**: How much revenue existing customers generate in Month N vs Month N-12, including churn, downgrades, and expansion. NDR >100% is a competitive moat.
- **Logo Churn**: % of customers (by count) who churn monthly (separate from revenue churn)
- **Revenue Churn**: $ revenue lost monthly from cancellations and downgrades

**Worked example - Series A SaaS:**
- ARPU: $5,000/year ($417/month)
- Gross margin: 75% ($3,125/year gross profit per customer)
- Monthly churn: 3% (12-month retention 69%, 24-month retention 48%)
- LTV: ($3,125 / 0.03) = $104,167
- CAC: $25,000 (fully loaded: AE salary allocation + marketing spend)
- LTV:CAC: 4.2:1 (healthy)
- CAC payback: 8 months
- Expansion revenue: 15% of new revenue from upsells to existing customers (good sign)

**What changes LTV:**
- Reducing churn by 1% increases LTV by ~3%
- Increasing ARPU by 10% increases LTV by 10%
- NDR >100% means LTV grows over time (customer becomes more valuable)

### Marketplace Unit Economics

Two-sided marketplints have different economics than pure SaaS:

**Key metrics:**
- **GMV (Gross Merchandise Value)**: Total transaction volume
- **Take Rate**: % of GMV retained by platform (remaining % goes to supply side)
- **Supply-side take home**: % of GMV sellers/suppliers keep
- **Network effects strength**: Does supply side grow with demand side?
- **Liquidity**: Can the platform match supply to demand efficiently?

**Benchmarks by category:**
| Category | Typical Take Rate | Supply Growth | Demand Growth |
|---|---|---|---|
| Payments processor | 1-3% | Limited | High (sticky customers) |
| Ride-sharing | 15-25% | Low (driver acquisition hard) | High (location supply) |
| E-commerce marketplace | 3-10% | Medium (seller onboarding) | Medium (two-sided friction) |
| Freelance services | 10-20% | Medium | Medium |
| SaaS integration marketplace | 15-30% | Low (limited developers) | High (app stores have network effects) |

**Chicken-and-egg problem:** Marketplaces often need to subsidize one side to bootstrap network effects. Estimate how much subsidies will cost and when you expect unit economics to flip positive (usually when critical mass is reached).

### Freemium Model Economics

Freemium is NOT a business model; it is a customer acquisition model. Separate economics:

**Acquisition side:**
- Free users acquire at near-zero CAC (word of mouth, organic)
- Target: 30-50% activation rate (free trial complete first core action)
- Typical conversion rate free to paid: 2-5%

**Monetization side:**
- Conversion rate matters far more than ARPU in freemium
- CAC is paid acquisition (e.g., ads to get free users to convert)
- LTV is only from paid users (free-to-paid conversions)
- Must achieve CAC payback in 12 months to be sustainable

**Unit economics worked example:**
- Free users acquired: 100k/month at ~$0 CAC
- Conversion rate (free to paid): 3%
- New paid customers: 3,000/month
- ARPU: $500/year
- LTV: $1,500 (assuming 3-year customer, 30% churn)
- Paid CAC: $500 (ads/sales to accelerate conversion)
- LTV:CAC: 3:1 (acceptable but tight; need to improve conversion rate or reduce CAC)

## Monetization Strategy Decision Tree

```
Do customers already have budget allocated for your problem?
├─ YES: Can you command higher pricing? (Can you create more value than alternatives?)
│  ├─ YES: Value-based pricing (price 10-20% lower than customer value realized)
│  └─ NO: Compete on cost or features
└─ NO: You must educate market on ROI
   ├─ Build case studies and ROI calculators
   └─ Start low to enable adoption, raise pricing over time

Is usage correlating with customer value?
├─ YES: Usage-based pricing (meter everything; charge for value used)
└─ NO: Flat-fee subscription (simpler, but may underprice high-value customers)

Is there a large price-sensitive segment that would use the product at lower price?
├─ YES: Freemium or free tier (builds network effects and top-of-funnel)
└─ NO: Paid-only (faster to revenue but smaller addressable market)

Can you lock in customer?
├─ YES: Annual contract with discount (improves NDR, reduces churn friction)
└─ NO: Month-to-month (lower friction but higher churn)
```

## Pricing Model Integration

Three primary pricing approaches:

| Approach | When to Use | Pros | Cons |
|---|---|---|---|
| Cost-plus | You have clear COGS (e.g., marketplace, data products) | Predictable margins | Ignores customer willingness to pay; vulnerable to competition |
| Competition-based | Your product is similar to existing solutions | Easy to justify; reduces sales objections | Leaves money on table if customer perceives more value |
| Value-based | Your product creates measurable ROI (productivity, revenue, cost-savings) | Captures customer value; improves margins; enables premium positioning | Requires clear ROI metrics; harder to implement in bottom-up buying |

**Tiering strategy (if using per-seat, per-feature, or per-usage tiers):**
- Good: $19/mo Starter, $79/mo Pro, $299/mo Enterprise (10x price steps, each tier has clear differentiation)
- Bad: $19, $24, $29, $34, $39 (too many tiers; customers confused about which to buy)
- Rule: Limit to 3 tiers maximum; each tier should have a reason to exist (different segment or use case)

## Business Model Innovation Patterns

Four ways to create competitive advantage through business model, not just product:

| Pattern | Definition | Example | When It Works |
|---|---|---|---|
| Unbundling | Separate one product feature into standalone product | Stripe (payments) unbundled from Shopify; Figma plugins unbundled design tools | Feature has separate buyer or distributes to new market |
| Platform Pivot | Move from selling to customers to enabling supply side | Shopify became app store + enterprise platform, not just hosted store | Network effects and ecosystem value outweigh single-product revenue |
| Razor-and-blades | Low-cost entry (razor), high-margin consumables (blades) | Slack gives free tier to build adoption; charges for enterprise features and compliance | Network effects drive adoption; willingness to pay increases with usage |
| Horizontal Expansion | Expand from one customer problem to adjacent problems | HubSpot expanded from email marketing to full CRM to sales to service | Same buyer, adjacent problems, increasing wallet share |

## Business Model Stress Test Framework

Test your model against extreme scenarios to find breaking points:

**At 10x scale:**
- Gross margin stays same? (Usually cost structure changes at scale)
- Support costs per customer scale with ARR or grow faster? (Often grow faster unless heavily automated)
- Customer acquisition channels have capacity? (Many channels have natural ceiling)
- Infrastructure costs support 10x growth? (Some technology stacks do not scale)

**If churn increases to worst-case (e.g., 7% monthly):**
- Does LTV still support CAC payback? (Higher churn kills unit economics faster than raising prices helps)
- What is retention breakeven point? (At what churn rate does unit economics break?)

**If major competitor enters at lower price:**
- Can you compete on product differentiation alone? (Or will you be forced to match pricing and lose margin?)
- Do you have cost advantage to undercut them? (Usually the better strategy than price match)
- Is your product/positioning defensible? (Or is this winner-take-most market?)

**If your largest customer segment dries up:**
- Can remaining segments support fixed costs? (Many SaaS companies have high fixed costs; smaller customer base may not support payroll)
- What is minimum revenue needed to sustain company? (Know this number; it guides how much growth is required)

## Anti-Patterns in Business Model Design

| Anti-Pattern | Why It Fails | Example of Failure |
|---|---|---|
| Pricing based on what you think customers will pay, not what they actually will | Customers vote with their wallet; assumption = disaster | SaaS startup prices at $999/month because "enterprise", ends up with 0 customers instead of profitable $199/month model |
| Freemium without clear path to paid conversion | Free users are customers until they are not; need measurement of free-to-paid funnel | Product has 1M free users, 0.1% conversion rate, no path to improve conversion: burning money |
| Revenue target drives everything else | You backwards-engineer absurd unit economics to hit revenue goal | "We need $10M ARR, so let's charge $5k/seat x 2000 customers" without verifying market will buy at that price |
| Two monetization models in tension | Charging users while also relying on viral loops (users have no incentive to refer if you charge them) | Charging per user while building viral features; viral metrics tank because referred users hit paywall |
| Business model misaligned with product | Product is land-and-expand (design for SMB), but business model is enterprise only (long sales cycle) | Intended for SMB adoption but priced at $50k/year minimum; no SMB will pay, sales cycle drags, cash burns |
| Metric moving but unit economics degrading | Growing at 200% but LTV:CAC dropping from 5:1 to 2:1 | Revenue growing but profitability path disappearing because you are burning acquisition dollars on lower-value customers |

## Output Template

---
**BUSINESS MODEL ANALYSIS**

**Product:** [Name]
**Stage:** [Pre-launch / Early traction / Growth / Scale]
**Date:** [Date]

**Business Model Type:** [Subscription / Freemium / Marketplace / Usage-based / Hybrid / Other]

**Revenue Streams**
| Segment | Pricing Model | Estimated ARPU | Target Volume | Annual Revenue |
|---|---|---|---|---|
| [Segment 1] | [Model] | [Price] | [# customers] | [Revenue] |

**Unit Economics** (Filled in for primary segment; others listed if significantly different)
- Monthly/Annual ARPU: [X]
- Gross margin: [X%]
- Customer acquisition cost (CAC): [X]
- CAC payback period: [X months]
- Estimated lifetime value (LTV): [X]
- LTV:CAC ratio: [X:1]
- Monthly/annual churn: [X%]
- Net dollar retention: [X%] (if applicable; SaaS only)

**Key Assumptions** (What must be true for unit economics to work?)
1. [Assumption]: [Why risky] - [How to validate]
2. ...

**Riskiest Assumptions** (What would break unit economics if wrong?)
1. [Assumption]: [Impact if wrong] - [Validation plan]
2. ...

**Monetization Stress Tests**
- At 10x customer scale, gross margin still [X%]? [Yes/No - explain]
- If churn increases to [X%], LTV still supports CAC payback? [Yes/No - explain]
- If largest customer segment shrinks, remaining segments support fixed costs? [Yes/No - explain]

**Monetization Alternatives Considered**
[1-2 alternative models worth evaluating and why, including brief analysis of pros/cons]

---
