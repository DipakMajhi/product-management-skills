---
name: prioritization
description: "Prioritize a product backlog, feature list, or set of opportunities using structured frameworks. Use this skill when someone needs to rank features, decide what to build next, apply RICE, ICE, MoSCoW, Kano, or other frameworks, or prepare for a PM interview question about prioritization."
---

# Product Prioritization Frameworks

You help PMs make defensible, structured prioritization decisions. The right framework depends on the context, and the best PMs know when to use which approach.

## Framework Selection Guide

Apply this skill to: $ARGUMENTS


| Situation | Best Framework | Why |
|---|---|---|
| Large backlog (50+ items), need a quick first cut | ICE Score | Fast scoring, low overhead |
| Need to justify decisions to stakeholders with data | RICE Score | Quantitative, transparent, defensible |
| Scoping a release: must-haves vs. nice-to-haves | MoSCoW | Forces explicit scope boundaries |
| Differentiating basics from delighters | Kano Model | Reveals what creates competitive advantage |
| Maximizing economic throughput | WSJF (Weighted Shortest Job First) | Incorporates cost of delay and job size |
| Understanding the financial cost of not doing something | Cost of Delay | Quantifies time-sensitivity of decisions |
| OKR-driven teams choosing what moves metrics | Impact on OKR | Aligns backlog directly to outcomes |
| Strategic bets vs. optimization work | Opportunity Scoring (ODI) | Identifies underserved, high-importance needs |
| Quick visual triage in a workshop | Value vs. Effort Matrix | Intuitive 2x2, great for group alignment |
| Small list, need honest forced ranking | Stack Ranking | No ties allowed, forces real comparison |
| Discovery prioritization (opportunities, not solutions) | Opportunity Solution Tree | Prioritizes the problem space before solutions |
| Portfolio allocation across time horizons | Three Horizons Framework | Balances core, adjacent, and transformative work |

## Framework Details

### RICE Score
**Formula**: (Reach x Impact x Confidence) / Effort
- **Reach**: How many users or accounts affected per quarter? Use actual data when possible.
- **Impact**: How much will it move the target metric? Use a consistent scale:
  - 3 = Massive (>2x improvement for affected users)
  - 2 = High (significant, measurable improvement)
  - 1 = Medium (noticeable improvement)
  - 0.5 = Low (minor improvement)
  - 0.25 = Minimal (barely noticeable)
- **Confidence**: How certain are we about our Reach, Impact, and Effort estimates?
  - 100% = High confidence (validated with data or prior experiments)
  - 80% = Medium confidence (reasonable estimates with some evidence)
  - 50% = Low confidence (gut feel, limited evidence)
- **Effort**: Person-months of work required. Include engineering, design, QA, and any other functions.

**When RICE breaks down**: RICE favors incremental wins over strategic bets. High-uncertainty, high-reward items score low because Confidence penalizes them. Supplement with portfolio-level thinking.

### ICE Score
**Formula**: Impact x Confidence x Ease (each rated 1-10)
Faster than RICE, less precise. Good for early-stage triage when data is limited. The main weakness is subjectivity in 1-10 ratings; calibrate by scoring 3-5 well-understood items first as anchors.

### WSJF (Weighted Shortest Job First)
**Formula**: (Business Value + Time Criticality + Risk Reduction/Opportunity Enablement) / Job Duration

| Component | Question to Answer | Scale |
|---|---|---|
| Business Value | How much revenue, user value, or strategic value does this deliver? | 1-10 |
| Time Criticality | What is the cost of delay? Is there a deadline, competitive window, or decaying opportunity? | 1-10 |
| Risk Reduction / Opportunity Enablement | Does this reduce a significant risk or unlock future opportunities? | 1-10 |
| Job Duration | How large is this work? (Relative sizing, not absolute) | 1-10 |

WSJF is particularly powerful because it explicitly accounts for the time value of features. An item with moderate value but high time criticality and low effort should be done first.

### Cost of Delay
**Core question**: "What would we lose per week/month by not doing this?"

Quantify in terms of:
- Revenue impact: Lost sales, delayed monetization, competitive displacement
- Customer impact: Churn risk, satisfaction degradation, support cost increase
- Strategic impact: Market window closing, regulatory deadline, partnership dependency
- Opportunity cost: What becomes possible only after this is done?

Cost of Delay is not a standalone framework but a powerful input to other frameworks (especially WSJF). It forces honest conversations about whether something is truly urgent or just loud.

### MoSCoW
- **Must Have**: Without this, the product fails, is not legally compliant, or cannot ship. If you can launch without it, it is not a Must Have.
- **Should Have**: High value, clear impact, but the product works without it. Workarounds exist.
- **Could Have**: Nice to have. Include if time permits, drop without consequence.
- **Will Not Have (this cycle)**: Explicitly deprioritized. Critical for scope management - this category should be large.

**MoSCoW discipline**: Must Haves should represent no more than 60% of available capacity. If everything is a Must Have, nothing is prioritized.

### Kano Model
- **Basic needs (Must-be)**: Absence causes strong dissatisfaction; presence is expected and unnoticed. Examples: app does not crash, data is saved, login works.
- **Performance needs (One-dimensional)**: More is linearly better. Examples: faster load times, more storage, better search relevance.
- **Excitement needs (Delighters)**: Unexpected features that create disproportionate satisfaction. Absence causes no dissatisfaction because users did not expect them. Examples: AI-powered suggestions, proactive notifications, beautiful animations.
- **Indifferent**: Users genuinely do not care. Do not build these.
- **Reverse**: Some users actively dislike this feature. Watch for these when adding complexity.

**Kano insight**: Basic needs are table stakes, not differentiators. Competing on performance needs is a race. Delighters are where competitive advantage lives, but they decay into performance needs over time as users come to expect them.

### Opportunity Scoring (Outcome-Driven Innovation / Anthony Ulwick)
Rate each opportunity on two dimensions (survey your users):
- **Importance**: How important is this outcome to you? (1-10)
- **Satisfaction**: How satisfied are you with current solutions? (1-10)

**Opportunity Score** = Importance + max(Importance - Satisfaction, 0)

High importance + low satisfaction = high opportunity. This framework is discovery-oriented: it prioritizes the problem space, not the solution space.

### Value vs. Effort Matrix (2x2)
Plot items on a two-dimensional grid:
- X-axis: Effort (Low to High)
- Y-axis: Value (Low to High)

| Quadrant | Action |
|---|---|
| High Value, Low Effort (Quick Wins) | Do first. Ship these immediately. |
| High Value, High Effort (Big Bets) | Plan carefully. Phase if possible. |
| Low Value, Low Effort (Fill-ins) | Do when capacity allows. Batch together. |
| Low Value, High Effort (Time Sinks) | Do not do. Actively kill these. |

**Variations**: Replace "Value" and "Effort" axes with User Satisfaction Impact vs. Technical Complexity, Market Potential vs. Operational Complexity, or Strategic Alignment vs. Resource Requirements depending on context.

### Stack Ranking (Forced Ranking)
Force every item into a strict ordered list. No ties allowed. No "these three are all priority 1."

Best for: Small backlogs (under 50 items), team alignment workshops, executive-level priority setting.
Advantage: Brutally honest. Reveals disagreements immediately.
Limitation: Does not scale to large backlogs and does not capture magnitude of difference between items.

**Technique**: Pair items and ask "If you could only ship one of these two, which one?" Repeat until the full ranking emerges.

### Three Horizons Framework (Portfolio-Level)
Allocate effort across time horizons:

| Horizon | Focus | Typical Allocation | Success Metric |
|---|---|---|---|
| H1: Core | Optimize and defend the current business | 70% of effort | Profit, retention, efficiency |
| H2: Adjacent | Extend into new segments, channels, or capabilities | 20% of effort | Growth rate, new revenue streams |
| H3: Transformative | Explore disruptive opportunities and future bets | 10% of effort | Return on learning, optionality created |

Some high-growth companies argue for equal allocation (33/33/33) to maintain innovation velocity. The right balance depends on market maturity and competitive pressure.

### Opportunity Solution Tree (Teresa Torres)
Prioritize the opportunity space before evaluating solutions:
1. Start with a business outcome (OKR or target metric)
2. Map customer opportunities (needs, pain points, desires) discovered through research
3. For each opportunity, brainstorm multiple possible solutions
4. For each solution, identify the riskiest assumptions
5. Prioritize opportunities (not solutions) by potential impact on the outcome
6. Then evaluate solutions within the highest-priority opportunities

This prevents the common trap of comparing apples to oranges (a UI improvement vs. a pricing change vs. a new feature) by first aligning on which problem is most worth solving.

## Handling Technical Debt and Platform Work

Technical debt is not separate from product prioritization. Include it on the same roadmap using the same frameworks:

- **Reframe in business terms**: "Reduce deployment time from 4 hours to 15 minutes" translates to "Ship features 16x faster, enabling 3 additional experiments per sprint."
- **Allocate consistently**: Reserve approximately 20% of sprint capacity for technical debt and platform work.
- **Prioritize by customer impact**: Fix the highest-impact technical liabilities first (bugs in frequently used features, performance in critical flows, security vulnerabilities).
- **Use Cost of Delay**: Technical debt often has compounding cost of delay. The longer you wait, the more expensive it becomes.

## Handling Constraints

Real-world prioritization must account for:
- **Dependencies**: Item B cannot start until Item A is complete. Map these explicitly.
- **Team capacity bottlenecks**: Specialized roles (security review, data science, legal approval) create constraints. Prioritize to minimize idle time for bottleneck resources.
- **Regulatory deadlines**: Compliance requirements with fixed dates override other prioritization.
- **Cross-team dependencies**: Features requiring work from multiple teams need coordination. Prioritize items that unblock other teams when possible.

## Stakeholder Alignment Techniques

When stakeholders disagree on priorities:
- **Make trade-offs explicit**: "We are choosing to do X instead of Y because [data/reasoning]. Here is what we would need to believe for Y to be more important."
- **Use shared criteria**: Agree on the prioritization framework and scoring criteria BEFORE evaluating items.
- **Present in audience-appropriate terms**: Revenue and risk for executives, feasibility and scope for engineers, user impact and design quality for designers.
- **MoSCoW workshop**: Force stakeholders to categorize together. The argument about whether something is a Must Have or Should Have is the productive conversation.
- **Opportunity cost framing**: "If we build feature X this quarter, it means we cannot build features Y and Z. Are we comfortable with that trade-off?"

## Prioritization Anti-Patterns

| Anti-Pattern | What It Looks Like | Countermeasure |
|---|---|---|
| **HiPPO** (Highest Paid Person's Opinion) | The VP says it, so we do it | Use transparent frameworks with visible scoring. Data beats title. |
| **Recency bias** | Last customer complaint dominates the roadmap | Use volume-weighted signals and trend analysis, not individual anecdotes |
| **Sunk cost fallacy** | "We already invested 3 months, we have to finish" | Evaluate every item on its future value only, not past investment |
| **Everything is P0** | No real prioritization has occurred | Force stack ranking or MoSCoW. If everything is priority 1, nothing is. |
| **Squeaky wheel** | The loudest stakeholder gets their way | Weight requests by customer segment size, revenue impact, and strategic alignment |
| **Shiny object syndrome** | Chasing new ideas instead of finishing current work | Require evidence (research, data) before any new item enters the top 10 |
| **Anchoring** | First scores stick even when new information arrives | Re-score periodically with fresh data |
| **Confirmation bias** | Seeking data that supports a predetermined decision | Assign a devil's advocate or run a pre-mortem |
| **Political prioritization** | Features prioritized by org chart, not user value | Cross-functional scoring sessions with explicit criteria |

## Process

1. Confirm: What is being prioritized? (features, opportunities, bets, technical debt)
2. Confirm: What is the decision context? (how many items, what data is available, who are the stakeholders, what constraints exist)
3. Recommend and agree on the appropriate framework
4. Apply the chosen framework, showing scoring for each item
5. Present the ranked list with scores and rationale
6. Flag items where the score seems counterintuitive and explain why
7. Identify dependencies and constraints that affect sequencing
8. Present the final recommended priority order with trade-off analysis

## Output Template

---
**PRIORITIZATION OUTPUT**
**Framework Used:** [Name and why it was chosen]
**Business Context:** [What outcome we are optimizing for]
**Input Items:** [Count]
**Constraints Considered:** [Dependencies, deadlines, capacity limits]

**Scored and Ranked List**

| Rank | Item | [Score Components] | Total Score | Key Rationale | Dependencies |
|---|---|---|---|---|---|
| 1 | [Item] | [Component scores] | [Score] | [One-line rationale] | [Blocked by / Blocks] |
| 2 | ... | ... | ... | ... | ... |

**Items Removed from Consideration**
| Item | Reason for Removal |
|---|---|
| [Item] | [Why it was disqualified before scoring] |

**Portfolio Allocation (if applicable)**
- H1 (Core): [Items and % of effort]
- H2 (Adjacent): [Items and % of effort]
- H3 (Transformative): [Items and % of effort]

**Technical Debt Allocation**
[Items classified as technical debt and their priority relative to feature work]

**Recommended Top 3-5 for Next Sprint/Quarter**
[Names with one sentence each on why they belong at the top, including expected impact on target metrics]

**Key Trade-Offs Made**
[2-3 explicit trade-offs: what was deprioritized and why]

**Prioritization Risks and Caveats**
[Items where the score may not tell the full story, areas of low confidence, assumptions to revisit]

**Review Cadence**
[When this prioritization should be revisited: weekly for sprints, monthly for quarters, quarterly for strategic bets]
---

## Interview Context

Prioritization is the most commonly tested PM interview skill. When asked "How would you prioritize this backlog?" or "You have these 5 features and can only ship 2, which ones?":

1. **Clarify the objective**: What is the business goal? Who is the user? What are the constraints?
2. **State the framework**: "I will use RICE because we need a quantitative, defensible ranking for a large backlog." Explain why you chose this framework over alternatives.
3. **Apply it explicitly**: Walk through the scoring for each item. Show your reasoning, not just the output.
4. **Acknowledge trade-offs**: "By choosing A over B, we accept that [trade-off]. I am comfortable with this because [reasoning]."
5. **Consider second-order effects**: "Shipping feature A first also unblocks features C and D, so the total value of prioritizing A is higher than its standalone score suggests."
6. **Propose a validation approach**: "Before committing, I would validate the top assumption by [experiment or data analysis]."
