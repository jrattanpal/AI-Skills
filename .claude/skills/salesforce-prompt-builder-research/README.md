# Salesforce Prompt Builder Research Skill v2.0

## Overview

This skill automates research about Salesforce Prompt Builder, Agentforce, Model Context Protocol (MCP), and related Salesforce AI platform capabilities. It uses **research caching** to avoid redundant work, **parallel research streams** for speed and depth, and **auto-publishes findings to Slack canvases** for team access.

## What's New in v2.0

| Feature | v1.1 | v2.0 |
|---------|------|------|
| Research caching | No (re-researches everything) | Yes (checks index, skips fresh topics) |
| Agent architecture | Single monolithic agent | Parallel focused streams |
| Internal tools | Web search only | Codesearch, enterprise search, GUS, browser |
| Output sharing | Local file only | Slack canvas auto-publish + local file |
| Confidence scoring | No | Yes (HIGH/MEDIUM/LOW per finding) |
| Token efficiency | High (large briefs) | Low (cached + focused briefs) |

## When to Use

Invoke this skill when you:
- Want to add a new feature to Prompt Builder
- Need to understand how Agentforce works
- Are researching MCP integration patterns
- Want to explore Salesforce AI platform capabilities
- Need to design integrations with other Salesforce products
- Want to understand security models for AI features
- Need competitive analysis of AI skill platforms
- Want to identify Salesforce's competitive advantages
- Need to understand how competitors handle a feature

## Quick Start

Just ask naturally:

```
"I want to add real-time collaboration to Prompt Builder"
"How does Agentforce integrate with Einstein Trust Layer?"
"Research MCP server authentication patterns for Salesforce"
"What's the best way to design a tool palette UI?"
"How do competitors handle visual skill builders?"
"Research OpenAI GPT Builder vs Salesforce Prompt Builder"
```

The skill will:
1. **Check the research cache** for existing findings on this topic
2. **Skip re-researching** anything that's already fresh in the cache
3. **Spawn parallel research agents** only for topics that need new/refreshed data
4. **Use internal tools** (codesearch, enterprise search, browser) when available for richer findings
5. **Synthesize** with confidence scores and comparison matrices
6. **Save locally** and present findings directly in conversation
7. **Optionally publish** to Slack canvas if tools are available and you request it
8. **Update the research index** so future requests are faster

## Skill Structure

```
salesforce-prompt-builder-research/
├── SKILL.md                    # Main skill definition (v2.0 methodology)
├── README.md                   # This file
├── references/
│   ├── research-sources.md     # Guide to documentation sources + MCP tools
│   └── competitive-analysis-framework.md  # Competitive research methodology
└── examples/
    └── example-research-briefs.md  # Template research briefs per stream

Supporting files:
.agents/artifacts/
├── research-index.md           # Research cache index (freshness tracking)
└── [research artifacts...]     # Saved research outputs
```

## How the Cache Works

The skill maintains a **research index** at `.agents/artifacts/research-index.md` that tracks:
- What topics have been researched
- When the research was done
- How long it stays fresh (30-180 days depending on category)
- Keywords for matching future requests

**Before any research, the skill checks this index.** If a matching fresh artifact exists, it reads it directly instead of spawning an expensive research agent. This saves 60-70% of token usage for repeat topics.

### Freshness Rules

| Category | Stale After | Example |
|----------|-------------|---------|
| Competitive | 30 days | "How does Glean compare?" |
| Salesforce docs | 90 days | "How does Prompt Builder work?" |
| Architecture | 180 days | "What's the skills platform plan?" |
| Internal/roadmap | 60 days | "What's on the team's sprint?" |
| Security | 90 days | "How does Einstein Trust Layer work?" |

## Parallel Research Streams

Instead of one large agent, v2.0 spawns focused parallel agents:

### Stream 1: Salesforce Internal Context
- **Tools:** Codesearch (real code), enterprise search (design docs), GUS (roadmap)
- **Output:** Current state, architecture, API patterns, internal context
- **Brief size:** ~400 words (focused)

### Stream 2: Competitive & Market
- **Tools:** Browser (live screenshots), web search (articles/reviews), Slack search (intel)
- **Output:** Competitor features, comparison matrix, user sentiment
- **Brief size:** ~400 words (focused)

### Synthesis (after streams complete)
- Merges stream outputs with cached artifacts
- Creates comparison matrix and positioning statements
- Produces standardized research document

**Not every request needs both streams.** Simple internal questions skip competitive research. Pure competitive analysis skips internal codesearch.

## Output & Sharing

### Always: Local Artifact + Direct Presentation
Every research output is:
1. Saved to `.agents/artifacts/` with a descriptive filename (serves as cache for future requests)
2. Presented directly in the conversation with executive summary, findings, and recommendations

This works for everyone regardless of what tools are available.

### Optional: Slack Canvas (if tools available)
If Slack MCP tools are configured in your environment, you can ask to publish findings to a Slack canvas:
- "Research [topic] and publish to Slack"
- The canvas includes executive summary, comparison matrix, positioning, and recommendations

### Optional: Google Doc
Ask "publish to Google Docs" to get a shareable Doc (requires Google MCP tools).

## Research Topics Covered

- **Salesforce Prompt Builder**: Current capabilities, architecture, APIs
- **Agentforce**: Atlas Reasoning Engine, Agent Builder, Topics, Actions
- **Model Context Protocol (MCP)**: Server implementation, tool design, authentication
- **Lightning Flow Builder**: UI patterns, action types, security model
- **Einstein Trust Layer**: Security features, prompt injection prevention
- **Salesforce Security**: OLS, FLS, sharing rules, audit logging
- **Integration Patterns**: APIs, external services, MCP servers
- **UI/UX Patterns**: Lightning Design System, canvas design, accessibility
- **Competitive Landscape**: OpenAI, Microsoft, Google, Anthropic, Amazon
- **Market Positioning**: Feature comparison, differentiation, go-to-market

## Research Patterns

| Pattern | Request | Streams Used | Output |
|---------|---------|--------------|--------|
| Feature Feasibility | "Can we add [X]?" | Internal + Competitive | Go/No-Go + positioning |
| Integration Design | "How to integrate with [Y]?" | Internal + Maybe Competitive | Architecture + differentiation |
| Competitive Analysis | "How do competitors do [Z]?" | Competitive only | Comparison matrix + strategy |
| Security Analysis | "How to secure [feature]?" | Internal + Maybe Competitive | Security architecture |
| UX/UI Patterns | "How to design [UI]?" | Internal + Competitive | Recommendations + screenshots |

## MCP Tools Used

The skill leverages these internal tools (no manual setup needed):

- **Codesearch** — Find real Salesforce implementation patterns in source code
- **Enterprise Search** — Confluence, Quip, internal docs for design decisions
- **GUS** — Epic and work item context for roadmap awareness
- **Browser** — Live screenshots of competitor product pages
- **Slack** — Read/create/update canvases, search for competitive intel
- **Google Docs** — Optional output format for shareable documents

## Tips for Best Results

### Be Specific
- Bad: "Research Agentforce"
- Good: "How does Agentforce's Atlas Reasoning Engine handle multi-step planning?"

### State Your Goal
- Bad: "Look up MCP servers"
- Good: "I need to design MCP server authentication for enterprise security"

### Mention Constraints
- Bad: "How to add notifications?"
- Good: "How to add Slack notifications using only Salesforce native features?"

### Control Sharing
- Default: saves locally + presents in conversation (works everywhere)
- Slack: "Research [topic] and publish to Slack canvas" (requires Slack tools)
- Google Doc: "Research [topic] and publish to Google Docs" (requires Google tools)

## Version History

- **v2.0.0** (2026-04-24): Research caching, multi-agent parallel streams, MCP tool integration, Slack canvas auto-publish, confidence scoring
- **v1.1.0** (2026-04-21): Added competitive analysis framework
- **v1.0.0** (2026-04-21): Initial skill creation

---

**Created**: 2026-04-21 | **Last Updated**: 2026-04-24
**Use case**: Product research for Salesforce Prompt Builder features
