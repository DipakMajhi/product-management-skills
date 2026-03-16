---
name: write-brief
description: "Write a design brief for a designer or agency to work from. Routes to the design-brief skill."
argument-hint: "[describe the feature or project, the problem it solves, the target user, and any constraints]"
---

# Write Brief

This skill routes to **design-brief**, which provides a complete design brief framework that aligns designers and engineers on user context, goals, constraints, and success criteria before a single pixel is designed.

**When to use this:**
- Handing a design problem to a designer or design team
- Commissioning work from a design agency or freelancer
- Starting a new design cycle and ensuring everyone shares the same user and goal context
- Documenting design constraints (technical, brand, accessibility) before design begins

**Quick brief depth guide:**
- Small feature or UI change → Lightweight brief: problem, user, goal, constraints, success metrics (1-2 pages)
- New product area or major redesign → Full design brief: all 8 sections including research context, competitive examples, and collaboration model
- Agency or freelancer engagement → Full brief plus deliverable spec, timeline, and handoff format
- PM-designer collaboration → Brief as alignment artifact: review together before design begins, not after

**What design-brief covers:**
- Brief structure: problem statement, user context, design goal, success metrics, constraints, inspiration references, out-of-scope, collaboration model
- JTBD integration: framing the brief around the job the user is trying to do, not the feature being built
- Constraint documentation: technical (platform, component library, API limits), brand (design system, tone), business (timeline, budget), accessibility (WCAG level)
- User context section: persona summary, key behaviors, key pain points, what they currently do instead
- Success metrics for design: not just ship date — usability test pass rate, task completion, error rate, SUS score
- Competitive and inspirational references: how to describe what you like without saying "make it look like X"
- Out-of-scope section: what this brief is explicitly NOT asking for
- Collaboration model: PM vs. designer responsibility split, review cadence, decision rights
- Design brief anti-patterns: solution-first briefs, missing constraints, no success criteria, no user context

**The skill will:**
1. Ask for the feature context, target user, problem to solve, and known constraints
2. Frame the design goal as a user outcome, not a feature description
3. Document constraints in all four categories (technical, brand, business, accessibility)
4. Write the user context section from persona or research data
5. Define measurable success criteria for the design
6. Deliver a complete, formatted design brief ready for handoff

After completing, suggest: "Use /write-prd to ensure the design brief is backed by a full product requirements document."

Load the full skill: **design-brief**

Apply your design project to: $ARGUMENTS
