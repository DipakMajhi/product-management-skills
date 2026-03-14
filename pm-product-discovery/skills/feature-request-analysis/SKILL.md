---
name: feature-request-analysis
description: "Analyze and categorize a batch of customer feature requests to find patterns, prioritize opportunities, and surface underlying needs. Use this skill when someone has a backlog of customer requests, NPS comments, support tickets, or sales feedback and wants to extract meaningful product insights."
---

# Feature Request Analyzer

You transform raw customer requests into structured product intelligence. Raw requests are noisy - your job is to find the signal.

## Analysis Process

Apply this skill to: $ARGUMENTS


### Step 1: Categorize by Type
- **Bug report disguised as a feature**: "Can you make X work?" (often a usability or reliability issue)
- **Workaround request**: "Can you export to CSV?" (suggests missing workflow support)
- **Outcome-based request**: "I need to do X faster" (points to a clear opportunity)
- **Feature copy from competitor**: "Can you add what [Competitor] does?" (signals competitive gap)
- **Edge case**: One-off request from a single user with unusual circumstances
- **Niche power user request**: Useful for a small segment but not broadly valuable

### Step 2: Theme Extraction
Group requests by underlying opportunity, not surface feature. Multiple requests for "better search", "filter options", and "sort by date" may all point to the same underlying opportunity: "Users cannot find what they are looking for quickly."

### Step 3: Frequency and Segment Analysis
For each theme:
- How many distinct customers requested it?
- Which customer segments are asking? (new users, power users, enterprise, etc.)
- Is this concentrated in high-value accounts?

### Step 4: JTBD Translation
Translate the top themes into proper JTBD format: "When [situation], I want to [motivation], so I can [outcome]."

### Step 5: Prioritization Signal
Flag which themes:
- Appear across multiple customer segments (broad applicability)
- Come from highest-value accounts (revenue signal)
- Block users from their primary goal (severity signal)
- Map to existing strategic priorities (alignment signal)

## Output Template

---
**FEATURE REQUEST ANALYSIS**
**Total Requests Analyzed:** [N]
**Date Range:** [Period]

**Theme Summary**

| Theme | Request Count | Unique Customers | Key Segments | Priority Signal |
|---|---|---|---|---|
| [Theme 1] | N | N | [Segments] | [High/Med/Low] |
| [Theme 2] | ... | | | |

**Top 3 Opportunity Translations**

1. **[Theme]**
   JTBD: "When [situation], I want to [motivation], so I can [outcome]"
   Sample requests: "[Quote 1]", "[Quote 2]"
   Recommended action: [Investigate further / Add to discovery / Add to roadmap / Decline]

2. ...

**Requests to Decline (with rationale)**
[Any requests that should be closed out with an explanation]

**Data Gaps**
[What additional segmentation or research would sharpen this analysis]
---
