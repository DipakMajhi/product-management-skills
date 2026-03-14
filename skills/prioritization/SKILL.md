---
name: prioritization
description: "Prioritize a product backlog, feature list, or set of opportunities using structured frameworks. Use this skill when someone needs to rank features, decide what to build next, apply RICE, ICE, MoSCoW, Kano, or other frameworks, or prepare for a PM interview question about prioritization."
---

# Product Prioritization Frameworks

You help PMs make defensible, structured prioritization decisions. The right framework depends on the context.

## Framework Selection Guide

Apply this skill to: $ARGUMENTS


| Situation | Best Framework |
|---|---|
| Large backlog, need a quick cut | ICE Score |
| Need to justify to stakeholders with data | RICE Score |
| Need to balance must-haves vs nice-to-haves | MoSCoW |
| Differentiating between delighters and basics | Kano Model |
| Strategic bets vs optimization | Opportunity Scoring |
| OKR-driven teams | Impact on OKR |

## Framework Details

### RICE Score
**Formula**: (Reach x Impact x Confidence) / Effort
- Reach: How many users affected per quarter?
- Impact: How much will it move the metric? (0.25=minimal, 0.5=low, 1=medium, 2=high, 3=massive)
- Confidence: How sure are we about estimates? (50%=low, 80%=medium, 100%=high)
- Effort: Person-months required

### ICE Score
**Formula**: Impact x Confidence x Ease (1-10 scales)
Faster than RICE, less precise. Good for early-stage triage.

### MoSCoW
- **Must Have**: Without this, the product fails or cannot ship
- **Should Have**: High value, but can be worked around temporarily
- **Could Have**: Nice to have, low impact if dropped
- **Will Not Have (this cycle)**: Explicitly deprioritized

### Kano Model
- **Basic needs (Must-be)**: Absence causes dissatisfaction; presence is expected
- **Performance needs (One-dimensional)**: More is better linearly
- **Excitement needs (Delighters)**: Unexpected features that create delight
- **Indifferent**: Users do not care either way
- **Reverse**: Some users dislike this feature

### Opportunity Scoring (Anthony Ulwick)
Rate each feature: How important is this outcome to users? (1-10) x How satisfied are users currently? (1-10)
Opportunity Score = Importance + max(Importance - Satisfaction, 0)
High importance + low satisfaction = high opportunity.

## Process

1. Confirm: What is being prioritized? (features, opportunities, bets)
2. Confirm: What is the decision context? (what framework fits best)
3. Apply the chosen framework
4. Present ranked list with scores
5. Flag any items where the score seems counterintuitive and explain why

## Output Template

---
**PRIORITIZATION OUTPUT**
**Framework Used:** [Name]
**Input Items:** [Count]

**Ranked List**

| Rank | Item | Score | Key Rationale |
|---|---|---|---|
| 1 | [Item] | [Score] | [One-line rationale] |
| 2 | ... | ... | ... |

**Items Removed from Consideration**
[Any items that were disqualified before scoring, with reason]

**Recommended Top 3 for Next Sprint/Quarter**
[Names with one sentence on why they belong at the top]

**Prioritization Risks**
[Any items where the score may not tell the full story]
---

## Interview Context
Prioritization is the most commonly tested PM interview skill. When asked "How would you prioritize this backlog?", always:
1. Clarify what problem you are solving and what the goal is
2. State the framework you will use and why
3. Apply it explicitly - do not just give a ranked list
4. Acknowledge trade-offs in your choices
