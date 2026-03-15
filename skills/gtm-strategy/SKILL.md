---
name: gtm-strategy
description: "Build a complete go-to-market strategy for a new product or feature launch. Covers beachhead segment selection (Geoffrey Moore Crossing the Chasm and Bowling Pin strategy), ICP definition (firmographics, behavioral, trigger events), GTM motion selection (PLG, Sales-Led, Marketing-Led, Partner-Led, ABM with ACV-based selection criteria), land-and-expand strategy, launch phasing (alpha/beta/GA), channel-market fit analysis, launch plan with pre-launch/launch-week/post-launch actions, success metrics (leading and lagging), and expansion revenue playbook. Use when planning a product launch, defining GTM motion, identifying beachhead segments, or preparing for PM interviews about taking products to market."
argument-hint: "[describe the product or feature being launched, target market, current stage (pre-launch / beta / GA), and any constraints]"
---

# Go-to-Market Strategy Builder

A go-to-market strategy defines how you will reach your target customers and deliver your value proposition. A great GTM strategy picks a specific beachhead, selects the right motion for the economics, and sequences expansion deliberately.

Apply this skill to: $ARGUMENTS

## Step 1: Beachhead Segment Selection

### Crossing the Chasm Framework (Geoffrey Moore)
The technology adoption lifecycle has a critical gap between early adopters and the early majority. Your beachhead is the specific segment that bridges this chasm.

**Adoption curve stages:**
Innovators (2.5%) --> Early Adopters (13.5%) --> **[CHASM]** --> Early Majority (34%) --> Late Majority (34%) --> Laggards (16%)

**Beachhead requirements:**
- Small enough to dominate (you can reach most potential customers)
- Large enough to matter (revenue potential justifies the focus)
- High pain intensity (they urgently need what you offer -- not nice-to-have)
- Accessible (you can reach them through specific, identified channels)
- Reference-able (winning here opens doors to the next segment)
- Whole product achievable (you can deliver a complete solution for this segment)

### Bowling Pin Strategy
Sequence expansion deliberately: each new segment should be adjacent to a previously won segment, so awareness, case studies, and references transfer.

```
Pin 1: [Beachhead segment -- dominate first]
  --> Pin 2: [Adjacent segment sharing same pain or buyer]
  --> Pin 3: [Next adjacent, leveraging Pin 1+2 references]
  --> Pin 4: [Broader market enabled by earlier wins]
```

**Example**: Salesforce started with small sales teams (Pin 1) --> mid-market sales orgs (Pin 2) --> enterprise sales (Pin 3) --> platform for all business processes (Pin 4)

## Step 2: Ideal Customer Profile (ICP)

### B2B ICP Definition
| Dimension | Details |
|---|---|
| **Firmographics** | Company size, industry, funding stage, geography, tech stack |
| **Buyer role** | Who has budget and authority (title, reporting line) |
| **Champion role** | Who will advocate internally (title, motivations) |
| **End user role** | Who uses the product daily (title, workflow) |
| **Trigger events** | What causes them to start looking (new hire, growth milestone, compliance deadline, competitor threat, tool migration) |
| **Disqualifiers** | What signals a bad fit (too small, wrong industry, no budget, misaligned expectations) |

### B2C ICP Definition
| Dimension | Details |
|---|---|
| **Demographics** | Age range, income, location, occupation |
| **Psychographics** | Values, lifestyle, aspirations, pain tolerance |
| **Behavioral** | Current tools, usage patterns, buying habits, content consumption |
| **Trigger events** | Life events, frustrations, seasonal patterns |
| **Disqualifiers** | Signals they won't convert or retain |

## Step 3: GTM Motion Selection

### Motion Selection by ACV and Complexity

| ACV Range | Recommended Motion | Sales Involvement | Example Companies |
|---|---|---|---|
| < $1K/year | **PLG** (self-serve) | None or minimal | Slack, Notion, Canva |
| $1K - $5K/year | **PLG + Inside Sales** (hybrid) | Sales assists expansion | Figma, Airtable, Loom |
| $5K - $50K/year | **Inside Sales + PLG** | Sales drives, PLG feeds pipeline | Datadog, Amplitude, dbt |
| $50K - $100K/year | **Field Sales** | Full sales cycle, CS handoff | Salesforce, Snowflake |
| > $100K/year | **Enterprise Sales + ABM** | Multi-threaded, long cycle | Palantir, Workday |

### Motion Fit Assessment
For each motion, evaluate:
- **Product-channel fit**: Does the product design support this motion? (PLG needs low TTV; sales-led needs demo-able value)
- **Channel-model fit**: Does the economics work? (High-touch sales on $500 ACV doesn't work)
- **Buyer behavior fit**: How does the target buyer prefer to buy? (Developers prefer self-serve; C-suite prefers consultative)

### Hybrid Motion Design (2026 standard)
Most successful B2B companies layer motions:
- **PLG bottom-up**: Individual users discover and adopt the product
- **Sales top-down**: Sales engages when usage signals indicate expansion opportunity (PQL triggers)
- **CS expansion**: Customer success drives upsell, cross-sell, and seat expansion in existing accounts

## Step 4: Land and Expand Strategy

### Landing Strategy
- Start with a specific use case, team, or department (not "the whole company")
- Minimize initial contract size to reduce buying friction
- Focus on fast time-to-value for the landing team
- Define what "success" looks like for the initial deployment

### Expansion Triggers
| Signal | Expansion Type | Action |
|---|---|---|
| Team exceeds seat limit | Seat expansion | CS proactive outreach |
| Second team starts using product | Cross-department expansion | Sales multi-thread |
| Usage hits tier ceiling | Tier upgrade | In-product upgrade prompt |
| Champion gets promoted | Executive sponsorship | Executive briefing |
| Contract renewal approaching | Multi-year deal | Discounted annual pricing |

### Expansion Economics
- Probability of closing new customer: 5-20%
- Probability of expanding existing customer: 60-70%
- Cost of expansion revenue: ~1/3 of new customer acquisition cost
- NRR target: 110-120%+ for healthy expansion

## Step 5: Messaging and Positioning

**Core messaging framework** (use value-proposition skill for depth):
- **Problem statement**: The specific pain, stated in customer language
- **Solution statement**: What the product does differently (not features -- outcomes)
- **Proof point**: One specific piece of evidence (customer result, benchmark, comparison)
- **Call to action**: What the target should do next (try free, book demo, read case study)

### Messaging by Audience

| Audience | Focus | Tone | Proof Type |
|---|---|---|---|
| End user | Ease of use, time saved | Practical, relatable | Product screenshots, workflow demos |
| Champion | Team impact, career win | Ambitious, data-driven | Case studies, ROI calculators |
| Buyer/executive | Business impact, risk reduction | Strategic, concise | Revenue impact, competitive advantage |
| Technical evaluator | Architecture, security, integrations | Detailed, honest | Documentation, security certifications |

## Step 6: Launch Phasing

### Alpha (Internal / Design Partners)
- 5-15 design partners with active feedback channels
- Focus: Does the product solve the core problem? (Validation, not scale)
- Duration: 4-8 weeks
- Exit criteria: 3+ design partners say "I'd be disappointed if this went away"

### Beta (Limited Public)
- 50-200 users, gated signup or waitlist
- Focus: Onboarding quality, activation rate, early retention signal
- Duration: 4-8 weeks
- Exit criteria: Activation rate >X%, no P0 bugs, support burden manageable

### GA (General Availability)
- Open to full target segment
- Focus: Acquisition channels, conversion optimization, scalability
- Launch amplification: PR, content, events, partnerships

## Step 7: Launch Plan

### Pre-Launch (6-8 weeks before GA)

| Week | Action | Owner |
|---|---|---|
| W-8 | Finalize ICP and beachhead segment | PM |
| W-7 | Draft messaging and positioning | PM + Marketing |
| W-6 | Prepare launch content (blog, video, landing page) | Marketing |
| W-5 | Sales enablement materials (demo script, FAQ, objection handling) | PM + Sales |
| W-4 | Beta user feedback synthesis and product fixes | PM + Engineering |
| W-3 | Press/analyst briefings (if applicable) | Comms |
| W-2 | Internal launch readiness review (product, sales, support, marketing) | PM |
| W-1 | Final dry run and contingency planning | All |

### Launch Week

| Day | Action | Owner |
|---|---|---|
| Day 1 | Product announcement (blog, email, social) | Marketing |
| Day 1 | Sales outreach to warm leads and beta advocates | Sales |
| Day 1-2 | Community engagement (Product Hunt, HN, Reddit if appropriate) | PM + Marketing |
| Day 2-3 | Monitor activation funnel and support volume | PM + Support |
| Day 3-5 | First customer success stories and social proof | CS + Marketing |
| Day 5 | Launch week retrospective | PM |

### Post-Launch (4-8 weeks after GA)

| Week | Action | Owner |
|---|---|---|
| W+1 | Activation funnel analysis and quick fixes | PM + Engineering |
| W+2 | First cohort retention analysis | PM + Analytics |
| W+3 | Win/loss analysis on first deals | PM + Sales |
| W+4 | Launch success metrics review vs. targets | PM |
| W+6 | Iteration plan based on launch learnings | PM |
| W+8 | Go/no-go on next segment expansion (Bowling Pin 2) | PM + Leadership |

## Step 8: Success Metrics

### Leading Indicators (track daily/weekly during launch)
| Metric | Target | Why It Matters |
|---|---|---|
| Signups / trials | [N] per day/week | Demand signal |
| Activation rate | [X%] | Product-market fit signal |
| Time-to-value | [N minutes/hours] | Onboarding quality |
| PQL generation rate | [N] per week | Sales pipeline quality |
| NPS from first 30-day cohort | [X] | Satisfaction signal |

### Lagging Indicators (track monthly/quarterly)
| Metric | Target | Why It Matters |
|---|---|---|
| MRR from launch cohort | [$X] | Revenue validation |
| D30 retention | [X%] | Product stickiness |
| Win rate vs. competitors | [X%] | Competitive positioning |
| CAC payback period | [N months] | Unit economics |
| NRR | [X%] | Expansion potential |

### Launch Risk Assessment

| Risk | Likelihood | Impact | Mitigation | Early Warning |
|---|---|---|---|---|
| Low activation rate | H/M/L | H/M/L | [Plan] | [Signal] |
| Support overwhelm | H/M/L | H/M/L | [Plan] | [Signal] |
| Competitive response | H/M/L | H/M/L | [Plan] | [Signal] |
| Pricing pushback | H/M/L | H/M/L | [Plan] | [Signal] |
| Technical scalability | H/M/L | H/M/L | [Plan] | [Signal] |

---

## Output Template

```
GO-TO-MARKET STRATEGY
Product/Feature: [Name]
Launch Stage: [Alpha / Beta / GA]
Target GA Date: [Date]

BEACHHEAD SEGMENT
[Specific description with bowling pin sequence]

ICP
[Full ICP table]

GTM MOTION
Primary: [PLG / Sales-Led / Marketing-Led / Partner-Led / ABM / Hybrid]
Supporting: [Secondary motions]
Rationale: [Why this motion fits product, economics, and buyer]

LAND AND EXPAND
Landing play: [Specific use case / team / department]
Expansion triggers: [Signals and actions]
NRR target: [X%]

MESSAGING
Problem: [One sentence]
Solution: [One sentence]
Proof: [One specific evidence item]
CTA: [Primary call to action]

LAUNCH PLAN
[Pre-launch / Launch week / Post-launch tables]

SUCCESS METRICS
[Leading and lagging indicator tables with targets]

TOP RISKS
[Risk table with mitigation and early warnings]

BOWLING PIN EXPANSION PLAN
Pin 1: [Beachhead] -- Timeline: [X months to dominate]
Pin 2: [Next segment] -- Trigger: [What signals readiness]
Pin 3: [Next segment] -- Trigger: [What signals readiness]
```
