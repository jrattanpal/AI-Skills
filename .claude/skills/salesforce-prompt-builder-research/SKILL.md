---
name: Salesforce Prompt Builder Research
description: This skill should be used when the user asks to "add a new feature in Prompt Builder", "research Prompt Builder capabilities", "understand Agentforce integration", "explore MCP for Salesforce", "competitive analysis for Prompt Builder", or needs to investigate Salesforce AI platform features for product development with competitive positioning.
version: 1.1.0
---

# Salesforce Prompt Builder Research

## Purpose

Research and analyze Salesforce Prompt Builder, Agentforce, Model Context Protocol (MCP), and related Salesforce AI platform capabilities to inform feature planning and product development decisions.

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

## Research Methodology

### Phase 1: Define Research Scope

Analyze the user's request to determine:
1. **Primary focus area**: Prompt Builder, Agentforce, MCP, Lightning Flow, Einstein, or combination
2. **Research depth**: Surface-level overview, technical architecture, or implementation details
3. **Specific topics**: Security, UI/UX patterns, integration points, data model, APIs, etc.
4. **Competitive scope**: Which competitors to analyze, what features to compare
5. **Output format**: Summary report, technical plan, comparison matrix, or architecture diagram

Ask clarifying questions if the scope is unclear:
- "Are you looking for current capabilities or planning new features?"
- "Do you need implementation details or high-level concepts?"
- "Should I focus on admin/user experience or developer APIs?"
- "What's the primary goal: feasibility check, technical design, or competitive analysis?"
- "Should I include competitive analysis and identify Salesforce's advantages?"

### Phase 2: Execute Research

Use the **Agent** tool to spawn a research agent with a comprehensive brief. The agent should:

**Research Sources to Explore:**

1. **Official Salesforce Documentation**
   - Trailhead learning paths
   - Developer documentation (developer.salesforce.com)
   - Setup and admin guides
   - Release notes and product announcements

2. **Technical Specifications**
   - API references (REST, SOAP, Metadata, Tooling APIs)
   - Schema definitions for relevant objects
   - Integration patterns and best practices
   - Governor limits and performance considerations

3. **Agentforce & AI Platform**
   - Atlas Reasoning Engine capabilities
   - Agent Builder features and modes (document, low-code canvas, pro-code)
   - Agent Topics, Actions, and Scripts
   - Einstein Trust Layer security model
   - Data grounding and zero-retention policies

4. **Model Context Protocol (MCP)**
   - MCP specification (modelcontextprotocol.io)
   - Available MCP server implementations
   - Salesforce-specific MCP patterns
   - Authentication and security models
   - Tool definition standards and best practices

5. **Related Salesforce Products**
   - Lightning Flow Builder (UI patterns, action types, security)
   - Einstein AI features (prediction, content generation, trust layer)
   - AppExchange ecosystem
   - Integration capabilities (MuleSoft, External Services, Named Credentials)

6. **Competitive Analysis** (Always include for feature requests)
   - Direct competitors (OpenAI GPT Builder, Microsoft Copilot Studio, Google Agent Builder, etc.)
   - Similar capabilities in competitor products
   - How competitors implement the requested feature
   - Gaps in competitor offerings
   - User feedback on competitor solutions
   
7. **Industry Context**
   - AI agent and skill platform trends
   - Enterprise security standards for AI
   - Portability and interoperability standards
   - Market positioning and differentiation opportunities

**Research Agent Instructions:**

```
Research the following topics related to Salesforce Prompt Builder and AI platform:

[Insert specific topics based on user request]

Your research should cover:

1. **Current State Analysis**
   - What exists today in Salesforce
   - How features currently work (architecture, UX, APIs)
   - Limitations and constraints
   - User feedback and pain points (if available)

2. **Technical Deep Dive**
   - Data models and object schemas
   - Integration patterns and APIs
   - Security and permission models
   - Performance characteristics and limits

3. **Best Practices & Patterns**
   - Recommended implementation approaches
   - UI/UX conventions used in Salesforce
   - Common integration patterns
   - Security best practices

4. **Ecosystem Context**
   - Related Salesforce features and how they integrate
   - Third-party tools and extensions
   - Open standards (like MCP) applicability
   - Community resources and examples

5. **Competitive Analysis** (REQUIRED for all feature requests)
   
   Research these competitor platforms:
   
   **Primary Competitors:**
   - OpenAI GPT Builder / Custom GPTs
   - Microsoft Copilot Studio
   - Google Vertex AI Agent Builder
   - Anthropic Claude (skill system, MCP)
   - Amazon Bedrock Agents
   
   **Adjacent Competitors:**
   - Low-code automation: Zapier, Make (Integromat), n8n
   - Workflow builders: Monday.com, Notion AI, ClickUp AI
   - AI agent platforms: LangChain, AutoGPT, AgentGPT
   - Enterprise AI: IBM watsonx, ServiceNow AI
   
   **For each relevant competitor, answer:**
   
   a) **Feature Implementation**
      - Does this competitor offer the requested feature?
      - How is it implemented (architecture, UI/UX)?
      - What does it do well?
      - What are its limitations or weaknesses?
   
   b) **User Experience**
      - How easy is it to use (no-code, low-code, or code-required)?
      - What's the learning curve?
      - User feedback and reviews (if available)
      - Common complaints or feature requests
   
   c) **Technical Approach**
      - What technology/architecture do they use?
      - Integration capabilities
      - Security and compliance features
      - Performance and scalability
   
   d) **Pricing & Business Model**
      - Free vs paid tiers
      - Enterprise pricing (if available)
      - What's included at each level
   
   e) **Market Position**
      - Target customer (SMB, mid-market, enterprise)
      - Primary use cases
      - Market share or adoption (if available)
   
   **Competitive Advantage Analysis (CRITICAL):**
   
   After researching competitors, identify Salesforce's advantages:
   
   1. **Unique Salesforce Strengths**
      - What can Salesforce do that competitors cannot?
      - Native CRM data access and integration
      - Established enterprise relationships
      - Salesforce security model and compliance
      - Einstein Trust Layer and data protection
      - AppExchange ecosystem
      - Multi-tenant architecture benefits
   
   2. **Feature Differentiation Opportunities**
      - How can we implement this feature BETTER than competitors?
      - What unique value does Salesforce bring?
      - How does this integrate with existing Salesforce products?
      - What makes this "Salesforce-native" vs bolted-on?
   
   3. **Competitive Gaps to Exploit**
      - What do competitors do poorly that we can excel at?
      - What features do they lack?
      - Where do users complain about competitors?
      - What enterprise needs are unmet?
   
   4. **Threats to Address**
      - What do competitors do better than us?
      - Where might we fall short?
      - What features are "table stakes" vs differentiators?
      - How can we mitigate our weaknesses?
   
   5. **Go-to-Market Positioning**
      - What's our compelling narrative?
      - "Unlike [competitor], Salesforce Prompt Builder..."
      - Target customer pain points we uniquely solve
      - ROI and business value differentiation

**Output Requirements:**
- Organize findings by topic with clear headings
- Include specific examples and technical details
- Cite sources where possible
- Flag any gaps in available information
- Keep the report under [800/1500/2500 words depending on depth]
- ALWAYS include competitive analysis section with comparison matrix
- ALWAYS include Salesforce competitive advantages section
- Focus on actionable insights for product development

**Search Strategy:**
- Start with official Salesforce documentation
- Research competitor products (documentation, blogs, reviews)
- Look for recent content (2023-2026) especially for Agentforce
- Check user review sites (G2, Capterra, TrustRadius)
- Search for "[competitor] vs Salesforce" comparisons
- Look for analyst reports (Gartner, Forrester) if available
- Cross-reference multiple sources for accuracy
- Note when information is inferred vs explicitly documented
```

### Phase 3: Synthesize Findings

After the research agent completes:

1. **Review Research Quality**
   - Verify key findings are well-sourced
   - Identify gaps requiring follow-up research
   - Assess relevance to user's original question

2. **Extract Actionable Insights**
   - Technical feasibility assessment
   - Architecture patterns to follow
   - Security considerations to address
   - Integration points to leverage
   - Competitive positioning and differentiation
   - Potential challenges and mitigations

3. **Analyze Competitive Positioning**
   
   After competitive research, create a positioning analysis:
   
   a) **Competitive Comparison Matrix**
      - Feature availability across competitors
      - Implementation quality ratings
      - Ease of use comparison
      - Pricing and value comparison
   
   b) **Salesforce Advantages**
      - Unique capabilities only Salesforce can offer
      - Areas where Salesforce can excel
      - Integration advantages with CRM
   
   c) **Competitive Threats**
      - Where competitors are stronger
      - Table stakes features we must match
      - Mitigation strategies
   
   d) **Differentiation Strategy**
      - How to position this feature uniquely
      - "Better than" narrative vs each major competitor
      - Target customer pain points we uniquely solve

4. **Create Structured Output**
   
   Organize the findings into a clear document:
   
   ```markdown
   # Research Summary: [Topic]
   
   ## Executive Summary
   [2-3 sentence overview of findings including competitive position]
   
   ## Current State
   [What exists today in Salesforce]
   
   ## Technical Architecture
   [How it works - data model, APIs, integrations]
   
   ## Key Capabilities
   [Specific features and functions available]
   
   ## Security Model
   [Authentication, authorization, data protection]
   
   ## Integration Patterns
   [How to connect with other systems/features]
   
   ## Competitive Analysis
   
   ### Competitor Landscape
   [Overview of competitors offering similar capabilities]
   
   ### Feature Comparison Matrix
   
   | Feature Aspect | Salesforce | OpenAI GPT Builder | Microsoft Copilot Studio | Google Agent Builder | Others |
   |----------------|------------|-------------------|-------------------------|---------------------|---------|
   | [Feature 1]    | Rating     | Rating            | Rating                  | Rating              | Rating  |
   | [Feature 2]    | Rating     | Rating            | Rating                  | Rating              | Rating  |
   | Ease of Use    | Rating     | Rating            | Rating                  | Rating              | Rating  |
   | Integration    | Rating     | Rating            | Rating                  | Rating              | Rating  |
   | Enterprise Security | Rating | Rating            | Rating                  | Rating              | Rating  |
   
   ### How Competitors Implement This Feature
   
   **OpenAI GPT Builder:**
   - [Implementation approach]
   - Strengths: [what they do well]
   - Weaknesses: [limitations]
   
   **Microsoft Copilot Studio:**
   - [Implementation approach]
   - Strengths: [what they do well]
   - Weaknesses: [limitations]
   
   **[Other competitors as relevant]**
   
   ## Salesforce Competitive Advantages
   
   ### Unique Strengths
   1. **[Advantage 1]**: [Why this matters and how to leverage it]
   2. **[Advantage 2]**: [Why this matters and how to leverage it]
   3. **[Advantage 3]**: [Why this matters and how to leverage it]
   
   ### Differentiation Opportunities
   - How we can implement this BETTER than competitors
   - What unique value Salesforce brings
   - Native integration advantages
   
   ### Competitive Gaps to Exploit
   - What competitors do poorly that we can excel at
   - Unmet enterprise needs
   - User pain points with competitor solutions
   
   ### Positioning Statement
   "Unlike [competitor], Salesforce Prompt Builder [unique value proposition] 
   because [competitive advantage], enabling customers to [customer benefit]."
   
   ## Best Practices
   [Recommended approaches and conventions]
   
   ## Constraints & Considerations
   [Limitations, governor limits, performance factors]
   
   ## Recommendations for Feature Development
   
   ### Technical Approach
   [Specific guidance for the requested feature]
   
   ### Differentiation Strategy
   [How to position and market this feature]
   
   ### Must-Have vs Nice-to-Have
   - Table stakes: [Features we must match]
   - Differentiators: [Features that set us apart]
   - Future potential: [Features for later consideration]
   
   ## Competitive Threats & Mitigation
   [Areas where competitors excel and how to address]
   
   ## Go-to-Market Implications
   [How competitive landscape affects positioning and messaging]
   
   ## Follow-Up Research Needed
   [Gaps or areas requiring deeper investigation]
   ```

4. **Save Research Artifacts**
   
   Store the research in `.agents/artifacts/` with a descriptive filename:
   - `salesforce-[topic]-research-[date].md` for general research
   - `prompt-builder-[feature]-analysis-[date].md` for feature-specific analysis
   - `mcp-integration-patterns-[date].md` for integration research

### Phase 4: Answer User's Question

Present the findings back to the user:

1. **Start with Direct Answer**
   - Address the user's original question immediately
   - Provide a clear recommendation or assessment

2. **Support with Research**
   - Summarize key findings that inform the answer
   - Reference specific Salesforce features or capabilities
   - Include technical details relevant to implementation

3. **Provide Context**
   - How this fits with existing Salesforce patterns
   - What similar features exist in the platform
   - Security and performance implications

4. **Offer Next Steps**
   - Suggest additional research areas if needed
   - Recommend prototyping or testing approaches
   - Point to relevant documentation or examples

5. **Share Artifact Location**
   - Tell the user where the full research is saved
   - Mention it's available for future reference

## Research Agent Configuration

When spawning the research agent, use these parameters:

```
Agent({
  description: "Research Salesforce [topic] for feature planning",
  subagent_type: "general-purpose",
  prompt: [Detailed research brief as outlined above]
})
```

**Tips for Effective Research Briefs:**

- **Be specific about what you need**: Architecture? UX patterns? Security model?
- **Set word count limits**: Prevents overly verbose reports
- **Request structured output**: Makes findings easier to parse
- **Include context**: Why this research matters helps agent prioritize
- **List specific questions**: Ensures all angles are covered

## Common Research Patterns

### Pattern 1: Feature Feasibility Assessment

**User asks**: "Can we add [feature] to Prompt Builder?"

**Research focus**:
- Existing similar features in Salesforce
- Technical constraints (governor limits, security)
- Required APIs or integration points
- Data model implications
- User permissions and access control

**Output**: Go/No-Go assessment with implementation complexity estimate

---

### Pattern 2: Integration Design

**User asks**: "How should Prompt Builder integrate with [Salesforce product]?"

**Research focus**:
- Target product's APIs and extension points
- Common integration patterns used in Salesforce
- Authentication and authorization models
- Data flow and synchronization requirements
- Error handling and resilience patterns

**Output**: Integration architecture with recommended approach

---

### Pattern 3: Competitive Analysis

**User asks**: "How do competitors handle [capability]?" or "What's our competitive advantage for [feature]?"

**Research focus**:
- Competitor product offerings and implementations
- Feature comparison across major platforms
- User reviews and feedback on competitor solutions
- Pricing and business model comparison
- Salesforce's unique advantages and differentiation
- Gaps in competitor offerings to exploit
- Threats from competitor strengths
- Industry-standard approaches and best practices
- User expectations based on market trends

**Competitors to research**:
- Primary: OpenAI, Microsoft, Google, Anthropic, Amazon
- Adjacent: Zapier, Make, Monday.com, LangChain, etc.
- Enterprise: IBM, ServiceNow, Oracle, SAP

**Output**: 
- Detailed comparison matrix with feature ratings
- Competitive advantage analysis
- Differentiation strategy recommendations
- Positioning statement ("Unlike X, Salesforce...")
- Go-to-market implications

---

### Pattern 4: Security & Compliance

**User asks**: "How do we secure [feature] in Prompt Builder?"

**Research focus**:
- Einstein Trust Layer capabilities
- Salesforce security model (OLS, FLS, sharing rules)
- Authentication patterns for external integrations
- Data residency and retention policies
- Audit and compliance requirements

**Output**: Security architecture with risk mitigations

---

### Pattern 5: UX/UI Patterns

**User asks**: "How should we design the UI for [feature]?"

**Research focus**:
- Lightning Design System components
- Common Salesforce UI patterns (Flow Builder, Setup pages)
- User personas and workflows
- Accessibility requirements
- Mobile considerations

**Output**: UI/UX recommendations with Salesforce pattern alignment

---

## Tools Available

### Web Research
- **WebSearch**: Find recent articles, documentation, announcements
- **WebFetch**: Retrieve specific documentation pages or API references

### Code Exploration
- **Grep**: Search for patterns in local documentation or code examples
- **Read**: Review documentation files or technical specs

### Agent Orchestration
- **Agent**: Spawn specialized research agents for deep dives

## Quality Standards

Research outputs should meet these criteria:

1. **Accuracy**: Cross-referenced with official sources
2. **Relevance**: Directly applicable to user's question
3. **Actionability**: Includes specific recommendations
4. **Completeness**: Covers all aspects of the topic
5. **Clarity**: Well-organized and easy to understand
6. **Timeliness**: Focuses on current capabilities (2024-2026)

## Common Pitfalls to Avoid

1. **Over-researching**: Don't spend hours on tangential topics
2. **Stale information**: Agentforce launched in 2024; prioritize recent sources
3. **Missing the question**: Always circle back to what user actually asked
4. **Technical jargon overload**: Balance detail with readability
5. **No clear recommendation**: User wants guidance, not just data dump

## Example Usage

**User request**: "I want to add a skill export feature to Prompt Builder that generates skill.md files compatible with Claude Code."

**Skill execution**:

1. **Scope definition**: Research skill.md format, MCP server configuration, Salesforce metadata export patterns, and file generation APIs
   
2. **Spawn research agent**: 
   ```
   Research: (1) Claude skill.md structure and requirements, 
   (2) MCP server configuration format, 
   (3) Salesforce metadata API export patterns, 
   (4) File generation and download in Lightning
   ```

3. **Synthesize findings**: Create export architecture plan covering:
   - skill.md format specification
   - Data model mapping (Salesforce objects → skill.md sections)
   - MCP config generation approach
   - File generation service design
   - Security considerations for export

4. **Answer user**: "Yes, skill export is feasible. Here's the recommended approach: [summary]. Full research saved to `.agents/artifacts/prompt-builder-skill-export-analysis-2026-04-21.md`"

## Continuous Improvement

After each research session:
- Note which sources were most valuable
- Identify gaps in research coverage
- Update this skill with new patterns or sources
- Refine research agent prompts based on output quality

---

## Version History

**v1.0.0** (2026-04-21)
- Initial skill creation
- Core research methodology defined
- Five common research patterns documented
