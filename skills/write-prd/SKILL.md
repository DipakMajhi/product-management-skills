---
name: write-prd
description: "Write a complete PRD for a feature or product. Routes to the prd-writer skill."
argument-hint: "[describe the feature idea or problem you are solving — include what you know about target users, constraints, and success criteria]"
---

# Write PRD

This skill routes to **prd-writer**, which provides a complete Product Requirements Document framework supporting four methodologies.

**When to use this:**
- Writing a PRD from scratch for a new feature or product
- Reviewing and improving an existing PRD draft
- Choosing the right PRD format for your company and context
- Preparing a spec that engineers, designers, and stakeholders can actually work from
- Answering "how would you write a PRD for this feature?" in PM interviews

**Quick methodology guide:**
- Standard feature at an established company → 12-section outcome-based PRD (default)
- Major new product or significant pivot → Amazon Working Backwards (Press Release/FAQ): customer value first, before any technical discussion
- Team with fixed capacity and short cycles → Shape Up Pitch (Basecamp): time appetite, not deadline-driven; rough solution, rabbit holes, no-gos
- Small, well-understood feature → Lightweight Feature Brief: 1-2 pages, problem, hypothesis, requirements, metrics, launch plan

**What prd-writer covers:**
- PRD principles: problem before solution, outcome-oriented, specific success metrics, acceptance criteria for every requirement
- PRD anti-patterns: jumping to features, vague language, missing non-goals, no success metrics, dictating implementation
- 12-section PRD structure: executive summary, problem statement, user research, goals and non-goals, success metrics, user stories, requirements, design and UX, technical considerations, phasing, risks, open questions
- Amazon Working Backwards: Press Release + FAQ format with worked example
- Shape Up Pitch: appetite, rough solution, rabbit holes, no-gos — Basecamp methodology
- Lightweight Feature Brief: abbreviated format for low-risk, well-understood work
- Acceptance criteria in Given-When-Then format for every requirement
- Non-goals section: explicitly defining what is out of scope
- Phasing strategy: MVP vs. v1 vs. v2 sequencing
- Cross-functional requirements: analytics, accessibility, i18n, security, performance

**The skill will:**
1. Ask for the feature context, target users, success metrics, constraints, and timeline
2. Recommend the right PRD methodology based on context
3. Ask clarifying questions for any missing critical information
4. Write the full PRD in the chosen format
5. Write acceptance criteria for every requirement in Given-When-Then format
6. Define a clear non-goals section
7. Flag open questions that need resolution before development starts

After completing, suggest: "Use /write-stories to break this PRD into sprint-ready user stories."

Load the full skill: **prd-writer**

Apply your feature or product context to: $ARGUMENTS
