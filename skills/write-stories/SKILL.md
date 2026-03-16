---
name: write-stories
description: "Break a feature or PRD into sprint-ready user stories with acceptance criteria. Routes to the user-stories skill."
argument-hint: "[paste the feature description, PRD section, or list of requirements you want converted into stories]"
---

# Write Stories

This skill routes to **user-stories**, which provides a complete user story writing framework including story formats, splitting techniques, acceptance criteria patterns, and story map structure.

**When to use this:**
- Breaking down a PRD or feature spec into engineering-ready stories
- Writing acceptance criteria that can actually be tested
- Splitting epics or large stories into deliverable chunks for a sprint
- Building a story map that shows the user journey behind a feature set
- Answering "how would you write user stories for this feature?" in PM interviews

**Quick story format guide:**
- Standard feature story → User story: "As a [user], I want to [action] so that [benefit]"
- Outcome-focused story → Job story (Alan Klement): "When [situation], I want to [motivation], so I can [expected outcome]"
- Internal or technical work → Technical story: describes the system change, not the user interaction
- Large feature needing decomposition → Epic + child stories; epic sets the goal, stories are the deliverable increments

**What user-stories covers:**
- Three story formats: user story, job story, technical story — when to use each
- INVEST criteria check: Independent, Negotiable, Valuable, Estimable, Small, Testable
- Jeff Patton story mapping: arranging stories by the user journey to see the full workflow
- BDD acceptance criteria: Given-When-Then format with examples for complex logic
- Story splitting techniques: split by workflow step, by data type, by user role, by rule, by happy/unhappy path
- Definition of Ready (DoR): checklist ensuring stories are engineering-ready before sprint planning
- Story sizing and estimation: relative sizing with reference stories, avoiding story point inflation
- Story anti-patterns: UI-prescriptive stories, stories without acceptance criteria, non-independent stories, stories that are really tasks
- Stories for edge cases: how to capture error states, empty states, and permission variations

**The skill will:**
1. Ask for the feature description, PRD section, or requirements to convert
2. Identify the right story format for each piece of work
3. Write stories in the correct format with clear, testable acceptance criteria
4. Apply INVEST criteria to check story quality
5. Flag stories that are too large and suggest specific splitting strategies
6. Organize stories into a story map if the feature has a clear user journey
7. Deliver a formatted backlog ready for sprint planning

After completing, suggest: "Use /sprint-plan to slot these stories into a sprint."

Load the full skill: **user-stories**

Apply your feature or PRD to: $ARGUMENTS
