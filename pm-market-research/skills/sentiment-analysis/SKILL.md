---
name: sentiment-analysis
description: "Analyze user feedback, reviews, NPS comments, or support tickets for sentiment patterns and product insights. Use this skill when someone has a batch of qualitative feedback and wants to extract themes, understand what users love and hate, or prioritize improvements based on customer voice."
---

# User Feedback Sentiment Analyzer

You extract structured product intelligence from unstructured user feedback. Raw feedback is noisy - your job is to find the patterns that drive decisions.

## Analysis Process

Apply this skill to: $ARGUMENTS


### Step 1: Sentiment Classification
Classify each piece of feedback as: Positive, Negative, Mixed, or Neutral.
Calculate the overall sentiment distribution (% of each type).

### Step 2: Theme Extraction
Group feedback by theme, not by feature. A theme is the underlying experience being described:
- "Onboarding confusion" (not "problems with step 3 of signup")
- "Speed and performance" (not "slow loading")
- "Customer support quality"
- "Value for money"

### Step 3: Intensity Mapping
Not all negative feedback is equal. Flag feedback that signals:
- **Churn risk**: "I'm looking at alternatives", "almost cancelled", "not renewing"
- **Advocacy signal**: "recommended to my team", "told my manager", "shared with others"
- **Critical path failures**: The product literally does not work for a core use case

### Step 4: Segment Patterns
Identify if sentiment differs by:
- User segment (new users vs. power users, free vs. paid)
- Use case or product area
- Geography or company size (if data is available)

### Step 5: Actionable Insights
Translate themes into actionable product decisions:
- What to fix immediately (high frequency negative, high churn risk signal)
- What to double down on (high frequency positive, advocacy signal)
- What to investigate further (ambiguous or contradictory signals)

## Output Template

---
**SENTIMENT ANALYSIS REPORT**
**Dataset:** [Description of source - NPS, G2 reviews, support tickets, etc.]
**Volume Analyzed:** [N items]
**Period:** [Date range]

**Overall Sentiment Distribution**
Positive: [X%] | Negative: [X%] | Mixed: [X%] | Neutral: [X%]

**Top Themes**
| Theme | Frequency | Sentiment | Sample Quote | Churn Risk Signal |
|---|---|---|---|---|
| [Theme 1] | [N / X%] | Pos/Neg/Mixed | "[Quote]" | Yes/No |
| [Theme 2] | | | | |

**Churn Risk Signals**
[Direct quotes or paraphrases that indicate churn risk, with frequency]

**Advocacy Signals**
[Quotes or indicators of users promoting the product to others]

**Recommended Actions**
1. **Fix now**: [Theme] - [Reasoning] - [Suggested action]
2. **Invest more**: [Theme] - [Reasoning] - [Suggested action]
3. **Investigate**: [Theme that is unclear and needs more research]

**Segments with Notably Different Sentiment**
[If any segment shows a very different pattern from the overall]
---
