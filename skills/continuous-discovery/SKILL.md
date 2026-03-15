---
name: continuous-discovery
description: "Guide a PM through continuous discovery using Teresa Torres' Continuous Discovery Habits, Marty Cagan's product discovery, Dual-Track Agile, and Opportunity Solution Trees. Covers weekly interview cadence, experience mapping and interview synthesis, opportunity scoring, atomic research nuggets (Tomer Sharon), research repositories, discovery-to-OKR connection, discovery cadence metrics, Product Trio collaboration, story mapping integration, discovery anti-patterns and failure modes, and outcome-based discovery. Use when running discovery, building an Opportunity Solution Tree, adopting continuous discovery habits, connecting discovery to delivery, or answering PM interview questions about discovery practices."
argument-hint: "[describe the product outcome you are pursuing, your current discovery practices (if any), your team composition, and what aspect of discovery you want to improve]"
---

# Continuous Discovery Guide

Continuous discovery is the ongoing practice of making small research touchpoints with customers each week to inform product decisions. Discovery is not a phase -- it is a weekly cadence embedded in how the team works.

Apply this skill to: $ARGUMENTS

## Step 1: Establish the Discovery Mindset

### Discovery Is Not a Phase

| Mindset | Feature Factory | Continuous Discovery |
|---|---|---|
| Decisions based on | Stakeholder requests, roadmap commitments | Customer evidence, validated assumptions |
| Customer contact | Quarterly research projects | Weekly touchpoints by the building team |
| Success measured by | Features shipped, velocity | Outcomes achieved, assumptions validated |
| Failure response | Ship more features | Learn faster, pivot earlier |
| Who does discovery | Dedicated research team | Product Trio (PM, Designer, Engineer) |

### The Product Trio

Discovery is most effective when three roles collaborate:

| Role | Discovery Contribution | Why They Must Participate |
|---|---|---|
| Product Manager | Connects opportunities to business outcomes, prioritizes | Ensures discovery serves strategy |
| Designer | Designs interview protocols, synthesizes behavioral patterns | Catches usability risks early |
| Engineer | Identifies feasibility constraints, suggests technical experiments | Prevents infeasible solutions from advancing |

All three should attend customer interviews together. When the building team hears directly from customers, shared understanding forms faster and handoff friction drops.

---

## Step 2: The Core Discovery Loop

The continuous discovery cadence runs weekly:

1. **Interview** at least one customer per week (30-minute sessions)
2. **Synthesize** insights using Interview Snapshots and Experience Maps
3. **Map** opportunities on the Opportunity Solution Tree
4. **Identify** assumptions behind the most promising solutions
5. **Design** the smallest experiment to test the riskiest assumption
6. **Learn** and update the OST based on results
7. Repeat

### Weekly Interview Cadence

| Element | Recommendation |
|---|---|
| Frequency | Minimum 1 per week; aim for 3-5 conversations |
| Duration | 30 minutes per session |
| Participants | Product Trio attends together |
| Recruitment | Automate recruitment (in-product intercepts, customer panel, CSM referrals) |
| Focus | Current behaviors and pain points, not feature wishlists |
| Format | Story-based interviews exploring specific recent experiences |

**Why weekly matters**: Monthly intervals mean the team goes an entire month making decisions without validating assumptions about customer reality. Weekly touchpoints keep teams calibrated.

**Recruitment automation**: The biggest barrier to continuous interviews is recruiting. Solve this by building an always-on recruitment channel: in-app prompts offering incentives, a standing panel of willing participants, or automated scheduling through CSM introductions.

---

## Step 3: The Opportunity Solution Tree (OST)

The OST is a visual map connecting business outcomes to customer opportunities to solutions to experiments.

```
Desired Outcome (measurable business goal the team owns)
    |
    Opportunities (unmet user needs, pain points, desires)
        |
        Solutions (product ideas that address a specific opportunity)
            |
            Experiments (tests to validate the solution before building)
```

### Level 1: Desired Outcome

One specific, measurable business outcome the team is responsible for. Not "improve engagement" but "increase weekly active users who complete at least 3 core actions from 34% to 45% by Q3."

**Quality test**: Can the team influence this outcome through product changes? Is it measurable within the team's sprint cadence?

### Level 2: Opportunities

Customer needs, pain points, and desires discovered through interviews. Opportunities are stated in the customer's language, not in product terms.

| Good Opportunity Framing | Bad Opportunity Framing |
|---|---|
| "I lose track of what my team is working on when traveling" | "Add a mobile dashboard" (this is a solution) |
| "I waste 20 minutes every morning finding yesterday's context" | "Improve the homepage" (too vague) |
| "I am afraid of making a mistake that affects the whole team" | "Users need better permissions" (product language, not customer language) |

**Well-framed opportunity test**: Can you imagine multiple different solutions that would address this opportunity? If only one solution fits, the opportunity is too narrow.

### Level 3: Solutions

Multiple solution candidates for each opportunity. One opportunity should have at least 2-3 solutions to enable compare-and-contrast decisions rather than binary go/no-go.

### Level 4: Experiments

The smallest, cheapest test to validate the key assumption behind each solution. See the assumption-testing skill for detailed experiment design.

### OST Best Practices

- Write the desired outcome before mapping opportunities
- Opportunities must come from validated customer research, not assumptions
- Work on one small opportunity at a time (limit work in progress)
- Treat the OST as a living document that evolves with each interview
- When solutions fail, revisit the opportunity framing, not just the solution approach
- Share the OST visibly with the full team (wall poster, Miro board)

### OST Common Mistakes

| Mistake | Why It Fails | Fix |
|---|---|---|
| Outcome is a feature metric ("increase button clicks") | Not a business outcome; optimizes output, not impact | Reframe as user behavior or business result |
| Opportunities are actually solutions in disguise | Closes solution space prematurely | Apply the multiple-solutions test |
| Only one solution per opportunity | No compare-and-contrast; binary thinking | Generate at least 2-3 alternatives |
| OST never updated after experiments | Tree becomes stale, team stops trusting it | Update after every experiment and interview cycle |
| Opportunities based on assumptions, not interviews | Confirmation bias; building what you already believed | Trace every opportunity to a specific interview quote |

---

## Step 4: Interview Synthesis

### Interview Snapshots (Immediate Synthesis)

After each interview, the Product Trio creates a one-page Interview Snapshot within 15 minutes:

| Section | Content |
|---|---|
| Participant | Role, context, relevant background |
| Story summary | The specific experience they described (2-3 sentences) |
| Key quotes | 2-3 verbatim quotes that reveal needs or pain |
| Opportunities identified | New opportunities or evidence for existing ones |
| Surprises | Anything unexpected that challenges current assumptions |

**Critical rule**: Create snapshots immediately after the interview, not days later. Memory degrades rapidly.

### Experience Mapping (Cross-Interview Synthesis)

As patterns emerge across multiple interviews, build Current-State Experience Maps:

1. Map how customers accomplish goals today, step by step
2. Note pain points, workarounds, and emotional highs/lows at each step
3. Identify where multiple interviewees report similar friction
4. These recurring friction points become opportunities on the OST

### Atomic Research (Tomer Sharon)

Instead of storing insights in static reports, use atomic research nuggets:

| Component | Description |
|---|---|
| Nugget | A single experience insight about customer behavior or need |
| Evidence | Video clip (15-45 seconds), quote, or observation supporting the nugget |
| Tags | Procedural, demographic, experience-oriented, business-oriented, service-design tags |

**Benefits**: Creates a dynamic, searchable research repository. Anyone can create custom playlists of insights by topic. More reusable than slide decks or reports. Continuously updated and accessible across teams.

### Synthesis Techniques

| Technique | When to Use | How It Works |
|---|---|---|
| Affinity mapping | Early pattern identification | Group related observations visually by similarity |
| Thematic analysis | Deeper systematic analysis | Code observations, then cluster codes into themes |
| Experience mapping | Understanding end-to-end journeys | Map steps, pain points, emotions across the journey |
| Opportunity mapping | Connecting insights to the OST | Translate themes into customer-language opportunities |

---

## Step 5: Opportunity Scoring and Prioritization

### Opportunity Scoring Formula

Opportunity Score = Importance + (Importance - Satisfaction)

| Input | How to Measure |
|---|---|
| Importance | Ask customers to rate how important this need is (1-10 scale) |
| Satisfaction | Ask how satisfied they are with current solutions (1-10 scale) |
| Score interpretation | High importance + low satisfaction = highest opportunity |

### Prioritization Criteria

When multiple opportunities compete, evaluate:

| Criterion | Question |
|---|---|
| Evidence strength | How many independent interviews support this opportunity? |
| Outcome alignment | How directly does this connect to our desired outcome? |
| Addressability | Can our team realistically address this with a product change? |
| Size | How many users face this problem? |
| Urgency | Is there time pressure (competitive, regulatory, seasonal)? |

**Rule**: Focus on one opportunity at a time. Spreading across multiple opportunities simultaneously dilutes learning velocity.

---

## Step 6: Dual-Track Agile (Discovery + Delivery)

### How Two Tracks Work in Parallel

| Track | Purpose | Who Leads | Cadence |
|---|---|---|---|
| Discovery | Produce, test, and validate product ideas | PM and Designer (Engineers participate) | Continuous, weekly rhythm |
| Delivery | Implement validated ideas into shippable increments | Engineers (PM and Designer support) | Sprint cadence (1-2 weeks) |

### Integration Points

- Discovery feeds validated solutions into the delivery backlog
- Delivery outcomes inform new discovery questions
- Ongoing communication ensures insights directly influence delivery priorities
- The Product Trio bridges both tracks, preventing handoff gaps

### Discovery vs. Design Sprints

| Aspect | Discovery Sprint | Design Sprint |
|---|---|---|
| Focus | Problem space exploration | Solution design and validation |
| Timeline | Flexible (1 week to 1 month) | Fixed 4-5 days |
| Activities | Research, assess, discover, recommend | Map, sketch, storyboard, prototype, test |
| Use case | High uncertainty about customer needs | Specific problem requiring quick alignment |
| When to use | Early product lifecycle, new market entry | Validate specific ideas or test features |

---

## Step 7: Connecting Discovery to OKRs

### Outcome-Based Discovery

Instead of "What do stakeholders want us to build?" ask "What change in user behavior or business metric are we aiming for?"

| OKR Level | Discovery Connection |
|---|---|
| Company objective | Sets the strategic context for which outcomes matter |
| Team key result | Becomes the Desired Outcome at the top of the OST |
| Learning goals | When the team lacks understanding, set OKRs to learn (not just perform) |
| Performance goals | When the path is clearer, set OKRs to move a metric |

**Learning vs. performance goals**: Not all OKRs need to be performance-based. Early in discovery, a valid Key Result is "Identify the top 3 opportunities for reducing churn in the onboarding flow" rather than "Reduce onboarding churn by 15%."

### Discovery Cadence Metrics

Track discovery health with these metrics:

| Metric | What It Measures | Target |
|---|---|---|
| Weekly interview completion rate | Consistency of customer contact | 90%+ weeks with at least 1 interview |
| Assumptions tested per sprint | Learning velocity | 1-2 assumptions validated per sprint |
| Time from insight to shipped value | Discovery-to-delivery cycle time | Decreasing trend quarter over quarter |
| OST update frequency | Whether the tree stays current | Updated at least weekly |
| Cross-functional participation | Trio involvement in discovery | All three roles attend 80%+ of interviews |

**Leading indicator of discovery quality**: How often a solution is thrown out based on evidence. Teams that never discard ideas are not learning; they are confirming.

---

## Step 8: Story Mapping Integration

Story mapping bridges discovery insights and delivery planning:

1. Assume your solution already exists
2. Map what customers must do to get value from it, step by step
3. Be explicit about who does what and when
4. Identify the thinnest possible slice that delivers the core value (walking skeleton)
5. Update the story map continuously as data arrives from analytics, support, interviews, and experiments

**Living document**: The story map is not a one-time artifact. As you learn from shipped increments, promote proven bets, reshape work, or drop low-impact ideas.

---

## Step 9: Discovery Anti-Patterns

| Anti-Pattern | What It Looks Like | Fix |
|---|---|---|
| "We know what to build" | No user research; founders pursuing vision without validation | Start with 5 interviews this week; let evidence challenge beliefs |
| Confirmation-biased discovery | Discovery as rubber stamp for pre-existing ideas | Pre-commit to kill criteria before testing |
| Outsourcing discovery | External agency runs all research | Trio must participate; agencies can assist but not replace |
| Ignoring support data | Customer support excluded from hypothesis generation | Include support lead in weekly synthesis; mine ticket data for patterns |
| Hypotheses without engineers | Developers excluded from assumption identification | Engineers attend interviews and contribute feasibility constraints |
| Discovery theater | Interviews happen but insights never change the roadmap | Connect every shipped feature to a specific discovery insight |
| Research hoarding | Insights trapped in one person's head or buried in docs | Use atomic research repository; make insights searchable |
| Irregular cadence | Discovery happens in bursts before planning, then stops | Automate recruitment; schedule standing weekly slots |

---

## Step 10: Research Repository (ResearchOps)

### Building an Organizational Research Repository

| Practice | Description |
|---|---|
| Centralize content | All interview recordings, snapshots, nuggets, and synthesis artifacts in one searchable location |
| Standardize descriptions | Define tagging taxonomy (participant type, product area, opportunity, date) |
| Curate actively | Designate a research ops owner who maintains quality and removes stale content |
| Make it accessible | Ensure any team member can search and browse insights without gatekeeping |

### Repository Benefits

- Reduces duplicate research (teams discover what others already learned)
- Enables cross-team pattern recognition
- Creates institutional memory that survives team turnover
- Supports regulatory and compliance documentation of user research

---

## Output Template

```
CONTINUOUS DISCOVERY PLAN
Product: [Name]
Team: [PM, Designer, Engineer names]
Desired Outcome: [Specific measurable outcome from OKRs]
Timeframe: [When we need to achieve it]
Date: [Today]

CURRENT DISCOVERY STATE
Interview cadence: [Current frequency]
Synthesis method: [How insights are captured today]
Key gap: [What is missing or broken in current discovery practice]

OPPORTUNITY SOLUTION TREE

Desired Outcome: [Metric and target]

Opportunity 1: [Customer-language statement]
  Evidence: [Interview quotes, data points, number of sources]
  Confidence: [High / Medium / Low]
  Solutions:
    Solution A: [Description]
      Riskiest assumption: [Statement]
      Experiment: [Cheapest valid test]
    Solution B: [Description]
      Riskiest assumption: [Statement]
      Experiment: [Cheapest valid test]

Opportunity 2: [Customer-language statement]
  Evidence: [Sources]
  Confidence: [Level]
  Solutions:
    Solution C: [Description]
    Solution D: [Description]

OPPORTUNITY PRIORITIZATION
Focus opportunity: [Which one and why]
Scoring: Importance [X/10], Satisfaction [X/10], Score [X]
Evidence strength: [Number of independent interviews]

DISCOVERY CADENCE PLAN
| Week | Interview Target | Synthesis Activity | Experiment |
|------|-----------------|-------------------|------------|
| W1   | [Who]           | [Snapshot + map]  | [Test]     |
| W2   | [Who]           | [Snapshot + map]  | [Test]     |
| W3   | [Who]           | [Cross-synthesis] | [Test]     |
| W4   | [Who]           | [OST review]      | [Decision] |

RECRUITMENT PLAN
Channel: [How we recruit interviewees]
Incentive: [What we offer]
Scheduling: [Automated or manual]

DISCOVERY HEALTH METRICS
| Metric | Current | Target |
|--------|---------|--------|
| Weekly interview rate | [X] | 1+ per week |
| Assumptions tested/sprint | [X] | 1-2 per sprint |
| OST update frequency | [X] | Weekly |
| Trio participation | [X%] | 80%+ |

ANTI-PATTERN CHECK
[Which anti-patterns is the team currently at risk of? What safeguards are in place?]
```
