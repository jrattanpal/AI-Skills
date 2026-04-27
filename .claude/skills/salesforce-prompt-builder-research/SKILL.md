---
name: Salesforce Prompt Builder Research
description: This skill should be used when the user asks to "add a new feature in Prompt Builder", "research Prompt Builder capabilities", "understand Agentforce integration", "explore MCP for Salesforce", "competitive analysis for Prompt Builder", or needs to investigate Salesforce AI platform features for product development with competitive positioning.
version: 2.0.0
---

# Salesforce Prompt Builder Research v2.0

## Purpose

Research and analyze Salesforce Prompt Builder, Agentforce, Model Context Protocol (MCP), and related Salesforce AI platform capabilities to inform feature planning and product development decisions. This skill uses research caching to minimize token usage and parallel research streams for depth and speed.

## When to Use This Skill

Trigger this skill when the user:
- Wants to add a new feature to Prompt Builder
- Needs to understand how existing Salesforce AI features work
- Is planning integration between Prompt Builder and other Salesforce products
- Needs competitive analysis of AI skill platforms and prompt builders
- Wants to identify Salesforce's competitive advantages for a feature
- Wants to understand MCP server implementation patterns
- Is designing features that involve Agentforce agents
- Needs to understand how competitors handle similar capabilities

---

## Research Methodology (5 Phases)

### Phase 1: Define Research Scope

Analyze the user's request to determine:
1. **Primary focus area**: Prompt Builder, Agentforce, MCP, Lightning Flow, Einstein, or combination
2. **Research depth**: Surface-level overview, technical architecture, or implementation details
3. **Specific topics**: Security, UI/UX patterns, integration points, data model, APIs, etc.
4. **Competitive scope**: Which competitors to analyze, what features to compare
5. **Output format**: Summary report, technical plan, comparison matrix, or architecture diagram
6. **Sharing preference**: Local artifact (default), Slack canvas (if available), or Google Doc

Ask clarifying questions if the scope is unclear:
- "Are you looking for current capabilities or planning new features?"
- "Do you need implementation details or high-level concepts?"
- "Should I focus on admin/user experience or developer APIs?"
- "Should I include competitive analysis and identify Salesforce's advantages?"
- "Would you like me to publish findings to a Slack canvas?" (only ask if Slack tools are available)

---

### Phase 2: Cache Check & Research Planning

**Goal: Avoid re-researching topics that already have fresh artifacts. This saves significant tokens.**

#### Step 1: Read the Research Index

Read `.agents/artifacts/research-index.md` to check for existing research.

#### Step 2: Match User's Request Against Index

For each topic the user is asking about:
- Search index entries by **keywords** and **category**
- Check the **date** against the **freshness rules**:

| Category | Stale After | Rationale |
|----------|-------------|-----------|
| competitive | 30 days | Competitor products change frequently |
| competitive-comparison | 30 days | Same as above |
| salesforce-docs | 90 days | Salesforce releases are quarterly |
| salesforce-internal | 60 days | Roadmap/team context shifts mid-quarter |
| architecture | 180 days | Patterns and plans are more stable |
| security | 90 days | Security models change with releases |
| industry-trends | 60 days | AI market moves fast |
| feature-analysis | 90 days | Feature research stays valid through a quarter |

#### Step 3: Classify Each Topic

- **Fresh cache hit**: Artifact exists and is within freshness window. Read the existing artifact and use its content. Do NOT spawn a research agent for this topic.
- **Stale cache hit**: Artifact exists but is past freshness window. Note what needs refreshing -- the research agent should focus on what has CHANGED since the artifact date, using the old artifact as baseline context.
- **Cache miss**: No matching artifact. Mark as "new research needed."

#### Step 4: Plan Research Streams

Based on the classification, determine which research streams to spawn:

| Request Type | Stream 1 (Internal) | Stream 2 (Competitive) | Synthesis |
|---|---|---|---|
| Feature feasibility | Yes | Yes | Yes |
| Competitive analysis | No | Yes | Yes |
| Integration design | Yes | Maybe | Yes |
| Security analysis | Yes | Maybe | Yes |
| Internal context only | Yes | No | Direct answer |

#### Step 5: Inform the User

Tell the user what was found:
> "I found existing fresh research on [X] (from [date]). I need new/refreshed research on [Y] and [Z]. Spawning focused research agents for those topics."

---

### Phase 3: Execute Research (Parallel Streams)

Spawn focused research agents in parallel. Each agent gets a narrow, specific brief (~400 words) rather than the full research scope. This reduces token usage per agent significantly.

#### Stream 1: Salesforce Internal Context

**When to spawn:** Feature feasibility, integration design, security analysis, internal context requests.

**Agent configuration:**
```
Agent({
  description: "Research Salesforce internal context for [topic]",
  subagent_type: "general-purpose",
  prompt: [Focused ~400-word brief for internal research]
})
```

**Brief template for Stream 1:**
```
Research Salesforce internal context for: [TOPIC]

Context: [Why this research is needed - 1-2 sentences]

Research using these tools IN THIS ORDER:
1. Use codesearch to find real implementation patterns (search for relevant class names, APIs, or features)
2. Use enterprise search (search tool) to find internal design docs, Confluence pages, or Quip docs
3. Use GUS skill to find related epics or work items on the roadmap
4. Fall back to web search for official Salesforce documentation

Specific questions to answer:
- [Question 1]
- [Question 2]
- [Question 3]

Tag each finding with confidence:
- HIGH: Verified from code or official docs
- MEDIUM: From credible secondary source
- LOW: Inferred or from dated source

Output: Structured findings under 800 words. Include code references where found.
```

**Tools this agent should use:**
- `mcp__plugin_codesearch_codesearch__search` — Find real Prompt Builder implementation code
- `mcp__plugin_codesearch_codesearch__blob` — Read specific source files
- `mcp__plugin_codesearch_codesearch__tree` — Browse repository structure
- `mcp__plugin_codesearch_codesearch__history` — See recent changes
- `mcp__plugin_search_search__search` — Search Confluence, Quip, internal docs
- GUS skill — Query work items, epics, sprint context

#### Stream 2: Competitive & Market Research

**When to spawn:** Feature feasibility, competitive analysis, any request where positioning matters.

**Agent configuration:**
```
Agent({
  description: "Research competitive landscape for [topic]",
  subagent_type: "general-purpose",
  prompt: [Focused ~400-word brief for competitive research]
})
```

**Brief template for Stream 2:**
```
Research how competitors handle: [TOPIC]

Context: [Why - 1-2 sentences]

Research these competitors (focus on top 3-4 most relevant):
- OpenAI GPT Builder / Custom GPTs
- Microsoft Copilot Studio
- Google Vertex AI Agent Builder
- Anthropic Claude (skills, MCP)
- Amazon Bedrock Agents
- [Adjacent: Zapier, LangChain, ServiceNow as relevant]

For each relevant competitor:
1. Does it offer this feature? How is it implemented?
2. What does it do well? What are its weaknesses?
3. User sentiment (check reviews if accessible)

Research approach:
1. Use browser to navigate to competitor product pages and take screenshots of relevant UI
2. Use web search for recent articles, documentation, user reviews
3. Use Slack search for any internal competitive intel discussions

Also identify:
- Table stakes features (must match)
- Differentiation opportunities (can excel at)
- Threats to mitigate

Tag findings with confidence (HIGH/MEDIUM/LOW).

Output: Structured comparison under 800 words. Include comparison matrix table.
```

**Tools this agent should use:**
- `mcp__plugin_browser_browser__browser_navigate` — Visit competitor product pages
- `mcp__plugin_browser_browser__browser_screenshot` — Capture competitor UIs
- `mcp__plugin_browser_browser__browser_a11y_tree` — Analyze competitor UI structure
- `mcp__plugin_search_search__search` — Web search for articles, reviews, docs
- `mcp__plugin_slack_slack__slack_search_public` — Find internal competitive discussions

#### Stream 3: Synthesis (runs AFTER Streams 1 and 2 complete)

**Always runs** (unless the request is trivially answered by a single cache hit).

This step does NOT spawn a separate agent. Instead, the main conversation synthesizes:

1. **Merge inputs:** Combine stream outputs with any cached artifacts from Phase 2
2. **Create comparison matrix:** Feature availability across competitors with ratings
3. **Identify advantages:** What Salesforce uniquely offers
4. **Develop positioning:** "Unlike [competitor], Salesforce Prompt Builder..."
5. **Produce recommendations:** Must Have / Should Have / Could Have
6. **Format final output:** Use the standardized template (see Phase 4)

---

### Phase 4: Produce Output & Share

#### Step 1: Format the Research Document

Use this standardized template:

```markdown
# Research: [Topic]
**Date:** [YYYY-MM-DD] | **Category:** [category] | **Confidence:** [high/medium/low]

## Executive Summary
[3-5 sentences: Direct answer + key finding + recommendation]

## Key Findings

### Current State in Salesforce
[What exists today — from Stream 1 or cache]

### Technical Architecture
[How it works — data model, APIs, integration points]

### Integration Points
[How this connects to other Salesforce features]

## Competitive Analysis

### Comparison Matrix

| Aspect | Salesforce | OpenAI | Microsoft | Google | Others |
|--------|-----------|---------|-----------|---------|---------|
| [Feature] | Rating | Rating | Rating | Rating | Rating |
| Ease of Use | Rating | Rating | Rating | Rating | Rating |
| Enterprise Security | Rating | Rating | Rating | Rating | Rating |
| Integration | Rating | Rating | Rating | Rating | Rating |

Rating scale: Strong / Adequate / Weak / Not Available

### How Competitors Implement This
[Key competitor approaches — from Stream 2 or cache]

### Salesforce Competitive Advantages
1. **[Advantage 1]**: [Why it matters]
2. **[Advantage 2]**: [Why it matters]
3. **[Advantage 3]**: [Why it matters]

## Positioning

### Positioning Statement
"Unlike [competitor], Salesforce Prompt Builder [unique value] because [advantage], enabling [customer] to [benefit]."

### Differentiation Strategy
- How to implement this BETTER than competitors
- What makes this "Salesforce-native" vs bolted-on

## Recommendations

### Must Have (Table Stakes)
- [Features we must match to be competitive]

### Should Have (Differentiators)
- [Features that set us apart]

### Could Have (Future)
- [Features for later consideration]

### Estimated Effort
[Low / Medium / High with brief rationale]

## Evidence & Sources
- **Internal code:** [codesearch references, if any]
- **Documentation:** [URLs consulted]
- **Competitor screenshots:** [descriptions of what was captured]
- **Confidence notes:** [areas where confidence is lower and why]

## Follow-Up Research Needed
[Gaps identified, areas requiring deeper investigation]
```

#### Step 2: Save Artifact Locally

Save to `.agents/artifacts/` with a descriptive filename:
- `salesforce-[topic]-research-[YYYY-MM-DD].md` for general research
- `prompt-builder-[feature]-analysis-[YYYY-MM-DD].md` for feature analysis
- `[competitor]-comparison-[YYYY-MM-DD].md` for competitive comparisons

#### Step 3: Update Research Index

Add a new entry to `.agents/artifacts/research-index.md` following the format:

```markdown
### [topic-key]: [Title]
- **Date:** [YYYY-MM-DD]
- **Artifact:** [filename]
- **Category:** [category from freshness rules]
- **Freshness:** [N days] (expires [date])
- **Topics covered:** [comma-separated list]
- **Keywords:** [comma-separated, for future matching]
- **Confidence:** [high/medium/low]
- **Slack Canvas ID:** [if published]
- **Summary:** [One sentence]
```

#### Step 4: Publish to Slack Canvas (Optional — only if user requests AND Slack tools are available)

This step is OPTIONAL. Only execute if:
- The user explicitly asks to publish to Slack, AND
- Slack MCP tools are available in the current environment

If both conditions are met:
1. **Check for existing canvas:** If the research-index entry for this topic has a Slack Canvas ID, use `slack_read_canvas` to get current content, then `slack_update_canvas` to replace relevant sections.
2. **Create new canvas:** If no existing canvas, use `slack_create_canvas` with the research formatted in Markdown.
3. **Announce:** Send a message to the team channel with a brief summary and link to the canvas.

**Canvas formatting guidelines:**
- Use headers (##, ###) for structure
- Use tables for comparison matrices
- Keep under 5,000 words for readability
- Include "Last updated: [date]" at the top

**If Slack is NOT available:** The local artifact in `.agents/artifacts/` IS the primary deliverable. Present the full research directly to the user in the conversation.

#### Step 5: Present to User

1. **Direct answer** to the original question (2-3 sentences)
2. **Key insight** that might not be obvious
3. **Top recommendation** with rationale
4. **Links:** artifact path + Slack canvas link (if published)
5. **Offer next steps:** "Want me to dive deeper on [specific area]?"

---

### Phase 5: Index Maintenance & Continuous Improvement

After each research session:

1. **Check index health:** If research-index.md exceeds 50 entries, archive the oldest stale entries to `research-index-archive.md`
2. **Note tool effectiveness:** Which MCP tools returned useful results vs. empty results
3. **Flag source gaps:** If a research source consistently returns nothing, note it for removal
4. **Update competitor profiles:** If a competitor has launched something new, flag the competitive-analysis-framework.md for update

---

## Tools Available (MCP Integration)

### Salesforce Code Intelligence

| Tool | Purpose | Example Query |
|------|---------|---------------|
| `mcp__plugin_codesearch_codesearch__search` | Find real implementation code | `content:"PromptTemplate" lang:java` |
| `mcp__plugin_codesearch_codesearch__blob` | Read a specific source file | Follow up on search results |
| `mcp__plugin_codesearch_codesearch__tree` | Browse repository structure | Find related files in a package |
| `mcp__plugin_codesearch_codesearch__history` | See recent changes to a file | What changed recently in Prompt Builder code |
| `mcp__plugin_codesearch_codesearch__blame` | See who wrote specific code | Understand ownership |

**Usage guidance:** When researching how a Salesforce feature works internally, use codesearch to find real implementation patterns. This is far more accurate than documentation alone. Start with broad search, then read specific blobs for detail.

### Enterprise Knowledge

| Tool | Purpose | Example Query |
|------|---------|---------------|
| `mcp__plugin_search_search__search` | Search Confluence, Quip, Slack, internal docs | "Prompt Builder architecture design doc" |
| GUS skill (`sfcli:gus`) | Query work items, epics, sprints | Related roadmap items, what's in flight |

**Usage guidance:** Always search enterprise knowledge sources before external web search. Internal design docs contain architectural decisions and rationale not found in public documentation.

### Competitive Intelligence

| Tool | Purpose | When to Use |
|------|---------|------------|
| `mcp__plugin_browser_browser__browser_navigate` | Visit competitor product pages live | Current feature state, pricing pages |
| `mcp__plugin_browser_browser__browser_screenshot` | Capture competitor UI evidence | Visual comparison for reports |
| `mcp__plugin_browser_browser__browser_a11y_tree` | Analyze competitor UI structure | Understanding interaction patterns |
| `mcp__plugin_search_search__search` | Search web for reviews, articles | User sentiment, announcements |
| `mcp__plugin_slack_slack__slack_search_public` | Find internal competitive intel | What has the team said about competitors |

**Usage guidance:** Navigate to competitor product pages and take screenshots for current visual evidence. This is more reliable than blog posts which may be outdated. Key URLs: platform.openai.com, copilotstudio.microsoft.com, cloud.google.com/vertex-ai.

### Output & Sharing

| Tool | Purpose | When to Use |
|------|---------|------------|
| `mcp__plugin_slack_slack__slack_create_canvas` | Create Slack canvas with research | Primary output for team sharing |
| `mcp__plugin_slack_slack__slack_update_canvas` | Update existing research canvas | Refresh findings, add sections |
| `mcp__plugin_slack_slack__slack_read_canvas` | Read existing canvas content | Check what was previously shared |
| `mcp__plugin_slack_slack__slack_send_message` | Announce research in channel | Notify team of new findings |
| `mcp__plugin_slack_slack__slack_search_channels` | Find team channels | Identify where to publish |
| `mcp__plugin_google_google__docs_create` | Create Google Doc with research | When user requests Doc format |
| `mcp__plugin_google_google__docs_search` | Find existing research Docs | Check for prior research in Docs |

**Usage guidance:** These tools are OPTIONAL. Not all users will have Slack configured. The local artifact is always the primary record. Only offer Slack publishing if these tools are available in the environment AND the user requests it.

---

## Common Research Patterns

### Pattern 1: Feature Feasibility Assessment

**User asks**: "Can we add [feature] to Prompt Builder?"

**Research focus:**
- Existing similar features in Salesforce (codesearch + enterprise search)
- Technical constraints (governor limits, security)
- How competitors implement it (browser + web search)
- Data model implications
- User permissions and access control

**Output**: Go/No-Go assessment with implementation complexity and competitive positioning

---

### Pattern 2: Integration Design

**User asks**: "How should Prompt Builder integrate with [Salesforce product]?"

**Research focus:**
- Target product's APIs (codesearch for real code patterns)
- Common integration patterns (enterprise search for design docs)
- Authentication and authorization models
- How competitors handle similar integrations (browser)

**Output**: Integration architecture with recommended approach and differentiation

---

### Pattern 3: Competitive Analysis

**User asks**: "How do competitors handle [capability]?"

**Research focus:**
- Competitor product pages and documentation (browser)
- User reviews and sentiment (web search)
- Internal competitive discussions (Slack search)
- Feature comparison matrix

**Output**: Detailed comparison matrix + positioning strategy + recommendations

---

### Pattern 4: Security & Compliance

**User asks**: "How do we secure [feature] in Prompt Builder?"

**Research focus:**
- Einstein Trust Layer capabilities (codesearch + docs)
- Salesforce security model (OLS, FLS, sharing rules)
- How competitors handle security (browser + search)
- Industry standards and compliance requirements

**Output**: Security architecture with competitive security advantages

---

### Pattern 5: UX/UI Patterns

**User asks**: "How should we design the UI for [feature]?"

**Research focus:**
- Lightning Design System components (docs)
- Existing Salesforce UI patterns (codesearch for LWC examples)
- Competitor UI approaches (browser screenshots)
- Accessibility requirements

**Output**: UI/UX recommendations with Salesforce pattern alignment and screenshots

---

## Confidence Scoring

All research findings must be tagged with confidence levels:

| Level | Meaning | Source Example |
|-------|---------|---------------|
| **HIGH** | Verified from official docs or source code | Codesearch result, official API docs, Salesforce Help |
| **MEDIUM** | From credible secondary source | Blog post, community answer, single documentation reference |
| **LOW** | Inferred, from dated source, or unverifiable | Old blog post, forum speculation, inference from patterns |

The synthesis step uses confidence to:
- Flag low-confidence findings for follow-up
- Prioritize high-confidence findings in recommendations
- Warn the user when recommendations rest on uncertain data

---

## Quality Standards

Research outputs must meet:

1. **Accurate**: Cross-referenced with official sources; confidence-tagged
2. **Relevant**: Directly applicable to user's question
3. **Actionable**: Includes specific recommendations with priority
4. **Complete**: Covers internal context + competitive landscape
5. **Efficient**: Uses cache hits; only researches what's needed
6. **Shareable**: Saved locally; optionally published to Slack canvas if available

---

## Common Pitfalls to Avoid

1. **Re-researching known topics**: Always check the research index first
2. **Oversized agent briefs**: Keep each stream's brief under 400 words
3. **Stale information**: Agentforce launched in 2024; prioritize recent sources
4. **Missing the question**: Always circle back to what user actually asked
5. **No clear recommendation**: User wants guidance, not just data dump
6. **Forgetting to update index**: After every research, update research-index.md
7. **Assuming Slack is available**: Only offer Slack publishing if tools are accessible and user requests it

---

## Version History

- **v2.0.0** (2026-04-24): Major upgrade — research caching, multi-agent parallel streams, MCP tool integration, Slack canvas auto-publish, confidence scoring
- **v1.1.0** (2026-04-21): Added competitive analysis framework
- **v1.0.0** (2026-04-21): Initial skill creation
