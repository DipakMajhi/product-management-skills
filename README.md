# Product Management Skills Plugin

A comprehensive Product Management skills suite for Claude. 40 expert skills and 43 shortcut commands covering the full PM lifecycle, from strategy and discovery through execution, growth, analytics, design, career development, and legal.

Each skill contains expert-level frameworks, named methodologies with attribution, worked examples, anti-patterns, and structured output templates.

Compatible with Claude Cowork (desktop) and Claude Code (CLI).

Built by [Dipak Majhi](https://mypminterview.com) for practicing PMs, PM interview candidates, and founders.

---

## Repository Structure

```
product-management-skills/
  .claude-plugin/
    plugin.json          # Plugin manifest
  skills/
    skill-name/
      SKILL.md           # Skill instructions (150-800+ lines each)
  README.md
```

Skills are organized as directories under `skills/`. Each directory contains a `SKILL.md` file with YAML frontmatter and detailed instructions. Short "router" skills delegate to comprehensive parent skills for specific modes of operation.

---

## Installation

### Claude Cowork (Desktop)

1. [Download the ZIP](https://github.com/DipakMajhi/product-management-skills/archive/refs/heads/main.zip) from this repository
2. Open Claude Cowork
3. Click **Customize** in the left sidebar
4. Click **+** beside **Personal Plugins**
5. Upload the downloaded ZIP file
6. Start using the skills

### Claude Code (CLI)

```bash
claude plugin marketplace add DipakMajhi/product-management-skills
claude plugin install pm-skills@product-management-skills
```

### Other AI Assistants (Universal SKILL.md format)

```bash
# Copy all skills to Gemini CLI
cp -r skills/* ~/.gemini/skills/ 2>/dev/null

# Copy all skills to Cursor (project-level)
mkdir -p .cursor/skills/
cp -r skills/* .cursor/skills/ 2>/dev/null
```

---

## How to Use

There are two ways to invoke skills:

**1. Slash commands** -- type a short command name and Claude routes to the right skill. For example, `/write-prd` invokes the `prd-writer` skill.

**2. Natural language** -- describe what you need and Claude matches the appropriate skill automatically. For example, "Help me define my North Star Metric" invokes the `metrics-and-okrs` skill.

Most skills accept an argument describing the product, feature, or context. For example:

```
/write-prd in-app collaboration for a project management tool
/strategy AI writing assistant for non-native English speakers
/pricing B2B developer tools platform
```

---

## Skills Reference

### Strategy (8 skills)

| Skill | Command | What It Does |
|---|---|---|
| product-strategy-canvas | `/strategy` | Build a complete strategy canvas using Playing to Win, Good Strategy Bad Strategy, and Rumelt's kernel |
| product-vision | `/vision` | Craft a product vision using narrative, Press Release/FAQ, and one-sentence formats |
| competitive-intelligence | `/competitive-scan`, `/profile-competitor`, `/battlecard` | Full competitive suite: landscape mapping, deep competitor profiling, and sales battlecards |
| business-model | `/business-model` | Design or stress-test a business model with BMC, Lean Canvas, and unit economics |
| pricing-strategy | `/pricing` | Build pricing strategy using value-based, competition-based, and cost-plus models |
| market-sizing | `/market-size` | Estimate TAM, SAM, and SOM using top-down, bottom-up, and Fermi techniques |
| strategic-frameworks | `/frameworks` | Apply 12 frameworks: SWOT/TOWS, PESTLE, Porter's Five Forces, Ansoff Matrix, and more |
| value-proposition | `/value-prop` | Define value proposition using JTBD, Strategyzer Canvas, and April Dunford's methodology |

### Discovery (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| continuous-discovery | `/discover` | Run discovery using Teresa Torres' Opportunity Solution Trees and Marty Cagan's dual-track |
| assumption-testing | `/brainstorm` | Map, score, and design pretotype tests for product assumptions |
| prioritization | `/prioritize` | Score and rank with RICE, ICE, MoSCoW, Kano, WSJF, and Eisenhower frameworks |

### User Research (2 skills)

| Skill | Command | What It Does |
|---|---|---|
| user-research | `/interview`, `/research-users`, `/journey-map` | Complete research suite: interview design, contextual inquiry, JTBD extraction, persona building, journey mapping |
| voice-of-customer | `/triage-requests`, `/analyze-feedback` | Sentiment classification, theme extraction, JTBD mapping, feature request triage, and opportunity scoring |

### Competitive Intelligence (1 skill)

| Skill | Command | What It Does |
|---|---|---|
| competitive-intelligence | `/competitive-scan`, `/profile-competitor`, `/battlecard` | Full suite: landscape mapping (Mode A), deep profiles (Mode B), battlecards (Mode C), win/loss (Mode D) |

### Data and Analytics (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| sql-for-pms | `/write-query` | Generate SQL for 25+ PM query patterns across BigQuery, PostgreSQL, MySQL, and Snowflake |
| ab-testing | `/analyze-test` | Design experiments, calculate sample size, and interpret results with Ship/Iterate/Stop framework |
| metrics-and-okrs | `/define-metrics`, `/plan-okrs`, `/north-star`, `/analyze-cohorts` | North Star definition, HEART/AARRR frameworks, metric trees, OKR writing with Doerr methodology |

### Marketing and Growth (4 skills)

| Skill | Command | What It Does |
|---|---|---|
| positioning | `/market-product` | Product positioning using Geoffrey Moore template and Al Ries/Jack Trout laws |
| growth-loops | `/growth-strategy` | Design growth loops using Reforge methodology, Andrew Chen, and Casey Winters frameworks |
| gtm-strategy | `/plan-launch` | Complete go-to-market strategy with beachhead selection (Geoffrey Moore) and launch planning |
| icp-builder | `/define-icp` | Define Ideal Customer Profile with scoring methodology, data sources, and ABM integration |

### Execution (6 skills)

| Skill | Command | What It Does |
|---|---|---|
| prd-writer | `/write-prd` | Write comprehensive 8-section PRDs with problem statements, user stories, and success metrics |
| roadmap-builder | `/roadmap` | Build roadmaps using Now/Next/Later (Janna Bastow), outcome-driven, and theme-based formats |
| user-stories | `/write-stories` | Write stories with INVEST criteria, Jeff Patton story mapping, and BDD acceptance criteria |
| sprint-lifecycle | `/sprint-plan`, `/retro` | Complete sprint toolkit: planning, capacity estimation, retrospectives, and release notes |
| stakeholder-management | `/stakeholder-map` | Map stakeholders with Mendelow's Power/Interest grid and design communication plans |
| okr-planner | `/plan-okrs` | Write OKRs using John Doerr's methodology with CFR cadence |

### Improvement (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| retention-toolkit | `/improve-retention`, `/analyze-cohorts` | Retention diagnosis, cohort analysis, activation moment identification, and intervention design |
| funnel-optimization | `/optimize-funnel` | Diagnose and optimize acquisition, onboarding, activation, and checkout funnels |
| product-iteration | `/iterate`, `/improve-product` | Structured iteration using Build-Measure-Learn, PDCA/Deming cycle, and hypothesis-driven development |

### Design (3 skills)

| Skill | Command | What It Does |
|---|---|---|
| design-thinking | `/design-sprint` | Apply IDEO 5-stage model, Stanford d.school methodology, and British Design Council Double Diamond |
| ux-critique | `/critique-design` | Evaluate UX using Nielsen's heuristics, Don Norman's principles, and cognitive load theory |
| design-brief | `/write-brief` | Write design briefs with JTBD integration, constraint documentation, and collaboration models |

### Career and Interview Prep (5 skills)

| Skill | Command | What It Does |
|---|---|---|
| interview-prep-coach | `/interview-prep` | PM interview coaching with CIRCLES method, company-specific patterns (Google, Meta, Amazon), and scoring rubrics |
| pm-career-ladder | `/career-growth`, `/career-check` | Career progression with IC vs Management tracks, company ladder mappings, and promotion planning |
| review-resume | `/review-resume` | Score and review PM resumes with XYZ formula, ATS optimization, and level-specific feedback |
| tailor-resume | `/tailor-resume` | Tailor resumes to job descriptions with JD decoding, mirror language, and ATS keyword strategy |
| grammar-check | `/proofread` | Proofread PM writing with BLUF pattern, Minto Pyramid, and document-type-specific guidelines |

### Legal (2 skills)

| Skill | Command | What It Does |
|---|---|---|
| draft-nda | `/draft-nda` | Draft NDAs with clause-by-clause guidance, carve-outs, remedies, and complete templates |
| privacy-policy | `/draft-privacy-policy` | Draft privacy policies covering GDPR, CCPA/CPRA, COPPA, LGPD, PIPEDA, and Privacy by Design |

---

## Quick Start

**Preparing for a PM interview:**
```
/interview-prep
/improve-product Spotify
/strategy AI writing assistant for non-native English speakers
```

**Starting a new product:**
```
/strategy
/discover
/write-prd
/plan-launch
```

**Improving an existing product:**
```
/analyze-feedback
/improve-retention
/optimize-funnel
/iterate
```

**Setting up metrics and goals:**
```
/north-star
/define-metrics
/plan-okrs
```

**Job search:**
```
/review-resume
/tailor-resume
/career-growth
```

**Competitive analysis:**
```
/competitive-scan
/profile-competitor Notion
/battlecard
```

---

## Skill Quality

Every skill in this plugin follows a consistent quality standard:

- Named frameworks with proper attribution (e.g., Teresa Torres, Geoffrey Moore, Reforge, Nielsen)
- Detailed tables comparing approaches, with pros, cons, and when-to-use guidance
- Worked examples with realistic numbers and scenarios
- Anti-patterns section documenting common mistakes and why they fail
- Structured output templates ready for stakeholder delivery
- Typical skill length: 150 to 800+ lines of expert-level content

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT
