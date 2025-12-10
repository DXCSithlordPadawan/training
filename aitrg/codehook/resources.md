# Claude Code Hooks Training Resources

This document provides a curated list of all resources used in the Claude Code Hooks training syllabus. All resources are freely accessible without payment or registration requirements.

---

## Primary Resources

### Official Claude Code Documentation

| Resource | URL | Type | Topics Covered |
|----------|-----|------|----------------|
| **Hooks Reference** | https://code.claude.com/docs/en/hooks.md | Documentation | Complete hook types, schemas, configuration |
| **Hooks Quickstart Guide** | https://code.claude.com/docs/en/hooks-guide.md | Tutorial | Getting started, examples, patterns |
| **Security Guide** | https://code.claude.com/docs/en/security.md | Documentation | Security model, best practices, threats |
| **Settings Configuration** | https://code.claude.com/docs/en/settings.md | Documentation | Configuration hierarchy, JSON structure |
| **Skills Documentation** | https://code.claude.com/docs/en/skills.md | Documentation | Skill structure, integration with hooks |

**Syllabus Coverage:** All days, all modules

---

### GitHub Repositories

| Resource | URL | Type | Topics Covered |
|----------|-----|------|----------------|
| **Claude Code Infrastructure Showcase** | https://github.com/diet103/claude-code-infrastructure-showcase | Repository | Production patterns, 6 hook examples, skill auto-activation |

**Key Files:**
- `skill-activation-prompt` (UserPromptSubmit hook)
- `post-tool-use-tracker` (PostToolUse hook)
- `tsc-check.sh` (TypeScript validation)
- `trigger-build-resolver.sh` (Build orchestration)
- `error-handling-reminder` (Development guardrails)
- `stop-build-check-enhanced` (Compilation check)
- `skill-rules.json` (Auto-activation configuration)

**Syllabus Coverage:**
- Day 1: Module 1.1, 1.2
- Day 3: Module 3.4
- Day 6: Module 6.1, 6.2
- Day 9: Module 9.2, 9.4
- Day 10: Module 10.1

---

### Video Resources

| Resource | URL | Channel | Topics Covered | Duration |
|----------|-----|---------|----------------|----------|
| **Claude Code Infrastructure Video** | https://www.youtube.com/watch?v=J5B9UGTuNoM | Various | Hook implementation, real-world examples | ~30-45 min |
| **Claude Code Hooks Tutorial** | https://www.youtube.com/watch?v=j0yyNQ5eTSk | Various | Hook configuration, practical demos | ~20-30 min |
| **MetalSole Channel** | https://www.youtube.com/@MetalSole | MetalSole | Claude Code workflows, advanced patterns | Various |

**Note:** YouTube videos may not always be accessible. Alternative text-based resources are provided in official documentation.

**Syllabus Coverage:**
- Day 1: Module 1.1
- Supplementary viewing throughout course

---

## Compliance and Security Resources

### UK Government Resources

| Resource | URL | Type | Topics Covered |
|----------|-----|------|----------------|
| **Secure by Design for AI** | https://www.gov.uk/government/publications/secure-by-design | Policy Document | Security principles for AI systems |
| **AI and Digital Regulations Service** | https://www.gov.uk/government/collections/ai-and-digital-regulation-service | Resource Collection | AI governance, compliance frameworks |

**Syllabus Coverage:**
- Day 1: Module 1.4
- Day 7: All modules

---

### NCSC (National Cyber Security Centre) Resources

| Resource | URL | Type | Topics Covered |
|----------|-----|------|----------------|
| **Guidelines for secure AI system development** | https://www.ncsc.gov.uk/collection/guidelines-secure-ai-system-development | Guidelines | Secure AI development lifecycle |
| **Principles for the security of machine learning** | https://www.ncsc.gov.uk/collection/machine-learning/principles-for-the-security-of-machine-learning | Principles | ML security fundamentals |
| **Supply chain security guidance** | https://www.ncsc.gov.uk/collection/supply-chain-security | Guidelines | Third-party risk management |
| **Secure development and deployment guidance** | https://www.ncsc.gov.uk/collection/developers-collection | Collection | Secure coding practices |

**Syllabus Coverage:**
- Day 1: Module 1.4
- Day 7: Module 7.4
- Referenced throughout security-focused modules

---

## Technical Tool Resources

### Programming and Scripting

| Tool | Documentation URL | Purpose in Training |
|------|------------------|---------------------|
| **Python 3** | https://docs.python.org/3/ | Hook script development |
| **Bash** | https://www.gnu.org/software/bash/manual/ | Shell hook scripts |
| **JSON** | https://www.json.org/ | Configuration format |
| **YAML** | https://yaml.org/spec/ | Alternative configuration format |
| **jq** | https://jqlang.github.io/jq/manual/ | JSON processing in hooks |

**Syllabus Coverage:** Throughout all practical exercises

---

### Code Quality Tools

| Tool | Documentation URL | Used In |
|------|------------------|---------|
| **Prettier** | https://prettier.io/docs/en/ | PostToolUse auto-formatting |
| **ESLint** | https://eslint.org/docs/latest/ | JavaScript/TypeScript linting |
| **Black** | https://black.readthedocs.io/ | Python code formatting |
| **Ruff** | https://docs.astral.sh/ruff/ | Python linting |
| **TypeScript Compiler** | https://www.typescriptlang.org/docs/ | Type checking hooks |

**Syllabus Coverage:**
- Day 3: Module 3.2
- Day 6: Module 6.1

---

### Development Tools

| Tool | Documentation URL | Purpose |
|------|------------------|---------|
| **Git** | https://git-scm.com/doc | Version control for hooks |
| **VS Code** | https://code.visualstudio.com/docs | Recommended editor |
| **ripgrep** | https://github.com/BurntSushi/ripgrep | Fast file searching |
| **Node.js** | https://nodejs.org/docs/ | JavaScript runtime for tools |

**Syllabus Coverage:** Throughout practical exercises

---

## Learning Resources by Module

### Week 1 Resources

#### Day 1: Introduction
- Official Hooks Reference
- Infrastructure Showcase repository
- Security Guide
- UK Gov Secure by Design document
- NCSC AI security guidelines

#### Day 2: PreToolUse Hooks
- Hooks Quickstart Guide
- Infrastructure Showcase (validation examples)
- Python documentation
- JSON processing guides

#### Day 3: PostToolUse and UserPromptSubmit
- Prettier documentation
- ESLint documentation
- Infrastructure Showcase (skill-activation-prompt)
- skill-rules.json examples

#### Day 4: Stop and Notification Hooks
- Hooks Reference (prompt-based hooks)
- Official documentation on LLM evaluation
- Notification integration examples

#### Day 5: Session Hooks
- Settings Configuration guide
- SessionStart examples from repository
- Environment variable documentation
- CLAUDE_ENV_FILE usage

---

### Week 2 Resources

#### Day 6: Advanced Patterns
- Infrastructure Showcase (tsc-check.sh, build-resolver)
- TypeScript compiler documentation
- Monorepo patterns
- Error handling examples

#### Day 7: Security Deep Dive
- NCSC Guidelines (all documents)
- UK Gov Secure by Design
- Security Guide (complete review)
- OWASP Top 10 (reference)

#### Day 8: Development Workflow
- Testing best practices
- Python unit testing documentation
- Bash testing frameworks
- Configuration management patterns

#### Day 9: Skills Integration
- Skills Documentation
- skill-rules.json specification
- Progressive disclosure pattern
- Infrastructure Showcase (skill examples)

#### Day 10: Production Deployment
- Case study: 50,000+ line TypeScript project
- All Infrastructure Showcase hooks
- Deployment best practices
- Performance monitoring guides

---

## Additional Reference Materials

### Hook Script Templates

These templates are derived from documentation examples:

1. **Python Hook Template** - Basic structure for validation hooks
2. **Bash Hook Template** - Shell script hook pattern
3. **Security Checklist** - Pre-deployment review
4. **Configuration Template** - Complete settings.json structure

**Location:** Embedded in lesson.md

---

### Cheat Sheets

1. **Hook Events Quick Reference** - All 10 event types
2. **Exit Code Reference** - Status communication
3. **JSON Schema Reference** - Input/output formats
4. **Matcher Patterns** - Regex examples

**Location:** README.md and lesson.md

---

## Free Tool Alternatives

If official tools require registration/payment, use these alternatives:

| Commercial Tool | Free Alternative | Documentation |
|----------------|-----------------|---------------|
| GitHub Copilot | Claude Code | https://code.claude.com |
| Prettier Pro | Prettier (free) | https://prettier.io |
| ESLint Premium | ESLint (free) | https://eslint.org |
| VS Code Pro | VS Code (free) | https://code.visualstudio.com |

---

## Accessibility Notes

All resources are designed to be accessible:

- **Text-based primary resources** - All critical content available in documentation
- **Video transcripts** - YouTube auto-generated captions available
- **Screen reader compatible** - Documentation sites follow WCAG guidelines
- **No paywalls** - All resources completely free
- **No registration required** - Direct access to all materials

---

## Resource Updates

This training uses resources current as of **December 2025**. Check for updates:

- **Claude Code Documentation:** Monthly updates, version-specific
- **NCSC Guidelines:** Quarterly reviews
- **UK Gov Publications:** Annual reviews
- **GitHub Repositories:** Check commit history for latest changes

---

## Troubleshooting Resource Access

### If a resource is unavailable:

1. **Official Documentation Down:**
   - Use cached version: https://web.archive.org/
   - Check GitHub repository README files
   - Use `/help` command in Claude Code CLI

2. **YouTube Videos Unavailable:**
   - All essential content available in text documentation
   - Videos are supplementary, not required
   - Check alternative channels listed

3. **GitHub Repository Access Issues:**
   - Clone repository locally when accessible
   - Repository content summarized in lesson.md
   - Core patterns documented in training materials

4. **Government Sites Down:**
   - Use archive.org cached versions
   - Core principles summarized in lesson plans
   - Alternative: EU AI regulations (similar principles)

---

## Resource Verification

All URLs verified as of: **2025-12-10**

| Resource Type | Count | Verification Status |
|--------------|-------|---------------------|
| Official Documentation | 5 | ✓ Accessible |
| GitHub Repositories | 1 | ✓ Accessible |
| Video Resources | 3 | ⚠ Requires browser |
| Government Sites | 6 | ✓ Accessible |
| Technical Tools | 11 | ✓ Free/Open Source |

**Legend:**
- ✓ Fully accessible, no restrictions
- ⚠ Accessible with minor limitations
- ✗ Requires registration/payment (not used)

---

## Recommended Reading Order

For self-study, follow this sequence:

1. **Start:** Hooks Reference documentation
2. **Then:** Hooks Quickstart Guide
3. **Review:** Infrastructure Showcase repository
4. **Security:** NCSC guidelines → UK Gov Secure by Design
5. **Practice:** Work through syllabus modules
6. **Reference:** Technical tool documentation as needed

---

## Learning Path Recommendations

### For Visual Learners
- Start with YouTube videos (if accessible)
- Use Mermaid diagrams in README.md
- Review code examples in repository
- Practice with hands-on labs

### For Text-Based Learners
- Focus on official documentation
- Work through examples in lesson.md
- Complete all reading materials first
- Reference videos only for clarification

### For Hands-On Learners
- Start immediately with practical exercises
- Reference documentation as needed
- Build personal hook library
- Experiment with variations

---

## Community Resources (Optional)

While not required, these may be helpful:

- **Claude Code GitHub Issues:** Community Q&A
- **Stack Overflow:** Search "claude-code hooks"
- **Developer Forums:** AI tool discussions

**Note:** These are supplementary only. All required knowledge is in primary resources.

---

## Copyright and Licensing

### Official Documentation
- Copyright: Anthropic PBC
- License: Proprietary, freely accessible
- Usage: Educational purposes permitted

### Open Source Tools
- Various licenses (MIT, Apache 2.0, etc.)
- Check individual tool repositories
- All listed tools permit educational use

### Government Publications
- Crown Copyright (UK publications)
- Open Government License
- Free to copy and redistribute

---

## Contact for Resource Issues

- **Claude Code Documentation Issues:** Use `/feedback` in CLI
- **GitHub Repository Issues:** Open issue on repository
- **Government Site Issues:** Check archive.org
- **Training Material Issues:** Contact training administrator

---

**Resource List Version:** 1.0
**Last Updated:** 2025-12-10
**Next Review:** Quarterly or upon major updates

---

*All resources comply with UK Government Secure by Design for AI and NCSC Secure Design Principles.*
