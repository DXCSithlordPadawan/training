# Claude Code Hooks Training - Self-Assessment Questionnaire

**Purpose:** This self-assessment helps you evaluate your understanding and competency after completing the Claude Code Hooks training syllabus.

**Instructions:**
1. Answer each question honestly based on your current understanding
2. Use the rating scale: 1 (Not confident) to 5 (Very confident)
3. Review any areas where you score 3 or below
4. Target score: Average of 4+ across all sections for certification readiness

---

## Section 1: Hook Fundamentals (10 questions)

Rate your confidence level (1-5) for each competency:

### 1.1 Hook Definition and Purpose

**Q1:** I can clearly explain what Claude Code hooks are and how they differ from skills and agents.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q2:** I understand the hook lifecycle and can explain when each hook type executes in the agent loop.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q3:** I can identify appropriate use cases for hooks and explain when NOT to use hooks.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

### 1.2 Hook Configuration

**Q4:** I can create and modify `.claude/settings.json` files with correct JSON syntax for hook configuration.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q5:** I understand the settings file hierarchy (local, project, user) and configuration priority.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q6:** I can correctly use environment variables (CLAUDE_PROJECT_DIR, CLAUDE_CODE_REMOTE, CLAUDE_ENV_FILE) in hook commands.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

### 1.3 Hook Types Knowledge

**Q7:** I can name and describe all 10 hook event types and their purposes.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q8:** I understand the difference between command-based and prompt-based hooks and when to use each.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q9:** I can create matcher patterns using exact match, regex, and wildcards for tool filtering.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q10:** I understand hook exit codes (0, 2, other) and their meanings.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Section 1 Total: _____ / 50**

---

## Section 2: PreToolUse and PermissionRequest Hooks (10 questions)

### 2.1 PreToolUse Hook Implementation

**Q11:** I can write a complete PreToolUse hook that reads JSON from stdin and makes permission decisions.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q12:** I understand the PreToolUse input schema and can access all fields (tool_name, tool_input, etc.).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q13:** I can create hooks that make permission decisions (allow/deny/ask) with proper JSON output.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q14:** I can implement input modification using the updatedInput field in hook responses.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q15:** I have created a working Bash command validator that blocks dangerous operations.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

### 2.2 PermissionRequest Hooks

**Q16:** I understand the difference between PreToolUse and PermissionRequest hooks and when to use each.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q17:** I can implement auto-approval logic for safe operations using PermissionRequest hooks.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q18:** I can use suppressOutput to hide permission decisions from the transcript.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q19:** I have implemented context-aware approval logic that considers file paths and directories.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q20:** I can test PreToolUse hooks locally with mock JSON inputs before deploying.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Section 2 Total: _____ / 50**

---

## Section 3: PostToolUse, UserPromptSubmit, and Other Hooks (10 questions)

### 3.1 PostToolUse Hooks

**Q21:** I can create PostToolUse hooks that process tool results and add feedback.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q22:** I have implemented auto-formatting hooks (Prettier, Black, ESLint) for code files.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q23:** I understand how to inject additional context into Claude's responses using PostToolUse.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

### 3.2 UserPromptSubmit Hooks

**Q24:** I can create UserPromptSubmit hooks that validate user prompts before processing.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q25:** I understand how to inject project context automatically using UserPromptSubmit hooks.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q26:** I have implemented the skill auto-activation pattern using skill-rules.json and UserPromptSubmit.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

### 3.3 Stop and Session Hooks

**Q27:** I can create prompt-based Stop hooks that make intelligent continue/stop decisions.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q28:** I understand SessionStart hooks and can use CLAUDE_ENV_FILE to persist environment variables.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q29:** I have created SessionEnd hooks for cleanup and logging.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q30:** I understand SubagentStop hooks and can verify subagent task completion.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Section 3 Total: _____ / 50**

---

## Section 4: Security and Compliance (10 questions)

### 4.1 Security Principles

**Q31:** I understand the security risks of hooks (credential access, arbitrary code execution).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q32:** I can identify and prevent path traversal vulnerabilities in hooks.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q33:** I know how to prevent command injection vulnerabilities (proper quoting, input validation).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q34:** I can implement sensitive file protection (env files, credentials, secrets).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q35:** I have implemented audit logging for all hook decisions.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

### 4.2 Compliance

**Q36:** I understand UK Government Secure by Design principles and how they apply to hooks.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q37:** I can apply NCSC Secure Design Principles for AI to hook implementations.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q38:** I implement "deny by default" and explicit allow lists in my hooks.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q39:** I follow the principle of least privilege in hook permissions.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q40:** I have completed the security checklist review for all my hooks before deployment.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Section 4 Total: _____ / 50**

---

## Section 5: Advanced Patterns and Production (10 questions)

### 5.1 Advanced Patterns

**Q41:** I understand the monorepo TypeScript validation pattern (tsc-check.sh).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q42:** I can implement build orchestration hooks (trigger-build-resolver pattern).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q43:** I have created error handling reminder hooks for development guardrails.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q44:** I understand the skill auto-activation system using skill-rules.json.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q45:** I can implement hooks for MCP tools using proper naming patterns (mcp__server__tool).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

### 5.2 Production Deployment

**Q46:** I have deployed hooks to a production environment successfully.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q47:** I can troubleshoot common hook issues (not executing, permission errors, timeouts).

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q48:** I have implemented performance monitoring and optimization for my hooks.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q49:** I have created documentation for my hooks including configuration examples and security notes.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Q50:** I understand the production patterns from the 50,000+ line TypeScript case study.

[ ] 1 - Not confident
[ ] 2 - Slightly confident
[ ] 3 - Moderately confident
[ ] 4 - Confident
[ ] 5 - Very confident

**Section 5 Total: _____ / 50**

---

## Overall Assessment Summary

### Total Score Calculation

- **Section 1 (Fundamentals):** _____ / 50
- **Section 2 (PreToolUse/PermissionRequest):** _____ / 50
- **Section 3 (Other Hooks):** _____ / 50
- **Section 4 (Security):** _____ / 50
- **Section 5 (Advanced/Production):** _____ / 50

**Total Score:** _____ / 250

**Average Score:** _____ / 5.0

---

## Competency Levels

Based on your average score:

### 4.5 - 5.0: Expert Level
- Ready for production deployment
- Can mentor others
- Capable of designing complex hook architectures
- Can contribute to community resources

**Recommended Next Steps:**
- Deploy hooks to production projects
- Share knowledge with team members
- Contribute to open-source hook examples
- Explore advanced integration patterns

---

### 4.0 - 4.4: Proficient Level
- Ready for supervised production use
- Strong understanding of core concepts
- Can implement most hook patterns
- May need guidance on edge cases

**Recommended Next Steps:**
- Practice advanced patterns (monorepo, MCP tools)
- Deploy hooks with peer review
- Study production case studies in detail
- Focus on performance optimization

---

### 3.5 - 3.9: Competent Level
- Can implement basic hooks independently
- Understands fundamental concepts
- Needs more practice with advanced patterns
- Should work with supervision initially

**Recommended Next Steps:**
- Complete all practical exercises again
- Build personal hook library
- Review security modules thoroughly
- Seek feedback on implementations

---

### 3.0 - 3.4: Basic Understanding
- Grasps fundamental concepts
- Can follow examples but struggles with novel scenarios
- Needs more hands-on practice
- Should not deploy to production alone

**Recommended Next Steps:**
- Revisit modules with low scores
- Complete additional practice exercises
- Work through Infrastructure Showcase examples
- Seek mentorship or additional training

---

### Below 3.0: Foundational Learning Needed
- Should revisit training materials
- Needs significant additional practice
- Not ready for independent hook development
- Consider repeating relevant modules

**Recommended Next Steps:**
- Retake training modules with low scores
- Focus on fundamentals first
- Work through examples step-by-step
- Schedule review session with instructor or mentor

---

## Practical Competency Verification

In addition to the self-assessment ratings, verify your practical skills:

### Practical Task 1: Basic Hook Creation
**Task:** Create a PreToolUse hook that blocks Bash commands containing "rm -rf".

**Completion Criteria:**
- [ ] Hook correctly configured in settings.json
- [ ] Python script properly reads JSON input
- [ ] Hook blocks dangerous commands
- [ ] Hook allows safe commands
- [ ] Proper error messages to stderr
- [ ] Exit code 2 used for blocking

**Status:** [ ] Completed successfully  [ ] Needs more practice

---

### Practical Task 2: Auto-Formatting Integration
**Task:** Create a PostToolUse hook that runs Prettier on edited TypeScript files.

**Completion Criteria:**
- [ ] Hook triggers only for Edit/Write tools
- [ ] File type detection works correctly
- [ ] Prettier executes successfully
- [ ] Hook handles formatter errors gracefully
- [ ] No unnecessary permission prompts

**Status:** [ ] Completed successfully  [ ] Needs more practice

---

### Practical Task 3: Sensitive File Protection
**Task:** Create a comprehensive file protection hook for .env, credentials, and secrets.

**Completion Criteria:**
- [ ] Protects all sensitive file patterns
- [ ] Works for Write, Edit, and Bash tools
- [ ] Clear error messages
- [ ] Audit logging implemented
- [ ] No false positives on safe files
- [ ] Security review passed

**Status:** [ ] Completed successfully  [ ] Needs more practice

---

### Practical Task 4: Session Management
**Task:** Create SessionStart and SessionEnd hooks for environment setup and cleanup.

**Completion Criteria:**
- [ ] SessionStart loads correct environment
- [ ] CLAUDE_ENV_FILE used correctly
- [ ] SessionEnd performs cleanup
- [ ] Statistics logged
- [ ] Works across multiple sessions

**Status:** [ ] Completed successfully  [ ] Needs more practice

---

### Practical Task 5: Skill Auto-Activation
**Task:** Implement skill auto-activation using UserPromptSubmit and skill-rules.json.

**Completion Criteria:**
- [ ] skill-rules.json configured correctly
- [ ] UserPromptSubmit hook checks rules
- [ ] Skills suggested based on patterns
- [ ] No false activations
- [ ] Performance acceptable (< 500ms)

**Status:** [ ] Completed successfully  [ ] Needs more practice

---

## Knowledge Gaps Identification

For each section where you scored below 4.0, identify specific knowledge gaps:

### Section 1 Gaps:
_List specific topics you need to review:_
-
-
-

### Section 2 Gaps:
_List specific topics you need to review:_
-
-
-

### Section 3 Gaps:
_List specific topics you need to review:_
-
-
-

### Section 4 Gaps:
_List specific topics you need to review:_
-
-
-

### Section 5 Gaps:
_List specific topics you need to review:_
-
-
-

---

## Action Plan

Based on your assessment results, create a personalized action plan:

### Immediate Actions (This Week):
1.
2.
3.

### Short-Term Goals (Next 2 Weeks):
1.
2.
3.

### Long-Term Goals (Next Month):
1.
2.
3.

---

## Certification Readiness

To be considered certification-ready, you must meet ALL criteria:

- [ ] Average score of 4.0 or higher across all sections
- [ ] No individual section below 3.5
- [ ] All 5 practical tasks completed successfully
- [ ] Security checklist review completed
- [ ] Quiz score of 80% or higher (see quiz.md)
- [ ] At least one production hook deployed (or equivalent project)
- [ ] Documented understanding of UK Gov and NCSC principles

**Certification Ready?** [ ] Yes  [ ] Not Yet

**Target Completion Date:** _______________

---

## Feedback and Reflection

### What aspects of hook development do you find most challenging?


### What topics would you like more training on?


### How confident do you feel deploying hooks to production?


### Additional comments or questions:


---

## Reassessment Schedule

If your score is below certification level, plan to reassess:

- **Score 3.0-3.4:** Reassess in 2 weeks after additional practice
- **Score 3.5-3.9:** Reassess in 1 week after focused study
- **Score 4.0+:** Proceed to quiz and final assessment

**Reassessment Date:** _______________

---

## Mentor/Instructor Review (If Applicable)

**Reviewed by:** _______________
**Date:** _______________
**Comments:**


**Recommendations:**


**Approved for Certification:** [ ] Yes  [ ] No  [ ] Conditional

---

**Self-Assessment Version:** 1.0
**Last Updated:** 2025-12-10
**Next Review:** Quarterly or upon training updates

---

*This self-assessment aligns with UK Government Secure by Design for AI and NCSC Secure Design Principles.*
