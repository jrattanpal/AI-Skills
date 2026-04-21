# Research Sources Guide

## Primary Salesforce Documentation Sources

### Trailhead
- **URL**: https://trailhead.salesforce.com
- **Best for**: Learning paths, getting started guides, conceptual overviews
- **Search tips**: 
  - Use filters for "Trails" (multi-module learning) vs "Modules" (single topic)
  - Look for badges related to: Einstein, Agentforce, Flow, Platform Development
  - Check "Related Resources" at bottom of modules for deeper technical docs

### Salesforce Developers Portal
- **URL**: https://developer.salesforce.com
- **Best for**: Technical documentation, API references, code samples
- **Key sections**:
  - `/docs/` - Documentation root
  - `/docs/atlas.en-us.api_rest.meta/api_rest/` - REST API reference
  - `/docs/platform/` - Platform event and architecture docs
  - `/docs/einstein/` - Einstein AI features

### Salesforce Help
- **URL**: https://help.salesforce.com
- **Best for**: Admin guides, feature setup, troubleshooting
- **Search tips**: Use "Setup" filter for admin content, "End User" for user guides

### Salesforce Release Notes
- **URL**: https://help.salesforce.com/s/articleView?id=release-notes
- **Best for**: Latest features, breaking changes, beta features
- **Key sections**: Einstein, Flow, Platform, API versions

## Agentforce-Specific Resources

### Agentforce Documentation
- **Search terms**: "Agentforce", "Atlas Reasoning Engine", "Agent Builder"
- **Key topics to research**:
  - Agent Topics and Actions
  - Agent Script syntax and capabilities
  - Integration with Einstein AI
  - Agent testing and deployment
  - Multi-step reasoning capabilities

### Agent Builder Modes
- **Document mode**: Natural language agent configuration
- **Canvas mode**: Visual workflow builder
- **Pro-code mode**: Direct script editing
- Research how each mode works and when to use them

## Model Context Protocol (MCP) Resources

### Official MCP Documentation
- **URL**: https://modelcontextprotocol.io
- **Best for**: Protocol specification, server implementation guides
- **Key sections**:
  - Protocol overview and architecture
  - Server types (stdio, SSE, HTTP, WebSocket)
  - Tool definition format (JSON Schema)
  - Authentication patterns
  - Best practices for tool design

### MCP SDKs
- **Languages**: TypeScript, Python, Java, Go, Rust, C#, PHP, Ruby, Swift, Kotlin
- **Best for**: Implementation examples, code patterns
- **Search for**: GitHub repos with "mcp-server" or "model-context-protocol"

### Salesforce MCP Integration
- **Search terms**: "Salesforce MCP", "AgentExchange", "External Services"
- **Look for**: 
  - How Salesforce agents connect to MCP servers
  - Authentication via Named Credentials
  - Tool discovery and registration
  - Error handling and retries

## Lightning Flow Builder Resources

### Flow Documentation
- **Search terms**: "Flow Builder", "Process Builder", "Lightning Flow"
- **Key topics**:
  - Flow types (Screen, Record-Triggered, Scheduled, etc.)
  - Flow actions and elements
  - Subflow patterns
  - Error handling
  - Testing flows

### UI/UX Patterns
- Research Flow Builder's Canvas UI:
  - Drag-and-drop mechanics
  - Properties panel design
  - Tool palette organization
  - Debugging and testing features
- These patterns should inform Prompt Builder UI design

## Einstein AI Platform

### Einstein Trust Layer
- **Key topics**:
  - Zero data retention architecture
  - Toxicity detection and filtering
  - Data grounding capabilities
  - Prompt injection prevention
  - Audit logging

### Einstein Features
- **Einstein GPT**: Generative AI capabilities
- **Einstein Prediction**: ML models
- **Einstein Bots**: Chatbot platform (predecessor to Agentforce)
- Research how these integrate with Prompt Builder

## Security & Compliance

### Salesforce Security Model
- **Key topics**:
  - Object-Level Security (OLS) - CRUD permissions
  - Field-Level Security (FLS) - Field visibility
  - Record-Level Security - Sharing rules, roles, hierarchy
  - Platform encryption
  - Event monitoring and audit logs

### OAuth & Authentication
- **Named Credentials**: External system authentication
- **Connected Apps**: OAuth 2.0 configuration
- **External Credentials**: Per-user authentication
- Research these for MCP server authentication patterns

## API References

### REST API
- **Endpoints to research**:
  - `/services/data/vXX.0/sobjects/` - Object metadata
  - `/services/data/vXX.0/query/` - SOQL queries
  - `/services/data/vXX.0/tooling/` - Tooling API for metadata

### Metadata API
- **Best for**: Deployment, package creation, org configuration
- **Research**: How to export/import custom metadata types

### Tooling API
- **Best for**: Development tools, code analysis, symbol tables
- **Use cases**: Skill validation, dependency analysis

## Community Resources

### Salesforce Stack Exchange
- **URL**: https://salesforce.stackexchange.com
- **Best for**: Real-world problems and solutions
- **Search tips**: Use tags like [agentforce], [flow], [einstein-ai]

### Salesforce Blogs
- **Developer Blog**: developer.salesforce.com/blogs
- **Product Blog**: www.salesforce.com/blog/category/products
- **Best for**: Announcements, best practices, case studies

### GitHub
- **Search for**: 
  - Salesforce sample apps and components
  - Community MCP server implementations
  - Open source Einstein integrations

## Search Strategies

### For Current State Research
1. Start with Trailhead for conceptual overview
2. Follow to Help documentation for setup/config details
3. Check API docs for technical implementation
4. Validate with release notes for latest changes

### For Technical Deep Dives
1. Search Developer docs for API endpoints
2. Look for code samples in GitHub/blogs
3. Check Stack Exchange for gotchas and limitations
4. Review governor limits documentation

### For UI/UX Patterns
1. Research Lightning Design System (lightningdesignsystem.com)
2. Study existing Salesforce UIs (Flow Builder, Setup pages)
3. Check Trailhead for user experience best practices
4. Look for accessibility guidelines (WCAG compliance)

### For Integration Patterns
1. Research External Services and Named Credentials
2. Study MuleSoft integration patterns
3. Check Platform Events for event-driven architecture
4. Review Change Data Capture for data sync patterns

## Research Workflow Checklist

When researching a new topic:

- [ ] Define specific questions to answer
- [ ] Start with official Salesforce docs
- [ ] Cross-reference multiple sources
- [ ] Note the date/version of information (especially for Agentforce)
- [ ] Capture code examples and patterns
- [ ] Document limitations and constraints
- [ ] Identify security considerations
- [ ] Note governor limits and performance factors
- [ ] Record sources for future reference
- [ ] Flag gaps requiring follow-up research

## Red Flags in Research

Be cautious of:
- **Outdated content**: Agentforce launched in 2024; ignore older "Einstein Bots" patterns
- **Beta features**: May change before GA release
- **Unofficial sources**: Verify against official docs
- **Missing version info**: API capabilities vary by version
- **Vague security claims**: Always verify with Trust Layer docs

## Keeping Research Current

- **Subscribe to**: Salesforce release notes, developer blog
- **Monitor**: Product announcements (Dreamforce, TrailblazerDX)
- **Check quarterly**: Major releases are Spring, Summer, Winter
- **Version awareness**: Note which API version features require
- **Beta program**: Consider joining for early access to new features
