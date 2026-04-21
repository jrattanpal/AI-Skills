# Quick Reference: Salesforce Prompt Builder Research Skill

## Skill Location
`.claude/skills/salesforce-prompt-builder-research/`

## How to Trigger

The skill activates when you ask questions like:

- "I want to add a new feature in Prompt Builder"
- "Research Prompt Builder capabilities"
- "How does Agentforce work?"
- "Explore MCP integration for Salesforce"
- "How should we design [feature] for Prompt Builder?"

## What It Does

**Automatically researches:**
- Salesforce Prompt Builder architecture and APIs
- Agentforce (Atlas Reasoning Engine, Agent Builder, Topics, Actions)
- Model Context Protocol (MCP) servers and tools
- Lightning Flow Builder patterns
- Einstein Trust Layer security
- Salesforce security model (OLS, FLS, sharing rules)
- Integration patterns and best practices

**Outputs:**
1. Direct answer to your question
2. Structured research report
3. Implementation recommendations
4. Saved artifact in `.agents/artifacts/`

## Common Use Cases

### 1. Feature Feasibility
**Ask:** "Can we add [feature] to Prompt Builder?"
**Get:** Go/No-Go assessment with technical approach

### 2. Integration Design
**Ask:** "How should Prompt Builder integrate with [system]?"
**Get:** Integration architecture with auth strategy

### 3. Security Analysis
**Ask:** "How do we secure [feature]?"
**Get:** Threat model and defense strategy

### 4. UI/UX Patterns
**Ask:** "How should we design the UI for [feature]?"
**Get:** UI recommendations aligned with Salesforce patterns

### 5. Competitive Analysis
**Ask:** "How do competitors handle [capability]?"
**Get:** Comparison matrix and recommendations

## Example Session

```
You: "I want to add real-time collaboration to Prompt Builder"

Skill executes:
1. Clarifies scope (if needed)
2. Spawns research agent with brief about:
   - Platform Events
   - Streaming API
   - Concurrent editing patterns
   - Security considerations
3. Synthesizes findings
4. Saves to: .agents/artifacts/prompt-builder-realtime-collab-2026-04-21.md

You get:
✓ Feasibility assessment
✓ Technical approach (Platform Events + LMS)
✓ Limitations (latency, concurrent users)
✓ Implementation complexity (Medium)
✓ Alternative approaches
```

## Research Coverage

- ✅ Salesforce official documentation
- ✅ Trailhead learning paths
- ✅ API references (REST, Metadata, Tooling)
- ✅ MCP specification and SDKs
- ✅ Security best practices
- ✅ UI/UX patterns (Lightning Design System)
- ✅ Integration patterns
- ✅ Community resources

## Skill Files

```
.claude/skills/salesforce-prompt-builder-research/
├── SKILL.md                           # Main skill logic
├── README.md                          # Full documentation
├── references/
│   └── research-sources.md           # Documentation sources guide
└── examples/
    └── example-research-briefs.md    # Template research briefs
```

## Tips for Best Results

✅ **Be specific**: "How does Atlas Reasoning Engine handle multi-step planning?"
✅ **State constraints**: "Using only Salesforce native features"
✅ **Mention goals**: "For enterprise security compliance"

❌ **Too vague**: "Research Agentforce"
❌ **No context**: "Tell me about MCP"

## Research Artifacts Location

All research saved to: `.agents/artifacts/`

Filename patterns:
- `salesforce-[topic]-research-YYYY-MM-DD.md`
- `prompt-builder-[feature]-analysis-YYYY-MM-DD.md`
- `agentforce-[capability]-research-YYYY-MM-DD.md`
- `mcp-integration-patterns-YYYY-MM-DD.md`

## Customization

To add your own research sources:
1. Edit `.claude/skills/salesforce-prompt-builder-research/references/research-sources.md`
2. Add internal documentation URLs
3. Include team-specific best practices

To add research templates:
1. Edit `.claude/skills/salesforce-prompt-builder-research/examples/example-research-briefs.md`
2. Add new example briefs for common scenarios

## Related Artifacts

- **Full planning document**: `.agents/artifacts/salesforce-prompt-builder-skills-plan.md`
  - Comprehensive plan for Prompt Builder skills feature
  - Architecture, security, implementation phases
  - This was the OUTPUT of using this research methodology

## Quick Test

To test the skill works:

```
You: "I want to add PDF export to Prompt Builder skills"
```

Expected behavior:
1. Skill activates (check for research agent spawn)
2. Researches PDF generation in Salesforce
3. Returns feasibility assessment
4. Saves artifact to `.agents/artifacts/`

---

**Created**: 2026-04-21  
**Purpose**: Quick reference for using the research skill
**Related**: Full plan in `salesforce-prompt-builder-skills-plan.md`
