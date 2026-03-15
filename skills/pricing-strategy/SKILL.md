---
name: pricing-strategy
description: "Design or evaluate a pricing strategy for a product. Use this skill when someone needs to set pricing for the first time, revisit existing pricing, understand willingness-to-pay, design pricing tiers, or prepare for a PM interview question about how to price a product."
---

# Pricing Strategy Advisor

Pricing is one of the highest-leverage strategic decisions a PM makes. A 1% improvement in pricing yields an average 11% improvement in profit. You help PMs think through pricing from value, psychology, competitive, and operational angles.

## Pricing Strategy Framework

Apply this skill to: $ARGUMENTS


### Step 1: Understand Value Delivered

Before setting a price, quantify the value the product delivers across three dimensions:
- **Economic value**: Time saved, revenue generated, cost reduced, risk eliminated. Be specific: "Saves the average user 4 hours per week at $75/hour = $300/week in value."
- **Emotional value**: Confidence, status, peace of mind, reduced anxiety
- **Competitive displacement value**: What would the customer pay (in money, time, and effort) for the next best alternative? Include switching costs.

The justified price range is typically 10-30% of the quantified economic value for B2B, or based on perceived value and competitive anchoring for B2C.

### Step 2: Select the Value Metric

The value metric is what you charge for. It determines how price scales with customer value. This is the single most important pricing decision.

**HOPE Framework for Value Metric Selection:**
Evaluate each candidate metric on two dimensions:
- **Clarity**: How directly does the metric correlate with the value the customer receives?
- **Ease**: How predictable, trackable, and billable is the metric?

| Metric Type | Example | Clarity | Ease | Best For |
|---|---|---|---|---|
| Per seat/user | $10/user/month | Medium | High | Collaboration tools where more users = more value |
| Per unit of usage | $0.01/API call | High | Medium | Infrastructure, API products, developer tools |
| Per outcome/result | $0.99/resolved ticket | Very High | Low | AI agents, automation, measurable deliverables |
| Per resource consumed | $X/GB stored, $X/compute hour | High | High | Cloud infrastructure, data platforms |
| Flat rate | $99/month | Low | Very High | Simple products with uniform value delivery |
| Revenue share | 2.9% + $0.30/transaction | Very High | Medium | Payments, marketplaces, fintech |
| Hybrid (base + usage) | $50/month + $0.005/request | High | Medium | Most modern SaaS (fastest-growing model) |

**Selection Criteria:**
- The metric should scale with the value the customer receives (customers who get more value pay more)
- Customers should be able to predict their costs (avoids bill shock and churn)
- You should be able to measure and bill it reliably
- Limit to 2-3 pricing dimensions maximum (David Skok's rule)

### Step 3: Understand Willingness-to-Pay

Methods to estimate willingness-to-pay, ordered by rigor:

**Van Westendorp Price Sensitivity Meter (Qualitative, Quick)**
Ask customers four questions about a described product:
1. At what price would this be so cheap you would question its quality?
2. At what price is this a bargain - a great buy for the money?
3. At what price is this getting expensive but you would still consider it?
4. At what price is this too expensive to consider?
Plot the cumulative distributions. The acceptable price range and optimal price point emerge from the intersections.

**Gabor-Granger Method (Quantitative, Moderate)**
Present a specific price and ask: "Would you buy this product at $X?" If yes, test a higher price. If no, test a lower price. Generates a demand curve showing price elasticity. Best after a MaxDiff analysis clarifies which features customers value most.

**MaxDiff / Best-Worst Scaling (Feature Valuation)**
Present sets of features and ask which is most and least important. Creates a robust ranking of what customers value, informing which features justify price increases and which belong in which tier.

**Discrete Choice Modeling / Conjoint Analysis (Gold Standard)**
Present realistic product configurations at different price points and ask customers to choose. Reveals trade-offs between features, price, and brand. Most comprehensive but requires 200+ respondents and statistical expertise.

**Champion/Challenger Testing (In-Market)**
Test two price points with comparable user groups. Measures actual conversion and revenue impact, not just stated intent. Requires careful experiment design (see ab-testing skill).

### Step 4: Choose a Pricing Model

| Model | How It Works | Best For | Risk |
|---|---|---|---|
| **Value-based** | Price anchored to quantified customer value | Products with clear, measurable ROI | Requires strong value narrative |
| **Usage-based** | Pay for what you use (API calls, storage, compute) | Infrastructure, developer tools, AI products | Revenue volatility, customer budget anxiety |
| **Hybrid (base + usage)** | Platform fee for access + usage-based overage | Modern SaaS (85% of high-growth SaaS by 2025) | Complexity in billing and communication |
| **Outcome-based** | Pay only when a defined outcome is achieved | AI agents, automation, high-confidence products | Revenue depends on product reliability |
| **Freemium** | Free tier with paid upgrades | PLG products with strong viral/network effects | Free tier cannibalization, slow conversion |
| **Cost-plus** | Cost to serve + target margin | Commodity services, low differentiation | Leaves money on the table |
| **Competitive** | Anchor to market rates | Entering established markets | Undifferentiating, race to bottom |
| **Penetration** | Price below market to gain share, then raise | Two-sided marketplaces, winner-take-most markets | Hard to raise prices later |
| **Skimming** | Launch high, reduce over time | Limited early adopters, luxury/premium positioning | Alienates late majority |

**AI/ML Product Pricing Considerations:**
AI products have fundamentally different cost structures (50-60% gross margins vs. 80-90% for traditional SaaS). Every inference incurs real compute costs. Consider:
- Token-based pricing (OpenAI model): Aligns cost with usage, familiar to developers
- Outcome-based pricing (Intercom Fin at $0.99/resolved conversation): Highest value alignment
- Hybrid base + usage: Most balanced for predictability and upside capture
- Cost monitoring: Track cost-per-inference and build in margin above COGS

### Step 5: Design the Packaging Architecture

**Good-Better-Best (Most Common, used by 72% of major SaaS)**
Three tiers mapping to distinct user segments:

| Design Principle | Implementation |
|---|---|
| Each tier maps to a clearly differentiated user segment | Starter = individuals, Pro = teams, Enterprise = organizations |
| Upgrade triggers are natural pain points, not artificial limits | Hit usage ceiling, need team features, require SSO/audit logs |
| The middle tier captures most revenue - make it compelling | Include the features that matter most, highlight as "Most Popular" |
| Enterprise tier justifies a sales conversation | Custom pricing, SLA, dedicated support, security features |
| Features flow downward over time | Today's Pro feature becomes tomorrow's Starter feature as you add new Pro value |

**Core + Add-On Modules**
Base platform with optional modules customers can add. Best for products with diverse use cases where not all customers need all features. Allows customers to build their own package.

**Platform + Marketplace**
Core platform with third-party extensions. Creates ecosystem lock-in and partnership revenue. Best for developer platforms and extensible tools.

**Feature Gating Strategy:**
- Horizontal gating (limit quantity: 3 projects, 100 API calls) works well for scaling-based upgrades
- Vertical gating (limit capability: no advanced analytics, no SSO) works well for sophistication-based upgrades
- Time-based gating (14-day trial of full product) works well for demonstrating value before requiring commitment

### Step 6: Pricing Psychology

**B2B Psychology:**
- Anchor with ROI calculation: "At $500/month, this pays for itself if it saves your team 7 hours"
- Present three tiers with the premium priced high to push buyers toward the middle option (compromise effect)
- Express price as cost per outcome when ROI is strong ($5 per hour saved, $0.50 per lead generated)
- Use annual billing discount (typically 15-20%) to improve retention and cash flow
- Credibility matters more than urgency. Avoid artificial scarcity tactics.

**B2C Psychology:**
- Charm pricing ($9.99 not $10) works for consumer products
- Anchor the highest tier first in top-down presentation
- Highlight "Most Popular" to reduce choice paralysis (social proof)
- Loss aversion: Frame around what the customer loses by not upgrading
- Free trial length matters: 14 days for simple products, 30 days for complex ones

### Step 7: Price Localization

**Purchasing Power Parity (PPP):**
Adjust prices by region based on local purchasing power. A $20/month plan in the US might be $6/month in India or $12/month in Brazil.

| Consideration | Approach |
|---|---|
| PPP index mapping | Use Big Mac Index or World Bank PPP data as starting points |
| Currency display | Show local currency, charge in USD or local currency depending on payment infrastructure |
| Anti-arbitrage | Geo-restrict accounts or use regional feature sets to prevent low-price resale |
| Regional packaging | Some markets may need different tier structures (e.g., mobile-first plans in emerging markets) |
| Legal/tax | VAT, GST, sales tax compliance varies by jurisdiction |

### Step 8: Net Revenue Retention and Expansion Design

Pricing should be designed not just for initial conversion but for expansion revenue. Best-in-class SaaS achieves 120-140% net revenue retention.

**Expansion Levers:**
- **Usage growth**: As customers use more, they naturally upgrade tiers (usage-based component)
- **Seat expansion**: More team members adopt the product over time
- **Module upsell**: Customers add capabilities as their needs mature
- **Cross-sell**: Related products or services sold alongside the core

**Design Principles for Expansion:**
- Make the upgrade trigger a natural moment of success, not a moment of frustration
- Price the initial tier to land the account; price expansion tiers to grow it
- Acquiring $1 of expansion ARR costs approximately $0.20-0.27 vs. $1.16 for new customer acquisition

### Common Pricing Mistakes

1. **Pricing too low** (43% of SaaS companies undercharge): Stems from fear, not data. Low prices signal low value.
2. **Treating pricing as static**: Markets evolve. Review pricing at least quarterly; test annually.
3. **Cost-plus thinking**: Software delivers value far exceeding production cost. Price on value, not cost.
4. **Hidden pricing**: Not showing prices on your website signals "we do not want your business" to smaller customers.
5. **Ignoring LTV:CAC ratio**: Healthy SaaS maintains minimum 3:1 LTV:CAC. Price must support sustainable unit economics.
6. **Too many tiers**: More than 4 tiers creates choice paralysis. 3 is optimal for most products.
7. **Artificial limitations that frustrate**: Crippling free tiers or creating arbitrary limits that do not correspond to value delivery damages trust.
8. **No grandfathering strategy**: Raising prices on existing customers without clear communication and value justification drives churn.
9. **Ignoring willingness-to-pay research**: Setting prices based on gut feel or competitor anchoring alone.
10. **Not testing**: Companies that test pricing quarterly outperform peers by 30% in net dollar retention.

## Pricing Experimentation

**Testing Approaches (ordered by risk):**
1. **New customer cohort testing** (safest, used by 75% of successful SaaS): Test new prices only with new customers.
2. **Geographic testing**: Different prices in different markets.
3. **Feature-based testing**: Test which features belong in which tier.
4. **Time-limited promotional pricing**: Test lower prices without permanently anchoring.
5. **A/B testing on pricing page**: Test presentation, anchoring, and packaging (not necessarily the actual price).

**Minimum Requirements:**
- 250-500 visitors per variant for statistical significance
- 30-60 day test duration
- Track: conversion rate, ARPU, CAC payback period, NRR, churn rate, gross margin

## Output Template

---
**PRICING STRATEGY RECOMMENDATION**

**Product:** [Name]
**Current Pricing:** [Existing pricing if applicable, or "New product"]
**Pricing Model:** [Recommended model with rationale]
**Value Metric:** [What you charge for, with HOPE analysis]

**Value Quantification**
- Economic value delivered per user/month: [Estimate with calculation]
- Next best alternative cost: [Estimate including switching costs]
- Justified price range: [$X - $Y] (10-30% of economic value for B2B)

**Recommended Packaging and Tier Structure**

| Tier | Target Segment | Monthly Price | Annual Price | Key Features | Usage Limits | Upgrade Trigger |
|---|---|---|---|---|---|---|
| Free / Trial | [Segment] | $0 | $0 | [Features] | [Limits] | [What drives conversion] |
| [Starter] | [Segment] | $X | $X | [Features] | [Limits] | [What drives upgrade] |
| [Pro] | [Segment] | $Y | $Y | [Features] | [Limits] | [What drives upgrade] |
| [Enterprise] | [Segment] | Custom | Custom | [Features] | [Custom] | Sales conversation |

**Expansion Revenue Design**
- Primary expansion motion: [Usage growth / Seat expansion / Module upsell]
- Expected NRR target: [X%]
- Key expansion trigger points: [List]

**Pricing Psychology Tactics**
[3-4 specific tactics applied to this pricing structure with rationale]

**Price Localization Recommendation**
[Regional pricing strategy or "Not applicable at this stage"]

**Unit Economics Validation**
- Target LTV:CAC ratio: [X:1]
- Estimated CAC payback period: [X months]
- Gross margin per tier: [Estimates]

**Risks**
| Risk | Likelihood | Mitigation |
|---|---|---|
| [Risk 1] | High/Med/Low | [Mitigation approach] |
| [Risk 2] | High/Med/Low | [Mitigation approach] |
| [Risk 3] | High/Med/Low | [Mitigation approach] |

**Recommended First Experiment**
[One specific pricing test to validate before full rollout, including test design, success criteria, and duration]

**Pricing Review Cadence**
[Quarterly review with annual re-evaluation recommendation]
---
