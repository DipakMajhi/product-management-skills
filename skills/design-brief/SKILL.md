---
name: design-brief
description: "Write a design brief or design spec that a product designer can work from. Use this skill when a PM needs to hand off a feature to a designer, create a design brief for a contractor, document design requirements, or write the design section of a PRD."
argument-hint: "feature name, user problem, or design goal you want to communicate"
---

# Design Brief Writer

A design brief gives a designer the context, constraints, and success criteria they need to produce the right design without prescribing the solution. The best briefs answer all ambiguous questions while leaving design decisions entirely to the designer.

Apply this skill to: $ARGUMENTS

## What Goes in a Design Brief

A good design brief answers these seven questions:

1. **Why are we building this?** (User problem and business goal - the motivation)
2. **Who are we designing for?** (Primary persona with relevant behavioral context)
3. **What must the design accomplish?** (Functional requirements expressed as user outcomes, not features)
4. **What constraints exist?** (Technical, time, brand, platform, accessibility, performance)
5. **What does success look like?** (How will we measure if the design works?)
6. **What is out of scope?** (Explicitly exclude scope to prevent scope creep)
7. **What context should the designer have?** (Research insights, competitive examples, design system patterns)

## Design Brief Types

Not all briefs are identical. Choose the type that matches your situation:

### Exploratory/Discovery Brief (for new problems)

Use when: You are exploring a new problem space; solution direction is unclear

Emphasis:
- Problem is well-researched but solution is open
- Designer has freedom to explore multiple directions
- Expect multiple rounds of exploration before convergence
- Success = learning about what is possible, not shipping a design

Structure:
- Problem statement (strong)
- User research (quotes, behavioral data, pain points)
- Competitive landscape (what exists, what is missing)
- Success criteria (what insights we seek)
- Timeline expectation (exploration phase = 2-3 weeks typically)

### Execution Brief (for defined solutions)

Use when: You know what problem you are solving and how; designer is executing a defined direction

Emphasis:
- Solution direction is clear from previous work (exploration, prototyping, stakeholder alignment)
- Designer needs to deliver high-fidelity execution
- Speed matters; limited design iteration expected
- Success = shipping a design that meets requirements

Structure:
- Problem statement (concise reference)
- Functional requirements (detailed list of user actions)
- Design system requirements (what components to use)
- Competitive reference (inspiration for execution quality bar)
- Timeline (clear deadline for first review)
- Technical constraints (specific limitations that affect execution)

### Redesign Brief (for existing features)

Use when: Redesigning existing features to improve UX, update visual design, or fix problems

Emphasis:
- Current state is understood; document what is broken
- Designer understands legacy constraints
- Change should be improvement not change for change sake
- Success = measurable improvement against current state

Structure:
- Current state description (what exists now)
- Problems with current state (from research, user feedback, analytics)
- Constraints from legacy system (what cannot change)
- Design goals (what specific aspects improve?)
- Examples of good redesigns (how competitors evolved similar features)
- A/B test criteria (how you measure improvement)

## Jobs-to-be-Done Integration for Framing User Needs

Jobs theory provides a more structured way to frame problems than personas alone:

**The Job Framework:**
People do not want products; they want to make progress on a meaningful job in their lives.

**Job anatomy:**
- Functional job (what task do users want to accomplish?)
- Emotional job (how do they want to feel while doing it? Or after?)
- Social job (what impression do they want to make on others?)

**Example: Email collaboration feature**
- Functional job: "Respond to emails without leaving conversation context" or "Know team member is drafting without interrupting them"
- Emotional job: "Feel confident that our team is aligned" or "Avoid feeling like I am bothering colleagues with constant messages"
- Social job: "Be seen as responsive and organized" or "Build reputation for thoughtful communication (not reactive)"

**In design brief:**
Instead of: "Design a way for team members to collaborate on email replies"
Frame it as: "Help team members draft email responses together without duplicating effort or feeling like they are interrupting each other"

This job-framed brief gives designer much better direction than feature-framed brief.

## Design Principle Selection Guidance

Design principles guide trade-off decisions; include 2-3 for your feature:

**Common design principles (pick 2-3 that guide this feature):**

| Principle | Definition | When to Use | Example Decision |
|---|---|---|---|
| Clarity over cleverness | Simple and obvious beats elegant but confusing | When many user segments have different mental models | Choose familiar terms over innovative terminology |
| Speed over completeness | Getting something done quickly beats having all information | When tasks are time-sensitive or user attention is scarce | Show quick-access actions before comprehensive menus |
| Confidence through visibility | Show relevant context and options rather than hiding | When users need to understand what they are doing | Confirmation screens and preview panes instead of hidden actions |
| Progressive disclosure | Show essentials first, advanced options when needed | When feature has many options but most users use 20% of them | Basic settings prominent, advanced settings in expandable section |
| Consistency over uniqueness | Reuse patterns from design system rather than invent new ones | When product is large and pattern coherence matters | Use existing button styles, not custom buttons |
| Elegance of constraint | Limit options to guide user toward right choice | When users are decision-fatigued or uncertain | Specific templates and presets instead of infinite customization |

## Competitive and Inspirational References

Provide reference examples, but do not prescribe solutions:

**What to include:**
- 2-3 examples of competitors or adjacent products solving similar problems
- For each: what works, what you like, what to avoid
- Photos/screenshots of the examples
- Why each example is relevant to your problem

**What NOT to do:**
- Do not say "Design it like Figma's component panel" (too prescriptive)
- Do say "Figma's component panel elegantly handles a large library with search, filtering, and favorites. We need similar UX for browsing saved templates" (shows the job, not the solution)

**How to frame references:**
"Inspiration: Notion's database views show how to let users switch between multiple views (table, calendar, gallery, kanban) of the same data. We want to apply similar pattern to saved report views."

This tells designer the pattern to solve for, not the exact design to copy.

## Technical Constraint Documentation

Designers often do not understand technical constraints; document them clearly:

**Technical constraints template:**

| Constraint | Impact on Design | Alternatives |
|---|---|---|
| API limit: 100 items per request | Cannot show unlimited list; must paginate or virtualize | Pagination, lazy-load infinite scroll, or search to narrow down |
| Database field limit: 255 characters | Long text input must have visible character limit | Hide excess characters; show count as user types |
| Mobile viewport: max 375px width | Cannot show wide multi-column layouts | Stack columns, use tabs, or hide secondary info on mobile |
| Performance budget: <3 second load time | Cannot load full dataset upfront; must be async | Show skeleton loader while data loads; prioritize above-fold content |
| Accessibility requirement: WCAG AA | Color contrast must be >4.5:1 for text; cannot use color alone as signal | Use color + icon + text; test with contrast checker in design tools |
| Email compatibility: Outlook 2019 | Many CSS features unsupported; must use simple layouts | HTML email template constraints; avoid flexbox, use tables |

Knowing these before design starts prevents multiple rounds of "that does not work because..."

## Collaboration Model and Handoff

Define when and how designer and PM will collaborate:

**Co-design approach:**
Use when: Problem is complex, ambiguous, or requires shared learning

- Designer attends research sessions (learns problem directly)
- Collaborative whiteboarding/ideation on solution direction
- PM and designer explore 2-3 directions together
- Designer then executes the selected direction

Cadence: Daily standup during active design phase; weekly critique reviews

**Handoff approach:**
Use when: Problem is well-defined; solution direction is clear

- PM hands off detailed brief to designer
- Designer works independently for 1-2 weeks
- Single design review at end to gather feedback
- Minimal back-and-forth; clear acceptance criteria

Cadence: Kickoff meeting, design review, refinement feedback

**Review cadence:**
- Discovery phase: Bi-weekly reviews of exploration work (5-10 design directions)
- Execution phase: Weekly reviews of increasing fidelity (low-fi to high-fi progression)
- Final phase: Single review of final design against brief criteria

## Design Brief Quality Checklist

Before sending a brief to designer, verify:

- [ ] Problem statement is clear and grounded in research (not assumption)
- [ ] User is defined (persona or JTBD job statement)
- [ ] Functional requirements are expressed as user outcomes ("user can do X" not "add button called Y")
- [ ] No wireframes or layout prescriptions in the brief (that is designer's job)
- [ ] Constraints are documented (technical, brand, accessibility, timeline)
- [ ] Success criteria are measurable (not "looks good" but "80% of users complete onboarding without help")
- [ ] Out of scope is explicitly stated (prevents scope creep)
- [ ] Design system requirements are clear (required components, new component approval process)
- [ ] Design principles are stated (2-3 max to guide trade-offs)
- [ ] Competitive references show pattern, not exact design to copy
- [ ] Timeline is realistic (not "need design in 2 days" for a complex feature)

## Anti-Patterns in Design Briefs

| Anti-Pattern | Why It Fails | Example |
|---|---|---|
| Too prescriptive on solution | Designer becomes pixel-filler; no real design thinking | "Create a card component at 400px width with rounded corners, 16px padding, shadow 0 4px 8px" - designer has no decision-making space |
| Too vague on problem | Designer cannot determine what success looks like | "Design a better way to manage settings" - what is broken about current settings? What outcome do we want? |
| Includes wireframes created by PM | Designer starts with "fill in the pixels" mentality; wireframe becomes anchor | Brief includes lo-fi mockup; designer tweaks pixels instead of rethinking layout |
| Lists features instead of explaining user problems | Designer does not understand why features matter | "Add search, sorting, and filtering" without explaining what user is trying to accomplish (finding data quickly in large dataset) |
| Misses key constraint until design is 80% done | Wasted design work; designer demoralized | Brief does not mention "must work on iOS 12" or "max API response time is 5 seconds" - designer learns constraint when execution time is critical |
| No success criteria | Designer cannot self-assess work; PM cannot evaluate fairly | No definition of what good design looks like; feedback becomes subjective ("I do not like the colors") |
| Mixing multiple problems in one brief | Designer unclear which problem is most important | Brief asks to redesign search, improve filtering, add favorites, improve mobile - which is primary? Affects prioritization |
| No reference to existing design system | Designer invents new components instead of reusing | Designer creates new button style that almost matches design system; component inconsistency spreads |

## Handoff and Review Process Guidance

**Pre-design kickoff (30 min meeting):**
- Designer reads brief, prepares 3-5 clarifying questions
- PM and designer align on problem, constraints, and timeline
- Confirm collaboration model (co-design vs handoff)
- Designer asks about reference competitors; PM provides context

**During design (asynchronous updates if not co-designing):**
- Designer shares early explorations (low-fidelity if doing discovery; higher-fidelity if execution)
- PM sees work in progress; minimal feedback during execution phase (to avoid 100 change requests)
- Designer asks clarifying questions as they arise

**Design review meeting:**
- Designer presents design with rationale (not "here is the design" but "here is the problem we solved and here is how")
- Present multiple directions if discovery phase (3+ approaches to same problem)
- Present high-fidelity mockups or prototype if execution phase (single direction, polished)
- PM evaluates against brief criteria, not personal taste
- Document feedback: critical (blocks shipping), important (should fix), nice-to-have (lower priority)

**Feedback format:**
- What works: "The progressive disclosure of advanced options on a toggle is clear and lets casual users stay simple"
- What does not work: "The error state color does not meet WCAG AA contrast requirement" or "The 3-step onboarding flows against our 'speed over completeness' principle"
- Suggested direction (not solution): "The error messaging could be more specific about what went wrong (e.g., 'email already in use' vs 'invalid input')"

**Revisions and shipping:**
- Designer revises based on critical feedback
- Second review of revisions (usually short; confirm critical issues resolved)
- If second review goes well: handoff to engineering with design spec
- If second review still has issues: escalate to design lead or product leader for alignment

## Output Template

---
**DESIGN BRIEF: [Feature Name]**

**Author:** [PM Name]
**Date:** [Date]
**Designer:** [Name if assigned]
**Design Start Date:** [Start date]
**Target First Review:** [Date]
**Target Ship Date:** [Date - if known]

**Brief Type:** [Exploratory / Execution / Redesign]

**Problem Statement**
[The user problem this design will solve. Ground in research: user interviews, usage data, support tickets, or other evidence. Include customer quote if available.]

Affected user segment: [Who experiences this problem most acutely?]
Frequency: [How often do they encounter this problem?]
Current workaround: [What do they do today instead?]

**Jobs-to-be-Done Framing** (optional but recommended)
Functional job: [What task must be accomplished?]
Emotional job: [How should the user feel doing this task?]
Social job: [What impression do they want to make?]

**User Context and Personas**
Primary persona: [Name and role from persona work]
Secondary persona (if applicable): [Name and role]
Behavioral context: [How will this user encounter and use this feature? Device, frequency, context, stress level?]
Relevant mental model: [How do users currently think about this problem?]

**Design Goals** (What must be true for this design to be successful?)
User goals:
1. [User outcome - e.g., "First-time user can X without assistance"]
2. [User outcome]

Business goals:
1. [Business outcome - e.g., "Reduce support tickets about X by 40%"]
2. [Business outcome]

**Functional Requirements** (What the design must enable, expressed as user actions)
- [User can do X]
- [User can do Y]
- [System provides Z feedback when...]
- [User can undo/cancel action A]

**Design System and Brand Requirements**
Design system components to use: [e.g., Card, Button, Modal from our design system]
New components requiring design: [If new components needed, approval process and timeline]
Brand guidelines: [Color palette, typography, tone of voice guidelines to follow]
Visual consistency: [Any existing patterns this feature should match?]

**Constraints**
Technical: [Any technical limitations that affect design options - API response time, data limits, browser compatibility]
Platform: [iOS, Android, Web, or all - with platform-specific constraints]
Accessibility: [WCAG level required; specific accessibility considerations]
Performance: [Load time budget, animation performance requirements if any]
Timeline: [Hard deadline dates; impacts design scope]
Internationalization: [Multiple languages? Right-to-left support?]

**Design Principles** (2-3 principles to guide trade-off decisions)
1. [Principle]: [Definition] - [How it applies to this feature]
2. [Principle]: [Definition]

**Out of Scope**
- [Explicitly excluded feature to prevent scope creep]
- [User audience not included in this phase]
- [Problem intentionally deferred to future phase]

**Research and Context**
Key insights from user research: [Quotes or findings that shaped this brief]
Relevant customer feedback: [Support tickets, feature requests, or feedback that led to this work]

**Inspirational References**
1. [Competitor or adjacent product name]
   - Link/screenshot
   - What works: [What is good about this solution]
   - What to avoid: [What did they get wrong or what is not applicable to us]
   - Why relevant: [How does this inform our design problem?]
2. [Reference 2]

**Existing Patterns to Follow**
[Any existing UI patterns in the product this feature should be consistent with. Provide links to design system or reference pages.]

**Intentional Departures from Existing Patterns**
[If this feature deliberately breaks from existing patterns, explain why. Example: "This feature has different user context (mobile-first) than our typical flows, so we are using bottom sheet instead of modal"]

**Success Criteria**
How will we know the design works?
- Usability metric: [e.g., "75% of new users complete onboarding in first session without help"]
- Adoption metric: [e.g., "Feature is used by 40% of active users within 30 days of launch"]
- Sentiment metric: [e.g., "NPS for this feature is >40"]
- Business metric: [e.g., "Conversion rate from step X to step Y improves by 20%"]
- Technical metric: [e.g., "Load time under 3 seconds on 4G connection"]

**Collaboration Model**
[Co-design / Handoff]
- Kick-off meeting scheduled: [Date]
- Weekly design review: [Day/time if applicable]
- Expected number of review rounds: [X]

---
