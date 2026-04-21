# Contributing to AI Skills

Thank you for your interest in contributing to the AI Skills repository! This document provides guidelines for contributing skills, improvements, and documentation.

## 🎯 Ways to Contribute

### 1. Report Issues
- Skill not working as expected
- Inaccurate research results
- Missing competitor information
- Documentation unclear

### 2. Improve Existing Skills
- Add new research sources
- Update competitor profiles
- Enhance research patterns
- Improve output quality

### 3. Add New Skills
- Create skills for other Salesforce products
- Create skills for different research domains
- Share domain-specific skills with team

### 4. Update Documentation
- Clarify usage instructions
- Add examples
- Document best practices
- Share learnings

## 📋 Contribution Process

### Reporting Issues

1. **Check existing issues** to avoid duplicates
2. **Create a new issue** with:
   - Clear, descriptive title
   - Skill version
   - Query that triggered the issue
   - Expected vs actual behavior
   - Screenshots if applicable

3. **Label appropriately:**
   - `bug` - Something isn't working
   - `enhancement` - New feature request
   - `documentation` - Documentation improvements
   - `question` - Need clarification

### Improving Skills

1. **Fork the repository**
   ```bash
   git fork https://github.com/jrattanpal/AI-Skills.git
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/improve-competitive-analysis
   ```

3. **Make your changes:**
   - Edit skill files
   - Add documentation
   - Test thoroughly

4. **Commit with clear messages:**
   ```bash
   git commit -m "feat: Add Oracle competitor profile to competitive framework"
   git commit -m "docs: Clarify research source usage"
   git commit -m "fix: Correct OpenAI GPT Builder pricing information"
   ```

5. **Push to your fork:**
   ```bash
   git push origin feature/improve-competitive-analysis
   ```

6. **Create a Pull Request:**
   - Describe what changed and why
   - Reference any related issues
   - Include before/after examples

### Adding Competitor Profiles

When adding a new competitor to track:

1. **Edit:** `.claude/skills/salesforce-prompt-builder-research/references/competitive-analysis-framework.md`

2. **Add profile section:**
   ```markdown
   #### X. [Competitor Name]
   **What they offer:**
   - [Key capabilities]
   
   **Target market:**
   - [Who they serve]
   
   **Strengths:**
   - [What they do well]
   
   **Weaknesses:**
   - [Limitations or gaps]
   
   **Research sources:**
   - Official documentation
   - Key URLs
   ```

3. **Update competitor list in SKILL.md:**
   - Add to "Competitors to Research" section
   - Include in research agent instructions

4. **Test:**
   - Ask skill to compare vs new competitor
   - Verify profile information appears in output

### Adding Research Patterns

To add a new research pattern:

1. **Document in SKILL.md:**
   ```markdown
   ### Pattern X: [Pattern Name]
   
   **User asks**: "[Example trigger phrase]"
   
   **Research focus**:
   - [Topic 1]
   - [Topic 2]
   
   **Output**: [Expected format]
   ```

2. **Add example brief:**
   - Edit `examples/example-research-briefs.md`
   - Include full example with expected output

3. **Test the pattern:**
   - Try multiple variations
   - Verify output quality
   - Document any edge cases

## ✅ Quality Standards

### Code Quality
- **Clarity:** Code and documentation should be clear
- **Completeness:** Include all necessary context
- **Accuracy:** Verify facts and sources
- **Maintainability:** Easy for others to update

### Research Quality
- **Sourced:** Cite where information comes from
- **Current:** Focus on 2024-2026 information
- **Accurate:** Cross-reference multiple sources
- **Balanced:** Present both strengths and weaknesses

### Documentation Quality
- **Clear:** Easy to understand
- **Complete:** Cover all necessary topics
- **Examples:** Include concrete examples
- **Updated:** Keep in sync with code changes

## 🔍 Testing Guidelines

### Before Submitting

Test your changes:

1. **Skill triggers properly:**
   ```
   "I want to add [feature] to Prompt Builder"
   ```

2. **Research completes successfully:**
   - No errors during execution
   - All sections populated
   - Output saved to artifacts

3. **Competitive analysis included:**
   - Competitors researched
   - Comparison matrix created
   - Salesforce advantages identified
   - Positioning statements generated

4. **Quality checks:**
   - Sources cited
   - Information current
   - Examples work
   - Links valid

### Test Queries

Use these test queries to verify functionality:

```
"I want to add skill versioning to Prompt Builder"
"How does Agentforce handle multi-step workflows?"
"Compare Salesforce vs Microsoft Copilot Studio for visual builders"
"Research MCP authentication patterns for enterprise security"
"What's our competitive advantage for skill export?"
```

## 📝 Commit Message Guidelines

Use conventional commit format:

- `feat:` New feature or capability
- `fix:` Bug fix
- `docs:` Documentation changes
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks

**Examples:**
```
feat: Add ServiceNow AI competitor profile
fix: Correct Microsoft Copilot Studio pricing info
docs: Clarify competitive analysis output format
refactor: Simplify research agent instructions
chore: Update competitor profiles for Q1 2026
```

## 🤝 Review Process

### What Reviewers Look For

- **Accuracy:** Is the information correct?
- **Completeness:** Are all sections filled in?
- **Clarity:** Is it easy to understand?
- **Testing:** Has it been tested?
- **Documentation:** Is it documented?

### Review Timeline

- **Initial review:** Within 2 business days
- **Follow-up questions:** Respond within 3 business days
- **Approval & merge:** After passing review

## 🔒 Security & Privacy

### What NOT to Include

❌ **Internal-only information:**
- Confidential roadmaps
- Internal pricing strategies
- Non-public customer data
- Proprietary research

❌ **Personal information:**
- API keys or credentials
- Personal email addresses
- Internal system URLs
- Sensitive data

❌ **Competitive intelligence from unauthorized sources:**
- Information obtained through deception
- Leaked documents
- Unauthorized access

### What IS Okay

✅ **Public information:**
- Official documentation
- Published pricing
- Public blog posts
- User reviews on public sites
- Conference presentations
- Press releases

## 🎓 Learning Resources

### For Skill Development

- **Claude Code Documentation:** https://docs.anthropic.com/claude/docs/claude-code
- **MCP Specification:** https://modelcontextprotocol.io
- **Skill.md Format:** See examples in this repo

### For Competitive Research

- **Competitor Documentation:** Official product docs
- **Review Sites:** G2, Capterra, TrustRadius
- **Analyst Reports:** Gartner, Forrester (if you have access)
- **Community:** Reddit, Stack Overflow, Discord

### For Salesforce Research

- **Trailhead:** https://trailhead.salesforce.com
- **Developer Docs:** https://developer.salesforce.com
- **Release Notes:** https://help.salesforce.com/s/articleView?id=release-notes

## 💬 Communication

### Channels

- **GitHub Issues:** Bug reports, feature requests
- **Pull Requests:** Code/documentation changes
- **Team Chat:** Quick questions (use `@ai-skills`)
- **Email:** [Your team email]

### Response Times

- **Issues:** 2 business days
- **PRs:** 3 business days
- **Questions:** 1 business day

## 🙏 Recognition

Contributors will be:
- Listed in CONTRIBUTORS.md
- Mentioned in release notes
- Credited in documentation

## 📜 License

By contributing, you agree that your contributions will be licensed under the MIT License.

## ❓ Questions?

If you have questions about contributing:

1. Check this document first
2. Search existing issues
3. Ask in team chat with `@ai-skills`
4. Create a GitHub issue with label `question`

---

**Thank you for contributing to AI Skills!** 🎉

Your contributions help the entire team build better Salesforce features with competitive intelligence built in.
