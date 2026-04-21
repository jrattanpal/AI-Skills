# Salesforce Prompt Builder: Planning & Research Artifacts

This directory contains comprehensive planning documents and a reusable research skill for Salesforce Prompt Builder product development.

## Artifacts Created (April 21, 2026)

### 1. Implementation Plan
**File:** `salesforce-prompt-builder-skills-plan.md`

Comprehensive 15-section implementation plan for building an AI skills platform in Salesforce Prompt Builder.

**Key contents:**
- Architecture for skill authoring (Canvas UI, metadata model)
- Integration with internal tools (Record operations) and external tools (MCP servers)
- Security model (prompt injection prevention, Einstein Trust Layer)
- Agentforce integration (Atlas Reasoning Engine, Agent Topics)
- Export/import to skill.md format for Claude Code compatibility
- 4-phase implementation roadmap (12 months)
- User personas, success metrics, risk mitigation

**Size:** ~40,000 words with code examples, UI mockups, security patterns

---

### 2. Research Skill
**Location:** `../.claude/skills/salesforce-prompt-builder-research/`

Reusable skill that automates research about Salesforce Prompt Builder, Agentforce, MCP, and related tools.

**Triggers on:**
- "I want to add a new feature in Prompt Builder"
- "Research Prompt Builder capabilities"
- "How does Agentforce work?"
- "Explore MCP integration patterns"

**Research methodology:**
1. Define research scope
2. Spawn research agent with comprehensive brief
3. Search official Salesforce docs, APIs, specs
4. Synthesize findings into structured report
5. Save artifact and answer question

**Skill structure:**
```
.claude/skills/salesforce-prompt-builder-research/
├── SKILL.md                          # Main skill definition (12k words)
├── README.md                         # Full documentation (8k words)
├── references/
│   └── research-sources.md          # Research sources guide (7k words)
└── examples/
    └── example-research-briefs.md   # Template briefs (13k words)
```

---

### 3. Quick Reference
**File:** `skill-usage-quick-reference.md`

One-page guide for using the research skill.

**Contents:**
- How to trigger the skill
- Common use cases
- Example session
- Tips for best results
- Artifact locations

---

### 4. Competitive Analysis Enhancement 🆕
**File:** `competitive-analysis-enhancement-summary.md`

Summary of v1.1.0 enhancement that adds automatic competitive analysis.

**What's New:**
- Automatic competitor research (OpenAI, Microsoft, Google, etc.)
- Competitive advantage identification
- Feature comparison matrices
- Positioning statements vs competitors
- Differentiation strategy recommendations
- Go-to-market implications

**Key Feature:**
- **Every research request now includes competitive intelligence automatically**
- No need to ask separately - it's built into the skill

---

## How These Artifacts Work Together

```
┌─────────────────────────────────────────────────────────────┐
│ 1. You ask: "I want to add [feature] to Prompt Builder"    │
└─────────────────────────────┬───────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│ 2. Research Skill Activates                                 │
│    (.claude/skills/salesforce-prompt-builder-research/)     │
└─────────────────────────────┬───────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│ 3. Spawns Research Agent                                    │
│    - Searches Salesforce docs                               │
│    - Investigates Agentforce, MCP, APIs                     │
│    - 🆕 Researches competitor platforms                     │
│    - 🆕 Analyzes competitive implementations                │
│    - Analyzes security, integration patterns                │
└─────────────────────────────┬───────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│ 4. Generates Research Report                                │
│    Saved to: .agents/artifacts/[topic]-research-[date].md   │
└─────────────────────────────┬───────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│ 5. You Get:                                                 │
│    ✓ Direct answer to your question                        │
│    ✓ Technical feasibility assessment                      │
│    ✓ Implementation recommendations                         │
│    ✓ 🆕 Competitive comparison matrix                       │
│    ✓ 🆕 Salesforce competitive advantages                   │
│    ✓ 🆕 Positioning strategy vs competitors                 │
│    ✓ Saved artifact for future reference                   │
└─────────────────────────────────────────────────────────────┘
```

---

## Example: How the Implementation Plan Was Created

The `salesforce-prompt-builder-skills-plan.md` was created using this exact research methodology:

1. **User request:** "Create a plan for building AI skills in Salesforce Prompt Builder"

2. **Research executed:**
   - Agent 1: Salesforce Prompt Builder, Agentforce, Atlas Reasoning Engine, security model
   - Agent 2: Claude skill.md format, MCP server structure, tool design patterns

3. **Findings synthesized:**
   - Combined research into comprehensive 15-section plan
   - Included architecture, security, UI/UX, implementation phases
   - Added code examples, mockups, risk mitigation

4. **Artifact saved:**
   - `salesforce-prompt-builder-skills-plan.md` (40k words)
   - Now you can reference this plan anytime

5. **Skill created:**
   - Codified the research methodology into reusable skill
   - Now you can research ANY Prompt Builder feature this way

---

## Using the Research Skill for Future Features

Now when you want to add any new feature to Prompt Builder, just ask:

### Example 1: New Feature
```
You: "I want to add version control to Prompt Builder skills"

Skill researches:
- Salesforce versioning patterns (API versions, package versions)
- Git integration options
- Metadata API change tracking
- Diff visualization in Lightning
- Rollback mechanisms

You get:
✓ Feasibility: Yes, using Metadata API
✓ Approach: Store versions as metadata records
✓ UI: Flow Builder-style version dropdown
✓ Full research saved to artifacts
```

### Example 2: Integration Question
```
You: "How should skills integrate with Tableau?"

Skill researches:
- Tableau REST API capabilities
- Salesforce-Tableau CRM integration
- Embedded analytics patterns
- MCP server for Tableau (if exists)
- Authentication with Connected Apps

You get:
✓ Integration architecture
✓ Auth strategy (OAuth 2.0 via Named Credential)
✓ Example skill workflow
✓ Security considerations
```

### Example 3: Security Question
```
You: "How do we handle PII in skill execution?"

Skill researches:
- Einstein Trust Layer data masking
- Platform encryption options
- Data Classification framework
- Shield Platform Encryption
- Audit logging requirements

You get:
✓ Data protection strategy
✓ Code examples for field masking
✓ Compliance considerations (GDPR, CCPA)
✓ Implementation checklist
```

---

## Research Coverage

The skill can research:

**Salesforce Core**
- ✅ Prompt Builder (when docs available)
- ✅ Agentforce (Atlas, Agent Builder, Topics, Actions)
- ✅ Einstein Trust Layer
- ✅ Lightning Flow Builder
- ✅ Apex, Visualforce, Lightning Web Components
- ✅ Security model (OLS, FLS, sharing rules)

**APIs & Integration**
- ✅ REST, SOAP, Bulk, Metadata, Tooling APIs
- ✅ Platform Events, Change Data Capture
- ✅ External Services, Named Credentials
- ✅ MuleSoft integration patterns

**AI & Automation**
- ✅ Model Context Protocol (MCP)
- ✅ Einstein AI features
- ✅ Automation tools (Flow, Process Builder, Apex)

**UI/UX**
- ✅ Lightning Design System
- ✅ Lightning App Builder patterns
- ✅ Accessibility (WCAG 2.1)
- ✅ Mobile considerations

---

## Future Research Topics

Use the skill to research:

- [ ] Real-time collaboration in Prompt Builder
- [ ] Skill versioning and change management
- [ ] A/B testing framework for skills
- [ ] Multi-language skill support
- [ ] Skill analytics and telemetry
- [ ] Cost allocation and rate limiting
- [ ] Integration with Slack, Teams, other platforms
- [ ] Advanced security: skill sandboxing, resource limits
- [ ] Skill marketplace design and moderation
- [ ] Cross-org skill deployment

---

## Customization

### Add Internal Sources
Edit `.claude/skills/salesforce-prompt-builder-research/references/research-sources.md`:

```markdown
## Internal Salesforce Resources

### Internal Wiki
- URL: https://internal.salesforce.com/wiki
- Search for: Architecture decision records, design docs

### GUS (Work Tracking)
- Use sfcli:gus skill for work item research
- Search for: Related features, implementation history
```

### Add Team Patterns
Edit `.claude/skills/salesforce-prompt-builder-research/examples/example-research-briefs.md`:

```markdown
## Example: Team-Specific Pattern

### User Request
"What's our team's preferred approach for [pattern]?"

### Research Agent Brief
[Your team's specific research template]
```

---

## Files in This Directory

```
.agents/artifacts/
├── README.md                                      # This file
├── salesforce-prompt-builder-skills-plan.md      # Full implementation plan
├── skill-usage-quick-reference.md                # Quick reference card
└── competitive-analysis-enhancement-summary.md   # 🆕 Competitive analysis v1.1.0
```

## Skill Location

```
.claude/skills/salesforce-prompt-builder-research/
├── SKILL.md (v1.1.0)                 # Main skill (triggers automatically)
├── README.md                         # Full skill documentation
├── references/
│   ├── research-sources.md          # Research source guide
│   └── competitive-analysis-framework.md  # 🆕 Competitive research guide
└── examples/
    └── example-research-briefs.md   # Research brief templates (incl. competitive)
```

---

## Quick Start

1. **Read the plan:** Open `salesforce-prompt-builder-skills-plan.md`
2. **Try the skill:** Ask "I want to add [feature] to Prompt Builder"
3. **Get research:** Skill auto-executes and saves findings here
4. **Reference later:** All artifacts saved in this directory

## Next Steps

1. ✅ Review implementation plan
2. ✅ Test research skill with a feature question
3. ✅ Customize skill with internal sources
4. ✅ Use skill throughout product development

---

**Created:** April 21, 2026  
**Purpose:** Planning and research for Salesforce Prompt Builder AI Skills feature  
**Maintained by:** Product team

**Questions?** Ask the research skill!
```
"How does [Salesforce feature] work?"
"I want to add [capability] to Prompt Builder"
"Research [integration pattern] for Salesforce"
```
