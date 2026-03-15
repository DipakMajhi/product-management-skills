---
name: prd-writer
description: "Write a comprehensive Product Requirements Document (PRD) for any feature or product. Use this skill when someone needs to create a PRD, product spec, feature brief, or requirements document. Also use when someone asks how to write a PRD, what sections a PRD should have, or wants to review and improve an existing PRD."
---

# PRD Writer

You write clear, complete, and actionable PRDs that engineers, designers, and stakeholders can work from without needing constant clarification.

## PRD Principles

Apply this skill to: $ARGUMENTS


A good PRD:
- States the problem before the solution, grounded in user research and evidence
- Is outcome-oriented: defines the business and user outcome, not just features to build
- Is specific about success criteria: not "improve engagement" but "increase day-7 retention from 28% to 35%"
- Contains enough detail for engineers to estimate accurately without dictating implementation
- Documents decisions and trade-offs, not just requirements
- Explicitly defines non-goals and out-of-scope items (these should exceed goals in early phases)
- Includes acceptance criteria for every requirement in Given-When-Then format
- Is a living document with version history and update cadence, not a one-time artifact

A bad PRD:
- Jumps straight to features without explaining why
- Uses vague language ("simple", "fast", "easy to use") without measurable thresholds
- Lists features as requirements without user stories or acceptance criteria
- Has no success metrics or ties to business OKRs
- Does not address edge cases, error states, or out-of-scope items
- Omits cross-functional requirements (analytics, accessibility, i18n, security)
- Dictates implementation details that should be left to engineering
- Has no phasing strategy (tries to ship everything at once)

## Methodology Selection

Different contexts call for different PRD approaches. Ask the user which fits their situation, or recommend based on context:

### Standard Outcome-Based PRD (Default)
Best for: Feature development at established companies, cross-functional alignment at scale.
Structure: 12-section template below.

### Amazon Working Backwards (PR/FAQ)
Best for: Major new products, significant pivots, zero-to-one launches.
Approach: Write a customer-facing press release (under 1 page) describing the product as if already launched, followed by an FAQ section (up to 5 pages) answering customer and internal stakeholder questions. Forces ruthless focus on customer value before any technical discussion.

### Shape Up Pitch (Basecamp Method)
Best for: Teams with fixed capacity and rapid cycles, scope-limited rather than deadline-driven work.
Approach: Define a specific problem, set a time appetite (how much time this is worth, not a deadline), sketch a rough solution, flag rabbit holes and no-gos, and let the team figure out implementation details within the appetite.

### Lightweight Feature Brief
Best for: Small features, incremental improvements, well-understood problem spaces.
Approach: Abbreviated 1-2 page version covering problem, hypothesis, requirements, success metrics, and launch plan.

## Standard PRD Structure (12 Sections)

### Section 1: Executive Summary
- One-paragraph overview: what we are building, for whom, why now, and the expected business impact
- Link to the strategic objective or OKR this supports

### Section 2: Problem Statement and Research Context
- What problem are we solving and for whom?
- Evidence that this problem exists and matters: user research findings, data analysis, support ticket volumes, competitive pressure, or revenue impact
- Current user behavior and workarounds (how users solve this problem today)
- Link to discovery artifacts: Opportunity Solution Tree, user interview synthesis, survey results
- Size of the opportunity: how many users affected, revenue at stake, strategic importance

### Section 3: Goals, Non-Goals, and Success Metrics
- **Primary goal**: The single outcome we are optimizing for, tied to a business OKR
- **Success metric (OEC)**: Overall Evaluation Criterion with current baseline and target (e.g., "Increase trial-to-paid conversion from 12% to 18% within 90 days of launch")
- **Secondary metrics**: Metrics we will watch to understand the mechanism and detect unintended consequences
- **Guardrail metrics**: Metrics that must NOT degrade (e.g., page load time stays under 2s, support ticket volume does not increase by more than 10%)
- **Non-goals**: What this project explicitly does NOT attempt to achieve. Be specific. Non-goals should outnumber goals, especially in early phases.

### Section 4: User Stories and Use Cases
- **Primary persona**: Who is the main user? Include name, role, key context.
- **Primary use case**: The most common, most important flow. Describe as a user story: "As a [persona], I want to [action] so that I can [outcome]."
- **Secondary use cases**: Less common but supported flows
- **Edge cases that must be handled**: Error states, empty states, boundary conditions, concurrent usage
- **Out-of-scope use cases**: Explicitly list flows we will NOT support and why

### Section 5: Functional Requirements
Number all requirements for traceability (FR-1, FR-2, etc.).

For each requirement, include:
- **Description**: What the product must do
- **Priority**: Must Have / Should Have / Could Have (MoSCoW)
- **Acceptance Criteria** (Given-When-Then format):
  - Given [precondition or context]
  - When [user action or system event]
  - Then [expected system response or outcome]
- **Notes**: Any constraints, dependencies, or design considerations

Example:
- FR-1: User can filter search results by date range
  - Priority: Must Have
  - Given the user is on the search results page with 10+ results
  - When the user selects a start date and end date from the date picker
  - Then only results within that date range are displayed, the result count updates, and the active filter is shown as a removable chip
  - Notes: Default range is "Last 30 days". Empty state needed if no results match the filter.

### Section 6: Non-Functional Requirements
- **Performance**: Response time targets (e.g., search returns results in under 500ms at P95), throughput, concurrent user targets
- **Reliability**: Uptime SLA, graceful degradation behavior, retry logic
- **Security**: Authentication requirements, data encryption, access control, audit logging
- **Accessibility**: WCAG 2.1 AA compliance minimum, screen reader compatibility, keyboard navigation, color contrast ratios, text scaling support
- **Internationalization (i18n)**: Languages supported at launch, text expansion handling (German, Japanese), date/time/currency formatting, RTL language support if applicable
- **Scalability**: Expected user growth, data volume projections, infrastructure requirements
- **Privacy and Compliance**: GDPR, CCPA, SOC 2, HIPAA (as applicable), data retention policies

### Section 7: Analytics and Instrumentation Plan
- **Events to track**: List specific analytics events that must be instrumented to measure success metrics
- **User properties to capture**: Attributes needed for segmentation and analysis
- **Funnel definition**: The conversion funnel this feature creates or modifies, with expected drop-off points
- **Dashboard requirements**: What the monitoring dashboard should show post-launch
- **A/B test plan**: If launching behind a feature flag, define the experiment parameters (see ab-testing skill)

### Section 8: UX and Design Direction
- Key user flows (describe step-by-step or reference wireframes/mocks)
- Design principles specific to this feature
- Existing patterns to follow or intentional departures with justification
- Error state designs and empty state designs
- Responsive behavior and mobile considerations
- Loading states and skeleton screens for async operations

### Section 9: Technical Considerations
- Known technical constraints or dependencies
- Data model changes (new tables, schema migrations, data relationships)
- API design considerations (new endpoints, breaking changes, versioning)
- Integration requirements (third-party services, internal systems, webhooks)
- Infrastructure requirements (new services, scaling needs, caching strategy)
- Migration plan if replacing existing functionality
- Known technical risks flagged by engineering with mitigation approaches

### Section 10: Phasing and Scope Management

**Phase 0 - MVP (Validates demand and core hypothesis)**
- Scope: Minimum feature set that tests the primary desirability assumption
- Success criteria: Specific metric thresholds that justify continued investment
- Timeline: [Target]
- What is explicitly excluded and why

**Phase 1 - V1 (Earns trust for repeat usage)**
- Scope: Features that make the product reliable and complete enough for daily use
- Success criteria: Retention and engagement thresholds
- Timeline: [Target]
- Dependencies on Phase 0 learnings

**Phase 2 - V2 (Scales and differentiates)**
- Scope: Features that drive growth, expansion, and competitive differentiation
- Success criteria: Business metrics (revenue, market share, NPS)
- Timeline: [Target]
- Dependencies on Phase 1 learnings

For each phase, clearly define: what is IN scope, what is OUT of scope, and what success looks like before advancing to the next phase.

### Section 11: Launch Plan
- Rollout strategy: Feature flag, beta group, percentage rollout, full launch
- Rollout audience: Who gets access first and why
- Go-to-market requirements: Marketing assets, help docs, support team training, changelog entry
- Rollback plan: How to revert if critical issues arise post-launch
- Post-launch monitoring: First 24 hours, first week, first month checkpoints
- Success review date: When we will evaluate whether to advance to the next phase

### Section 12: Open Questions, Decisions Log, and Risks

**Open Questions**
| Question | Owner | Due Date | Status |
|---|---|---|---|
| [Question] | [Name] | [Date] | Open / Resolved |

**Decisions Made**
| Decision | Rationale | Date | Decided By |
|---|---|---|---|
| [Decision] | [Why this choice over alternatives] | [Date] | [Name/Group] |

**Risk Register**
| Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|
| [Risk description] | High/Med/Low | High/Med/Low | [Mitigation plan] | [Name] |

## AI/ML Feature Addendum (Include When Applicable)

When the feature involves AI or machine learning:
- **Model requirements**: Which model(s), inference latency targets, accuracy thresholds, confidence score handling
- **Cost implications**: Estimated cost per inference, monthly compute budget, cost optimization strategy
- **Failure modes**: What happens when the model produces low-confidence results, incorrect outputs, or fails entirely
- **Human oversight**: Escalation paths, human-in-the-loop review triggers, override mechanisms
- **Data requirements**: Training data sources, annotation needs, data freshness requirements, bias considerations
- **Transparency**: How users are informed that AI is being used, explanation/attribution requirements
- **Evaluation plan**: How model quality is measured and monitored post-launch (precision, recall, F1, user satisfaction)

## Process

1. Ask for the feature idea or problem statement if not provided
2. Ask for: target users, success metrics (or help derive them), constraints, and any existing research
3. Determine the appropriate methodology (Standard PRD, Working Backwards, Shape Up, Lightweight Brief)
4. Write the full PRD using the selected structure
5. Flag any sections where assumptions were made that the PM should verify
6. Highlight the top 3 risks and top 3 open questions that need resolution before development begins

## Output Template

Use the selected methodology's structure. For the standard PRD, begin with a header block:

---
**PRODUCT REQUIREMENTS DOCUMENT**
**Feature:** [Name]
**Author:** [If provided]
**Status:** Draft | In Review | Approved | In Development
**Version:** 1.0
**Last Updated:** [Today's date]
**Stakeholders:** [If provided]
**OKR Alignment:** [Which team/company OKR this supports]
**Target Phase:** [MVP / V1 / V2]

[12 sections follow]

**Appendix**
- Supporting research data, interview synthesis, or survey results
- Wireframes or design mockups (linked or described)
- Competitive analysis references
- Related PRDs or technical design documents
---

## PRD Review Checklist

Before finalizing, verify the PRD passes these checks:

- [ ] Problem statement is grounded in evidence, not assumptions
- [ ] Success metrics have specific baselines and targets
- [ ] Every functional requirement has acceptance criteria in Given-When-Then format
- [ ] Non-goals are explicitly stated and outnumber goals for early phases
- [ ] Non-functional requirements cover performance, security, accessibility, and i18n
- [ ] Analytics instrumentation plan is included with specific events
- [ ] Phasing is defined with clear criteria for advancing between phases
- [ ] Edge cases and error states are addressed
- [ ] Open questions have owners and due dates
- [ ] Top risks have mitigation plans
- [ ] Cross-functional dependencies are identified
- [ ] Launch plan includes rollback strategy
