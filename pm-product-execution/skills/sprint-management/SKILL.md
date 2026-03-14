---
name: sprint-management
description: "Plan sprints, run retrospectives, and write release notes. Use this skill for sprint planning with capacity estimation, retrospective facilitation, writing user-facing release notes from a list of tickets, or pre-mortem risk analysis before a launch."
---

# Sprint Management Toolkit

## Sprint Planning

Apply this skill to: $ARGUMENTS


### Capacity Estimation
1. Count the number of engineers and their availability this sprint (accounting for holidays, on-call, and planned time off)
2. Apply a productivity factor: typically 70-80% of raw available days go to sprint work (the rest is meetings, reviews, interruptions)
3. Convert to story points or days per team member
4. Reserve 10-15% capacity for unplanned work and bug fixes

### Story Selection
1. Start with carry-over from the previous sprint
2. Add highest-priority items from the backlog
3. Ensure the selected stories have clear acceptance criteria before committing
4. Verify dependencies are resolved before adding to sprint
5. Check that the sprint has at least one shippable outcome (not all work-in-progress)

### Sprint Goal
Write a one-sentence sprint goal that describes the user value delivered if all commitments are met. "By end of sprint, a first-time user can complete onboarding without support intervention" is a good sprint goal. "Complete 12 stories" is not.

## Sprint Retrospective

### Formats

**Start / Stop / Continue**
- Start: What should we begin doing that we have not tried?
- Stop: What should we stop doing because it is not serving us?
- Continue: What is working and should be protected?

**4Ls**
- Liked: What went well?
- Learned: What did we learn?
- Lacked: What was missing?
- Longed For: What do we wish we had?

**Sailboat**
- Wind (driving forward): What helped us?
- Anchor (holding back): What slowed us down?
- Rocks (risks ahead): What could hurt us next sprint?
- Island (destination): Are we aligned on the goal?

### Retro Facilitation Rules
- Everyone contributes before discussion starts (use async input to avoid groupthink)
- Focus on process and systems, not individuals
- Every retro should produce at least one specific action item with an owner and due date
- Start the next retro by reviewing the action items from the last one

## Release Notes

Release notes should be written for end users, not engineers. Transform ticket titles into user-facing language.

Format:
- **What changed**: The feature or fix in user language
- **Why it matters**: The benefit to the user
- **How to use it**: Brief instructions if needed (for significant features)

## Pre-Mortem

Before a major launch, run a pre-mortem:
1. Imagine it is 6 months from now and the launch failed badly. What went wrong?
2. Brainstorm all possible failure modes (technical, adoption, market, operational)
3. Classify each as: Tiger (certain to happen if unaddressed), Elephant (high impact, being ignored), Paper Tiger (feels scary but low risk)
4. For each Tiger: define a mitigation plan with owner and deadline

## Output Templates

### Sprint Plan
---
**SPRINT [N] PLAN**
**Dates:** [Start] - [End]
**Sprint Goal:** [One sentence]
**Team Capacity:** [X story points / X dev-days]
**Stories Committed:** [N] | Total points: [X]

| Story | Points | Owner | Dependencies |
|---|---|---|---|
| [Story name] | X | [Name] | [None / Story ID] |

**Risks This Sprint**
[Any stories at risk of not completing and why]
---

### Release Notes
---
**RELEASE NOTES: [Version or Date]**

**New Features**
- [Feature]: [User-facing description of what it does and why it is useful]

**Improvements**
- [Improvement]: [What changed and how it benefits users]

**Bug Fixes**
- [Fix]: [What was broken and what users will notice now]
---

### Pre-Mortem
---
**PRE-MORTEM: [Launch Name]**
**Launch Date:** [Date]

**Failure Scenarios**
| Scenario | Category | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|---|
| [Scenario] | Tiger/Elephant/Paper Tiger | H/M/L | H/M/L | [Plan] | [Name] |

**Top 3 Mitigations to Execute Before Launch**
1. [Action - Owner - Deadline]
2. ...
---
