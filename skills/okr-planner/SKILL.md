---
name: okr-planner
description: "Write well-structured OKRs for a product team or individual PM. Use this skill when someone needs to draft OKRs for a quarter, review and improve existing OKRs, cascade company OKRs to a team level, understand what makes a good Key Result, run an OKR grading session, or set up the CFR operating cadence around OKRs."
argument-hint: "[describe your team's goal or the company OKR you need to cascade from, the planning period, and any existing OKR drafts you want reviewed]"
---

# OKR Planner

You write focused, measurable OKRs that drive behavior, create accountability, and connect daily work to company strategy. You also help teams avoid the most common OKR failure modes: task KRs, vanity KRs, cascades that are just copies of the parent, and OKRs that nobody looks at after the planning meeting.

Apply this skill to: $ARGUMENTS

---

## OKR Fundamentals

### What OKRs Are

OKRs (Objectives and Key Results) are a goal-setting framework popularized at Intel by Andy Grove and scaled at Google by John Doerr. They separate direction from measurement:

**Objective**: A qualitative, inspirational statement of *what* you want to achieve. It should be:
- Memorable and motivating — not bureaucratic ("Improve product" is bad; "Make onboarding so good users never call support" is better)
- Directional but not prescriptive — it points where to go, not how
- Achievable within the OKR cycle (quarter or half-year)
- Meaningful: if you achieve it, it should feel like genuine progress

**Key Results**: 2-4 quantitative measures that define *what success on the Objective looks like*. Each KR should:
- Start with a verb (Increase, Decrease, Launch, Achieve, Reduce, Grow)
- Have a clear metric with a from-X-to-Y format where possible
- Be measurable without ambiguity at the end of the period
- Represent an *outcome*, not a task or activity
- Have a named owner

### OKR vs. KPI vs. Project

| Element | Purpose | Example |
|---|---|---|
| **OKR** | Stretchy, time-bound goals for a period | "Increase D7 retention from 28% to 40%" (Q1) |
| **KPI** | Ongoing health metrics, always tracked | "D7 retention is 28%" (current state) |
| **Project / Initiative** | Activity or deliverable that enables an OKR | "Redesign onboarding flow" (a task, not a KR) |

---

## The Ambitious Calibration

OKRs should be ambitious. John Doerr calls this "moonshot thinking": aim for 10x, not 10%.

| Score at End of Cycle | Interpretation |
|---|---|
| 1.0 (100%) | Either the KR was too easy, or you had an exceptional quarter |
| 0.7 (70%) | This is the success zone — good ambition, strong progress |
| 0.5 (50%) | Acceptable, but review whether the target was ambitious enough |
| < 0.3 | Something went significantly wrong — root cause it |

**Critical principle**: If your team consistently scores 1.0 on everything, your OKRs are not ambitious enough. If you consistently score 0.2, they are unrealistic. Calibrate until 0.7 feels achievable but requires real work.

---

## Common OKR Mistakes

### Mistake 1: Task KRs (the most common failure)
**Wrong**: "Launch the redesigned onboarding flow by March 15"
**Why it fails**: This is a milestone, not an outcome. Launching doesn't tell you if it worked.
**Fix**: "Launch redesigned onboarding flow by March 15, increasing D7 retention from 28% to 38%"

### Mistake 2: Vanity KRs
**Wrong**: "Publish 10 blog posts about our product"
**Why it fails**: 10 blog posts is an activity. It says nothing about whether anything improved.
**Fix**: "Increase organic traffic from content by 40% (baseline: 12K monthly visitors)"

### Mistake 3: Too Many KRs
**Wrong**: 7 Key Results for one Objective
**Why it fails**: Loses focus. People don't know what to prioritize.
**Fix**: Maximum 4 KRs per Objective. If you have more, you probably have two Objectives.

### Mistake 4: Activity-Only KRs
**Wrong**: "Run 20 customer interviews"
**Why it fails**: You could run 20 bad interviews and learn nothing. Activity ≠ outcome.
**Fix**: "Identify 3 validated high-priority opportunities from 20+ customer interviews"

### Mistake 5: Objectives That Are Actually Projects
**Wrong Objective**: "Redesign the onboarding flow"
**Why it fails**: This is a project, not an aspiration. It has no inspirational quality.
**Fix**: "Eliminate onboarding as a reason customers choose competitors"

### Mistake 6: Sandbagging Key Results
Deliberately low targets to ensure 1.0. Destroys OKR culture and misleads leadership.
Signs of sandbagging: teams always hit 1.0, targets barely move from baseline.

### Mistake 7: OKRs Divorced from Strategy
Key Results that move metrics nobody actually cares about, or that aren't connected to company priorities.
Fix: Every Objective should map to a company-level OKR or strategic initiative.

---

## Cascading OKRs

Cascading ensures team OKRs contribute to company OKRs. Cascading does NOT mean copying the company OKR downward.

### How to Cascade Correctly

1. Start with the company or department OKR
2. Ask: "What is our team's specific contribution to this company KR being achieved?"
3. Define the team OKR as that contribution — not a copy of the parent
4. Ensure the team's KR, if achieved, would meaningfully move the company KR

### Cascade Example

**Company OKR:**
- Objective: Become the market leader in SMB project management
- KR: Grow revenue from SMB segment from $2M to $3M MRR

**Product Team OKR (cascaded correctly):**
- Objective: Make the product so easy to adopt that SMBs don't need sales help
- KR 1.1: Increase self-serve activation rate from 35% to 60%
- KR 1.2: Reduce time-to-first-value from 4 days to 1 day for SMB sign-ups
- KR 1.3: Grow PLG-sourced MRR from $200K to $600K

**What's wrong with this cascade (copied OKR):**
- Objective: Grow SMB revenue
- KR: Contribute to $3M MRR target ← meaningless; doesn't describe what the product team does

### Alignment Check
After writing team OKRs, ask: "If we hit all our KRs, would it materially contribute to the company KRs?" If the answer is "probably not directly," the cascade is broken.

---

## OKR Types and Contexts

### Committed OKRs vs. Aspirational OKRs (Google's distinction)

| Type | Description | Expected Score | Example |
|---|---|---|---|
| **Committed** | Must achieve. Failure requires explanation. | 1.0 | "Maintain 99.9% uptime" |
| **Aspirational** | Stretch goal. 0.7 is success. | 0.6-0.7 | "Grow NPS from 32 to 50" |

Most product OKRs should be aspirational. Infrastructure OKRs and compliance goals are often committed.

### Individual OKRs vs. Team OKRs

| Level | Owner | Cadence | Connected to |
|---|---|---|---|
| Company | CEO / Leadership | Annual + Quarterly | Mission + strategy |
| Department | VP / Director | Quarterly | Company OKRs |
| Team | Product/Eng lead | Quarterly | Department OKRs |
| Individual | PM / IC | Quarterly | Team OKRs |

Individual OKRs should reflect what only that person can move — not a diluted copy of team OKRs.

---

## OKR Quality Test (apply before finalizing)

For each Key Result, answer:

| Test | Question | Pass condition |
|---|---|---|
| Outcome test | Is this a result, not an activity? | "Users retained" vs. "emails sent" |
| Measurability test | Can we unambiguously measure this? | Clear metric, clear data source |
| Baseline test | Do we know the current number? | "From X to Y" — X is known |
| Ownership test | Is there one clear owner? | Not "the team" — a person |
| Ambition test | Does this require real effort? | Hitting 0.7 should not be easy |
| Independence test | Is this KR mostly in our control? | Depends on our team's actions, not external luck |
| Significance test | Does hitting this actually matter? | Someone would notice if we didn't hit it |

---

## OKR Grading and Retrospective

At the end of each OKR cycle:

### 1. Score Each KR (0.0 – 1.0)
- 1.0: Fully achieved
- 0.7: Strong progress, broadly achieved
- 0.5: Partial progress
- 0.3: Limited progress
- 0.0: No progress or deprioritized

### 2. Objective Score = Average of KR Scores

### 3. Retrospective Questions
- Which KRs underperformed? What were the root causes?
- Which KRs we didn't achieve — did they still deserve to be OKRs?
- What did we deprioritize to focus on OKRs — was that right?
- Which KR had the biggest impact? What does that tell us?
- What would we do differently for next quarter?

---

## CFR Operating Cadence (John Doerr)

OKRs only work if there is a regular operating cadence. Doerr calls this CFR: Conversations, Feedback, Recognition.

### Weekly Check-In (15 minutes, synchronous or async)

For each OKR:
1. **Confidence score**: "How confident are you this KR will be achieved this quarter?" (1-10)
2. **Progress update**: What moved since last week?
3. **Blocker**: What is the one thing most likely to prevent this KR from being hit?
4. **Ask**: What do you need to unblock it?

### Monthly OKR Review (30-60 minutes)

- Review each KR's trend line: are we on track, ahead, behind?
- For KRs at risk: root cause analysis + revised plan
- Decide if any OKR needs to be deprioritized (life happens)
- Celebrate progress — recognition is the "R" in CFR

### End-of-Quarter Retrospective

- Score and grade all OKRs
- Retrospective discussion: see grading section above
- Inform next quarter's OKR planning with lessons learned

---

## OKR Output Template

---
**TEAM OKRs: [Team Name] — [Quarter/Period]**

**Strategic Alignment:** [Which company or department OKR do these support?]

**Team Context:** [1-2 sentences on the team's focus area and why these OKRs now]

---

**Objective 1:** [Inspiring, qualitative statement]

| Key Result | Baseline | Target | Owner | Type |
|---|---|---|---|---|
| KR1.1: [Measurable outcome] | [Current X] | [Target Y] | [Name/Role] | Aspirational/Committed |
| KR1.2: [Measurable outcome] | [Current X] | [Target Y] | [Name/Role] | Aspirational/Committed |
| KR1.3: [Measurable outcome] | [Current X] | [Target Y] | [Name/Role] | Aspirational/Committed |

**Key initiatives:** *(not KRs — just work that will drive these KRs)*
- [Initiative 1]
- [Initiative 2]

---

**Objective 2:** [Inspiring, qualitative statement]

| Key Result | Baseline | Target | Owner | Type |
|---|---|---|---|---|
| KR2.1: ... | | | | |
| KR2.2: ... | | | | |

---

**OKR Review Notes:**
- [KRs that read like tasks with suggested fixes]
- [Ambition calibration assessment]
- [Missing baselines that need to be established]
- [Alignment check: do these OKRs cascade from the right company OKRs?]

---

## Worked Example: Product Team OKRs

**Context:** 6-person product team at a B2B SaaS company. Company OKR: Reduce churn from enterprise accounts from 12% to 8% annually.

---

**Objective 1:** Make enterprise onboarding fast enough that customers see value before they doubt the purchase

| Key Result | Baseline | Target | Owner | Type |
|---|---|---|---|---|
| KR1.1: Increase enterprise time-to-first-value from 14 days to 4 days | 14 days | 4 days | Sarah (PM) | Aspirational |
| KR1.2: Increase onboarding completion rate from 45% to 75% | 45% | 75% | Sarah (PM) | Aspirational |
| KR1.3: Reduce implementation support tickets in first 30 days by 40% | 120/month | 72/month | James (PM) | Aspirational |

**Key initiatives:**
- Redesign onboarding flow (UX + Eng, 6 weeks)
- Build self-serve configuration templates for top 5 use cases
- Create in-app guided tours for core workflows

---

**Objective 2:** Give customer success teams visibility they need to save at-risk accounts before they decide to leave

| Key Result | Baseline | Target | Owner | Type |
|---|---|---|---|---|
| KR2.1: Launch account health dashboard used by 80% of CS team weekly | 0 (no dashboard) | 80% adoption | James (PM) | Committed |
| KR2.2: Enable CS to identify at-risk accounts 30+ days before renewal | 0 days lead time | 30+ days | James (PM) | Aspirational |
| KR2.3: Reduce churn among accounts flagged as at-risk by 25% | unknown (new capability) | 25% reduction | Sarah (PM) | Aspirational |

---

## Workflow

1. **Gather context**: Ask for the company/department OKRs to cascade from, the team's focus area, and the planning period.
2. **Define Objectives first**: Write 2-3 aspiring Objectives before touching Key Results.
3. **Write Key Results**: For each Objective, draft 2-4 KRs in from-X-to-Y format with owners.
4. **Apply quality test**: Check each KR against the 7-point test and flag issues.
5. **Check cascade**: Verify each Objective traces to a company or department OKR.
6. **Calibrate ambition**: Would 0.7 require real effort? Would 1.0 feel like an exceptional quarter?
7. **Finalize and format**: Deliver the completed OKR document with the output template.
8. **Set up CFR**: Propose the weekly check-in structure and end-of-quarter grading approach.

After completing, suggest: "Use /define-metrics to ensure your KRs are connected to the right North Star and input metrics."
