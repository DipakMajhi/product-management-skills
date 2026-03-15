---
name: funnel-optimization
description: "Diagnose and optimize product funnels including acquisition, onboarding, activation, upgrade, and checkout flows. Covers funnel mapping with micro-conversions, bottleneck analysis with impact modeling, drop-off diagnosis (5 root causes), BJ Fogg Behavior Model (B=MAP) application, progressive disclosure design, behavioral nudges, experiment design for each funnel stage, AARRR pirate metrics optimization, funnel benchmarks by category, and multi-touch attribution. Use when improving conversion rates, diagnosing drop-offs, designing funnel experiments, optimizing onboarding, or answering 'how would you improve this funnel?' in PM interviews."
argument-hint: "[describe the funnel (acquisition, onboarding, upgrade, checkout), share any conversion data you have, and describe the primary goal]"
---

# Funnel Optimization Framework

A funnel is a sequence of steps where users must complete each step to reach the goal. Every step has a conversion rate; improving any step improves the overall funnel. The key insight: focus on the step with the highest marginal improvement potential, not the step with the lowest absolute conversion.

Apply this skill to: $ARGUMENTS

## Step 1: Map the Funnel with Micro-Conversions

Write out EVERY step a user takes from entry to goal. "Signup" is not a step -- "enter email, click verify link, set password, complete profile" are four steps.

### Funnel Types

**Acquisition Funnel**: Ad/Content --> Landing Page --> CTA Click --> Signup Form --> Email Verification --> Account Created

**Onboarding Funnel**: Account Created --> Welcome Screen --> First Core Action --> Second Core Action --> Activation Milestone

**Upgrade Funnel**: Free User --> Hits Usage Limit --> Views Pricing --> Selects Plan --> Enters Payment --> Confirms Purchase

**Checkout Funnel**: Add to Cart --> View Cart --> Begin Checkout --> Shipping Info --> Payment Info --> Order Confirmation

### Micro-Conversion Mapping
Between each major step, identify micro-conversions:
- Page load (did the page render?)
- Scroll depth (did they see the CTA?)
- Field interaction (did they start filling the form?)
- Error encounters (did they hit validation errors?)
- Abandonment point (where exactly did they leave?)

Micro-conversions reveal WHERE within a step the drop-off actually happens.

---

## Step 2: Measure Each Step

| Step | Description | Entry N | Completions | Completion % | Drop-off % | Median Time | P90 Time |
|---|---|---|---|---|---|---|---|
| 1 | [Step] | [N] | [N] | [%] | [%] | [Time] | [Time] |
| 2 | [Step] | [N] | [N] | [%] | [%] | [Time] | [Time] |
| ... | | | | | | | |

**Overall funnel conversion** = Step 1 CR x Step 2 CR x Step 3 CR x ... Step N CR

---

## Step 3: Bottleneck Analysis (Impact Modeling)

For each step, calculate: "If I improved this step by 20%, what would the overall funnel conversion become?"

**Example:**
```
Current: 60% x 80% x 70% x 50% = 16.8% overall
Improve Step 4 (50% --> 60%): 60% x 80% x 70% x 60% = 20.2% (+20% lift)
Improve Step 1 (60% --> 72%): 72% x 80% x 70% x 50% = 20.2% (+20% lift)
Improve Step 3 (70% --> 84%): 60% x 80% x 84% x 50% = 20.2% (+20% lift)
```

In this case, all steps have equal leverage. But often one step dominates -- that's the bottleneck.

**Priority = Impact x Feasibility**. A 20% improvement in a step with 30% CR is harder than 20% improvement in a step with 70% CR.

---

## Step 4: Diagnose Drop-off (5 Root Causes)

For each high-drop-off step, investigate which root cause applies:

### Cause 1: Confusion
Users don't understand what's being asked or what to do next.

**Signals**: High time-on-step, rage clicks, help article visits, back-button usage
**Diagnostic methods**: Session recordings, 5-second test, user interview
**Fixes**: Rewrite copy, add tooltip, simplify the ask, add visual hierarchy, reduce options

### Cause 2: Friction
The step is unnecessarily difficult, slow, or annoying.

**Signals**: High time-on-step, form field abandonment, error messages, page load time
**Diagnostic methods**: Form analytics, performance monitoring, error logs
**Fixes**: Remove fields, pre-fill data, reduce steps, add autofill, improve load time, allow save-and-continue

### Cause 3: Motivation Loss
Users have lost confidence in the value by this point.

**Signals**: Quick abandonment (low time-on-step), no interaction before leaving, high bounce from pricing page
**Diagnostic methods**: Exit surveys, value proposition testing, pricing perception research
**Fixes**: Reorder steps to deliver value before asking for effort, add social proof, show progress indicators, reduce commitment level

### Cause 4: Distraction
Users navigate away rather than dropping out intentionally.

**Signals**: Click-away to other pages, tab switching, new session starts (resumed funnel)
**Diagnostic methods**: Click heatmaps, navigation flow analysis
**Fixes**: Remove navigation distractions, minimize outbound links, add urgency cues, use modal/focused flow

### Cause 5: Technical Failure
Bugs, errors, or performance issues cause drop-off.

**Signals**: Error logs, 500/400 responses, JavaScript errors, crash reports
**Diagnostic methods**: Error monitoring (Sentry, Datadog), performance dashboards
**Fixes**: Fix the bug. Always fix technical failures before optimizing UX -- broken funnels can't be optimized.

---

## Step 5: Apply the BJ Fogg Behavior Model (B = MAP)

For each funnel step, assess:

**Behavior = Motivation x Ability x Prompt**

| Component | Question | If Weak... |
|---|---|---|
| **Motivation** | Does the user want to complete this step? | Add value reinforcement, social proof, urgency, or reduce perceived risk |
| **Ability** | Can the user easily complete this step? | Simplify, reduce fields, pre-fill, provide defaults, reduce cognitive load |
| **Prompt** | Is there a clear trigger telling them what to do? | Add CTA, notification, visual cue, or contextual nudge |

**All three must be present for the behavior to occur.** If any element is missing or weak, the step will have high drop-off regardless of the other two.

### Prompt Types
- **Spark**: Adds motivation to users with high ability (e.g., "Join 10,000 teams already using this")
- **Facilitator**: Reduces friction for motivated users (e.g., "Sign up with Google" instead of email form)
- **Signal**: Reminds capable, motivated users to act (e.g., email reminder "You left items in your cart")

---

## Step 6: Progressive Disclosure

Reveal information and complexity gradually. Don't ask for everything upfront.

### Progressive Profiling
| Visit | What You Ask | What You Give |
|---|---|---|
| First visit | Email only | Access to free content or trial |
| After activation | Name, company, role | Personalized experience |
| After demonstrated value | Full profile, preferences | Advanced features |
| At upgrade | Payment info | Full product access |

### Commitment Escalation
Design the funnel so each step asks for slightly more commitment than the previous:
1. Browse freely (zero commitment)
2. Create free account (email)
3. Complete onboarding (time investment)
4. Invite teammate (social commitment)
5. Upgrade to paid (financial commitment)

Each step should deliver enough value to justify the next level of commitment.

---

## Step 7: Behavioral Nudges

| Nudge | Mechanism | When to Apply | Example |
|---|---|---|---|
| **Social proof** | People follow others | Signup, pricing, upgrade | "Used by 50,000+ product teams" |
| **Scarcity** | Limited availability increases urgency | Pricing, trials | "Free trial ends in 3 days" |
| **Anchoring** | First number sets expectations | Pricing pages | Show highest tier first to anchor |
| **Default effect** | People accept pre-set options | Plan selection, settings | Pre-select the recommended plan |
| **Loss aversion** | Losses feel stronger than equivalent gains | Upgrade, retention | "You'll lose access to X, Y, Z" |
| **Progress effect** | Completion momentum motivates continuation | Onboarding, checkout | "You're 75% done!" |
| **Reciprocity** | Giving triggers desire to give back | Before asking for info | Provide value/insight before asking for email |
| **Endowment effect** | People value what they already have | Trial-to-paid conversion | "Your data, settings, and history will be preserved" |

---

## Step 8: Experiment Design

For each diagnosed problem, design an A/B test:

| Experiment | Hypothesis | Step Targeted | Primary Metric | Guardrail Metric | Min. Sample | Duration |
|---|---|---|---|---|---|---|
| [Name] | "By [change], [metric] will improve by [X%] because [reason]" | Step [N] | Step CR | Overall funnel CR / NPS | [N] | [weeks] |

### Experiment Prioritization (ICE Score)
Score each experiment 1-10:
- **Impact**: How much will this move the metric?
- **Confidence**: How sure are we this will work?
- **Ease**: How easy is this to implement?

ICE Score = (Impact + Confidence + Ease) / 3

### Quick Wins (No A/B Test Needed)
Some changes are safe to ship without testing:
- Fixing broken functionality (errors, bugs, load time)
- Removing unnecessary form fields
- Adding clear error messages to form validation
- Improving page load speed
- Adding HTTPS/trust indicators

---

## Funnel Benchmarks

### SaaS Onboarding Benchmarks
| Metric | Good | Great | Elite |
|---|---|---|---|
| Visit-to-signup | 2-5% | 5-10% | 10%+ |
| Signup-to-activation | 20-40% | 40-60% | 60%+ |
| Free-to-paid conversion | 2-5% | 5-10% | 10%+ |
| Time-to-value | < 1 day | < 1 hour | < 5 min |

### E-Commerce Checkout Benchmarks
| Metric | Average | Good | Elite |
|---|---|---|---|
| Add-to-cart rate | 5-10% | 10-15% | 15%+ |
| Cart-to-checkout | 30-50% | 50-70% | 70%+ |
| Checkout completion | 40-60% | 60-75% | 75%+ |
| Overall conversion | 1-3% | 3-5% | 5%+ |

---

## AARRR Stage Optimization

| AARRR Stage | Primary Question | Key Funnel | Top Optimization Levers |
|---|---|---|---|
| **Acquisition** | Are we attracting the right users? | Channel --> Landing --> Signup | Channel-market fit, landing page messaging, ad targeting |
| **Activation** | Do they experience core value? | Signup --> Onboarding --> Aha moment | Time-to-value reduction, onboarding simplification, progressive disclosure |
| **Retention** | Do they come back? | First session --> Return visit --> Habit | Engagement hooks, lifecycle emails, habit loop design |
| **Revenue** | Do they pay? | Free use --> Upgrade trigger --> Payment | Pricing page design, value demonstration, upgrade prompts |
| **Referral** | Do they bring others? | Value moment --> Share --> New signup | Share mechanics, referral incentives, viral loop design |

**Rule**: Optimize in this order: Retention first (no point acquiring users who leave), then Activation (no point retaining users who never experienced value), then Acquisition (now you have a product worth acquiring users for), then Revenue and Referral.

---

## Output Template

```
FUNNEL ANALYSIS: [Funnel Name]
Entry Point: [Where users enter]
Goal: [What successful completion looks like]
Date: [Today]
Period: [Data date range]

FUNNEL MAP
[Step-by-step with micro-conversions]

FUNNEL METRICS
[Table with entry N, completion %, drop-off %, time for each step]

Overall Conversion: [X%]
Benchmark: [Y% -- source]

BOTTLENECK ANALYSIS
Primary bottleneck: Step [N] -- [Name] ([X%] drop-off)
Impact of 20% improvement: Overall conversion from [X%] to [Y%] (+[Z] pp)

DIAGNOSIS
Root cause: [Confusion / Friction / Motivation Loss / Distraction / Technical]
Evidence: [Specific data or observation]
B=MAP assessment: Motivation [H/M/L] | Ability [H/M/L] | Prompt [H/M/L]

EXPERIMENT ROADMAP
[ICE-scored experiment list with hypotheses]

QUICK WINS
[Changes to ship without testing]

EXPECTED IMPACT
If all experiments succeed: Overall conversion from [X%] to [Y%] (+[Z] pp)
Revenue/user impact: [Estimated]
```
