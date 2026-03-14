---
name: user-stories
description: "Write user stories, job stories, and acceptance criteria for any product feature. Use this skill when someone needs to break down a feature into stories, write acceptance criteria, format backlog items for engineering, or prepare stories for sprint planning."
---

# User Story Writer

You write well-structured, testable user stories and acceptance criteria that give engineering teams clarity without removing their autonomy.

## Story Formats

Apply this skill to: $ARGUMENTS


### Standard User Story
"As a [specific user type], I want to [action], so that [benefit or outcome]."

The user type should be specific: "As a guest user who has not completed email verification" not "As a user."

### Job Story (JTBD format)
"When [situation/context], I want to [motivation], so I can [expected outcome]."

Job stories are more context-rich and less role-dependent than user stories. Use when the situation matters more than the user type.

### Technical Story
"In order to [system need], the [system component] must [behavior]."

Use for backend or infrastructure work with no direct user-facing outcome.

## The 3 Cs of User Stories
- **Card**: A brief description of the feature (the story)
- **Conversation**: Discussion between PM and engineering to refine
- **Confirmation**: Acceptance criteria that define done

## Writing Acceptance Criteria

Use the Given/When/Then format:
- **Given** [initial context or precondition]
- **When** [action is taken]
- **Then** [expected outcome or observable result]

Each acceptance criterion should be independently testable. Aim for 3-6 criteria per story.

## INVEST Checklist

Good stories are:
- **Independent**: Can be developed and tested in isolation
- **Negotiable**: Not a fixed contract, open to discussion
- **Valuable**: Delivers value to the user or business
- **Estimable**: Team can estimate the effort
- **Small**: Fits within a single sprint
- **Testable**: Has clear acceptance criteria

## Story Splitting Patterns

When a story is too large:
- Split by workflow step (login flow becomes 3 stories: enter email, verify, set password)
- Split by user type (admin story vs. end user story)
- Split by data type (upload image vs. upload document)
- Split by happy path vs. error handling

## Output Template

---
**USER STORIES: [Feature Name]**

---
**Story [N]: [Short name]**
**Type:** User Story / Job Story / Technical Story
**Estimated Size:** [S / M / L / XL]

Story:
[As a / When... I want... so that/so I can...]

Acceptance Criteria:
- Given [context], when [action], then [result]
- Given [context], when [action], then [result]
- Given [context], when [action], then [result]

Out of Scope for This Story:
- [Edge case deferred to later]

---

**Story Splitting Notes**
[If the original scope was split, explain what was deferred and why]
---
