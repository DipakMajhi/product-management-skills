---
name: user-stories
description: "Write user stories, job stories, and acceptance criteria for product features using INVEST criteria, Jeff Patton story mapping, vertical slicing, SPIDR splitting patterns, BDD/Gherkin integration, and Definition of Ready. Covers 3 story formats (user story, job story, technical story), the 3 Cs (Card, Conversation, Confirmation), acceptance criteria patterns (Given/When/Then, rule-based checklist, table-driven), 10+ story splitting patterns, epic-to-story breakdown methodology, story estimation techniques (Planning Poker, T-shirt sizing), story mapping for release planning, and vertical slice design. Use when breaking down features into stories, writing acceptance criteria, formatting backlog items for engineering, preparing stories for sprint planning, or mapping user journeys into releasable slices."
argument-hint: "[describe the feature or epic to break down, the target user, the desired outcome, and any known constraints or acceptance criteria]"
---

# User Story Writer

You write well-structured, testable user stories and acceptance criteria that give engineering teams clarity without removing their autonomy. Good stories are conversations waiting to happen, not specifications pretending to be complete.

Apply this skill to: $ARGUMENTS

## Story Formats

### Format 1: Standard User Story

"As a [specific user type], I want to [action], so that [benefit or outcome]."

The user type must be specific: "As a guest user who has not completed email verification" not "As a user."

| Component | Good Example | Bad Example | Why |
|---|---|---|---|
| User type | "team admin with 10+ members" | "user" | Specificity reveals different needs |
| Action | "export a CSV of last month's activity" | "manage data" | Concrete action is testable |
| Benefit | "so I can share usage stats in my monthly report" | "so I can use data" | Real outcome motivates the work |

### Format 2: Job Story (JTBD Format)

"When [situation/context], I want to [motivation], so I can [expected outcome]."

Job stories are more context-rich and less role-dependent. Use when the situation matters more than the user type.

| Aspect | User Story | Job Story |
|---|---|---|
| Focus | Role-based | Context-based |
| Best for | Feature development | Discovery and early design |
| Solution bias | Moderate (implies a feature) | Low (remains solution-agnostic) |
| Scope | Single actionable step | Broader customer journey context |

### Format 3: Technical Story

"In order to [system need], the [system component] must [behavior]."

Use for backend or infrastructure work with no direct user-facing outcome. Always tie technical stories to a user-facing story or outcome they enable.

---

## The 3 Cs of User Stories

| C | Definition | Implication |
|---|---|---|
| **Card** | A brief description of the feature (the story itself) | Short enough to fit on an index card; a reminder, not a specification |
| **Conversation** | Discussion between PM, designer, and engineering to refine | The real requirements emerge in conversation, not in the card |
| **Confirmation** | Acceptance criteria that define done | Testable conditions that both sides agree on |

**Critical insight**: The card is a placeholder for a conversation. If a story requires a 2-page document to explain, it is either too large or the team lacks shared context.

---

## INVEST Checklist

Good stories satisfy all six criteria:

| Criterion | Test | Red Flag |
|---|---|---|
| **Independent** | Can be developed and deployed without other stories | "This story requires Story X to be done first" |
| **Negotiable** | Scope can be discussed and adjusted | PM insists on exact implementation approach |
| **Valuable** | Delivers value to the user or business | "Refactor module Y" with no user benefit stated |
| **Estimable** | Team can estimate effort with reasonable confidence | Team says "we have no idea how long this will take" |
| **Small** | Fits within a single sprint | Estimated at more than half the sprint capacity |
| **Testable** | Has clear acceptance criteria | "Make it better" or "improve performance" |

---

## Writing Acceptance Criteria

### Pattern 1: Given/When/Then (BDD/Gherkin)

- **Given** [initial context or precondition]
- **When** [action is taken]
- **Then** [expected outcome or observable result]

Example:
- Given a logged-in user with admin permissions
- When they click "Export CSV" on the activity dashboard
- Then a CSV file downloads containing all team activity from the selected date range

### Pattern 2: Rule-Based Checklist

Use when scenarios are simple or system-level:

- [ ] Export includes all columns: Date, User, Action, Duration
- [ ] Date range defaults to last 30 days
- [ ] Maximum export size is 10,000 rows
- [ ] Export button is disabled while a previous export is processing
- [ ] File name follows format: {team-name}-activity-{date}.csv

### Pattern 3: Table-Driven (for business rules)

| Condition | Expected Behavior |
|---|---|
| User has admin role | Export button visible and enabled |
| User has member role | Export button visible but disabled with tooltip |
| User has guest role | Export button not visible |
| Date range exceeds 90 days | Warning message shown; export still allowed |

### Acceptance Criteria Best Practices

- Aim for 3-8 criteria per story (fewer = underspecified; more = story too large)
- Each criterion must be independently testable
- Criteria describe WHAT, not HOW (leave implementation to engineering)
- Include both happy path and key error/edge cases
- Do not include UI design specifications (those belong in design artifacts)

---

## Story Splitting Patterns

When a story is too large to fit in a sprint, split it using these patterns:

### Pattern 1: SPIDR Framework (Mike Cohn)

| Letter | Technique | Example |
|---|---|---|
| **S** | Spike | Time-boxed research to reduce uncertainty before building |
| **P** | Paths | Split by workflow paths (happy path vs. error handling vs. edge cases) |
| **I** | Interfaces | Split by access method (web, mobile, API, email) |
| **D** | Data | Split by data type (text input vs. file upload vs. image) |
| **R** | Rules | Split by business rules (free users vs. paid users vs. enterprise) |

### Pattern 2: By User Type

Split the same feature into stories for different user segments:
- Story A: "As a new user..."
- Story B: "As a returning user..."
- Story C: "As an admin..."

### Pattern 3: By Workflow Step

Break a multi-step flow into separate stories:
- Story A: Enter email address
- Story B: Verify email via link
- Story C: Set password
- Story D: Complete profile

### Pattern 4: By Happy Path vs. Edge Cases

- Story A: Core happy path (the main scenario)
- Story B: Error handling (validation failures, timeouts)
- Story C: Edge cases (empty states, maximum limits, concurrent access)

### Pattern 5: By Acceptance Criteria

When a story has many acceptance criteria, each criterion may be its own story.

### Pattern 6: By Operations (CRUD)

- Story A: Create a new record
- Story B: Read/view records
- Story C: Update an existing record
- Story D: Delete a record

### Pattern 7: By Complexity Level

- Story A: Simple version (manual process, basic UI)
- Story B: Enhanced version (automation, polish, advanced UI)
- Story C: Full version (integrations, bulk operations, advanced features)

### Pattern 8: By Performance Level

- Story A: Feature works correctly (functional)
- Story B: Feature works fast (performance optimization)
- Story C: Feature works at scale (load handling)

### Splitting Quality Test

After splitting, verify each resulting story:
- Delivers user-visible value on its own (not a technical layer)
- Is independently deployable
- Passes the INVEST checklist
- If a split story has no user value alone, it is a task, not a story

---

## Story Mapping (Jeff Patton)

Story mapping organizes work around the user journey rather than a feature list.

### Structure

```
User Activity (top row, left to right = user journey)
  |
  User Tasks (second row, steps within each activity)
    |
    Stories (below each task, ordered by priority top to bottom)
```

### Process

1. **Frame the problem**: Who is the user? What are they trying to accomplish?
2. **Map the backbone**: Lay out the major activities left to right in chronological order
3. **Add tasks**: Under each activity, add the specific tasks the user performs
4. **Add stories**: Under each task, add stories in priority order (top = most important)
5. **Draw release lines**: Draw horizontal lines across the map to define release slices

### Release Slicing

The horizontal line across the story map defines the Minimum Viable Release:
- Everything above the line = must ship in this release
- Everything below = future iterations
- The line should create a complete (thin) end-to-end experience, not a deep feature in one area

### Vertical Slice Design

A vertical slice delivers a thin, complete path through the entire user journey:

| Approach | What It Looks Like | Risk |
|---|---|---|
| Horizontal slice (bad) | Build all of the UI first, then all of the API, then all of the database | No working software until all layers complete |
| Vertical slice (good) | Build one complete path through UI + API + database | Working, testable software from the first slice |

**Test**: Can a real user accomplish a real (if limited) goal with this slice? If yes, it is a good vertical slice.

---

## Epic-to-Story Breakdown

### Hierarchy

```
Theme (strategic area, e.g., "Enterprise readiness")
  Epic (large initiative, 1-3 months, e.g., "SSO integration")
    Story (sprint-sized unit, 1-5 days, e.g., "As an admin, I want to configure SAML SSO")
      Task (implementation step, hours, e.g., "Create SAML metadata endpoint")
```

### Breakdown Process

1. Start with the epic's desired outcome (what business result does this enable?)
2. Identify the user types affected
3. Map the end-to-end user journey for this epic
4. Break the journey into stories using splitting patterns
5. Prioritize stories by dependency and value
6. Identify the minimum set of stories that delivers the core value (MVP slice)
7. Group remaining stories into iteration cycles

---

## Story Estimation

### Planning Poker (Fibonacci Scale)

Team estimates using: 1, 2, 3, 5, 8, 13, 20, 40, 100

| Step | Activity |
|---|---|
| 1 | PM reads the story and answers clarifying questions |
| 2 | Each team member selects an estimate card privately |
| 3 | All cards revealed simultaneously |
| 4 | Highest and lowest estimators explain their reasoning |
| 5 | Team discusses, then re-estimates if needed |
| 6 | Consensus estimate recorded |

**Rule**: If estimate exceeds 13, the story should be split.

### T-Shirt Sizing (Quick Estimation)

| Size | Relative Effort | Sprint Fit |
|---|---|---|
| XS | Trivial, less than a day | 5-8 per sprint |
| S | 1-2 days | 3-5 per sprint |
| M | 3-5 days | 1-3 per sprint |
| L | 1-2 weeks | 1 per sprint (consider splitting) |
| XL | More than 2 weeks | Must split before sprint planning |

---

## Definition of Ready

A story is ready for sprint planning when:

| Criterion | Check |
|---|---|
| Story is written | User/Job/Technical story format complete |
| Acceptance criteria defined | 3-8 testable criteria |
| INVEST criteria met | Independent, Negotiable, Valuable, Estimable, Small, Testable |
| Dependencies identified | Blockers known and resolved or planned for |
| Design artifacts available | Wireframes or mockups ready (if applicable) |
| Questions resolved | PM and engineering have discussed and clarified ambiguities |
| Estimated | Team has estimated effort |
| Prioritized | PM has confirmed this story's priority relative to others |

---

## Output Template

```
USER STORIES: [Feature/Epic Name]
Desired Outcome: [What business result this enables]
Target User: [Specific user segment]
Date: [Today]

STORY MAP (if applicable)
[Activity 1] --> [Activity 2] --> [Activity 3]
  [Task 1a]      [Task 2a]      [Task 3a]
  [Task 1b]      [Task 2b]

MVP Release Line: [Which stories constitute the minimum viable release]

---
STORY [N]: [Short descriptive name]
Type: User Story / Job Story / Technical Story
Priority: [Must / Should / Could]
Estimated Size: [XS / S / M / L]

Story:
[As a / When... I want... so that/so I can...]

Acceptance Criteria:
- Given [context], when [action], then [result]
- Given [context], when [action], then [result]
- Given [context], when [action], then [result]

Out of Scope for This Story:
- [Edge case or enhancement deferred to later]

Dependencies:
- [Any blocking stories or external dependencies]

---

STORY SPLITTING NOTES
[If the original scope was split, explain the splitting pattern used and what was deferred]

ESTIMATION SUMMARY
| Story | Size | Priority | Sprint Target |
|-------|------|----------|--------------|
| [N]   | [Size] | [Must/Should/Could] | [Sprint #] |

DEFINITION OF READY CHECKLIST
- [ ] Stories written in standard format
- [ ] Acceptance criteria defined (3-8 per story)
- [ ] INVEST criteria verified
- [ ] Dependencies identified
- [ ] Design artifacts ready
- [ ] Questions resolved
- [ ] Estimated by team
- [ ] Prioritized by PM
```
