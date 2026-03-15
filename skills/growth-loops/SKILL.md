---
name: growth-loops
description: "Design sustainable growth loops and flywheels using Reforge methodology, Andrew Chen growth systems, and Casey Winters growth models. Covers 7 loop types (viral, content, data network effect, marketplace, PLG, paid, sales), growth accounting (new/returning/resurrected/churned), Four Fits framework (market-product, product-channel, channel-model, model-market), network effects taxonomy (direct, cross-side, data, local), channel-market fit, paid vs organic mix analysis, Quick Ratio calculation, and loop compounding mechanics. Use when designing growth engines, diagnosing growth quality, identifying viral mechanics, or answering PM interview questions about growth."
argument-hint: "[describe your product, current growth channels, user acquisition sources, and what kind of growth loop you want to explore]"
---

# Growth Loop Designer

Growth loops are circular, compounding systems where the output of one cycle becomes the input of the next. Unlike funnels (linear, one-time), loops compound -- each cycle produces more input for the next. This is the fundamental difference between products that grow sustainably and those that require ever-increasing acquisition spend.

Apply this skill to: $ARGUMENTS

## Growth Loops vs. Funnels

| Property | Funnels | Growth Loops |
|---|---|---|
| Shape | Linear (top to bottom) | Circular (output feeds input) |
| Compounding | No -- each cohort is independent | Yes -- each cycle amplifies the next |
| Sustainability | Requires constant top-of-funnel investment | Self-reinforcing once established |
| Failure mode | Dries up when acquisition spend stops | Degrades when loop efficiency drops |

---

## 7 Types of Growth Loops

### 1. Viral / Word-of-Mouth Loop
User gets value --> User invites/refers others --> New users join --> Each creates value and refers more

**Examples**: Slack (invite teammates), Calendly (share scheduling link), Loom (send video), Dropbox (referral program)

**Key metric**: Viral coefficient (k) = invites sent per user x conversion rate of invites
- k > 1: Exponential growth (rare and powerful)
- k = 0.5-1.0: Meaningful viral contribution to growth
- k < 0.3: Viral component exists but doesn't drive growth alone

**Sub-types:**
- Organic viral: Product use naturally exposes non-users (Calendly, Figma shared links)
- Incentivized viral: Explicit reward for referring (Dropbox storage, Uber credits)
- Social viral: Content shared on social platforms (Spotify Wrapped, Wordle results)

### 2. Content Loop
User creates content --> Content is indexed/discovered --> New users find content --> Some create more content

**Examples**: YouTube, Reddit, Stack Overflow, Substack, Pinterest

**Key metrics**: Content creation rate, content-to-discovery ratio (what % of content gets meaningful views), discovery-to-signup rate

### 3. Data Network Effect Loop
More users --> More data --> Better product intelligence --> Better product --> More users

**Examples**: Google Search, Waze, Duolingo (adaptive learning), Spotify Discover Weekly, Netflix recommendations

**Key metrics**: Prediction accuracy vs. data volume curve, marginal value of next data point (diminishing returns threshold)

### 4. Marketplace Loop
More buyers --> More sellers attracted --> More inventory/selection --> More buyers attracted

**Examples**: Etsy, Airbnb, App Store, Uber, DoorDash

**Key metrics**: Liquidity (probability of finding a match), matching efficiency, time-to-match, take rate sustainability

**Marketplace-specific challenges:**
- Chicken-and-egg problem (which side to seed first?)
- Liquidity density (enough supply/demand in a specific geography or category?)
- Multi-homing (do users use multiple competing marketplaces?)
- Disintermediation risk (do parties bypass the platform after matching?)

### 5. Product-Led Growth (PLG) Loop
User achieves success --> Shares output with non-users --> Non-users see value --> Convert to users

**Examples**: Figma (share designs), Airtable (share base), Notion (share page), Miro (share board)

**Key metrics**: PQL conversion rate (25-30% benchmark), time-to-value (target: 3-5 min), activation rate, expansion revenue rate

### 6. Paid Acquisition Loop
Revenue from users --> Reinvest in paid acquisition --> Acquire more users --> Generate more revenue

**Examples**: DTC brands, mobile gaming, subscription boxes

**Key metrics**: LTV:CAC ratio (target: 3:1+), payback period, ROAS (return on ad spend), blended CAC across channels

**Sustainability test**: If you stopped paid spend tomorrow, how much growth would remain? If the answer is "almost none," this loop is fragile.

### 7. Sales-Led Loop
Customer success stories --> Sales team uses as proof points --> Close new deals --> Create more success stories

**Examples**: Salesforce, Snowflake, enterprise SaaS

**Key metrics**: Win rate, deal cycle length, case study production rate, reference customer availability

---

## Growth Accounting

Track growth quality, not just growth quantity:

### User Growth Decomposition
```
Active Users This Period = Active Users Last Period + New + Resurrected - Churned

Where:
  New = First-time active users
  Returning = Active in both current and prior period
  Resurrected = Previously churned, now active again
  Churned = Active last period, inactive this period
```

### Quick Ratio
Quick Ratio = (New + Resurrected) / Churned

| Quick Ratio | Interpretation |
|---|---|
| > 4.0 | Exceptional growth quality (high retention, strong acquisition) |
| 2.0 - 4.0 | Healthy growth (adding faster than losing) |
| 1.0 - 2.0 | Marginal growth (barely adding more than losing) |
| < 1.0 | Shrinking (losing users faster than gaining) |

### Revenue Growth Accounting
```
MRR This Month = MRR Last Month + New MRR + Expansion MRR + Reactivation MRR - Contraction MRR - Churn MRR
```

**Healthy mix evolution as companies scale:**
- Early ($5M ARR): 90% new / 10% expansion
- Growth ($20M ARR): 70% new / 30% expansion
- Scale ($50M ARR): 60% new / 40% expansion
- Mature ($200M ARR): 33% new / 67% expansion

---

## The Four Fits Framework (Reforge)

For $100M+ growth potential, all four fits must align:

### Fit 1: Market-Product Fit
Does the product solve a real problem for a large enough market?
- Market category and size
- Problem frequency and severity
- Willingness to pay

### Fit 2: Product-Channel Fit
Does the product design fit the distribution channel?
- Products must fit channels; channels don't mold to products
- Example: Viral products need share-worthy output. SEO products need indexable content. PLG needs low time-to-value.

### Fit 3: Channel-Model Fit
Does the acquisition channel economics support the business model?
- High-touch sales requires high ACV to justify CAC
- PLG requires high volume to offset low ACV
- Content/SEO requires long payback period tolerance

### Fit 4: Model-Market Fit
Is the business model sustainable in this market?
- Willingness to pay vs. pricing model
- Expected LTV vs. acquisition cost
- Market growth rate vs. required payback period

**Diagnostic**: If growth stalls, identify which fit is broken. Most teams assume Market-Product Fit and optimize channels, but the problem is often Channel-Model or Product-Channel misfit.

---

## Network Effects Taxonomy

| Type | Mechanism | Strength | Example |
|---|---|---|---|
| **Direct (same-side)** | More users of same type = more value | Strong if critical mass reached | Phone network, social media |
| **Cross-side (two-sided)** | More on one side = more value for other side | Moderate; requires balance | Uber (drivers/riders), Airbnb |
| **Data network effects** | More usage = better AI/ML/recommendations | Moderate; diminishing returns | Netflix, Spotify, Google |
| **Local network effects** | Value increases within geographic/social cluster | Strong locally, weak globally | Nextdoor, WhatsApp (early) |
| **Expertise network effects** | More expert contributors = more value | Strong if knowledge is unique | Stack Overflow, Wikipedia |
| **Protocol/standard** | More adopters = more compatibility | Very strong once established | TCP/IP, USB, Ethereum |

### Network Effect Strength Assessment
For your product, evaluate:
- At what user count does the network effect become meaningful? (Critical mass)
- How quickly do returns diminish? (Linear, logarithmic, or asymptotic)
- Can a competitor replicate the network? (Multi-homing risk)
- Is the network local or global? (Affects expansion strategy)

---

## Paid vs. Organic Growth Mix

| Dimension | Organic | Paid |
|---|---|---|
| CAC | 25-30% lower | Higher but predictable |
| LTV | 10-15% higher | Lower (less qualified intent) |
| Retention | 30% better retention | Higher churn |
| Scalability | Slow to build, compounds over time | Immediate volume, linear spend |
| Attribution | Harder to measure | Easier to measure (but halo effects exist) |

**Halo effect warning**: Paid campaigns boost apparent organic traffic, making organic look better than it is. Use holdout tests to measure true incremental impact of paid.

**Healthy mix**: Most sustainable businesses derive 60-80% of growth from organic/product channels and 20-40% from paid. If >80% comes from paid, the growth is fragile.

---

## Loop Design Process

1. **Identify the value moment**: What is the single most valuable thing a user does or gets in your product?
2. **Find the natural spread mechanism**: Does that value moment naturally cause the product to reach non-users? How?
3. **Map the loop**: Draw the circular chain from user action to new user acquisition/re-engagement
4. **Measure each stage**: Conversion rate at every step in the loop
5. **Identify break points**: Where does the loop lose the most efficiency?
6. **Design interventions**: Product changes that improve the weakest link
7. **Test compounding**: After improvement, does the loop actually compound (each cycle bigger than the last)?

---

## Output Template

```
GROWTH LOOP ANALYSIS
Product: [Name]
Date: [Today]

PRIMARY LOOP
Type: [Viral / Content / Data / Marketplace / PLG / Paid / Sales]
Loop Map:
  Step 1: [Action] (metric: [X])
  --> Step 2: [Result] (metric: [X])
  --> Step 3: [User acquisition or re-engagement] (metric: [X])
  --> Step 4: [Returns to Step 1] (metric: [X])

LOOP EFFICIENCY
| Stage | Metric | Current | Benchmark | Gap |
|-------|--------|---------|-----------|-----|
| 1->2  | [Rate]  | X%     | Y%        | Z%  |
| 2->3  | [Rate]  | X%     | Y%        | Z%  |
| 3->4  | [Rate]  | X%     | Y%        | Z%  |

Overall loop efficiency: [X%]
Viral coefficient (if applicable): [k = X]

GROWTH ACCOUNTING
Quick Ratio: [X]
New: [N] | Returning: [N] | Resurrected: [N] | Churned: [N]
Growth quality: [Exceptional / Healthy / Marginal / Shrinking]

FOUR FITS ASSESSMENT
Market-Product: [Strong / Moderate / Weak]
Product-Channel: [Strong / Moderate / Weak]
Channel-Model: [Strong / Moderate / Weak]
Model-Market: [Strong / Moderate / Weak]
Weakest fit: [Which one and why]

BREAK POINTS
1. [Stage]: [Why it loses efficiency] -- [Intervention]
2. [Stage]: [Why it loses efficiency] -- [Intervention]

SECONDARY LOOP
[Description of a supporting loop that reinforces the primary]

PAID vs. ORGANIC MIX
Current: [X% organic / Y% paid]
Target: [X% organic / Y% paid]
Action: [What to shift]

NETWORK EFFECTS
Type: [Direct / Cross-side / Data / Local / None]
Strength: [Strong / Moderate / Weak / Not applicable]
Critical mass status: [Achieved / Approaching / Far from]

LOOP HEALTH: [Healthy / Needs Work / Broken]
TOP PRIORITY: [The single highest-impact intervention]
```
