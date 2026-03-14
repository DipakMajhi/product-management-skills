# PM Skills Repository

A complete Product Management skills suite for Claude. 10 plugins, 45 skills, and 46 commands covering the full PM lifecycle.

Compatible with Claude Cowork (desktop) and Claude Code (CLI).

Built by [Dipak Majhi](https://mypminterview.com) for practicing PMs, PM interview candidates, and founders.

---

## Repository Structure

Every plugin follows this layout:

```
pm-plugin-name/
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

All 10 plugins install automatically.

### Claude Code (CLI)

```bash
claude plugin marketplace add DipakMajhi/product-management-skills

claude plugin install pm-toolkit@product-management-skills
claude plugin install pm-product-strategy@product-management-skills
claude plugin install pm-product-discovery@product-management-skills
claude plugin install pm-market-research@product-management-skills
claude plugin install pm-data-analytics@product-management-skills
claude plugin install pm-marketing-growth@product-management-skills
claude plugin install pm-product-go-to-market@product-management-skills
claude plugin install pm-product-execution@product-management-skills
claude plugin install pm-product-design@product-management-skills
claude plugin install pm-product-improvement@product-management-skills
```

### Other AI Assistants (Universal SKILL.md format)

```bash
# Copy all skills to Gemini CLI
for plugin in pm-*/; do
  cp -r "${plugin}skills/"* ~/.gemini/skills/ 2>/dev/null
done

# Copy all skills to Cursor (project-level)
for plugin in pm-*/; do
  mkdir -p .cursor/skills/
  cp -r "${plugin}skills/"* .cursor/skills/ 2>/dev/null
done
```

---

## Available Plugins

| Plugin | Skills | Commands | What It Covers |
|---|---|---|---|
| pm-toolkit | 7 | 7 | Resume, career, interview, NDA, proofreading |
| pm-product-strategy | 8 | 7 | Vision, strategy canvas, competitive analysis, business models, pricing, market sizing |
| pm-product-discovery | 5 | 5 | Opportunity mapping, user interviews, assumption testing, prioritization |
| pm-market-research | 4 | 4 | Personas, journey maps, competitor profiling, feedback analysis |
| pm-data-analytics | 3 | 3 | SQL queries, A/B testing, cohort analysis |
| pm-marketing-growth | 3 | 3 | Positioning, North Star Metric, growth loops |
| pm-product-go-to-market | 2 | 3 | GTM strategy, ICP definition, launch planning |
| pm-product-execution | 7 | 8 | PRDs, OKRs, roadmaps, user stories, sprints, stakeholder maps, metrics |
| pm-product-design | 3 | 3 | Design thinking, UX critique, design briefs |
| pm-product-improvement | 3 | 4 | Retention diagnosis, funnel optimization, product iteration |

---

## Quick Start

**Preparing for a PM interview:**
```
/pm-toolkit:interview-prep
/pm-product-improvement:improve-product Spotify
/pm-product-strategy:strategy AI writing assistant for non-native English speakers
```

**Starting a new product:**
```
/pm-product-strategy:strategy
/pm-product-discovery:discover
/pm-product-execution:write-prd
/pm-product-go-to-market:plan-launch
```

**Improving an existing product:**
```
/pm-market-research:analyze-feedback
/pm-product-improvement:improve-retention
/pm-product-improvement:optimize-funnel
```

**Job search:**
```
/pm-toolkit:review-resume
/pm-toolkit:tailor-resume
/pm-toolkit:career-growth
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT
