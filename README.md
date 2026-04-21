# AI Skills for Salesforce Prompt Builder

A collection of reusable AI skills for researching, planning, and building features in Salesforce Prompt Builder.

## 🎯 Overview

This repository contains production-ready skills for automating research and competitive analysis for Salesforce Prompt Builder feature development.

## 📦 Skills Included

### 1. Salesforce Prompt Builder Research (v1.1.0)

**Purpose:** Automate comprehensive research for any Prompt Builder feature, including competitive analysis and positioning strategy.

**Location:** `.claude/skills/salesforce-prompt-builder-research/`

**What it does:**
- Researches Salesforce capabilities (Prompt Builder, Agentforce, MCP, APIs)
- Analyzes competitors (OpenAI, Microsoft, Google, Amazon, etc.)
- Identifies Salesforce competitive advantages
- Creates feature comparison matrices
- Generates positioning statements
- Provides implementation recommendations

**Triggers:**
```
"I want to add [feature] to Prompt Builder"
"Research Prompt Builder capabilities for [use case]"
"How does Agentforce handle [capability]?"
"What's our competitive advantage for [feature]?"
"Compare Salesforce vs [competitor] for [feature]"
```

**Research Coverage:**
- ✅ Salesforce: Prompt Builder, Agentforce, Einstein Trust Layer, Flow Builder
- ✅ Competitors: OpenAI, Microsoft, Google, Anthropic, Amazon + 4 more
- ✅ Technical: APIs, security, integration patterns
- ✅ Strategic: Positioning, differentiation, go-to-market

## 🚀 Quick Start

### Installation

1. **Clone this repository:**
   ```bash
   git clone https://github.com/jrattanpal/AI-Skills.git
   cd AI-Skills
   ```

2. **Copy skill to your Claude Code skills directory:**
   ```bash
   cp -r .claude/skills/salesforce-prompt-builder-research ~/.claude/skills/
   ```

3. **Verify installation:**
   ```bash
   ls ~/.claude/skills/salesforce-prompt-builder-research/
   ```
   You should see: `SKILL.md`, `README.md`, `references/`, `examples/`

### Usage

Just ask Claude naturally:

```
"I want to add real-time collaboration to Prompt Builder"
```

The skill will automatically:
1. Research Salesforce capabilities
2. Research competitor implementations
3. Identify Salesforce advantages
4. Create comparison matrix
5. Generate positioning statements
6. Provide recommendations
7. Save research artifact to `.agents/artifacts/`

### Example Output

For: `"I want to add skill export to Prompt Builder"`

**You get:**
- Technical feasibility (Salesforce metadata API, file generation)
- Competitor analysis (OpenAI: no export, Microsoft: proprietary, Anthropic: skill.md)
- Comparison matrix across 5+ platforms
- Salesforce advantages (portability, metadata bundle, governance)
- Positioning: "Unlike OpenAI which locks skills in their platform, Salesforce..."
- Must-have vs differentiator features
- Implementation recommendations

**Saved to:** `.agents/artifacts/prompt-builder-skill-export-research-YYYY-MM-DD.md`

## 📚 Documentation

### Skill Files

```
.claude/skills/salesforce-prompt-builder-research/
├── SKILL.md (21KB)                      # Main skill definition
├── README.md (9.4KB)                    # Full documentation
├── references/
│   ├── competitive-analysis-framework.md (19KB)  # Competitive research guide
│   └── research-sources.md (7.3KB)               # Research source guide
└── examples/
    └── example-research-briefs.md (27KB)         # Template research briefs
```

### Quick Links

- **[Skill Documentation](/.claude/skills/salesforce-prompt-builder-research/README.md)** - How to use the skill
- **[Competitive Framework](/.claude/skills/salesforce-prompt-builder-research/references/competitive-analysis-framework.md)** - Competitive research methodology
- **[Research Sources](/.claude/skills/salesforce-prompt-builder-research/references/research-sources.md)** - Where to find information
- **[Example Briefs](/.claude/skills/salesforce-prompt-builder-research/examples/example-research-briefs.md)** - Research templates

### Additional Resources

- **[Implementation Plan](/.agents/artifacts/salesforce-prompt-builder-skills-plan.md)** - Full 40k-word implementation plan for Prompt Builder skills
- **[Quick Reference](/.agents/artifacts/skill-usage-quick-reference.md)** - One-page quick start
- **[Complete Summary](/.agents/artifacts/COMPLETE-SUMMARY.md)** - Comprehensive overview

## 🎯 Research Topics Covered

### Salesforce
- Prompt Builder (capabilities, architecture, APIs)
- Agentforce (Atlas Reasoning Engine, Agent Builder, Topics, Actions)
- Model Context Protocol (MCP) servers and tools
- Lightning Flow Builder (UI patterns, security)
- Einstein Trust Layer (security, prompt injection prevention)
- Salesforce Security (OLS, FLS, sharing rules)
- Integration patterns (APIs, external services)
- UI/UX patterns (Lightning Design System)

### Competitors
- **OpenAI** - GPT Builder, Custom GPTs, API
- **Microsoft** - Copilot Studio, Power Platform
- **Google** - Vertex AI Agent Builder
- **Anthropic** - Claude, skill.md, MCP
- **Amazon** - Bedrock Agents
- **Adjacent** - Zapier, Make, LangChain
- **Enterprise** - IBM watsonx, ServiceNow AI

### Analysis
- Feature comparison matrices
- User sentiment and reviews
- Pricing and business models
- Technical implementations
- Security and compliance
- Integration capabilities

## 🔍 Research Patterns

The skill recognizes and handles these common patterns:

| Pattern | Trigger | Output |
|---------|---------|--------|
| **Feature Feasibility** | "Can we add [feature]?" | Go/No-Go + competitive positioning |
| **Integration Design** | "How to integrate with [system]?" | Architecture + differentiation |
| **Competitive Analysis** | "How do competitors handle [thing]?" | Detailed comparison + positioning |
| **Security** | "How do we secure [feature]?" | Security architecture + competitive advantages |
| **UX/UI** | "How should we design [UI]?" | UI recommendations + differentiation |

## 🏆 Competitive Advantages Identified

The skill automatically identifies these Salesforce advantages:

1. **Native CRM Data Access** - No integration needed
2. **Einstein Trust Layer** - Enterprise-grade security
3. **Enterprise Relationships** - 150,000+ customers
4. **Agentforce Platform** - Atlas Reasoning Engine
5. **AppExchange Ecosystem** - 7,000+ apps
6. **Multi-Tenant Architecture** - Automatic scaling
7. **Flow Builder Integration** - Existing automation
8. **Industry Solutions** - Vertical-specific features

## 🛠️ Customization

### Add Internal Research Sources

Edit `.claude/skills/salesforce-prompt-builder-research/references/research-sources.md`:

```markdown
## Internal Resources

### Internal Wiki
- URL: https://your-internal-wiki.com
- Best for: Architecture decisions, internal APIs

### Work Tracking
- GUS work items, JIRA tickets
- Look for: Related features, implementation history
```

### Add Custom Research Patterns

Edit `.claude/skills/salesforce-prompt-builder-research/SKILL.md`:

```markdown
### Pattern 6: [Your Pattern]
**User asks**: "[Your trigger]"
**Research focus**: [Your areas]
**Output**: [Your format]
```

### Adjust Research Depth

Modify word limits in `SKILL.md`:
- Quick: 800 words
- Standard: 1,500 words  
- Deep: 2,500 words

## 📊 Version History

### v1.1.0 (2026-04-21)
- ✅ Added automatic competitive analysis
- ✅ 9+ competitor profiles
- ✅ Salesforce advantage identification
- ✅ Positioning statement generation
- ✅ Feature comparison matrices
- ✅ Go-to-market recommendations

### v1.0.0 (2026-04-21)
- ✅ Initial skill creation
- ✅ Core research methodology
- ✅ Salesforce documentation research
- ✅ Technical feasibility assessment
- ✅ Implementation recommendations

## 🤝 Contributing

### Adding New Competitors

1. Edit `.claude/skills/salesforce-prompt-builder-research/references/competitive-analysis-framework.md`
2. Add competitor profile with:
   - What they offer
   - Target market
   - Strengths/weaknesses
   - Research sources
3. Update competitor list in `SKILL.md`

### Adding Research Patterns

1. Document pattern in `SKILL.md`
2. Add example brief in `examples/example-research-briefs.md`
3. Test with sample queries
4. Submit PR with examples

### Improving Research Quality

1. Track which sources provide best information
2. Document findings in `references/research-sources.md`
3. Update research agent instructions in `SKILL.md`
4. Share learnings with team

## 📝 Use Cases

### Product Management
- Feature planning with competitive context
- Roadmap prioritization (table stakes vs differentiators)
- Go-to-market strategy

### Product Marketing
- Competitive battle cards
- Positioning statements
- Key messaging vs competitors

### Engineering
- Technical feasibility assessments
- Architecture decisions
- Integration design

### Sales Enablement
- Competitive intelligence
- Why choose Salesforce
- Objection handling

## 🔒 Security & Privacy

**Data Handling:**
- All research happens locally via Claude Code
- No data sent to external services except documented APIs
- Research artifacts saved locally in `.agents/artifacts/`
- No PII or sensitive data in skill files

**Competitor Research:**
- Uses public documentation and sources only
- Reviews aggregated user feedback (G2, Reddit, etc.)
- No unauthorized access to competitor systems
- Ethical research practices

## 📞 Support

### Issues
- Report issues via GitHub Issues
- Include: query used, expected vs actual output, skill version

### Questions
- Check [Skill README](/.claude/skills/salesforce-prompt-builder-research/README.md) first
- Review [Competitive Framework](/.claude/skills/salesforce-prompt-builder-research/references/competitive-analysis-framework.md)
- Ask in team chat with `@ai-skills` tag

### Feature Requests
- Open GitHub Issue with label `enhancement`
- Describe: use case, expected behavior, benefits

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with Claude Code
- Inspired by the need for systematic competitive research
- Leverages Model Context Protocol (MCP) standards
- Follows Salesforce architecture patterns

## 🚀 Roadmap

### Planned Enhancements
- [ ] Additional competitor profiles (Oracle, SAP AI)
- [ ] Automated competitor monitoring alerts
- [ ] Integration with internal competitive intelligence tools
- [ ] Research quality metrics and tracking
- [ ] Team collaboration features (shared research library)
- [ ] Custom report templates

### Under Consideration
- [ ] Jupyter notebook integration for data analysis
- [ ] Slack bot for quick competitive queries
- [ ] Quarterly competitive review automation
- [ ] Win/loss analysis integration

---

**Created:** 2026-04-21  
**Version:** 1.1.0  
**Maintained by:** Salesforce Prompt Builder Team  
**Repository:** https://github.com/jrattanpal/AI-Skills

---

## 🎯 Get Started Now

1. Clone this repo
2. Copy skill to `~/.claude/skills/`
3. Ask: `"I want to add [feature] to Prompt Builder"`
4. Get comprehensive research with competitive analysis

**That's it!** 🎉
