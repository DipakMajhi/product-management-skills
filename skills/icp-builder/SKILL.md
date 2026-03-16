---
name: icp-builder
description: "Define an Ideal Customer Profile (ICP) for a B2B product. Use this skill when someone needs to define who their perfect customer is, create an ICP for sales and marketing alignment, build a target account list framework, or understand what firmographic and behavioral signals indicate a high-fit prospect."
argument-hint: "product/company name, current customer list, or target market description"
---

# ICP Builder

An Ideal Customer Profile defines the characteristics of customers who will get the most value from your product, buy most quickly, stay longest, and provide the best references. ICP is the foundation for GTM strategy, account-based marketing, sales efficiency, and product roadmap prioritization.

Apply this skill to: $ARGUMENTS

## Why ICP Matters

Without a clear ICP:
- Sales pursues deals that close fast but churn quickly (bad unit economics)
- Marketing generates volume but low-quality leads (wastes budget)
- Product builds for too many use cases (loses focus and velocity)
- Customer success spends disproportionate time on bad-fit accounts (reduces efficiency)
- Company cannot scale because low-fit customers create high support burden

With clear ICP:
- Sales focuses on accounts most likely to close and stay, improving efficiency
- Marketing targets high-intent prospects, improving conversion rates
- Product roadmap aligns with customers who matter most
- CS can predict churn and allocate resources proactively
- Company grows efficiently with high retention and expansion revenue

## ICP Dimensions Framework

### Firmographic (Company-Level Characteristics)

These describe the type of company you target. They are relatively static (less frequently change):

- **Industry / vertical**: Specific industries where product delivers most value (e.g., B2B SaaS, Fintech, Healthcare Tech, not "all industries")
- **Company size** (by employee count or ARR): Where product delivers best ROI and fits processes (e.g., Series A-C startups 20-300 people, not SMBs or enterprises unless that is your sweet spot)
- **Funding stage**: Seed, Series A-C, Series D+, Growth-stage private, Public, Bootstrapped (affects budget availability and buying process)
- **Geographic market**: Where you have support, legal compliance, language coverage (e.g., US/Canada English market, not APAC if you lack support)
- **Revenue range**: Annual revenue that indicates ability to pay and organizational maturity (e.g., $10M-$100M ARR)
- **Tech stack signals**: Integration dependencies or required compatibility (e.g., uses Salesforce, Zendesk, AWS, not on-premises legacy systems)
- **Growth rate signal**: High-growth companies (>40% YoY) have different needs than stable/mature companies

### Situational (Trigger Events and Context)

These describe what is happening at the company that creates urgency:

- **Trigger events that create urgency**:
  - Rapid headcount growth (hiring new team, scaling process, need for infrastructure)
  - Recent funding round (capital to spend, mandate to show results)
  - Regulatory change (compliance requirement creates need)
  - Competitive disruption (market shift forces adaptation)
  - Leadership change (new CTO/CMO brings new priorities and budget)
  - Failed alternative (just tried competitor, or internal tool; open to new solution)
  - Department reorganization or new role creation (rebuilding function)

- **Problem maturity**:
  - Are they aware of the problem? (Have they named it? Are they frustrated enough to act?)
  - Are they actively searching for a solution? (Searching on Google, looking at competitors?)
  - Have they allocated budget? (Or is this "nice to have" with no money behind it?)
  - Actively searching + budget allocated = 10x faster sales cycle than problem awareness only

### Persona (Individual Buyer and User Roles)

Different people play different roles in the buying and using process:

| Role | Definition | What They Care About | How to Appeal |
|---|---|---|---|
| Economic Buyer | Signs the contract; approves budget | ROI, risk mitigation, vendor reliability | Show business metrics: revenue impact, cost savings, churn reduction |
| Champion | Internal advocate for your product; pushes for adoption | Personal success, making their job easier, career advancement | Empower them with collateral to convince their peers |
| Decision-Maker | Has veto power but not necessarily budget control | Process, risk, organizational fit, team consensus | Emphasize processes you support and teams you integrate with |
| End User | Uses your product day-to-day | Usability, time-to-value, integration with current workflow | Emphasize ease of use, support, training |
| Influencer | Not the buyer but influences the decision | Technical feasibility, integration, data security | Technical depth, integration documentation, security certifications |

**Persona template (for each key role):**
- Title: [Role name at company]
- Industry context: [Where they typically work: finance, ops, eng, etc.]
- Goals: [What success looks like for them in their role - "increase customer retention", "reduce time to close", "improve team visibility"]
- Pain: [What specifically frustrates them about current state]
- Objections: [What would prevent them from recommending you]
- Why they advocate for you: [What personal win do they get from you succeeding?]

### Behavioral (Signals of Fit)

Observable product behaviors that indicate a customer is high-fit:

**Product-led signals (if you have a freemium tier or trial):**
- Signed up and completed onboarding (reached activation milestone)
- Used more than one core feature in first week (not just one feature, actually exploring)
- Invited team members within first 7 days (indicates champion potential)
- Connected to an integration (reducing friction of adoption)
- Returned to the product 4+ times in first 30 days (habit formation starting)
- Created/configured something persistent (not just exploring; building with your tool)

**Sales signals (for enterprise deals):**
- Took a product demo
- Spent 20+ minutes in the demo talking about their specific use case
- Introduced other stakeholders to the process (championing internally)
- Asked about pricing and contract terms (seriously considering purchase)
- Started a pilot or trial with a real use case (not theoretical)

**Post-sale signals (predicting good fit):**
- Completed onboarding activities with <5% drop-off
- Adoption rate (% of intended users activated) >70% within first 30 days
- Using multiple features, not just one (risk: single-feature churn risk)
- Expanding to additional departments or team members within 3-6 months
- Responding to check-ins and feedback surveys (engaged customer)

## Negative ICP (Exclusion Criteria)

Equally important: define who you should NOT pursue. Negative ICP predicts churn, low engagement, or high support cost.

**Define the characteristics that disqualify a prospect:**

- **Company too small**: Cannot afford your product relative to their budget (e.g., <$1M ARR is too small for $10k/month SaaS)
- **Company too large**: Requires enterprise features you do not have (e.g., >$1B ARR wants SOC2, single sign-on, dedicated support - if you cannot provide, do not sell)
- **Industry with regulatory constraints**: You lack compliance certifications needed (e.g., Healthcare without HIPAA, Finance without SOC2)
- **Use case that requires significant customization**: Your product philosophy is SaaS (no custom code); if they want customization, churn risk is high
- **Already invested in competitor**: Even if competitor is suboptimal, switching costs and organizational inertia are too high
- **Cannot articulate their problem**: If they cannot describe what they are trying to solve, they are not ready to buy
- **Budget controlled by person not in conversation**: If decision-maker is not in early discussions, deal will stall during procurement
- **Competing priority**: Department is being reorganized, cut, or deprioritized; your product will get defunded

## ICP Evolution Stages

Your ICP should evolve as your product matures. Do not lock it in stone:

| Stage | ICP Characteristics | How to Refine | Goal |
|---|---|---|---|
| Hypothesis (Pre-PMF) | Best guess based on founder intuition and initial customer feedback | Talk to 20-30 potential customers; validate they have urgent problem and budget | Validate problem, not yet refining ICP |
| Early Traction (10-50 customers) | Analyze first 10-20 actual customers: who bought fastest, stayed longest, expanded most? | Cohort analysis: compare early customers to later cohorts; identify patterns in best ones | Find customer DNA: common attributes of your best customers |
| Product-Market Fit (50-200 customers) | Clear pattern emerges: specific industry/role/company size shows 4x better retention | Segment revenue by firmographic/behavioral dimensions; see which cohort has best LTV | Concentrate GTM on best-fit segment; consider narrowing positioning |
| Scale (200+ customers) | ICP narrows as unit economics data becomes clear; some segments more profitable than others | Monthly metrics: LTV, churn, expansion revenue by segment; compare top 20% to bottom 20% | Defend ICP boundaries: drop low-fit customers from marketing, redeploy to high-fit |

## ICP Alignment with GTM Motion

Your GTM strategy should match your ICP. Misalignment creates friction and inefficiency:

| GTM Motion | ICP Characteristics Required | Why It Matters |
|---|---|---|
| Product-led (self-serve freemium) | ICP must have: low-friction, self-service decision-making; small deal size; distributed buying (not budget committee) | If your ICP is enterprise with long sales cycles, product-led GTM will fail |
| Sales-led (direct sales) | ICP must have: concentrated buying process; budget-aware; long sales cycles acceptable; decision committee | If your ICP is SMBs wanting instant decisions, sales-led will be too slow |
| Channel-led (resellers, partners) | ICP must have: integration points with partner ecosystem; value from bundling | If your ICP is disaggregated use case, channel model will not work |
| Community/community-led | ICP must have: technical or enthusiast buyer; willing to evangelize; peer-driven adoption | If ICP is risk-averse enterprises, community-led will fail |

## Account-Based Marketing (ABM) Integration

If pursuing ABM (target 50-200 high-value accounts with personalized campaigns):

**Account selection criteria should align with ICP:**
1. **Tier 1 (strategic accounts)**: Top 10-20 accounts that, if won, would validate market and create referenceable case study (e.g., top companies in target industry)
2. **Tier 2 (core accounts)**: Next 50-100 accounts matching ICP most precisely (high close probability + good fit)
3. **Tier 3 (opportunistic accounts)**: Remaining prospects matching some (not all) ICP criteria; pursue only if they inbound

**ABM requires alignment:**
- Sales team owns accounts, not leads
- Marketing produces account-specific campaigns (not one-size-fits-all nurtures)
- Product involvement in earlier sales cycle (not demos only at end)

## Customer Segmentation Frameworks

After ICP is defined, segment customers for different strategies:

### Value-Based Segmentation (What Customer Is Worth)

| Segment | LTV | Strategy |
|---|---|---|
| High-value (LTV >$100k) | Accounts to defend fiercely | Account-based customer success; executive sponsorship |
| Mid-value (LTV $20-100k) | Core segment | Standard CS; nurture for expansion |
| Low-value (LTV <$20k) | Cost of serving must be low | Self-service CS; automate everything possible |

### Needs-Based Segmentation (What Problem They Solve For)

- **Operations segment**: Cares about efficiency, integration, automation
- **Data/Analytics segment**: Cares about insights, visualization, accuracy
- **Strategy segment**: Cares about insights enabling planning and forecasting

(Different messaging, positioning, and product emphasis for each)

### Behavior-Based Segmentation (How They Use Product)

- **Power users**: Use 8+ features; multiple team members; high engagement
- **Standard users**: Use 3-5 core features; single team usage
- **light users**: Use 1-2 features; low engagement risk

(Different onboarding, success metrics, and intervention strategies for each)

## ICP Documentation for Cross-Functional Teams

Different teams need different ICP details:

**What Sales Needs:**
- Firmographic targeting (company size, industry, stage, geography)
- Trigger events and buying signals
- Buyer persona details (titles, objectives, objections)
- Deal size and typical sales cycle length
- Account list criteria for prospecting

**What Marketing Needs:**
- Target segment description (who are you talking to?)
- Problem statement (what keeps them up at night?)
- Key differentiator vs competing alternatives
- Messaging angles by persona
- Campaign metrics (target CAC, ideal conversion rate by stage)

**What Product Needs:**
- Core use cases (what problems are you solving for which roles?)
- Personas and their workflows
- Feature priorities by segment (if ICP has multiple segments, prioritize accordingly)
- Churn risk signals (behavioral indicators of at-risk customers)
- Expansion opportunities (what adjacent use cases or features expand within ICP?)

**What Customer Success Needs:**
- Positive and negative behavioral signals (what indicates customer is thriving vs at-risk?)
- Onboarding milestones (what is "success" at each stage for ICP customers?)
- Expansion playbooks (how to identify and execute expansion opportunities?)
- Churn indicators (early warning signs of churn risk)
- Segment-specific goals (what does success look like for each segment?)

## ICP Scoring Methodology

Once ICP is defined, score prospects to predict fit and prioritize sales efforts.

**Weighted scoring matrix:**

| Firmographic Criterion | Weight | Scoring |
|---|---|---|
| Industry match | 25% | Exact match = 100 pts, Adjacent = 50 pts, Unrelated = 0 pts |
| Company size | 25% | In range = 100 pts, Slightly out = 50 pts, Way out = 0 pts |
| Funding stage | 15% | In stage = 100 pts, Adjacent = 50 pts, Out = 0 pts |
| Trigger event present | 20% | Recent trigger = 100 pts, Potential trigger = 50 pts, None = 0 pts |
| Budget available | 15% | Budget allocated = 100 pts, Exploring = 50 pts, No budget = 0 pts |

**Total score:** Sum (criterion score x weight). Accounts scoring >75 are high-ICP-fit and should get immediate sales attention. Accounts scoring 50-75 are possible but lower priority. <50 should not be pursued.

## Data Sources for ICP Validation

Where to find signals to validate and refine ICP:

| Data Source | What It Tells You | Cost |
|---|---|---|
| Your existing customer database | Who actually bought (cohort analysis on best customers) | Free |
| Customer interviews (20-30 customers) | What problems they solved, why they bought, what triggers they experienced | Time only |
| Industry reports (Gartner, CB Insights, etc.) | Market size, growth by segment, typical buyer priorities | $1-5k per report |
| LinkedIn Sales Navigator | Ability to search and filter by company, title, industry, job changes | $60/month |
| Company enrichment tools (Apollo, Hunter, RocketReach) | Verify company data, find buyer contact info, see common titles | $200-500/month per user |
| Sales engagement platforms (HubSpot, Outreach) | Track buyer engagement signals, time-to-response, email open rates | Built in to platform |
| Firmographic databases (ZoomInfo, D&B Hoovers) | Verify company details, find decision-makers, see spending signals | $1-10k/month |
| Your product analytics | Behavioral signals: who uses what features, time-to-value, expansion patterns | Free if you have instrumentation |
| Your support/CS system | Who has high support cost, who has quick onboarding, who expands vs churns | Free if you have ticketing system |

## Anti-Patterns in ICP Definition

| Anti-Pattern | Why It Fails | Example |
|---|---|---|
| ICP too broad | "All B2B SaaS companies" does not narrow anything; GTM will be unfocused | Sales spends time on many mediocre leads instead of prioritizing best-fit accounts |
| ICP too narrow | Excludes adjacent segments that would love your product; limits addressable market | "Only Series B SaaS founded in 2018 in SF" excludes entire segments with high LTV |
| ICP based on competitor, not actual customers | Assumes competitors have it right; they may have wrong ICP too | Define ICP based on your existing best customers, not your competitor's positioning |
| ICP ignores negative characteristics | Spend time on prospects you should avoid | Never define negative ICP; then pursue every $100k company only to find 80% churn at >$10B scale |
| ICP defined but not enforced | Sales pursues deals outside ICP because commission is commission | ICP becomes aspiration; actual GTM stays unfocused. Sales quota must align with ICP |
| ICP never evolves | Defined once, forgotten, company scales into different segment | Company's best customers are now different than original ICP; GTM misaligned with actual strength |

## Output Template

---
**IDEAL CUSTOMER PROFILE**

**Product:** [Name]
**Version:** [1.0, date]
**Last Updated:** [Date]

**Firmographic Profile (Positive ICP)**
| Dimension | Ideal Range | Strong Signal | Weak Signal | Exclusion Criteria |
|---|---|---|---|---|
| Industry | [List 2-3 priority verticals] | [Most ideal specific sub-verticals] | [Adjacent but lower priority] | [Industries to avoid] |
| Company Size | [Range, e.g., 50-500 employees or $5-50M ARR] | [Sweet spot] | [Borderline acceptable] | [Too small or too large] |
| Funding Stage | [Stage(s), e.g., Series A-C] | [Most common in best customers] | [Less common but possible] | [Stage to avoid] |
| Geography | [Markets where you operate] | [Primary market] | [Secondary market] | [Out of scope] |
| Tech Stack | [Tools they likely use] | [Integration priorities] | | |
| Growth Rate | [Indicator, e.g., >40% YoY] | [Best fit threshold] | | |

**Firmographic Scoring (for prospect qualification)**
| Criterion | Weight | Scoring Logic |
|---|---|---|
| [Dimension] | [X%] | [How you score: 0-100 points] |

**Trigger Events** (What indicates this company is actively looking?)
1. [Event]: [How you detect it] - [Where to find signal]
2. ...

**Economic Buyer Persona**
Title: [e.g., VP Marketing, CFO]
Goals: [What success looks like for them]
Pain: [Current frustration point]
Cares about: [Business metrics: ROI, risk reduction, vendor reliability]
Objection likely: [What would prevent them from sponsoring purchase]
How to appeal: [What messaging/data moves them]

**Champion Persona** (Internal advocate)
Title: [e.g., Product Manager, Team Lead]
Goals: [Personal win]
Pain: [What your product solves for them]
Why they advocate for you: [How you make them successful]
What you need to provide: [Collateral, training, support]

**End User Persona** (Primary daily user)
Title: [e.g., Marketing Manager, Data Analyst]
Cares about: [Usability, time-to-value, integration]
Pain with current solution: [What frustrated them before you]

**Negative ICP** (Do not pursue if...)
- [Disqualifying firmographic, e.g., private equity-owned with legacy systems]
- [Disqualifying use case, e.g., requires customization we do not do]
- [Disqualifying signal, e.g., evaluating 4+ competitors (long sales cycle)])

**Behavioral Signals of High Fit**
Product-led (if applicable):
- [Observable behavior 1]: [Why it predicts success]
- [Observable behavior 2]

Sales-led:
- [Buying signal 1]: [Why it predicts success]
- [Buying signal 2]

Post-sale:
- [Engagement signal 1]: [Why it predicts retention]
- [Engagement signal 2]

**Customer Segmentation** (if ICP contains multiple segments)
| Segment | Definition | GTM Strategy | Messaging Angle |
|---|---|---|---|
| [Segment 1] | [Characteristics] | [How you win them] | [Key message] |

**ICP Validation Status**
Based on: [Existing customers analyzed / Hypothetical research / Mix]
Confidence level: [High / Medium / Low]
Sample size: [# of customers analyzed]
Key validation finding: [Most interesting insight from customer analysis]
Next validation step: [What you will do to improve confidence]

---
