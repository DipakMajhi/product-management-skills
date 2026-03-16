---
name: sprint-plan
description: "Plan a sprint including capacity, story selection, and sprint goal. Routes to the sprint-lifecycle skill."
argument-hint: "[list your backlog items and provide team size, sprint length, and any known constraints or dependencies]"
---

# Sprint Plan

This skill routes to **sprint-lifecycle** Mode A (Sprint Planning), which provides a complete sprint planning framework including capacity calculation, story selection, sprint goal writing, and risk identification.

**When to use this:**
- Preparing for a sprint planning meeting with the team
- Calculating realistic capacity before committing to a sprint scope
- Writing a clear, outcome-oriented sprint goal (not just a list of tickets)
- Identifying the riskiest commitments before the sprint starts
- Answering "how would you run a sprint planning?" in PM interviews

**Quick guide by situation:**
- New to Scrum → sprint-lifecycle covers the full Scrum framework with PM-specific guidance at each stage
- Experienced team, need better goals → Focus on sprint goal writing: the goal must be a business outcome, not "complete tickets A, B, C"
- Capacity uncertainty (people out, dependencies) → Capacity calculation with buffer for unplanned work
- Post-planning risk review → After selecting stories, run a pre-mortem on the riskiest commitment

**What sprint-lifecycle Mode A covers:**
- Capacity calculation: team members × available days × focus factor (typically 70%) − planned time off − ceremonies
- Velocity-based planning: using historical data (last 3 sprints) as input, not a target
- Sprint goal writing: outcome-oriented format, single sentence, answers "what will users be able to do after this sprint?"
- Story selection criteria: sprint goal alignment, technical dependencies, definition of ready (DoR) check
- Story sizing calibration: relative estimates, not hours; using reference stories as anchors
- Risk identification: which stories have the highest uncertainty? What are the dependencies?
- Pre-mortem: imagining the sprint failed — what most likely went wrong?
- Definition of Done (DoD) alignment: ensuring the team agrees on what "done" means before committing
- Dependency mapping: cross-team, cross-squad, and external dependencies that could block the sprint

**The skill will:**
1. Ask for team size, sprint length, known absences, and backlog items
2. Calculate available capacity with buffer for unplanned work
3. Help select stories that fit capacity and align to a coherent sprint goal
4. Write the sprint goal as a clear business outcome
5. Identify the 2-3 riskiest commitments
6. Offer to run a pre-mortem on those risks
7. Deliver the sprint plan document: goal, committed stories, capacity breakdown, risks, dependencies

Load the full skill: **sprint-lifecycle**

Apply your sprint context to: $ARGUMENTS
