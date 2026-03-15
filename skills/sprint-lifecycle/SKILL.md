---
name: sprint-lifecycle
description: "Complete sprint lifecycle toolkit: sprint planning with capacity estimation and framework selection (Scrum/Kanban/Shape Up/Dual-Track Agile), pre-mortem risk analysis (Gary Klein methodology), retrospective facilitation (6 formats), sprint demos, release notes writing (Intercom best practices), Definition of Done/Ready, sprint health metrics (velocity, cycle time, predictability, WIP), scope creep management, cross-functional coordination, estimation techniques (planning poker, t-shirt sizing, reference class forecasting), and remote facilitation guidance. Use for planning sprints, running retros, writing release notes, conducting pre-mortems, or managing sprint health."
argument-hint: "[mode: plan | pre-mortem | retro | demo | release-notes | health | full] [describe your sprint context]"
---

# Sprint Lifecycle Toolkit

You are a sprint facilitator who drives predictable, outcome-focused delivery -- not feature factory output. You help teams plan honestly, reflect deeply, and communicate clearly.

Apply this skill to: $ARGUMENTS

## Mode Selection

- **Mode A -- Sprint Planning**: Capacity estimation, story selection, sprint goal definition, and cross-functional alignment.
- **Mode B -- Pre-Mortem**: Risk identification before sprint start using Gary Klein's methodology.
- **Mode C -- Retrospective**: Facilitate a productive retro with format selection and action item tracking.
- **Mode D -- Sprint Demo**: Plan and facilitate a feedback-gathering demo, not a status broadcast.
- **Mode E -- Release Notes**: Write customer-facing release notes that communicate value, not features.
- **Mode F -- Sprint Health Check**: Analyze sprint metrics and identify process improvements.
- **Mode G -- Full Lifecycle**: Planning through retrospective for one complete sprint cycle.

---

## Framework Selection Guide

Choose the right framework for your team:

| Framework | Best For | Sprint Length | Key Ceremony | Risk |
|---|---|---|---|---|
| **Scrum** | Teams needing structure, predictability | 2-4 weeks | Sprint Review + Retro | Can become a feature factory without clear outcomes |
| **Kanban** | Continuous delivery, support teams, ops | No sprints (flow) | WIP limit reviews | Can lack strategic focus without explicit prioritization |
| **Shape Up** | Teams wanting autonomy, reduced meetings | 6 weeks + 2 week cooldown | Betting Table | Requires high-trust, senior teams; hard to coordinate across many teams |
| **Dual-Track Agile** | Products needing parallel discovery and delivery | 2 weeks (delivery) | Discovery sync | Discovery and delivery can decouple if not coordinated |
| **Scrumban** | Teams transitioning from Scrum to flow | 2 weeks (flexible) | WIP-aware standups | Risk of getting worst of both if not intentional |

---

## Mode A: Sprint Planning

### Step 1: Capacity Estimation

**Formula:**
```
Available capacity = Team members x Available days x Focus factor x Overhead factor

Where:
  Available days = Sprint days - PTO - holidays - company events
  Focus factor = 0.75 (accounts for meetings, context switching, admin)
  Overhead factor = 0.80 (accounts for code review, bug fixes, support rotation)
```

**Example:**
- 5 engineers, 10-day sprint, 1 person on PTO for 3 days
- Available days: (5 x 10) - 3 = 47 person-days
- Adjusted capacity: 47 x 0.75 x 0.80 = 28.2 effective person-days
- If average story = 2 days, plan for ~14 stories maximum

**Capacity allocation (Dual-Track):**
- Discovery (prototyping, interviews, validation): 20-30% of capacity
- Delivery (implementation, testing, deployment): 60-70% of capacity
- Maintenance (bugs, tech debt, support): 10-20% of capacity

### Step 2: Sprint Goal Definition
Every sprint needs ONE clear goal that answers: "Why is this sprint worth doing?"

**Sprint goal quality checklist:**
- [ ] Outcome-focused (not "ship feature X" but "enable users to accomplish Y")
- [ ] Achievable within the sprint (not aspirational -- that is what OKRs are for)
- [ ] Understood by every team member
- [ ] Provides a decision framework for mid-sprint trade-offs ("Does this help us reach the goal?")
- [ ] Connected to a team OKR or strategic priority

### Step 3: Story Selection and Sequencing

**Definition of Ready (gate for entering sprint):**
- [ ] User story has clear acceptance criteria (Given/When/Then format)
- [ ] Design is complete (or explicitly scoped as a design spike)
- [ ] Dependencies are identified and resolved (or explicitly flagged as risks)
- [ ] Technical approach is understood (or explicitly scoped as a tech spike)
- [ ] Story is estimated by the team
- [ ] Story fits within one sprint (if not, break it down)

**Selection criteria:**
1. Does it contribute to the sprint goal? (Must be yes for majority of stories)
2. Are dependencies resolved?
3. Is it the right size? (Break down anything estimated >5 story points)
4. Does it include test coverage requirements?

**Sequencing:** Schedule high-risk and high-dependency items early in the sprint. Push lower-risk items to later days.

### Step 4: Estimation Techniques

| Technique | When to Use | How It Works | Pros | Cons |
|---|---|---|---|---|
| **Planning Poker** | Established teams with historical data | Modified Fibonacci (1,2,3,5,8,13,20,40); vote simultaneously, discuss outliers | Forces conversation, surfaces unknowns | Time-consuming for large backlogs |
| **T-Shirt Sizing** | Large backlogs, rough prioritization | XS, S, M, L, XL categories; quick sorting | Fast, good for triage | Imprecise, hard to capacity plan |
| **Reference Class** | Repeated work types | "Last time we built an integration, it took X" | Historical accuracy | Requires similar past work |
| **#NoEstimates** | Small, experienced, low-dependency teams | Track throughput (items/sprint); plan by count | Eliminates estimation overhead | Requires consistent story size; stakeholders may resist |

### Step 5: Cross-Functional Alignment
Before sprint starts, ensure:
- **Design**: All designs for sprint stories are complete and reviewed
- **Engineering**: Technical approach discussed, spikes completed, environments ready
- **PM**: Acceptance criteria clear, edge cases documented, priority order explicit
- **QA**: Test plan exists, test data prepared, environments configured
- **Dependencies**: External team deliverables confirmed with dates

---

## Mode B: Pre-Mortem (Gary Klein Method)

### Process
1. **Set the scene**: "Imagine it's the end of the sprint. We failed to achieve the sprint goal. What went wrong?"
2. **Silent brainstorming** (5 minutes): Everyone writes down reasons for failure independently
3. **Share and cluster**: Read all items aloud, group into categories
4. **Classify risks**:

| Risk Type | Description | Example |
|---|---|---|
| **Tiger** | Clear, known, dangerous | "The API dependency from Team X isn't ready" |
| **Elephant** | Large, obvious, but everyone avoids discussing | "We all know the tech debt makes this 3x harder" |
| **Paper Tiger** | Looks scary but actually manageable | "The new framework seems complex but we have docs" |

5. **Mitigation planning**: For each Tiger and Elephant, assign:
   - **Owner**: Who will monitor this risk?
   - **Trigger**: What signal tells us this risk is materializing?
   - **Mitigation**: What do we do if it happens?
   - **Prevention**: What can we do NOW to reduce likelihood?

### Pre-Mortem Output Template
```
PRE-MORTEM: Sprint [N] -- [Sprint Goal]
Date: [Date]

TIGERS (high probability, high impact)
1. [Risk] -- Owner: [Name] -- Mitigation: [Plan]
2. [Risk] -- Owner: [Name] -- Mitigation: [Plan]

ELEPHANTS (known but undiscussed)
1. [Risk] -- Owner: [Name] -- Mitigation: [Plan]

PAPER TIGERS (manageable with preparation)
1. [Risk] -- Why it's manageable: [Reason]

PREVENTION ACTIONS (do before sprint starts)
1. [Action] -- Owner: [Name] -- Due: [Date]
```

---

## Mode C: Retrospective

### Format Selection Guide

| Format | Best When | Duration | Focus |
|---|---|---|---|
| **Start/Stop/Continue** | Default for routine sprints | 45 min | Actionable behavior changes |
| **4Ls** (Loved/Learned/Lacked/Longed for) | After milestones or releases | 60 min | Emotional and educational reflection |
| **Sailboat** (Wind/Anchor/Rocks) | Teams stuck in repetitive patterns | 60 min | Metaphor breaks formulaic thinking |
| **Mad/Sad/Glad** | After difficult or emotional sprints | 45 min | Surfaces personal frustrations safely |
| **Starfish** (More/Less/Start/Stop/Keep) | Teams with nuanced process issues | 60 min | Granular process tuning |
| **Data-Driven** | Mature teams with metrics | 60 min | Ground discussion in facts, not feelings |

### Retrospective Facilitation Guide
1. **Set the stage** (5 min): Establish safety. "What's said here stays here. We're improving the process, not blaming people."
2. **Gather data** (15 min): Use chosen format. Silent writing first, then share.
3. **Generate insights** (15 min): Group items. Ask "Why?" for each cluster. Identify root causes.
4. **Decide what to do** (10 min): Pick 1-2 specific, measurable actions. Assign owners and due dates.
5. **Close** (5 min): Quick round -- one word about how you feel about next sprint.

### Action Item Quality
Every retro action must be:
- **Specific**: "Add 15-min dependency check to Monday standup" not "communicate better"
- **Owned**: One person responsible (not "the team")
- **Time-bound**: Completed by specific date or reviewed at next retro
- **Measurable**: How will we know it worked?

### Anti-Pattern Detection
Flag if retros show these patterns:
- Same issues appear sprint after sprint (actions aren't working or aren't being implemented)
- Only one or two people contribute (psychological safety issue)
- All feedback is positive (team isn't being honest)
- Actions are never reviewed (retro is theater, not improvement)

---

## Mode D: Sprint Demo

### Demo Planning
- **Audience**: Who is attending? (Executives, stakeholders, users, other teams)
- **Goal**: Gather feedback, not broadcast status
- **Duration**: 20-30 minutes maximum
- **Format**: Story-driven (user scenario), not feature-list driven

### Demo Structure
1. **Sprint goal reminder** (2 min): "This sprint we set out to [goal]. Here's what we achieved."
2. **User story walkthrough** (15-20 min): Demo each completed story as a user scenario
   - "As a [user], I was trying to [goal]..."
   - Show the before/after experience
   - Highlight the decision-making behind trade-offs
3. **Metrics impact** (3 min): If available, show early signals of metric movement
4. **Feedback gathering** (5-10 min): Structured questions, not open floor
   - "What surprised you?"
   - "What concerns you?"
   - "What would you change?"
5. **What didn't ship and why** (2 min): Transparency on de-scoped items

### Post-Demo Follow-Up
- Document all feedback received
- Update backlog with new items from feedback
- Communicate decisions back to stakeholders: "Based on your feedback, we are planning to..."
- Track feedback influence on next sprint planning

---

## Mode E: Release Notes

### Release Notes Principles (Intercom approach)
- **Benefit-first, not feature-first**: "Ship 50% faster" not "Added caching layer"
- **Customer language, not engineering language**: Translate technical changes into user value
- **Only noteworthy changes**: Skip minor bug fixes and internal improvements
- **Consistent cadence**: Set expectations for when release notes appear
- **Scannable format**: Users should understand what changed in 15 seconds

### Transformation Table

| Engineering Language | Customer Language |
|---|---|
| "Implemented caching layer for API responses" | "Dashboards now load 3x faster" |
| "Refactored authentication module" | "Login is now more reliable with fewer errors" |
| "Added webhook support for event notifications" | "Get real-time alerts in Slack when things change" |
| "Fixed race condition in concurrent writes" | "Your data now saves correctly even when multiple people edit at once" |
| "Upgraded database to PostgreSQL 16" | (Don't include -- no user impact) |

### Release Note Template
```
[Product Name] -- [Date] Release

NEW
[Benefit headline]: [1-2 sentence description of what changed and why it matters]

IMPROVED
[Benefit headline]: [What's better and how it helps]

FIXED
[Problem that was affecting users]: [How it's resolved]

WHAT'S NEXT
[Brief preview of upcoming changes to set expectations]
```

---

## Mode F: Sprint Health Check

### Core Metrics to Track

| Metric | What It Measures | Healthy Range | Warning Signs |
|---|---|---|---|
| **Velocity** | Work completed per sprint | Stable within 20% of 3-sprint average | Declining or wildly variable |
| **Predictability** | % of committed work delivered | >85% | <70% consistently |
| **Cycle Time** | Time from start to done for one item | Consistent and shortening | Lengthening or high variance |
| **Throughput** | Items completed per sprint | Stable or increasing | Declining without explanation |
| **WIP** | Items in progress simultaneously | At or below WIP limit | Consistently exceeds limit |
| **Escaped Defects** | Bugs found after release | Declining trend | Increasing per sprint |
| **Sprint Goal Hit Rate** | Did the team achieve the sprint goal? | >80% of sprints | <60% of sprints |

### Health Check Questions
- Is velocity stable? (If not, why? Scope changes? Team changes? Estimation drift?)
- Is predictability improving? (If not, are stories too large? Dependencies unresolved?)
- Is cycle time consistent? (If not, are items getting blocked? WIP too high?)
- Are sprint goals being met? (If not, are goals too ambitious? Scope creep?)
- Is the team improving sprint-over-sprint? (Are retro actions having effect?)

### Scope Creep Management
When new requests arrive mid-sprint:

1. **Classify urgency**: Is this a P0 production issue? If not, it can wait.
2. **Trade-off conversation**: "We can add this, but what do we remove?"
3. **Document the change**: Track scope additions and their impact on sprint goal
4. **Pattern detection**: If scope creep happens every sprint, the root cause is likely planning quality or stakeholder expectation management

---

## Definition of Done (DoD) Template

```
A story is DONE when ALL of the following are true:
- [ ] Code is written and peer-reviewed
- [ ] Unit tests pass (coverage meets team standard)
- [ ] Integration tests pass
- [ ] Acceptance criteria verified (manually or automated)
- [ ] No known regressions introduced
- [ ] Documentation updated (if user-facing change)
- [ ] Feature flag configured (if applicable)
- [ ] Analytics events instrumented and verified
- [ ] Accessibility requirements met (WCAG 2.1 AA)
- [ ] Performance within acceptable thresholds
- [ ] Deployed to staging and smoke-tested
- [ ] Product owner has accepted the story
```

Customize per team. Review and update the DoD quarterly.

---

## Remote Sprint Facilitation

### Async-First Practices
- **Pre-planning**: Share sprint goal candidates and prioritized backlog 24 hours before planning
- **Async standups**: Written updates in Slack/Teams by 10am local ("Done yesterday / Doing today / Blocked")
- **Demo recordings**: Record demos for async viewing; gather feedback via comments
- **Retro pre-work**: Share retro prompts 24 hours before; collect written responses before the meeting

### Synchronous Meeting Tips
- **Keep cameras on** for retros and planning (builds trust and reads the room)
- **Use timers** visibly (prevents meetings from expanding)
- **Facilitate actively**: Call on quiet participants by name ("Alex, what do you think?")
- **Use collaborative tools**: Miro, FigJam, or shared docs for real-time input
- **Record decisions, not discussions**: Meeting notes capture actions and decisions only

### Timezone Management
- Rotate meeting times to share the burden across time zones
- Keep synchronous meetings to <60 minutes
- Double-down on async documentation and decision trails
