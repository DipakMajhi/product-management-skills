---
name: ux-critique
description: "Evaluate a product's UX design against usability principles and PM-relevant design criteria. Use this skill when someone wants to critique a product's UX, prepare for a 'how would you improve this product's design?' PM interview question, evaluate design options, or give structured feedback to a design team."
argument-hint: "product URL, product name, or specific feature to critique"
---

# UX Critique Framework

As a PM, your role in design critique is not to redesign the product - it is to evaluate whether the design solves the user's problem effectively and identify specific friction points that will affect adoption, retention, and business metrics. This skill teaches you multiple evaluation frameworks and how to give feedback constructively.

Apply this skill to: $ARGUMENTS

## Jakob Nielsen's 10 Usability Heuristics (Simplified for PMs)

The foundational heuristics for usability evaluation:

1. **Visibility of system status**: Does the user always know what is happening? (Loading states, progress indicators, confirmation messages)
   - Example good: "Sending..." status while email is being sent; success confirmation when sent
   - Example bad: Clicking "Send" with no feedback; user uncertain if action registered

2. **Match with real world**: Does the product use language and concepts the user already knows?
   - Example good: "Save" button uses language user already knows from file systems
   - Example bad: "Persist to local storage" (technical jargon, not user language)

3. **User control and freedom**: Can users undo mistakes? Exit unwanted states easily?
   - Example good: Undo button; Cancel button on every form
   - Example bad: Destructive action (delete) with no undo and no confirmation

4. **Consistency**: Do similar things look and behave consistently? Does the product follow platform conventions?
   - Example good: All modal dialogs have consistent size, position, close button location
   - Example bad: Some modals close with X button, others with Cancel button, others have no close button

5. **Error prevention**: Does the design prevent mistakes before they happen?
   - Example good: Disabled "Submit" button until required fields are filled; confirm before destructive action
   - Example bad: Allow email send without a recipient; user only discovers error after click

6. **Recognition over recall**: Does the product show options rather than requiring users to remember them?
   - Example good: Dropdown menu shows all options; user recognizes the one they want
   - Example bad: Command-line interface requiring users to remember command names

7. **Flexibility and efficiency of use**: Can expert users use shortcuts while the interface stays simple for beginners?
   - Example good: Simple form for beginners; keyboard shortcuts for power users; bulk actions for experts
   - Example bad: Keyboard shortcuts only; no visual menu for beginners to discover them

8. **Aesthetic and minimalist design**: Does every element earn its place? Is there visual noise that distracts?
   - Example good: Feature-rich page with clear hierarchy; important actions prominent
   - Example bad: Every button is the same size and color; user does not know what to do first

9. **Error recovery**: When errors occur, are messages clear and helpful?
   - Example good: "Username already in use. Try another name or use forgot password." (Clear error, suggests recovery)
   - Example bad: "Error 502" (User has no idea what went wrong or how to fix it)

10. **Help and documentation**: Is help available when needed and easy to find?
    - Example good: Context-sensitive help; hover tooltips on unclear fields
    - Example bad: Help menu buried in footer; does not exist

## Don Norman's Design Principles

Design principles that prevent user errors and create intuitive interfaces:

| Principle | Definition | PM-Relevant Application | Example |
|---|---|---|---|
| Affordances | Design reveals what actions are possible (door handle shape tells you to pull) | Does UI reveal what user can do? Or is it ambiguous? | Button that looks clickable; text field that looks editable |
| Signifiers | Signals that something is interactive or actionable | Use color, shape, animation, text to signal actions | Blue underlined text signals link; pause icon in video suggests you can click to pause |
| Mapping | Relationship between control and outcome is logical and visible | Do controls map intuitively to outcomes? | Volume slider going up-down matches intuition; light switch toggle matches intuition |
| Feedback | System tells user the result of their action immediately | Does user know their action registered? | Button press feedback (color change); form submission success message |
| Constraints | Limit possible actions to prevent mistakes | Does design prevent user from making wrong choice? | Disable "next" button until required fields filled; prevent invalid dates |
| Conceptual Model | System design matches user's mental model of how it works | Does system behave the way user expects? | Search bar at top (user expects to search); file save as familiar file dialog |

## Emotional Design: Norman's Three Levels

Design affects emotion at three levels:

| Level | Definition | What Affects It | PM Application |
|---|---|---|---|
| Visceral | Initial emotional reaction to appearance | Color, shape, typography, visual aesthetics, feel | Does product look professional and trustworthy? Or cheap and risky? |
| Behavioral | Emotional response while using product | Ease of use, speed, responsiveness, feedback | Does product feel fast and responsive? Or frustrating and slow? |
| Reflective | Emotional response to meaning and ownership | Brand story, identity, values, social status | Does product make user feel smart, capable, successful? Or inadequate? |

**Example critique:**
- Visceral: "Design looks dated (2010 era) with poor typography; user might distrust credibility"
- Behavioral: "Adding item to cart has 3-second delay before confirmation; user uncertain if action registered"
- Reflective: "Product succeeds as tool, but no sense of accomplishment or progress; missing feedback of what user built or achieved"

## Cognitive Load Theory Application

Users have limited working memory. Design should minimize unnecessary cognitive load:

**Hick's Law (decision complexity):** Time to decide = f(number of choices)
- More choices = longer decision time = higher cognitive load
- Application: Limit initial options; progressive disclosure of advanced options
- Example bad: 15 filters on search page; user overwhelmed before entering first term
- Example good: 3 key filters visible; more available on advanced search

**Miller's Law (working memory capacity):** Humans can hold ~7 items in working memory at once
- Application: Chunk information into groups; do not show 20 unrelated options at once
- Example bad: Address form with 20 separate fields on one screen
- Example good: Address form with 3 sections (street, city/state, zip) - reduces cognitive load

**Fitts's Law (motor control):** Larger targets and shorter distances are easier to click
- Application: Make important buttons larger; place them closer to where user is looking
- Example bad: Delete button same size as Save button; both hard to target on mobile
- Example good: Confirm button large and prominent; cancel button smaller, secondary placement

**Gestalt Principles (visual grouping):** Proximity, similarity, continuity, closure
- Application: Group related items visually; use whitespace to separate unrelated items
- Example bad: All form fields same spacing; user cannot tell which fields go together
- Example good: Billing info grouped with extra whitespace before shipping info

## Information Architecture Evaluation

How well is information organized for users to find what they need?

| Criterion | Good | Bad | PM Impact |
|---|---|---|---|
| Labeling | Labels are user language, not jargon | Labels are technical or ambiguous ("System Settings" vs "Notifications and Privacy") | Users get lost; cannot find features they are looking for |
| Navigation | Clear mental model of site structure; breadcrumbs show path | Navigation hidden or illogical; user cannot orient themselves | Users struggle to find features; support tickets increase |
| Search | Search finds what user searched for; results are ranked by relevance | Search returns too many irrelevant results; keyword matching is poor | Users give up on search; revert to browsing |
| Organization | Objects grouped by user task, not by backend system | Objects grouped by technical implementation | Users find it hard to accomplish tasks |
| Scalability | IA works with 10 items and 100 items (growth does not break structure) | IA breaks at scale (works with 10 items, collapses with 100) | Product cannot scale without UX redesign |

## Mobile-Specific UX Criteria

Mobile has unique constraints (small screen, touch input, 1-handed use, distraction):

| Criterion | Mobile Best Practice | Common Failure | PM Impact |
|---|---|---|---|
| Thumb zones | Primary actions in thumb-reachable zone (bottom 40% of screen) | Important action at top of screen, requires stretching | Lower conversion on mobile; user frustration |
| Gesture patterns | Use standard gestures (swipe, tap, long-press); clear visual targets | Non-standard gestures; unclear what is swipeable | User confusion; lower engagement |
| Above-the-fold | Critical info and CTA visible without scrolling | Important information below fold; user never sees it | Lower awareness of feature; lower adoption |
| Loading states | Show progress; let user know something is happening | No feedback while loading; user thinks app is broken and exits | Higher abandonment rate |
| Micro-interactions | Subtle feedback on tap (slight color change, brief animation) | No tactile feedback; tap feels dead | Users less confident about whether they tapped correctly |
| Form input | Large input fields (44px min height); number keyboard for numeric fields | Tiny input fields; wrong keyboard (text for phone number) | Slower input; higher error rate; frustration |

## Accessibility Evaluation (WCAG Basics for PM Context)

You do not need to be WCAG expert, but know enough to spot major issues:

| WCAG Criterion | What to Look For | Common Failure | PM Implication |
|---|---|---|---|
| Color contrast | Text contrast >=4.5:1 for normal text; 3:1 for large text | Light gray text on white; unreadable for vision-impaired | ~8% of men, 0.5% of women have color blindness; exclusion of users |
| Keyboard navigation | All functions accessible via keyboard; clear focus state | Cannot tab to all buttons; focus state invisible | Power users and users with motor disabilities cannot use product |
| Alt text | Images have descriptive alt text; screen reader gets meaning | Images missing alt text or alt text is "image1.png" | Blind users cannot understand images |
| Captions | Video has captions or transcript | Video without captions | Deaf and hard-of-hearing users excluded |
| Link text | Links have descriptive text ("Learn more about pricing") | Links are generic ("click here") | Screen reader users have no context; confusing navigation |
| Semantic HTML | Headings, landmarks, form labels are proper HTML | Styled divs to look like buttons; no semantic structure | Screen reader users get no structure; navigation is lost |

**For PMs: In design critique, flag** "Do we have alt text for all images?" and "Can this be navigated with keyboard only?" These spot-checks catch major accessibility issues.

## PM-Specific Critique Etiquette

How to give feedback to designers constructively (and have them actually listen):

**DO:**
- Start with what works: "The progressive disclosure of advanced options is clean and keeps the interface simple"
- Be specific: "When I click 'save', there is no confirmation message; I am uncertain if the save worked"
- Ask questions: "What happens if a user has 500 saved templates? Is search scalable here?"
- Suggest direction, not solution: "The error messaging could be more specific about what went wrong"
- Reference framework: "This violates Nielsen's heuristic 9 (error recovery); the error message is too technical"

**DON'T:**
- Only criticize: "I do not like this design" (offers no direction)
- Prescribe solution: "Make the button blue instead" (removes designer's agency)
- Use vague language: "This looks off" or "Make it better" (designer cannot act on this)
- Compare to competitors directly: "Figma does this better" (demoralizes without helping)
- Ignore the actual design: "This should be a pop-up" without acknowledging current design works well

**Framing structure:**
"I see what you are doing here [acknowledge intent]. What works is [specific positive observation]. One thing I notice is [specific issue] which affects [user impact]. Have you considered [suggested direction]?"

Example: "I see you are using a modal to collect feedback. What works is the clear layout and required fields validation. One thing I notice is the modal can be closed without saving, and users might lose their feedback. Have you considered a progress save mechanism or warning on close?"

## Severity Rating Framework

When identifying issues, rate severity by business impact, not aesthetic preference:

| Severity | Definition | Frequency | Business Impact | Example | Action |
|---|---|---|---|---|---|
| Critical | Blocks user from completing task; or exposes risk | Always or often | Loss of revenue or trust | Cannot submit payment form; security vulnerability | Must fix before ship |
| Major | Significant friction; user can complete but with effort | Often or occasionally | Reduced conversion or retention | 3-second load delay; confusing error message | Fix before ship if possible |
| Minor | Small friction or incorrect behavior; does not block task | Occasionally or rarely | Cosmetic or nice-to-have improvement | Slightly wrong color; tooltip with typo | Fix in next iteration |

**When rating, ask yourself:** "If we shipped this, what is the impact on key metrics (conversion, retention, support cost, user satisfaction)?"

- Critical: Metric would decline significantly (>10% impact)
- Major: Metric would decline moderately (3-10% impact)
- Minor: Metric would decline slightly (<3% impact)

## Competitive UX Benchmarking

Evaluate product against competitive alternatives on specific dimensions:

**Process:**
1. Identify 3-5 comparable products (direct competitors or adjacent solutions)
2. Choose 1-2 key user tasks (sign up, search, checkout, etc.)
3. Execute the task in each competitor's product
4. Compare speed, friction, clarity, and delight

**Benchmark table:**

| Task | Your Product | Competitor A | Competitor B | Winner | Insight |
|---|---|---|---|---|---|
| "Add collaborator to doc" | 4 steps, clear | 2 steps, unclear flow | 3 steps, fast | Competitor A | We are too slow; Competitor B's approach is clearer |
| "Search for saved item" | Search bar visible, fast results | Search hidden in menu, slower | No search, browse only | Your product | We have clear advantage here |

**Use this for:**
- Identifying where product lags (and prioritizing improvements)
- Finding uncompetitive weaknesses before customers notice
- Celebrating areas where product is better
- Spotting best-in-class patterns worth emulating or improving on

## Anti-Patterns in UX Critique

| Anti-Pattern | Why It Fails | Example of Failure |
|---|---|---|
| Feedback based on personal preference, not usability principle | Designer cannot improve if feedback is subjective | "I do not like the color blue; make it purple" - not actionable, may not improve UX |
| Critique without understanding user context | You suggest fixes for problem that does not exist | "Make this button bigger" without knowing this is power user interface where accuracy matters more than size |
| Focusing only on visual design, missing interaction problems | You miss the real friction point | Complimenting modern design while 30% of users fail at primary task due to confusing flow |
| Requesting feature instead of critiquing UX | Conflating product and design feedback | "Add a favorites feature" is not UX critique; UX critique is "users struggle to relocate items, suggesting need for quick access" |
| Treating all issues as equally important | Designer does not know what to prioritize | Listing 50 issues without severity rating; designer overwhelmed and does not know where to start |
| Critique without business context | Suggest improvements that do not affect metrics | Critique focuses on "app is not beautiful enough" when retention is already 90% and conversion is industry-leading |
| Comparing to non-comparable product | Misleads designer about best practice | "Slack does it this way" for a feature Slack has zero use for |

## Output Template

---
**UX CRITIQUE: [Product or Feature Name]**

**Product/Competitor:** [URL or name]
**Date:** [Date]
**Reviewer:** [Your name]
**Context:** [What user task or scenario were you evaluating?]

**Executive Summary**
[1-2 sentence summary: What works well, and what is the primary friction point?]

**What Works Well**
1. [Positive observation with specific example and why it matters]
2. [Positive observation with specific example and why it matters]
3. ...

**Issues Found**

| Issue | Framework | Severity | Frequency | User Impact | Suggested Direction | Business Impact |
|---|---|---|---|---|---|---|
| [Issue: Be specific - "No feedback when saving, user uncertain if action registered"] | [Nielsen #1: Visibility] | Critical/Major/Minor | Always/Often/Occasionally | [What happens to user?] | [Direction, not solution] | [Does this affect conversion / retention / support cost?] |

**Critical Issue Deep Dive: [Most Critical Issue]**
[Detailed explanation of the most important issue, why it is critical, and how fixing it would impact key metrics]

Example: "When user clicks Save on large forms, there is no feedback for 3-5 seconds while data is being uploaded. User is uncertain if click registered and often clicks multiple times, creating duplicate submissions. This violates Nielsen's heuristic #1 (visibility of system status). Fixing with a 'Saving...' indicator would reduce duplicate form submissions by estimated 20% and support cost by $X annually."

**Quick Wins** (Low effort, high impact improvements)
1. [Change that could be made quickly with significant improvement]: [Specific fix and impact]
2. ...

**Areas Needing Deeper Investigation**
[Any areas where usability testing would reveal issues that cannot be determined from inspection alone]

Example: "Cannot determine from inspection alone whether users understand what 'Advanced Filters' contains. Recommend user test with 5 users on filter discovery task to see if they find the feature."

**Competitive Benchmarking** (if applicable)
Task: [User task being benchmarked]
| Product | Steps | Time | Friction | Winner |
|---|---|---|---|---|
| Your product | [X steps] | [Time] | [Friction points] | [Who wins on this metric?] |
| Competitor A | | | | |
| Competitor B | | | | |

**Mobile-Specific Observations** (if applicable)
[Any mobile-specific issues: thumb zones, gesture patterns, load times, form inputs, etc.]

**Accessibility Observations** (if applicable)
[Major accessibility issues: color contrast, keyboard navigation, alt text, captions, semantic HTML]

**Recommendations by Priority**
1. [Critical]: [Issue and fix by ship date]
2. [Major]: [Issue and fix in next iteration]
3. [Minor]: [Issue and fix when bandwidth allows]

---
