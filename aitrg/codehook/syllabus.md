# Claude Code Hooks Training Syllabus

**Program Duration:** 2 Weeks (75 hours total)
**Study Schedule:** 37.5 hours per week, full-time self-study
**Target Audience:** Enterprise Architects, DevOps Engineers, AI Tool Administrators
**Prerequisites:** Basic understanding of CLI tools, JSON/YAML, and shell scripting

---

## Week 1: Foundations and Hook Types

### Day 1: Introduction to Claude Code Hooks (7.5 hours)

#### Module 1.1: What Are Hooks? (2 hours)
**Topics:**
- Understanding Claude Code architecture
- Hook lifecycle and execution flow
- Deterministic control vs LLM-based decisions
- When to use hooks vs skills vs agents

**Resources:**
- [Claude Code Infrastructure Showcase](https://github.com/diet103/claude-code-infrastructure-showcase)
- [Claude Code Hooks Documentation](https://code.claude.com/docs/en/hooks.md)
- [MetalSole YouTube Channel](https://www.youtube.com/@MetalSole)

**Duration:** 2 hours

---

#### Module 1.2: Hook Configuration Basics (2 hours)
**Topics:**
- Settings file hierarchy (local, project, user)
- JSON configuration structure
- Environment variables (CLAUDE_PROJECT_DIR, CLAUDE_CODE_REMOTE)
- Configuration priority and merging

**Resources:**
- [Settings Configuration Guide](https://code.claude.com/docs/en/settings.md)
- GitHub repository examples

**Hands-on Exercise:**
- Create `.claude/settings.json` file
- Configure first simple hook
- Test hook execution

**Duration:** 2 hours

---

#### Module 1.3: Hook Types Overview (1.5 hours)
**Topics:**
- Core hook events (10 types)
- Hook matchers and patterns
- Exit codes and status communication
- Parallel vs sequential execution

**Resources:**
- Official hooks reference documentation
- Pattern matching examples

**Duration:** 1.5 hours

---

#### Module 1.4: Security Fundamentals (2 hours)
**Topics:**
- Hook security model and risks
- Credential access and isolation
- Path traversal prevention
- Input validation best practices
- UK Gov Secure by Design principles for AI
- NCSC Secure Design Principles for AI

**Resources:**
- [Claude Code Security Guide](https://code.claude.com/docs/en/security.md)
- [UK Government Secure by Design for AI](https://www.gov.uk/government/publications/secure-by-design)
- [NCSC Guidelines for secure AI system development](https://www.ncsc.gov.uk/collection/guidelines-secure-ai-system-development)

**Duration:** 2 hours

---

### Day 2: PreToolUse and PermissionRequest Hooks (7.5 hours)

#### Module 2.1: PreToolUse Hook Deep Dive (3 hours)
**Topics:**
- PreToolUse hook input schema
- Tool matchers (exact, regex, wildcard)
- Permission decisions (allow, deny, ask)
- Input modification and validation
- Blocking dangerous commands

**Resources:**
- [Hooks Quickstart Guide](https://code.claude.com/docs/en/hooks-guide.md)
- Example scripts from GitHub repository

**Hands-on Exercises:**
1. Create Bash command validator
2. Implement file protection hook
3. Build regex-based matcher

**Duration:** 3 hours

---

#### Module 2.2: Command-Based PreToolUse Hooks (2 hours)
**Topics:**
- Python hook script structure
- Reading JSON from stdin
- Writing JSON to stdout
- Exit code handling
- Error messaging to stderr

**Hands-on Lab:**
- Build complete validation hook in Python
- Test with various tool calls
- Debug hook execution

**Duration:** 2 hours

---

#### Module 2.3: PermissionRequest Hooks (1.5 hours)
**Topics:**
- Auto-approval patterns
- Conditional permission logic
- Suppressing output
- User permission dialog interaction

**Hands-on Exercise:**
- Create auto-approve hook for Read operations
- Implement conditional approval logic

**Duration:** 1.5 hours

---

#### Module 2.4: Best Practice Review (1 hour)
**Topics:**
- Security checklist review
- Performance optimization
- Common pitfalls and solutions

**Duration:** 1 hour

---

### Day 3: PostToolUse and UserPromptSubmit Hooks (7.5 hours)

#### Module 3.1: PostToolUse Hook Fundamentals (2.5 hours)
**Topics:**
- PostToolUse input schema
- Tool result processing
- Additional context injection
- Feedback mechanisms

**Resources:**
- Official documentation examples
- GitHub repository patterns

**Duration:** 2.5 hours

---

#### Module 3.2: Auto-Formatting with PostToolUse (2 hours)
**Topics:**
- Prettier integration for TypeScript/JavaScript
- Black integration for Python
- Linter execution (ESLint, Ruff)
- File type detection

**Hands-on Lab:**
1. Configure Prettier auto-formatting
2. Add TypeScript compilation check
3. Integrate linting feedback

**Duration:** 2 hours

---

#### Module 3.3: UserPromptSubmit Hooks (2 hours)
**Topics:**
- Prompt validation and filtering
- Context injection on user input
- Blocking sensitive prompts
- Adding project context automatically

**Hands-on Exercise:**
- Create prompt validator
- Implement context loader
- Test with various user inputs

**Duration:** 2 hours

---

#### Module 3.4: Skill Auto-Activation Pattern (1 hour)
**Topics:**
- skill-rules.json configuration
- Automatic skill suggestion
- UserPromptSubmit + skill integration
- Pattern from infrastructure showcase

**Resources:**
- [Claude Code Infrastructure Showcase](https://github.com/diet103/claude-code-infrastructure-showcase)

**Duration:** 1 hour

---

### Day 4: Stop, SubagentStop, and Notification Hooks (7.5 hours)

#### Module 4.1: Stop Hook Introduction (2 hours)
**Topics:**
- Stop event trigger conditions
- Intelligent continue/stop decisions
- LLM-based evaluation hooks
- Prompt-based hook syntax

**Duration:** 2 hours

---

#### Module 4.2: Prompt-Based Hooks (2.5 hours)
**Topics:**
- Prompt hook vs command hook comparison
- Response schema structure
- Decision field (approve/block)
- Reason and stopReason fields
- Timeout configuration for LLM calls

**Hands-on Lab:**
- Create prompt-based Stop hook
- Test evaluation logic
- Measure performance impact

**Duration:** 2.5 hours

---

#### Module 4.3: SubagentStop Hooks (1.5 hours)
**Topics:**
- Subagent task verification
- Error detection in subagent output
- Task completion criteria
- Multi-agent workflow control

**Hands-on Exercise:**
- Implement subagent verification hook
- Test with Task tool

**Duration:** 1.5 hours

---

#### Module 4.4: Notification Hooks (1.5 hours)
**Topics:**
- Notification event types
- Desktop notification integration
- Logging and monitoring
- Non-blocking hook behavior

**Hands-on Exercise:**
- Create desktop notification script
- Implement logging hook

**Duration:** 1.5 hours

---

### Day 5: Session and Lifecycle Hooks (7.5 hours)

#### Module 5.1: SessionStart Hooks (3 hours)
**Topics:**
- Session initialization workflow
- Environment variable persistence
- CLAUDE_ENV_FILE usage
- Dependency installation
- Context loading patterns

**Resources:**
- GitHub repository session examples
- Official documentation

**Hands-on Lab:**
1. Create environment setup script
2. Implement NVM/Node.js configuration
3. Load project context automatically
4. Test persistence across session

**Duration:** 3 hours

---

#### Module 5.2: SessionEnd Hooks (1.5 hours)
**Topics:**
- Cleanup operations
- Session statistics collection
- Log finalization
- Resource deallocation

**Hands-on Exercise:**
- Build session cleanup hook
- Implement statistics logging

**Duration:** 1.5 hours

---

#### Module 5.3: PreCompact Hooks (1.5 hours)
**Topics:**
- Context compaction triggers
- Pre-compaction logging
- State preservation strategies
- Non-blocking operations

**Duration:** 1.5 hours

---

#### Module 5.4: Lifecycle Hook Integration (1.5 hours)
**Topics:**
- Combining SessionStart + PostToolUse + SessionEnd
- End-to-end session management
- Hook orchestration patterns

**Hands-on Lab:**
- Build complete session lifecycle
- Test full workflow

**Duration:** 1.5 hours

---

## Week 2: Advanced Patterns and Production Implementation

### Day 6: Advanced Hook Patterns (7.5 hours)

#### Module 6.1: Monorepo Hook Patterns (2.5 hours)
**Topics:**
- TypeScript compilation check pattern
- Multi-package validation
- Build orchestration hooks
- Workspace detection

**Resources:**
- [Claude Code Infrastructure Showcase - tsc-check.sh](https://github.com/diet103/claude-code-infrastructure-showcase)

**Hands-on Lab:**
- Implement monorepo TypeScript check
- Create workspace-aware hooks

**Duration:** 2.5 hours

---

#### Module 6.2: Error Handling and Guardrails (2 hours)
**Topics:**
- Development guardrail patterns
- Error message enhancement
- Common mistake prevention
- Build verification hooks

**Resources:**
- error-handling-reminder hook example
- stop-build-check-enhanced pattern

**Hands-on Exercise:**
- Create error handling reminder hook
- Implement build verification

**Duration:** 2 hours

---

#### Module 6.3: MCP Tool Hooks (1.5 hours)
**Topics:**
- MCP tool naming patterns (mcp__server__tool)
- Regex matchers for MCP tools
- Memory server integration
- Custom MCP tool validation

**Duration:** 1.5 hours

---

#### Module 6.4: Hook Performance Optimization (1.5 hours)
**Topics:**
- Specific vs wildcard matchers
- Timeout tuning
- Parallel execution strategies
- Deduplication patterns
- Performance measurement

**Hands-on Lab:**
- Profile hook execution times
- Optimize slow hooks
- Implement caching strategies

**Duration:** 1.5 hours

---

### Day 7: Security and Compliance (7.5 hours)

#### Module 7.1: Security Threat Modeling (2 hours)
**Topics:**
- Hook-specific attack vectors
- Malicious hook detection
- External modification warnings
- Configuration snapshots

**Resources:**
- [Claude Code Security Guide](https://code.claude.com/docs/en/security.md)
- UK Gov Secure by Design principles

**Duration:** 2 hours

---

#### Module 7.2: Input Sanitization Deep Dive (2 hours)
**Topics:**
- Path traversal prevention
- Command injection protection
- JSON injection attacks
- Shell variable quoting
- Regex validation patterns

**Hands-on Lab:**
1. Build comprehensive input validator
2. Test against known vulnerabilities
3. Implement sanitization library

**Duration:** 2 hours

---

#### Module 7.3: Sensitive File Protection (1.5 hours)
**Topics:**
- Environment file detection
- Credentials and secrets protection
- Git internals protection
- Lock file protection patterns

**Hands-on Exercise:**
- Create sensitive file protection hook
- Build whitelist/blacklist system

**Duration:** 1.5 hours

---

#### Module 7.4: NCSC AI Security Principles Application (2 hours)
**Topics:**
- Secure development for AI systems
- Supply chain security for hooks
- Audit logging requirements
- Incident response for hook failures

**Resources:**
- [NCSC Guidelines for secure AI system development](https://www.ncsc.gov.uk/collection/guidelines-secure-ai-system-development)
- [NCSC Principles for the security of machine learning](https://www.ncsc.gov.uk/collection/machine-learning/principles-for-the-security-of-machine-learning)

**Duration:** 2 hours

---

### Day 8: Hook Development Workflow (7.5 hours)

#### Module 8.1: Hook Testing Strategies (2 hours)
**Topics:**
- Local testing with mock inputs
- Unit testing hook scripts
- Integration testing with Claude Code
- Debugging with --debug flag

**Hands-on Lab:**
1. Create test harness for hooks
2. Write unit tests for validation logic
3. Debug failing hooks

**Duration:** 2 hours

---

#### Module 8.2: Hook Script Structure Best Practices (2 hours)
**Topics:**
- Python hook template
- Bash hook template
- Error handling patterns
- Logging best practices
- Exit code conventions

**Hands-on Exercise:**
- Create reusable hook templates
- Build hook library structure

**Duration:** 2 hours

---

#### Module 8.3: Configuration Management (1.5 hours)
**Topics:**
- Local vs project vs user settings
- Settings file organization
- Version control strategies
- Team collaboration patterns

**Duration:** 1.5 hours

---

#### Module 8.4: Documentation and Maintenance (2 hours)
**Topics:**
- Hook documentation standards
- Inline comments best practices
- Configuration documentation
- Handoff procedures

**Hands-on Exercise:**
- Document existing hooks
- Create configuration README

**Duration:** 2 hours

---

### Day 9: Skills and Hook Integration (7.5 hours)

#### Module 9.1: Skill Architecture Review (1.5 hours)
**Topics:**
- Skill structure and SKILL.md format
- 500-line modular pattern
- Resource organization
- Skill vs hook comparison

**Resources:**
- [Claude Code Skills Documentation](https://code.claude.com/docs/en/skills.md)
- Infrastructure showcase examples

**Duration:** 1.5 hours

---

#### Module 9.2: Auto-Activation System (3 hours)
**Topics:**
- skill-rules.json structure
- File path pattern matching
- Keyword detection
- Context-based triggers
- UserPromptSubmit integration for skills

**Resources:**
- [Claude Code Infrastructure Showcase](https://github.com/diet103/claude-code-infrastructure-showcase)

**Hands-on Lab:**
1. Create skill-rules.json configuration
2. Implement auto-activation hook
3. Test with various prompts
4. Debug activation logic

**Duration:** 3 hours

---

#### Module 9.3: Skill Guardrails with Hooks (2 hours)
**Topics:**
- Validating skill inputs
- Restricting skill execution
- Logging skill usage
- Skill-specific PostToolUse hooks

**Hands-on Exercise:**
- Create skill validation hook
- Implement usage logging

**Duration:** 2 hours

---

#### Module 9.4: Progressive Disclosure Pattern (1 hour)
**Topics:**
- 500-line limit rationale
- Resource splitting strategies
- Dynamic content loading
- Context window management

**Duration:** 1 hour

---

### Day 10: Production Deployment and Case Studies (7.5 hours)

#### Module 10.1: Production Hook Examples (2.5 hours)
**Topics:**
- 6 production microservices case study
- 50,000+ TypeScript lines scenario
- Real-world patterns and solutions
- Lessons learned

**Resources:**
- [Claude Code Infrastructure Showcase](https://github.com/diet103/claude-code-infrastructure-showcase)

**Case Studies:**
1. TypeScript monorepo validation
2. Build orchestration system
3. Tool usage tracking
4. Skill auto-activation

**Duration:** 2.5 hours

---

#### Module 10.2: Deployment Checklist (2 hours)
**Topics:**
- Pre-deployment security review
- Configuration validation
- Testing procedures
- Rollback strategies
- Documentation requirements

**Hands-on Exercise:**
- Create deployment checklist
- Perform security audit
- Document deployment process

**Duration:** 2 hours

---

#### Module 10.3: Troubleshooting Common Issues (1.5 hours)
**Topics:**
- Hook not executing
- Permission errors
- Timeout issues
- JSON parsing errors
- Path resolution problems

**Resources:**
- Common error patterns
- Debug command reference

**Duration:** 1.5 hours

---

#### Module 10.4: Performance Monitoring (1.5 hours)
**Topics:**
- Execution time tracking
- Resource usage monitoring
- Performance regression detection
- Optimization techniques

**Hands-on Lab:**
- Implement performance logging
- Analyze hook metrics
- Identify bottlenecks

**Duration:** 1.5 hours

---

## Assessment Schedule

### Formative Assessments
- **End of Day 2:** PreToolUse hooks quiz (30 min)
- **End of Day 4:** Hook types comprehensive quiz (45 min)
- **End of Day 7:** Security and compliance quiz (45 min)
- **End of Day 9:** Skills integration quiz (30 min)

### Summative Assessment
- **Day 10 Final Assessment:** Comprehensive knowledge test (2 hours included in Day 10)
- **Practical Project:** Build production-ready hook system (evaluated via self-assessment)

---

## Learning Outcomes

By completing this syllabus, participants will be able to:

1. **Understand** Claude Code hook architecture and lifecycle
2. **Configure** all 10 hook types with proper JSON/YAML syntax
3. **Implement** secure command-based and prompt-based hooks
4. **Apply** UK Gov and NCSC security principles to AI tooling
5. **Create** production-ready validation, formatting, and guardrail hooks
6. **Integrate** hooks with skills for auto-activation
7. **Deploy** and maintain enterprise hook configurations
8. **Troubleshoot** common hook issues and optimize performance
9. **Design** monorepo and multi-service hook architectures
10. **Document** hook systems for team collaboration

---

## Study Tips

1. **Hands-on Practice:** Complete all practical exercises - theory alone is insufficient
2. **Experiment Safely:** Use isolated test environments for security testing
3. **Document Everything:** Keep notes on patterns and solutions
4. **Review Daily:** Spend 15 minutes reviewing previous day's content
5. **Build Portfolio:** Create a personal hook library as you learn
6. **Security First:** Always consider security implications before implementation
7. **Ask Questions:** Use Claude Code `/feedback` for clarification
8. **Collaborate:** Share patterns with team members (where appropriate)

---

## Prerequisites Checklist

Before starting this training, ensure you have:

- [ ] Claude Code CLI installed and configured
- [ ] Basic understanding of JSON and YAML syntax
- [ ] Python 3.x installed (for hook scripts)
- [ ] Bash/shell scripting familiarity
- [ ] Git installed and basic Git knowledge
- [ ] Text editor or IDE (VS Code recommended)
- [ ] Node.js/npm installed (for formatting tools)
- [ ] Access to test/sandbox environment
- [ ] Read access to provided GitHub repositories
- [ ] Completed basic Claude Code tutorial

---

## Support Resources

- **Official Documentation:** https://code.claude.com/docs
- **GitHub Issues:** https://github.com/anthropics/claude-code/issues
- **Command:** Use `/help` in Claude Code CLI
- **Feedback:** Use `/feedback` command for questions
- **Security Reporting:** Follow responsible disclosure process

---

**Total Training Time:** 75 hours (37.5 hours/week × 2 weeks)

**Certification:** Upon completion of all modules, self-assessment, and quiz with 80%+ score

---

*This syllabus aligns with UK Government Secure by Design for AI principles and NCSC Secure Design Principles for AI systems.*

**Version:** 1.0
**Last Updated:** 2025-12-10
**Next Review:** Quarterly or upon major Claude Code updates
