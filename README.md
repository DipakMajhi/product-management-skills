# Product Management Skills for Claude

82 expert skills for product managers — covering the full PM lifecycle from strategy and discovery through execution, growth, analytics, design, career development, and legal.

Each skill contains named frameworks with attribution, worked examples, anti-patterns, and structured output templates. Skills range from 150 to 800+ lines of expert-level content.

Compatible with **Claude Code** (CLI) and **Claude.ai** (desktop).

Built by [Dipak Majhi](https://mypminterview.com) for practicing PMs, PM interview candidates, and founders.

---

## What This Does

When you install this plugin, Claude gains deep PM expertise through structured skills. Instead of getting a generic response, Claude follows proven methodologies, asks the right clarifying questions, applies the appropriate framework to your context, and delivers structured outputs you can use directly with your team.

**Without the plugin:**
```
You: Help me prioritize my backlog.
Claude: Here are some ways to prioritize your backlog: 1. Consider business value...
```

**With the plugin:**
```
You: /prioritize
Claude: I'll help you prioritize your backlog. Before I apply a framework, a few questions:

1. How many items are we prioritizing? (10, 50, 200+?)
2. What's the primary decision you're trying to make — what to build next sprint,
   what to cut from a release, or how to allocate a quarter?
3. Do you have quantitative data (user counts, revenue impact) or are we working
   from qualitative judgment?
4. Who are the stakeholders who need to buy in to this ranking?

Based on your answers, I'll apply the right framework — RICE for stakeholder-ready
scoring, WSJF if time-sensitivity matters, MoSCoW for release scoping, or Opportunity
Solution Trees if you're still in discovery.
```

---

## Installation

### Claude Code (CLI)

```bash
claude plugin marketplace add DipakMajhi/product-management-skills
claude plugin install pm-skills@product-management-skills
```

### Claude.ai (Desktop)

1. [Download the ZIP](https://github.com/DipakMajhi/product-management-skills/archive/refs/heads/main.zip)
2. Open Claude.ai → **Customize** → **+** beside **Personal Plugins**
3. Upload the ZIP

### Other AI Assistants

```bash
# Cursor (project-level)
mkdir -p .cursor/skills/ && cp -r skills/* .cursor/skills/

# Gemini CLI
cp -r skills/* ~/.gemini/skills/ 2>/dev/null
```

---

## How to Use

### Slash commands

Type `/skill-name` and Claude invokes the right skill:

```
/write-prd in-app collaboration for a project management tool
/strategy AI writing assistant for non-native English speakers
/prioritize RICE scoring for our Q3 backlog
/pricing B2B developer tools platform, usage-based model
```

### Natural language

Describe what you need — Claude matches the skill automatically:

```
Help me run a discovery sprint for our onboarding problem.
I need to write OKRs for next quarter focused on retention.
Can you help me prep for a Google PM interview?
```

### Chaining skills

Skills are designed to hand off to each other. Claude suggests the next skill at the end of each output:

```
/discover → maps opportunity tree, suggests /interview to validate top opportunity
/interview → designs research plan, suggests /write-prd once insights are ready
/write-prd → writes full PRD, suggests /write-stories to break it into sprint tickets
/write-stories → generates user stories, suggests /sprint-plan to slot them in
```

---

## Example Interactions

### Writing a PRD

```
You: /write-prd guest checkout for our e-commerce platform

Claude: I'll write this PRD. A few things to confirm first:

- Target user: Occasional buyers who don't want to create an account?
- Success metric: What's the current cart abandonment rate at the account creation step?
- Constraint: Do we have a deadline tied to a seasonal campaign?
- Scope: Mobile web only, or also native apps?

[After you answer...]

---
PRD: Guest Checkout
Version 1.0 | Status: Draft

**Executive Summary**
Guest checkout removes the forced account creation step that currently causes 34% of
users to abandon at the registration screen. We will allow users to complete a purchase
with only an email address, reducing friction for first-time buyers and recovering an
estimated $2.1M in annual revenue from abandoned carts.

**Problem Statement**
Based on funnel analysis (Mixpanel, Q2), 34% of users who add to cart abandon at the
account creation step — the highest single drop-off point in the purchase funnel...

[Continues with all 12 sections: user stories, success metrics, requirements,
edge cases, out-of-scope, phasing, launch checklist, and open questions]
---

Next: Use /write-stories to break this PRD into sprint-ready user stories.
```

---

### Prioritizing a backlog with RICE

```
You: /prioritize here's our Q3 backlog:
- Guest checkout
- Bulk CSV import
- Mobile push notifications
- Dark mode
- Team permission roles
- Improved search

Claude: I'll apply RICE scoring. Let me ask a few calibration questions to make
the scoring defensible to stakeholders...

[After gathering context]

| Feature | Reach | Impact | Confidence | Effort | RICE Score |
|---|---|---|---|---|---|
| Guest checkout | 2400 | 2 | 80% | 2 | 1920 |
| Team permissions | 800 | 3 | 80% | 3 | 640 |
| Mobile push | 3200 | 1 | 50% | 4 | 400 |
| Bulk CSV import | 400 | 2 | 80% | 1 | 640 |
| Improved search | 4000 | 0.5 | 80% | 2 | 800 |
| Dark mode | 4000 | 0.25 | 100% | 1 | 1000 |

**Counterintuitive result**: Dark mode ranks #2 purely on RICE, but this is a
satisfaction feature (Kano: expected), not a growth driver. Recommend treating it
as a low-effort addition to a sprint with capacity, not a headlining feature.

**Recommended Q3 sequence**: Guest checkout → Search → Bulk CSV → Team permissions

Next: Use /discover to run a full discovery sprint on guest checkout before building.
```

---

### Running a discovery sprint

```
You: /discover we want to improve activation for new B2B users

Claude: I'll guide you through a full discovery cycle using Teresa Torres'
Opportunity Solution Trees.

**Step 1: Define your desired outcome**
Before mapping opportunities, let's anchor to a measurable outcome.

- What does "activation" mean for your product? (e.g., "user completes their
  first core action within 7 days of signup")
- What's the current activation rate?
- What team outcome are you working toward this quarter?

[After you answer...]

**Step 2: Opportunity Map**
Based on your interviews and data, here are the opportunities I'd map:

Outcome: Increase 7-day activation from 22% → 40%

├── Opportunity 1: Users don't understand what to do first (confusion)
│   ├── Sub-opportunity: No clear starting point in empty state
│   └── Sub-opportunity: Jargon in onboarding flow doesn't match user's mental model
├── Opportunity 2: Users can't import their existing data (friction)
│   └── Sub-opportunity: CSV import requires IT involvement
└── Opportunity 3: Value isn't demonstrated before first action required (trust)
    └── Sub-opportunity: No sample data or guided demo mode

**Step 3: Opportunity to focus on**
Opportunity 1 (confusion) affects 67% of churned users in exit interviews.
I recommend this as your focus area.

**Step 4: Assumption mapping for top solution candidate**...

Next: Use /interview to design your next round of customer interviews on this opportunity.
```

---

### Interview prep (PM interviews)

```
You: /interview-prep I have a Google L5 PM interview next week

Claude: I'll coach you for a Google L5 interview. Google's process typically includes:
- 4-5 rounds: Product Design, Analytical, Strategy, Execution, and sometimes
  Leadership/Behavioural
- They evaluate on: data-driven decision making, user empathy, structure, and
  cross-functional leadership at scale

**Let's start with Product Design.**

Walk me through how you'd improve Google Maps.

[You answer...]

**Feedback on your answer:**

Structure: You opened with users — good. But you skipped the "why Maps" strategic
context Google expects at L5. Add one sentence on Maps' role in Google's ecosystem
before diving into users.

Depth: You identified 3 user segments but treated them equally. At L5, interviewers
expect you to justify which segment you're optimizing for and why.

Framework: You used a solid design framework but missed accessibility as a segment —
Google specifically probes for this.

Revised opening they'd want to hear: "Maps is Google's primary gateway to the
physical world and a key driver of local ad revenue. To improve it, I'd focus on
[segment] because they represent [metric/strategic reason]..."

**Score: 3.5/5** — strong structure, needs more strategic framing. Let's run it again.
```

---

## Skills Reference

### Strategy (8 skills)

| Skill | Command | What It Does |
|---|---|---|
| product-strategy-canvas | `/strategy` | Build a complete strategy canvas using Playing to Win, Good Strategy Bad Strategy, and Rumelt's kernel |
| product-vision | `/vision` | Craft a product vision using narrative, Press Release/FAQ, and one-sentence formats |
| competitive-intelligence | `/competitive-scan`, `/profile-competitor`, `/battlecard` | Full competitive suite: landscape mapping, deep competitor profiling, and sales battlecards |
| business-model | `/business-model` | Design or stress-test a business model with BMC, Lean Canvas, and unit economics |
| pricing-strategy | `/pricing` | Build pricing strategy using value-based, competition-based, and cost-plus models |
| market-sizing | `/market-size` | Estimate TAM, SAM, and SOM using top-down, bottom-up, and Fermi techniques |
| strategic-frameworks | `/frameworks` | Apply 12 frameworks: SWOT/TOWS, PESTLE, Porter's Five Forces, Ansoff Matrix, and more |
| value-proposition | `/value-prop` | Define value proposition using JTBD, Strategyzer Canvas, and April Dunford's methodology |

### Discovery (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| continuous-discovery | `/discover` | Run discovery using Teresa Torres' Opportunity Solution Trees and Marty Cagan's dual-track |
| assumption-testing | `/brainstorm` | Map, score, and design pretotype tests for product assumptions |
| prioritization | `/prioritize` | Score and rank with RICE, ICE, MoSCoW, Kano, WSJF, and Eisenhower frameworks |

### User Research (2 skills)

| Skill | Command | What It Does |
|---|---|---|
| user-research | `/interview`, `/research-users`, `/journey-map` | Complete research suite: interview design, contextual inquiry, JTBD extraction, persona building, journey mapping |
| voice-of-customer | `/triage-requests`, `/analyze-feedback` | Sentiment classification, theme extraction, JTBD mapping, feature request triage, and opportunity scoring |

### Data and Analytics (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| sql-for-pms | `/write-query` | Generate SQL for 25+ PM query patterns across BigQuery, PostgreSQL, MySQL, and Snowflake |
| ab-testing | `/analyze-test` | Design experiments, calculate sample size, and interpret results with Ship/Iterate/Stop framework |
| metrics-and-okrs | `/define-metrics`, `/plan-okrs`, `/north-star`, `/analyze-cohorts` | North Star definition, HEART/AARRR frameworks, metric trees, OKR writing with Doerr methodology |

### Marketing and Growth (4 skills)

| Skill | Command | What It Does |
|---|---|---|
| positioning | `/market-product` | Product positioning using Geoffrey Moore template and Al Ries/Jack Trout laws |
| growth-loops | `/growth-strategy` | Design growth loops using Reforge methodology, Andrew Chen, and Casey Winters frameworks |
| gtm-strategy | `/plan-launch` | Complete go-to-market strategy with beachhead selection (Geoffrey Moore) and launch planning |
| icp-builder | `/define-icp` | Define Ideal Customer Profile with scoring methodology, data sources, and ABM integration |

### Execution (6 skills)

| Skill | Command | What It Does |
|---|---|---|
| prd-writer | `/write-prd` | Write comprehensive 8-section PRDs with problem statements, user stories, and success metrics |
| roadmap-builder | `/roadmap` | Build roadmaps using Now/Next/Later (Janna Bastow), outcome-driven, and theme-based formats |
| user-stories | `/write-stories` | Write stories with INVEST criteria, Jeff Patton story mapping, and BDD acceptance criteria |
| sprint-lifecycle | `/sprint-plan`, `/retro` | Complete sprint toolkit: planning, capacity estimation, retrospectives, and release notes |
| stakeholder-management | `/stakeholder-map` | Map stakeholders with Mendelow's Power/Interest grid and design communication plans |
| okr-planner | `/plan-okrs` | Write OKRs using John Doerr's methodology with CFR cadence |

### Improvement (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| retention-toolkit | `/improve-retention`, `/analyze-cohorts` | Retention diagnosis, cohort analysis, activation moment identification, and intervention design |
| funnel-optimization | `/optimize-funnel` | Diagnose and optimize acquisition, onboarding, activation, and checkout funnels |
| product-iteration | `/iterate`, `/improve-product` | Structured iteration using Build-Measure-Learn, PDCA/Deming cycle, and hypothesis-driven development |

### Design (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| design-thinking | `/design-sprint` | Apply IDEO 5-stage model, Stanford d.school methodology, and British Design Council Double Diamond |
| ux-critique | `/critique-design` | Evaluate UX using Nielsen's heuristics, Don Norman's principles, and cognitive load theory |
| design-brief | `/write-brief` | Write design briefs with JTBD integration, constraint documentation, and collaboration models |

### Career and Interview Prep (5 skills)

| Skill | Command | What It Does |
|---|---|---|
| interview-prep-coach | `/interview-prep` | PM interview coaching with CIRCLES method, company-specific patterns (Google, Meta, Amazon), and scoring rubrics |
| pm-career-ladder | `/career-growth`, `/career-check` | Career progression with IC vs Management tracks, company ladder mappings, and promotion planning |
| review-resume | `/review-resume` | Score and review PM resumes with XYZ formula, ATS optimization, and level-specific feedback |
| tailor-resume | `/tailor-resume` | Tailor resumes to job descriptions with JD decoding, mirror language, and ATS keyword strategy |
| grammar-check | `/proofread` | Proofread PM writing with BLUF pattern, Minto Pyramid, and document-type-specific guidelines |

### Legal (2 skills)

| Skill | Command | What It Does |
|---|---|---|
| draft-nda | `/draft-nda` | Draft NDAs with clause-by-clause guidance, carve-outs, remedies, and complete templates |
| privacy-policy | `/draft-privacy-policy` | Draft privacy policies covering GDPR, CCPA/CPRA, COPPA, LGPD, PIPEDA, and Privacy by Design |

---

## Quick Start Workflows

**Preparing for a PM interview:**
```
/interview-prep
/improve-product Spotify
/strategy AI writing assistant for non-native English speakers
```

**Starting a new product:**
```
/strategy → /discover → /write-prd → /plan-launch
```

**Improving an existing product:**
```
/analyze-feedback → /improve-retention → /optimize-funnel → /iterate
```

**Setting up metrics and goals:**
```
/north-star → /define-metrics → /plan-okrs
```

**Competitive intelligence sprint:**
```
/competitive-scan → /profile-competitor Notion → /battlecard
```

**Running a sprint:**
```
/write-stories → /sprint-plan → /retro
```

---

## Skill Quality Standard

Every skill follows a consistent quality bar:

- Named frameworks with proper attribution (Teresa Torres, Geoffrey Moore, Reforge, Nielsen, etc.)
- Tables comparing approaches with pros, cons, and when-to-use guidance
- Worked examples with realistic numbers and scenarios
- Anti-patterns section documenting common mistakes and why they fail
- Structured output templates ready for stakeholder delivery
- 150 to 800+ lines of expert-level content per skill

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Contributions welcome — new skills, improved frameworks, additional examples.

## License

MIT
