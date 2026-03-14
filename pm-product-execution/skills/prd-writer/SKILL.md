---
name: prd-writer
description: "Write a comprehensive Product Requirements Document (PRD) for any feature or product. Use this skill when someone needs to create a PRD, product spec, feature brief, or requirements document. Also use when someone asks how to write a PRD, what sections a PRD should have, or wants to review and improve an existing PRD."
---

# PRD Writer

You write clear, complete, and actionable PRDs that engineers, designers, and stakeholders can work from without needing constant clarification.

## PRD Principles

Apply this skill to: $ARGUMENTS


A good PRD:
- States the problem before the solution
- Is specific about success criteria - not "improve engagement" but "increase day-7 retention from 28% to 35%"
- Contains enough detail for engineers to estimate accurately
- Documents decisions and trade-offs, not just requirements
- Is a living document, not a one-time artifact

A bad PRD:
- Jumps straight to features without explaining why
- Uses vague language ("simple", "fast", "easy to use")
- Lists features as requirements without user stories
- Has no success metrics
- Does not address edge cases or out-of-scope items

## Standard PRD Structure (8 Sections)

### Section 1: Problem Statement
- What problem are we solving and for whom?
- Evidence that this problem exists and matters (data, quotes, research)
- Current user behavior and workarounds

### Section 2: Goals and Success Metrics
- Primary goal (the outcome we are optimizing for)
- Success metric with current baseline and target
- Secondary metrics we will watch
- Counter-metrics (what we should NOT hurt)

### Section 3: User Stories and Use Cases
- Primary use case (most common, most important)
- Secondary use cases
- Edge cases that must be handled
- Out-of-scope use cases (explicit)

### Section 4: Requirements
- Functional requirements (what the product must do) - numbered for traceability
- Non-functional requirements (performance, reliability, accessibility, security)
- Constraints (technical limitations, legal requirements, time constraints)

### Section 5: UX and Design Direction
- Key user flows (describe or reference wireframes/mocks)
- Design principles specific to this feature
- Existing patterns to follow or intentional departures

### Section 6: Technical Considerations
- Known technical constraints or dependencies
- Data requirements (what data must be captured, migrated, or accessed)
- Integration requirements (APIs, third-party services, internal systems)
- Known risks flagged by engineering

### Section 7: Launch Plan
- Target launch date
- Rollout strategy (full launch, beta, feature flag, phased by segment)
- Go-to-market requirements (marketing, comms, support training)

### Section 8: Open Questions and Decisions Log
- Questions still to be answered (with owner and due date)
- Decisions already made (with rationale)

## Process

1. Ask for the feature idea or problem statement if not provided
2. Ask for: target users, success metrics (or help derive them), and any constraints
3. Write the full PRD
4. Flag any sections where you made assumptions that the PM should verify

## Output Template

Use the 8-section structure above. Begin with a header block:

---
**PRODUCT REQUIREMENTS DOCUMENT**
**Feature:** [Name]
**Author:** [If provided]
**Status:** Draft
**Last Updated:** [Today's date]
**Stakeholders:** [If provided]

[8 sections follow]

**Appendix**
[Any supporting data, research links, or reference documents]
---
