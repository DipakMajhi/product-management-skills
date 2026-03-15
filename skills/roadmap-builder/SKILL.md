---
name: roadmap-builder
description: "Build or transform product roadmaps using Now/Next/Later (Janna Bastow), outcome-driven (Josh Seiden), theme-based, opportunity-driven (Teresa Torres), and GIST (Itamar Gilad) formats. Covers roadmap types and when to use each, transforming feature lists into outcome roadmaps, audience-specific roadmaps (board, engineering, sales, customers), confidence levels and commitment spectrum, dependency mapping, roadmap review cadence and governance, roadmap communication anti-patterns, and PM interview application. Use when creating a roadmap, converting a feature list into an outcome-driven roadmap, structuring roadmap presentations for different audiences, or answering PM interview questions about roadmap building."
argument-hint: "[describe the product, the audience for this roadmap, current state (feature list, backlog, or existing roadmap), strategic priorities, and time horizon]"
---

# Product Roadmap Builder

A roadmap is a communication tool. Its job is to tell a coherent story about where the product is going and why, not to be a detailed project plan. Different audiences need different roadmaps. The best roadmaps connect work to outcomes and use confidence levels instead of fixed dates.

Apply this skill to: $ARGUMENTS

## Step 1: Choose the Right Roadmap Format

### Format 1: Now / Next / Later (Janna Bastow)

| Column | Definition | Confidence | Detail Level |
|---|---|---|---|
| **Now** | In active development this sprint/quarter | High (80-100%) | Specific initiatives with owners |
| **Next** | Planned for next 1-2 quarters | Medium (40-70%) | Defined initiatives, scope may shift |
| **Later** | On the horizon, directional | Low (10-30%) | Themes or opportunity areas, not commitments |

**Best for**: Teams that want to reduce over-promising without losing stakeholder visibility. Replaces deadline-driven planning with outcome-focused delivery.

### Format 2: Outcome-Driven Roadmap (Josh Seiden)

Group work by the outcome it drives, not the features being shipped:

```
Outcome: Reduce onboarding drop-off from 65% to 45%
  - Initiative: Redesign step 2 of onboarding
  - Initiative: Add progress indicator
  - Initiative: In-app guided tour

Outcome: Increase expansion revenue from $200K to $350K MRR
  - Initiative: Usage-based upgrade prompts
  - Initiative: Team admin dashboard
  - Initiative: API access for power users
```

**Best for**: Teams that have adopted OKRs and want to connect features to goals. Prevents the team from becoming a "feature factory."

### Format 3: Theme-Based Roadmap

Group work by strategic theme across time horizons:

| Theme | Now | Next | Later |
|---|---|---|---|
| "Make it fast for power users" | [Initiative] | [Initiative] | [Direction] |
| "Unlock enterprise buyers" | [Initiative] | [Initiative] | [Direction] |
| "Expand into mobile" | [Initiative] | [Initiative] | [Direction] |

**Best for**: Leadership presentations, board updates, and investor communications. Themes tell a strategic story.

### Format 4: Opportunity-Driven Roadmap (Teresa Torres)

Use the Opportunity Solution Tree as input to roadmapping:

```
Desired Outcome (from OKRs)
  Opportunity 1 (customer need discovered through research)
    Solution A (in progress)
    Solution B (next to test)
  Opportunity 2
    Solution C (later -- needs more discovery)
```

**Best for**: Teams practicing continuous discovery who want the roadmap to reflect what they have learned about customer needs.

### Format 5: GIST Framework (Itamar Gilad)

| Level | Time Horizon | Cadence | Example |
|---|---|---|---|
| **Goals** | 1+ year | Set yearly, adjusted quarterly | "Achieve 40% market share in SMB segment" |
| **Ideas** | Ongoing | Constantly collected, prioritized by evidence | Idea bank scored by confidence |
| **Step-Projects** | Quarter | Planned quarterly, executed in short cycles | "Run 3 onboarding experiments this quarter" |
| **Tasks** | 1-2 weeks | Managed within sprints | Sprint-level work items |

**Best for**: Teams that want to reduce roadmap overhead while increasing velocity and evidence-based decision-making.

### Format Selection Guide

| Situation | Recommended Format |
|---|---|
| Early-stage startup, high uncertainty | Now/Next/Later or GIST |
| Mature product with OKRs | Outcome-Driven |
| Board or investor presentation | Theme-Based |
| Team practicing continuous discovery | Opportunity-Driven |
| PM interview ("build a roadmap for X") | Outcome-Driven (shows strategic thinking) |

---

## Step 2: Audience-Specific Roadmaps

Different stakeholders need different levels of detail and different framing:

| Audience | Focus | Detail Level | Format | Avoid |
|---|---|---|---|---|
| **Board / Executives** | Strategic direction, market opportunity, growth metrics | High-level themes and outcomes | Theme-Based or Outcome-Driven | Feature-level detail, technical jargon |
| **Engineering** | What to build, dependencies, technical requirements | Feature-level with acceptance criteria | Now/Next/Later with epics | Vague outcomes without actionable scope |
| **Sales** | Customer benefits, competitive differentiation, timing | Feature benefits and customer impact | Theme-Based with customer value | Hard dates (undermine credibility when missed) |
| **Customers** | What is coming and why it matters to them | Generalized, outcome-focused | Public roadmap or changelog | Technical details, dependencies, internal priorities |
| **Customer Success** | What is changing, training needs, support implications | Feature details with timeline windows | Now/Next/Later | Uncertainty language (CS needs to plan) |

**Key principle**: Never present the same roadmap to every audience. The board version and engineering version should tell the same story at different zoom levels.

---

## Step 3: Confidence Levels and Commitment Spectrum

Replace hard dates with confidence levels:

| Confidence | Meaning | Communication | Example |
|---|---|---|---|
| 90-100% | Committed, in active development | "We are building this" | Current sprint items |
| 60-80% | High confidence, scoped and prioritized | "We plan to build this next" | Next quarter initiatives |
| 30-50% | Medium confidence, directional | "We are exploring this" | Later bucket items |
| 10-20% | Low confidence, aspirational | "We are thinking about this" | Future opportunity areas |
| 0% | Not planned | "This is not on our roadmap" | Explicitly deprioritized |

**Critical rule**: A roadmap is a plan, not a promise. Forecasts do not represent commitments. Communicate this framing explicitly to stakeholders.

---

## Step 4: Transform Feature Lists into Outcome Roadmaps

When given a feature backlog and asked to create a roadmap:

1. **Identify outcomes**: For each feature, ask "What outcome does this drive?" (retention, acquisition, activation, revenue, satisfaction)
2. **Group by outcome**: Cluster features that serve the same business outcome
3. **Prioritize outcomes**: Sequence outcome groups by strategic priority and evidence strength
4. **Sequence within outcomes**: Order features by dependency and impact within each group
5. **Add confidence levels**: Mark each item with a confidence level based on evidence and scope clarity
6. **Identify what is NOT on the roadmap**: Explicitly list notable items that were deprioritized and why

### Prioritization Frameworks for Roadmap Sequencing

| Framework | Formula | Best For |
|---|---|---|
| RICE | (Reach x Impact x Confidence) / Effort | Quantitative prioritization with data |
| ICE | (Impact + Confidence + Ease) / 3 | Quick scoring when data is limited |
| MoSCoW | Must/Should/Could/Won't classification | Stakeholder alignment on scope |
| Value vs. Effort | 2x2 matrix of value and effort | Visual prioritization in workshops |
| Cost of Delay | Revenue impact of delaying by one month | Time-sensitive prioritization |

---

## Step 5: Dependency Mapping

### Dependency Types

| Type | Description | Example |
|---|---|---|
| Feature dependencies | One feature requires another to function | Search requires indexing infrastructure |
| Technical dependencies | Code or architecture sequencing | API must exist before frontend integration |
| Resource dependencies | Same team or specialist needed for multiple items | Design team bottleneck across 3 initiatives |
| External dependencies | Third-party APIs, partner integrations, regulatory approvals | Payment processor certification |

### Dependency Management Process

1. **Identify**: Map all dependencies during roadmap construction
2. **Eliminate**: Can we restructure work to remove the dependency?
3. **Manage**: For unavoidable dependencies, assign owners and track status
4. **Communicate**: Make dependencies visible on the roadmap (not hidden in backlogs)
5. **Buffer**: Add time buffers for external dependencies outside your control

---

## Step 6: Roadmap Review Cadence and Governance

| Activity | Frequency | Participants | Purpose |
|---|---|---|---|
| Roadmap review | Quarterly | PM, Engineering Lead, Design Lead, Leadership | Reprioritize based on new data and strategy shifts |
| Progress check | Bi-weekly | PM, Engineering Lead | Are we on track? Any blockers? |
| Stakeholder update | Monthly | All stakeholders (format varies by audience) | Communicate progress and changes |
| Major pivot decision | As needed | PM, Leadership, affected teams | When evidence invalidates a roadmap bet |

### Governance Rules

- Items move between Now/Next/Later based on evidence, not stakeholder pressure
- New requests go through a consistent intake process (not straight onto the roadmap)
- Every item on the roadmap must connect to a strategic outcome
- Deprioritized items are explicitly communicated, not silently dropped

---

## Step 7: Roadmap Anti-Patterns

| Anti-Pattern | What It Looks Like | Fix |
|---|---|---|
| Date-driven roadmap | Specific dates for items more than 6 weeks out | Use confidence levels instead of dates |
| Feature list without outcomes | List of features with no explanation of the problem they solve | Group by outcome; state the "why" for each theme |
| Everything is P1 | Every item marked high priority | Force-rank; if everything is P1, nothing is |
| Roadmap as contract | Stakeholders treat the roadmap as a binding commitment | Communicate the plan-not-promise framing repeatedly |
| Same roadmap for all audiences | Board sees sprint-level detail; engineers see vague themes | Create audience-specific versions |
| Stale roadmap | Last updated 6 months ago | Review quarterly at minimum; update after major learnings |
| No explicit trade-offs | No mention of what was deprioritized | Include a "What is NOT on this roadmap" section |
| Kitchen sink roadmap | 4+ themes with 20+ items | Limit to 3-4 themes per roadmap view |
| No learning built in | Roadmap assumes all bets will succeed | Include discovery and validation milestones |
| Accepting every request | Customer or sales requests go directly onto the roadmap | Route requests through prioritization framework |

---

## Output Template

```
PRODUCT ROADMAP: [Product Name]
Format: [Now/Next/Later | Outcome-Driven | Theme-Based | GIST]
Period Covered: [Timeframe]
Audience: [Who this version is for]
Last Updated: [Date]

STRATEGIC CONTEXT
[1-3 sentences on what this roadmap is optimizing for in this period]
Company OKRs this connects to: [List relevant OKRs]

ROADMAP

[Format varies by type chosen. Example for Outcome-Driven:]

Outcome 1: [Measurable outcome with target]
Confidence: [%]
| Initiative | Status | Confidence | Evidence Basis | Dependencies |
|-----------|--------|-----------|---------------|-------------|
| [Name]    | [Now/Next/Later] | [%] | [What supports this bet] | [Blocking items] |

Outcome 2: [Measurable outcome with target]
[Same structure]

WHAT IS NOT ON THIS ROADMAP
| Item | Why Deprioritized | Could Revisit If |
|------|------------------|-----------------|
| [Feature/Theme] | [Reason] | [Condition that would change this] |

DEPENDENCIES AND RISKS
| Dependency | Owner | Status | Impact if Delayed |
|-----------|-------|--------|------------------|
| [Item]    | [Team/Person] | [Green/Yellow/Red] | [What shifts] |

ROADMAP REVIEW SCHEDULE
Next review: [Date]
Review trigger: [What would cause an off-cycle review]

KEY ASSUMPTIONS
[3-5 assumptions this roadmap is built on that, if wrong, would change priorities]
```
