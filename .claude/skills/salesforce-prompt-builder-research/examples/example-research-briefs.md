# Example Research Briefs

## Example 1: Feature Feasibility Research

### User Request
"I want to add real-time collaboration to Prompt Builder so multiple users can edit a skill simultaneously like Google Docs."

### Research Agent Brief

```
Research real-time collaboration capabilities for adding to Salesforce Prompt Builder.

## Context
We want to enable multiple users to simultaneously edit Prompt Builder skills with 
live cursor tracking, conflict resolution, and presence indicators.

## Research Topics

1. **Salesforce Real-Time Technologies**
   - Platform Events for real-time updates
   - Streaming API capabilities
   - Lightning Message Service (LMS) for component communication
   - Change Data Capture (CDC) for record changes
   - Existing Salesforce features with real-time collaboration (if any)

2. **Concurrent Editing Patterns**
   - Record locking mechanisms in Salesforce
   - Optimistic vs pessimistic locking
   - Conflict resolution strategies
   - Multi-user editing in Flow Builder (does it exist?)

3. **Technical Constraints**
   - Governor limits on Platform Events
   - API rate limits for streaming
   - Data model considerations for operational transforms
   - Browser compatibility for WebSocket/SSE

4. **Similar Features in Salesforce**
   - How does Salesforce handle concurrent record editing?
   - Are there any collaborative editing features in the platform?
   - What patterns exist in Lightning Experience?

5. **Security Considerations**
   - User permissions during collaborative editing
   - Field-level security enforcement
   - Audit trail for multi-user changes
   - Session management and timeout handling

6. **Competitive Analysis**
   - How do Google Docs, Figma, Notion handle real-time collaboration?
   - Does OpenAI GPT Builder support collaborative editing?
   - Does Microsoft Copilot Studio support multi-user editing?
   - What do users expect from collaborative editing tools?
   - What are the table stakes features vs differentiators?

## Competitive Research

Research how competitors implement real-time collaboration:

**Primary Competitors:**
- OpenAI GPT Builder: Do multiple users can edit Custom GPTs simultaneously?
- Microsoft Copilot Studio: Multi-user bot editing capabilities?
- Google Vertex AI: Collaborative agent building?

**Adjacent Products:**
- Google Docs: Real-time collaboration patterns
- Figma: Design collaboration architecture
- Notion: Multi-user editing approach

**For each, document:**
- Is real-time collaboration supported?
- How is it implemented (cursors, presence, conflict resolution)?
- User feedback (what works, what frustrates users)?
- Performance characteristics (latency, scale)

**Salesforce Competitive Advantages:**
- What unique advantages does Salesforce have for this feature?
- How can we leverage Salesforce infrastructure (Platform Events)?
- What can we do better than competitors?
- What makes this "Salesforce-native" vs bolted-on?

## Specific Questions to Answer
- Can Platform Events handle real-time cursor position updates?
- What's the latency we can expect?
- How many concurrent editors can the system support?
- Do we need external infrastructure (WebSocket server) or can we use native Salesforce?

## Output Format
Provide a feasibility assessment with:
1. Technical approach (recommended architecture)
2. Salesforce capabilities available today
3. Potential limitations and workarounds
4. Implementation complexity estimate (low/medium/high)
5. Alternative approaches if direct real-time is not feasible

Keep report under 1,500 words. Focus on actionable technical insights.
```

---

## Example 2: Integration Architecture Research

### User Request
"How should Prompt Builder skills integrate with Slack for notifications and interactions?"

### Research Agent Brief

```
Research integration patterns between Salesforce and Slack for Prompt Builder skill capabilities.

## Context
We want Prompt Builder skills to:
- Send notifications to Slack channels
- Post interactive messages with buttons
- Respond to Slack commands and trigger skills
- Access Slack data for context (channels, users, messages)

## Research Topics

1. **Official Salesforce-Slack Integration**
   - Slack for Salesforce app capabilities
   - Built-in integration features
   - API access and limitations
   - Setup and configuration requirements

2. **Integration Patterns**
   - Outbound messaging: Salesforce → Slack
   - Inbound actions: Slack → Salesforce
   - Bidirectional conversations
   - Event-driven integration (triggers, platform events)

3. **Authentication & Security**
   - OAuth 2.0 flows for Slack
   - Named Credentials configuration
   - User identity mapping between systems
   - Token refresh and session management

4. **MCP Server Approach**
   - Can we expose Slack via MCP server?
   - Existing Slack MCP server implementations
   - Tool definitions for common Slack operations
   - Comparison: Native integration vs MCP approach

5. **Agentforce Integration**
   - Can Agentforce agents post to Slack?
   - Slack app for Agentforce (if exists)
   - Bot user patterns
   - Multi-channel conversation handling

6. **API Capabilities**
   - Slack Web API methods available
   - Webhook patterns for real-time events
   - Interactive message components
   - Rate limits and quotas

## Specific Questions to Answer
- Should we use native Salesforce-Slack integration or build custom?
- Can skills invoke Slack API directly or do we need an MCP server?
- How do we handle authentication for multi-user scenarios?
- What's the best pattern for two-way conversations?
- Are there governor limits we need to worry about?

## Output Format
Provide an integration architecture with:
1. Recommended approach (native vs custom vs MCP)
2. Architecture diagram (describe components and data flow)
3. Authentication pattern
4. Example skill workflow using Slack integration
5. Security considerations
6. Implementation complexity and timeline estimate

Keep report under 2,000 words with focus on practical implementation.
```

---

## Example 3: Security Model Research

### User Request
"How do we prevent prompt injection attacks in Prompt Builder skills that take user input?"

### Research Agent Brief

```
Research prompt injection attack vectors and prevention strategies for Salesforce Prompt Builder.

## Context
Prompt Builder skills will execute user-provided input in combination with system instructions
to LLMs. We need to prevent malicious users from:
- Overriding system instructions
- Accessing unauthorized data
- Exfiltrating sensitive information
- Bypassing security controls

## Research Topics

1. **Einstein Trust Layer**
   - How does Einstein Trust Layer prevent prompt injection?
   - Built-in security features we can leverage
   - Toxicity detection and content filtering
   - Input/output validation capabilities

2. **Prompt Injection Attack Patterns**
   - Common attack vectors and examples
   - "Ignore previous instructions" patterns
   - Context poisoning techniques
   - Tool misuse scenarios
   - Data exfiltration methods

3. **Industry Best Practices**
   - OWASP recommendations for LLM applications
   - Prompt engineering for security
   - Input sanitization techniques
   - Output validation patterns

4. **Salesforce Security Model Integration**
   - How to enforce FLS/OLS in AI-generated queries
   - Sharing rules in skill execution context
   - User permissions vs system context
   - Audit logging for AI operations

5. **Defense Strategies**
   - Instruction isolation techniques
   - Structured input/output formats
   - Tool allowlisting and sandboxing
   - Rate limiting and anomaly detection
   - Human-in-the-loop for sensitive operations

6. **Testing & Validation**
   - How to test for prompt injection vulnerabilities
   - Red team exercises for AI features
   - Automated security scanning
   - Bug bounty considerations

## Specific Questions to Answer
- What specific prompt injection attacks should we defend against?
- Does Einstein Trust Layer handle this automatically?
- Do we need additional validation layers?
- How do we balance security with flexibility?
- What audit logging is required for compliance?

## Output Format
Provide a security architecture with:
1. Attack vector catalog (what we're defending against)
2. Multi-layer defense strategy
3. Code examples for input validation
4. Integration with Salesforce security model
5. Testing methodology
6. Compliance considerations (SOC 2, GDPR, etc.)

Keep report under 2,500 words. Include specific code patterns and examples.
```

---

## Example 4: UI/UX Pattern Research

### User Request
"What's the best way to design the tool palette in Prompt Builder's canvas UI?"

### Research Agent Brief

```
Research UI/UX patterns for tool palettes in Salesforce and industry-standard design tools.

## Context
Prompt Builder needs a tool palette that displays:
- Internal Salesforce tools (record operations, flow actions)
- External MCP tools (dynamically loaded)
- Search/filter capabilities
- Tool documentation and previews
- Drag-and-drop to canvas

## Research Topics

1. **Lightning Flow Builder**
   - How is the tool palette organized?
   - Categories and grouping patterns
   - Search and filter UI
   - Tool previews and documentation
   - Drag-and-drop mechanics

2. **Lightning Design System (LDS)**
   - Recommended components for tool palettes
   - Docked panels vs modals
   - Tree views, accordions, tabs
   - Search input patterns
   - Icon usage and visual hierarchy

3. **Salesforce Setup Pages**
   - Object Manager tool organization
   - Quick Actions palette
   - Field palette in page layouts
   - Component palette in App Builder

4. **Industry Patterns**
   - Figma tool palette design
   - VS Code extension panel
   - Adobe Creative Suite tool organization
   - Notion slash commands / block menu

5. **Accessibility Requirements**
   - WCAG 2.1 AA compliance for palettes
   - Keyboard navigation patterns
   - Screen reader support
   - Color contrast requirements

6. **Mobile Considerations**
   - How do tool palettes work on tablets?
   - Touch-friendly interactions
   - Responsive design patterns
   - Bottom sheets vs side panels

7. **Dynamic Content**
   - How to handle 100+ tools?
   - Lazy loading patterns
   - Favorites and recently used
   - Customization and pinning

## Specific Questions to Answer
- Should tools be organized by category, type, or alphabetically?
- Fixed sidebar vs collapsible vs popover?
- How do users discover new MCP tools?
- What preview information do users need before using a tool?
- How do we handle tool documentation inline?

## Output Format
Provide UI/UX recommendations with:
1. Recommended tool palette layout (describe or ASCII mockup)
2. Organization and categorization scheme
3. Search and discovery patterns
4. Lightning Design System components to use
5. Accessibility considerations
6. Mobile/responsive design approach
7. User workflow examples

Keep report under 1,800 words. Include visual descriptions or ASCII mockups.
```

---

## Example 5: Competitive Analysis Research

### User Request
"How do other platforms handle AI skill marketplaces? Should we build one for Prompt Builder?"

### Research Agent Brief

```
Research AI skill marketplaces and platforms to inform Prompt Builder marketplace strategy.

## Context
We're considering building a marketplace where users can:
- Browse and install pre-built skills
- Share custom skills with community
- Rate and review skills
- Discover MCP servers and tools

## Research Topics

1. **Claude Code Skills Ecosystem**
   - How are Claude skills discovered and shared?
   - Skill.md format and structure
   - Distribution mechanisms (GitHub, marketplace, etc.)
   - Community patterns and best practices

2. **OpenAI GPT Store**
   - Custom GPT discovery and sharing
   - Monetization options
   - Quality control and moderation
   - Usage analytics for creators

3. **Salesforce AppExchange**
   - How AppExchange works (listing, review, install)
   - Security review process
   - Packaging and distribution
   - Pricing and licensing models
   - Discovery and search patterns

4. **Other AI Agent Platforms**
   - Hugging Face Spaces
   - LangChain Hub
   - Microsoft Copilot Studio
   - Any emerging skill marketplaces

5. **Community Patterns**
   - Open source vs commercial skills
   - Attribution and licensing
   - Version management and updates
   - Support and maintenance models

6. **Quality & Security**
   - Marketplace approval processes
   - Security scanning and validation
   - User ratings and feedback systems
   - Abuse prevention

7. **Business Model**
   - Free vs paid skills
   - Subscription models
   - Revenue sharing
   - Salesforce's positioning (open vs controlled)

## Specific Questions to Answer
- Is there demand for a skill marketplace in enterprise software?
- What's the right balance between open sharing and quality control?
- Should skills be free or allow monetization?
- How do we prevent malicious skills?
- What's unique about Salesforce's position vs competitors?

## Output Format
Provide a marketplace strategy with:
1. Competitive landscape overview (who's doing what)
2. Best practices from each platform
3. Gaps and opportunities
4. Recommended approach for Salesforce
5. Phased rollout plan (if we build it)
6. Success metrics and KPIs

Keep report under 2,000 words. Include comparison matrix if helpful.
```

---

## Tips for Writing Effective Research Briefs

### Structure Every Brief With:
1. **Context**: Why this research matters, what we're building
2. **Research Topics**: 5-7 specific areas to investigate
3. **Specific Questions**: Concrete questions that need answers
4. **Output Format**: What structure you want the report in
5. **Word Limit**: Keep agents focused (800/1500/2500 words)

### Be Specific About:
- Technical depth needed (overview vs implementation details)
- Target audience (developers, admins, product managers)
- Timeline sensitivity (need answer today vs can wait)
- Existing constraints (must use Salesforce native features)

### Include When Relevant:
- Competitive context (how do others solve this?)
- Security requirements (PII handling, compliance)
- Scale considerations (how many users/requests?)
- Integration points (what systems are involved?)

### Request Structured Output:
- Numbered sections for easy reference
- Code examples where applicable
- Comparison matrices for options
- Decision recommendations with rationale
- Follow-up research areas identified

### Set Clear Boundaries:
- "Focus on Salesforce-native solutions"
- "Prioritize security over flexibility"
- "Must work within governor limits"
- "Mobile-first approach required"

---

## Common Research Brief Templates

### Template: Technical Feasibility

```
Research [FEATURE] feasibility for Salesforce Prompt Builder.

Context: [Why we want this feature]

Research Topics:
1. Existing Salesforce capabilities
2. Technical constraints and limits
3. Required APIs and integration points
4. Security and permission considerations
5. Performance and scale implications
6. Alternative approaches

Questions:
- Is this technically possible in Salesforce?
- What are the limitations?
- What's the implementation complexity?
- Are there alternative approaches?

Output: Feasibility assessment (Go/No-Go) with technical approach
Word Limit: 1,500 words
```

### Template: Integration Design

```
Research integration between [SYSTEM A] and [SYSTEM B] for [USE CASE].

Context: [What we're trying to accomplish]

Research Topics:
1. Existing integration points
2. Authentication and security
3. Data flow and synchronization
4. API capabilities and limits
5. Error handling and resilience
6. Example implementations

Questions:
- What's the best integration pattern?
- How do we handle authentication?
- What are the failure modes?
- Any existing Salesforce integrations we can learn from?

Output: Integration architecture with data flow diagram
Word Limit: 2,000 words
```

### Template: Security Analysis

```
Research security considerations for [FEATURE] in Salesforce Prompt Builder.

Context: [What the feature does and security concerns]

Research Topics:
1. Attack vectors and threat model
2. Einstein Trust Layer capabilities
3. Salesforce security model integration
4. Industry best practices
5. Defense strategies and patterns
6. Testing and validation approaches

Questions:
- What are we defending against?
- What security controls exist in Salesforce?
- Do we need additional defense layers?
- How do we test for vulnerabilities?

Output: Security architecture with defense strategy
Word Limit: 2,500 words
```

### Template: Competitive Analysis

```
Research competitive landscape for [FEATURE] in AI skill platforms and identify Salesforce's competitive advantages.

Context: [What feature we're considering and why]

Competitors to Research:

**Primary AI Platforms:**
- OpenAI GPT Builder / Custom GPTs
- Microsoft Copilot Studio
- Google Vertex AI Agent Builder
- Anthropic Claude (skills, MCP)
- Amazon Bedrock Agents

**Adjacent Competitors:**
- [Relevant adjacent platforms for this feature]

Research Topics:

1. **Feature Availability & Implementation**
   - Which competitors offer this feature?
   - How do they implement it (architecture, UX)?
   - What do they do well?
   - What are their limitations?

2. **User Experience Comparison**
   - Ease of use (no-code, low-code, code-required)
   - Setup time and learning curve
   - User feedback and reviews
   - Common complaints and feature requests

3. **Technical Approach**
   - What technology/architecture do they use?
   - Integration capabilities
   - Security and compliance features
   - Performance and scalability

4. **Pricing & Availability**
   - Free vs paid tiers
   - Enterprise pricing
   - What's included at each level

5. **Salesforce Competitive Advantages**
   - What unique advantages does Salesforce have?
   - Native CRM integration benefits
   - Einstein Trust Layer vs competitor security
   - Agentforce vs competitor agent platforms
   - AppExchange ecosystem advantages
   - Multi-tenant architecture benefits

6. **Differentiation Opportunities**
   - How can we implement this BETTER than competitors?
   - What unique value can Salesforce provide?
   - What competitive gaps can we exploit?
   - What makes this "Salesforce-native"?

7. **Competitive Threats**
   - What do competitors do better than us?
   - What are table stakes features we must match?
   - Where might we fall short?
   - How do we mitigate weaknesses?

Questions to Answer:
- Which competitors offer the best version of this feature?
- What do users love/hate about competitor implementations?
- What unique advantages does Salesforce have?
- How should we differentiate our implementation?
- What's our competitive positioning statement?
- Are there features we must match vs features that differentiate?

Output Format:

1. **Competitive Landscape Overview**
   - Brief description of each competitor's offering
   
2. **Feature Comparison Matrix**
   | Aspect | Salesforce | OpenAI | Microsoft | Google | Amazon | Others |
   |--------|-----------|---------|-----------|---------|---------|---------|
   | Feature X | Rating | Rating | Rating | Rating | Rating | Rating |
   | Ease of Use | Rating | Rating | Rating | Rating | Rating | Rating |
   | Integration | Rating | Rating | Rating | Rating | Rating | Rating |
   | Enterprise | Rating | Rating | Rating | Rating | Rating | Rating |
   | Price/Value | Rating | Rating | Rating | Rating | Rating | Rating |

3. **Detailed Competitor Analysis**
   For each major competitor:
   - How they implement this feature
   - Strengths and weaknesses
   - User sentiment
   - Pricing

4. **Salesforce Competitive Advantages**
   - Unique strengths we can leverage
   - Differentiation opportunities
   - Competitive gaps to exploit
   
5. **Competitive Threats & Mitigation**
   - Where competitors excel
   - How we address weaknesses
   
6. **Positioning Recommendations**
   - Positioning statement: "Unlike [competitor], Salesforce Prompt Builder..."
   - Key messages vs each major competitor
   - Go-to-market implications

7. **Feature Prioritization**
   - Must have (table stakes to match competitors)
   - Should have (features that differentiate us)
   - Could have (nice to have / future)

Word Limit: 2,500 words
Focus: Actionable competitive intelligence for product strategy
```

---

## Example 6: Full Competitive Analysis Research

### User Request
"I want to add a visual canvas skill builder to Prompt Builder. Research how competitors handle visual skill building and identify our competitive advantages."

### Research Agent Brief

```
Research visual skill builder interfaces in competitive AI platforms and identify Salesforce Prompt Builder's competitive advantages.

## Context
We're considering building a visual canvas interface for skill creation, similar to Lightning Flow Builder. We need to understand:
- How competitors implement visual skill builders
- What users expect from visual builders
- How we can differentiate with Salesforce-native advantages

## Primary Competitors to Research

1. **Microsoft Copilot Studio**
   - Visual bot builder interface
   - Topic/action organization
   - User experience and feedback

2. **OpenAI GPT Builder**
   - Configuration interface
   - How visual/conversational it is
   - Ease of use analysis

3. **Google Vertex AI Agent Builder**
   - Visual components (if any)
   - Developer experience

4. **Zapier / Make (Integromat)**
   - Visual workflow builders (adjacent competitor)
   - Drag-and-drop patterns
   - User satisfaction

5. **Salesforce Flow Builder**
   - Our own visual builder (benchmark)
   - What patterns work well
   - User feedback

## Research Topics

### 1. Visual Builder Capabilities

For each competitor, research:

**Interface Design:**
- Canvas-based or form-based?
- Drag-and-drop support?
- Visual connections between steps?
- How are tools/actions represented?
- Preview and testing capabilities?

**User Experience:**
- How long to create first skill?
- Learning curve (reviews mention this?)
- Common user complaints?
- What do users love about it?

**Technical Capabilities:**
- What can you build visually vs requiring code?
- Complexity limits (when do users hit walls)?
- Debugging and troubleshooting tools?

### 2. Feature Comparison Matrix

Create a comparison matrix:

| Feature | Salesforce (Proposed) | Microsoft Copilot | OpenAI | Google | Zapier | Make |
|---------|---------------------|-------------------|---------|---------|---------|------|
| Visual Canvas | TBD | ? | ? | ? | ✓ | ✓ |
| Drag-and-Drop | TBD | ? | ? | ? | ✓ | ✓ |
| No-Code Friendly | TBD | ? | ? | ? | ✓ | ✓ |
| AI Assistance | TBD | ? | ? | ? | ? | ? |
| Real-time Preview | TBD | ? | ? | ? | ? | ? |
| Tool Palette | TBD | ? | ? | ? | ✓ | ✓ |

### 3. User Sentiment Analysis

Search for:
- G2 reviews mentioning "ease of use", "visual", "builder"
- Reddit discussions about each platform's builder
- YouTube tutorials (are users struggling?)
- Twitter feedback

**Key questions:**
- What do users say is easy?
- What frustrates users?
- What features do they wish existed?
- How do technical vs non-technical users rate it?

### 4. Salesforce Competitive Advantages

Identify unique advantages for visual skill builder:

**Potential Advantages:**

1. **Flow Builder Familiarity**
   - Millions of Salesforce users already know Flow Builder
   - Similar patterns = lower learning curve
   - Reuse existing UI components and patterns
   
2. **Native CRM Tool Palette**
   - Pre-built tools for Account, Contact, Case, etc.
   - One-click record operations
   - No configuration required
   
3. **Salesforce Data Preview**
   - Test with real org data
   - See actual CRM records in preview
   - Understand exactly how skill will work
   
4. **Security Visual Indicators**
   - Show FLS/OLS in real-time
   - Visual indication of which fields are accessible
   - Preview as different users
   
5. **AppExchange Tool Integration**
   - Visual catalog of AppExchange tools
   - One-click tool addition
   - Pre-configured for your org

**For each advantage:**
- How significant is it? (High/Medium/Low)
- Can competitors easily copy it? (Yes/No)
- How do we communicate it to users?

### 5. Differentiation Strategy

Based on competitor research, recommend:

**Must-Have Features (Table Stakes):**
- [Features all competitors have - we must match]

**Differentiating Features (Set Us Apart):**
- [Features that leverage Salesforce advantages]

**Future Enhancements (Nice to Have):**
- [Features that could come later]

### 6. Positioning

Develop positioning statements:

**vs Microsoft Copilot Studio:**
"Unlike Microsoft Copilot Studio which requires Power Platform expertise, Salesforce Prompt Builder's visual canvas is instantly familiar to anyone who's used Flow Builder, enabling business users to build AI skills in minutes, not days."

**vs OpenAI GPT Builder:**
"Unlike OpenAI GPT Builder which only offers text-based configuration, Salesforce Prompt Builder provides a visual canvas with drag-and-drop simplicity, making it easy for non-technical users to create sophisticated skills without writing instructions from scratch."

**vs Zapier:**
"Unlike Zapier which treats Salesforce as an external integration, Salesforce Prompt Builder's visual canvas has native CRM tools built-in, giving you one-click access to customers, cases, and opportunities without API configuration."

### 7. UX/UI Recommendations

Based on competitive research:

**What to Adopt from Competitors:**
- [Best practices from competitor UIs]

**What to Avoid from Competitors:**
- [Common complaints or anti-patterns]

**Salesforce-Specific Innovations:**
- [Unique UI patterns we can pioneer]

## Specific Questions to Answer

1. Which competitor has the best visual builder UX? Why?
2. What's the #1 complaint about visual builders?
3. What do non-technical users struggle with?
4. How can Flow Builder patterns give us an advantage?
5. What unique visual representations can we provide for CRM data?
6. How do competitors handle debugging/testing in visual builders?
7. What makes a visual builder "enterprise-grade"?
8. How can we make this easier than OpenAI GPT Builder?

## Output Requirements

Provide:

1. **Executive Summary** (200 words)
   - Should we build a visual canvas? (Yes/No/Maybe)
   - Key competitive insights
   - Recommended differentiation strategy

2. **Competitor Analysis** (800 words)
   - Detailed review of each competitor's approach
   - Comparison matrix
   - User sentiment summary

3. **Salesforce Competitive Advantages** (400 words)
   - Unique strengths we can leverage
   - How to communicate advantages
   - Differentiation opportunities

4. **Positioning Statements** (200 words)
   - Statement for each major competitor
   - Key messaging

5. **UX/UI Recommendations** (400 words)
   - What to adopt, avoid, and innovate
   - Specific design patterns

6. **Feature Prioritization** (200 words)
   - Must-have vs differentiator features

**Total Word Limit:** 2,200 words
**Focus:** Actionable competitive intelligence for product and UX decisions

## Search Strategy

1. Research Microsoft Copilot Studio visual builder thoroughly (primary competitor)
2. Try OpenAI GPT Builder hands-on (understand the baseline UX)
3. Study Flow Builder patterns (our internal benchmark)
4. Check user reviews on G2, Capterra for "ease of use" mentions
5. Search YouTube for "[competitor] tutorial" to see user struggles
6. Read Reddit r/salesforce for Flow Builder feedback
7. Look for "[competitor] vs [competitor]" comparisons
```

---

These templates and examples should help you quickly construct effective research briefs for any Prompt Builder feature investigation, with comprehensive competitive analysis included.
