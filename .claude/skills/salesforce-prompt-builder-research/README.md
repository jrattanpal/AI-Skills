# Salesforce Prompt Builder Research Skill

## Overview

This skill automates research about Salesforce Prompt Builder, Agentforce, Model Context Protocol (MCP), and related Salesforce AI platform capabilities. It codifies the research methodology used to investigate features, design integrations, and plan product development.

## When to Use

Invoke this skill when you:
- Want to add a new feature to Prompt Builder
- Need to understand how Agentforce works
- Are researching MCP integration patterns
- Want to explore Salesforce AI platform capabilities
- Need to design integrations with other Salesforce products
- Want to understand security models for AI features
- **Need competitive analysis of AI skill platforms**
- **Want to identify Salesforce's competitive advantages**
- **Need to understand how competitors handle a feature**

## Quick Start

Just ask naturally:

```
"I want to add real-time collaboration to Prompt Builder"
"How does Agentforce integrate with Einstein Trust Layer?"
"Research MCP server authentication patterns for Salesforce"
"What's the best way to design a tool palette UI?"
"How do competitors handle visual skill builders? What's our competitive advantage?"
"Research OpenAI GPT Builder vs Salesforce Prompt Builder"
```

The skill will:
1. Clarify your research needs
2. Spawn a research agent with a comprehensive brief
3. **Research competitors and identify Salesforce advantages** (automatically)
4. Synthesize findings into a structured report with competitive analysis
5. Save the research to `.agents/artifacts/` for future reference
6. Answer your question with actionable recommendations and positioning strategy

## Skill Structure

```
salesforce-prompt-builder-research/
├── SKILL.md                    # Main skill definition (with competitive analysis)
├── README.md                   # This file
├── references/
│   ├── research-sources.md     # Guide to documentation sources
│   └── competitive-analysis-framework.md  # 🆕 Competitive research methodology
└── examples/
    └── example-research-briefs.md  # Template research briefs (incl. competitive)
```

## What This Skill Does

### Phase 1: Define Research Scope
- Analyzes your request to determine focus areas
- Asks clarifying questions if needed
- Identifies specific topics to research
- Determines appropriate research depth

### Phase 2: Execute Research
- Spawns a specialized research agent
- Provides a comprehensive research brief
- Searches official Salesforce documentation
- Explores technical specifications and APIs
- Investigates Agentforce, MCP, and related tools
- **Researches competitor platforms** (OpenAI, Microsoft, Google, etc.)
- **Analyzes competitive implementations and user feedback**
- Reviews industry patterns and best practices

### Phase 3: Synthesize Findings
- Reviews research quality and completeness
- Extracts actionable insights
- **Creates competitive comparison matrix**
- **Identifies Salesforce's unique advantages**
- **Develops positioning statements vs competitors**
- Creates structured documentation
- Saves research artifacts for future reference

### Phase 4: Answer Your Question
- Provides direct answer to your original question
- Supports with research findings
- Offers implementation recommendations
- Suggests next steps

## Research Topics Covered

- **Salesforce Prompt Builder**: Current capabilities, architecture, APIs
- **Agentforce**: Atlas Reasoning Engine, Agent Builder, Topics, Actions
- **Model Context Protocol (MCP)**: Server implementation, tool design, authentication
- **Lightning Flow Builder**: UI patterns, action types, security model
- **Einstein Trust Layer**: Security features, prompt injection prevention
- **Salesforce Security**: OLS, FLS, sharing rules, audit logging
- **Integration Patterns**: APIs, external services, MCP servers
- **UI/UX Patterns**: Lightning Design System, canvas design, accessibility
- **🆕 Competitive Landscape**: OpenAI, Microsoft, Google, Anthropic, Amazon AI platforms
- **🆕 Competitive Analysis**: Feature comparison, user feedback, pricing, positioning
- **🆕 Salesforce Advantages**: Native CRM, Enterprise security, AppExchange, Trust Layer
- **🆕 Differentiation Strategy**: Positioning statements, go-to-market implications

## Example Usage

### Example 1: Feature Feasibility

**You ask:**
> "Can we add a skill export feature that generates skill.md files?"

**Skill executes:**
1. Researches skill.md format structure
2. Investigates Salesforce metadata export patterns
3. Explores file generation APIs in Lightning
4. Reviews MCP configuration format

**You get:**
- Feasibility assessment (Yes/No)
- Recommended technical approach
- Implementation complexity estimate
- Full research saved to artifacts

### Example 2: Integration Design

**You ask:**
> "How should Prompt Builder integrate with Slack?"

**Skill executes:**
1. Researches Salesforce-Slack native integration
2. Explores MCP server approach
3. Studies authentication patterns
4. Investigates bidirectional messaging

**You get:**
- Integration architecture recommendation
- Authentication strategy
- Example skill workflow
- Security considerations

### Example 3: Security Analysis

**You ask:**
> "How do we prevent prompt injection in skills?"

**Skill executes:**
1. Researches Einstein Trust Layer capabilities
2. Studies prompt injection attack vectors
3. Reviews industry best practices
4. Explores input validation techniques

**You get:**
- Attack vector catalog
- Multi-layer defense strategy
- Code examples for validation
- Testing methodology

## Research Patterns

The skill recognizes these common patterns:

| Pattern | User Request | Research Focus | Output |
|---------|--------------|----------------|--------|
| **Feature Feasibility** | "Can we add [feature]?" | Technical constraints, APIs, alternatives, **competitors** | Go/No-Go assessment + **competitive positioning** |
| **Integration Design** | "How to integrate with [system]?" | APIs, auth, data flow, **competitor integrations** | Architecture recommendation + **differentiation** |
| **Competitive Analysis** | "How do competitors do [thing]?" | Competitor implementations, user feedback, **Salesforce advantages** | **Detailed comparison matrix + positioning strategy** |
| **Security & Compliance** | "How do we secure [feature]?" | Trust Layer, threat model, **competitor security**, defenses | Security architecture + **competitive security advantages** |
| **UX/UI Patterns** | "How should we design [UI]?" | LDS components, **competitor UX**, Salesforce patterns | UI/UX recommendations + **differentiation opportunities** |

## Research Quality Standards

All research outputs meet these criteria:

- ✅ **Accurate**: Cross-referenced with official sources
- ✅ **Relevant**: Directly applicable to your question
- ✅ **Actionable**: Includes specific recommendations
- ✅ **Complete**: Covers all aspects of the topic
- ✅ **Clear**: Well-organized and understandable
- ✅ **Current**: Focuses on 2024-2026 capabilities

## Research Sources

The skill searches these primary sources:

- **Trailhead**: Learning paths, conceptual overviews
- **Salesforce Developers**: Technical docs, API references
- **Salesforce Help**: Admin guides, setup instructions
- **Release Notes**: Latest features, breaking changes
- **modelcontextprotocol.io**: MCP specification
- **Community**: Stack Exchange, blogs, GitHub

See `references/research-sources.md` for detailed source guide.

## Artifacts Saved

Research is saved to `.agents/artifacts/` with descriptive names:

```
salesforce-[topic]-research-2026-04-21.md
prompt-builder-[feature]-analysis-2026-04-21.md
mcp-integration-patterns-2026-04-21.md
agentforce-capabilities-research-2026-04-21.md
```

These artifacts are permanent and can be referenced in future conversations.

## Tips for Best Results

### Be Specific
❌ "Research Agentforce"
✅ "How does Agentforce's Atlas Reasoning Engine handle multi-step planning?"

### State Your Goal
❌ "Look up MCP servers"
✅ "I need to design MCP server authentication for enterprise security"

### Mention Constraints
❌ "How to add notifications?"
✅ "How to add Slack notifications using only Salesforce native features?"

### Request Specific Depth
❌ "Tell me about Flow Builder"
✅ "I need technical details about Flow Builder's drag-and-drop canvas implementation"

## Customization

To customize this skill for your needs:

1. **Add Sources**: Edit `references/research-sources.md` to include internal wikis or documentation
2. **Add Templates**: Create new research brief templates in `examples/`
3. **Adjust Depth**: Modify default word limits in `SKILL.md`
4. **Add Patterns**: Document new research patterns you discover

## Version History

- **v1.0.0** (2026-04-21): Initial skill creation

## Future Enhancements

Potential improvements for this skill:

- [ ] Cache research results to avoid duplicate work
- [ ] Integration with Salesforce's internal documentation systems
- [ ] Automatic following of documentation links and references
- [ ] Multi-agent parallel research for complex topics
- [ ] Comparison matrix generation for feature options
- [ ] Risk assessment templates for new features

## Feedback

As you use this skill, note:
- Which research briefs worked best
- What sources were most valuable
- What topics need deeper coverage
- How to improve research quality

Update the skill based on your learnings!

---

**Created**: 2026-04-21  
**Use case**: Product research for Salesforce Prompt Builder features  
**Maintained by**: [Your team]
