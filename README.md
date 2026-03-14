# PM Skills Repository

A complete Product Management skills suite for Claude. 45 skills and 46 commands covering the full PM lifecycle.

Compatible with Claude Cowork (desktop) and Claude Code (CLI).

Built by [Dipak Majhi](https://mypminterview.com) for practicing PMs, PM interview candidates, and founders.

---

## Repository Structure

```
product-management-skills/
├── .claude-plugin/
│   └── plugin.json        # Plugin manifest
├── skills/
│   └── skill-name/
│       └── SKILL.md       # Skill instructions
├── commands/
│   └── command-name.md    # Slash command definitions
└── README.md
```

---

## Installation

### Claude Cowork — Install from GitHub

1. Open Claude Cowork (desktop app)
2. Click **Customize** in the left sidebar
3. Click **Browse plugins**
4. Click **+** then **Add marketplace from GitHub**
5. Enter: `DipakMajhi/product-management-skills`

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

## Available Skills & Commands

### Strategy
| Skill | Command | What It Does |
|---|---|---|
| product-vision | `/vision` | Craft a clear product vision |
| product-strategy-canvas | `/strategy` | Build a complete strategy canvas |
| competitive-analysis | `/competitive-scan` | Map and analyze competitors |
| business-model | `/business-model` | Design or critique a business model |
| pricing-strategy | `/pricing` | Build a pricing strategy |
| market-sizing | `/market-size` | Estimate TAM, SAM, and SOM |
| strategic-frameworks | — | Apply SWOT, Porter's Five Forces, and more |
| value-proposition | — | Define your value proposition |

### Discovery
| Skill | Command | What It Does |
|---|---|---|
| continuous-discovery | `/discover` | Run ongoing opportunity discovery |
| user-interview | `/interview` | Plan and run user interviews |
| assumption-testing | `/brainstorm` | Surface and test key assumptions |
| prioritization | `/prioritize` | Score and rank opportunities |
| feature-request-analysis | `/triage-requests` | Analyse incoming feature requests |

### Market Research
| Skill | Command | What It Does |
|---|---|---|
| user-personas | `/research-users` | Build research-backed user personas |
| customer-journey-map | `/journey-map` | Map the end-to-end user journey |
| competitor-intelligence | `/profile-competitor` | Deep-dive a single competitor |
| sentiment-analysis | `/analyze-feedback` | Analyse qualitative feedback at scale |

### Data & Analytics
| Skill | Command | What It Does |
|---|---|---|
| sql-for-pms | `/write-query` | Write SQL queries for product data |
| ab-testing | `/analyze-test` | Design and interpret A/B tests |
| cohort-analysis | `/analyze-cohorts` | Run cohort retention analysis |

### Marketing & Growth
| Skill | Command | What It Does |
|---|---|---|
| positioning | `/market-product` | Write positioning and messaging |
| north-star-metric | `/north-star` | Define your North Star Metric |
| growth-loops | `/growth-strategy` | Design compounding growth loops |

### Go-to-Market
| Skill | Command | What It Does |
|---|---|---|
| gtm-strategy | `/plan-launch` | Plan a full product launch |
| icp-builder | `/define-icp` | Define your Ideal Customer Profile |
| — | `/battlecard` | Create a competitive battlecard |

### Execution
| Skill | Command | What It Does |
|---|---|---|
| prd-writer | `/write-prd` | Write a complete 8-section PRD |
| okr-planner | `/plan-okrs` | Write focused OKRs |
| roadmap-builder | `/roadmap` | Build a prioritised roadmap |
| user-stories | `/write-stories` | Convert PRDs into sprint-ready stories |
| sprint-management | `/sprint-plan` | Plan and run a sprint |
| stakeholder-management | `/stakeholder-map` | Map stakeholders and build alignment |
| metrics-framework | `/define-metrics` | Define success metrics |
| — | `/retro` | Run a sprint retrospective |

### Design
| Skill | Command | What It Does |
|---|---|---|
| design-thinking | `/design-sprint` | Run a design thinking sprint |
| ux-critique | `/critique-design` | Critique a design or flow |
| design-brief | `/write-brief` | Write a design brief |

### Improvement
| Skill | Command | What It Does |
|---|---|---|
| retention-analysis | `/improve-retention` | Diagnose and fix retention problems |
| funnel-optimization | `/optimize-funnel` | Find and fix funnel drop-offs |
| product-iteration | `/iterate` | Run structured product iteration |
| — | `/improve-product` | Answer "How would you improve X?" |

### Toolkit
| Skill | Command | What It Does |
|---|---|---|
| interview-prep-coach | `/interview-prep` | Prep for PM interviews |
| pm-career-ladder | `/career-growth` | Plan your PM career growth |
| review-resume | `/review-resume` | Get feedback on your PM resume |
| tailor-resume | `/tailor-resume` | Tailor your resume to a job description |
| grammar-check | `/proofread` | Proofread and fix grammar |
| draft-nda | `/draft-nda` | Draft a basic NDA |
| privacy-policy | — | Draft a privacy policy |
| — | `/career-check` | Audit where you are in your PM career |

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
```

**Job search:**
```
/review-resume
/tailor-resume
/career-growth
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT
