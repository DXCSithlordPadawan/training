# Claude Code Hooks Training - Knowledge Quiz

**Purpose:** Test your understanding of Claude Code hooks concepts, implementation, and best practices.

**Instructions:**
- Answer all 50 questions
- Passing score: 40/50 (80%)
- Time limit: 90 minutes (recommended)
- Open book: You may reference documentation
- Show your work for coding questions

---

## Part 1: Multiple Choice (20 questions, 1 point each)

### Question 1
What is the primary purpose of Claude Code hooks?

A) To replace Claude's decision-making entirely
B) To provide deterministic control over Claude Code's behavior
C) To make Claude Code run faster
D) To store conversation history

**Answer:** B

**Explanation:** Hooks provide deterministic, programmatic control over Claude's behavior at various lifecycle points, ensuring certain actions always happen rather than relying on the LLM to choose.

---

### Question 2
Which exit code should a hook script use to BLOCK a tool execution?

A) Exit 0
B) Exit 1
C) Exit 2
D) Exit 3

**Answer:** C

**Explanation:** Exit 2 indicates a blocking error. Only stderr is shown, and the tool call is prevented. Exit 0 is success, and other exit codes are non-blocking errors.

---

### Question 3
Where is CLAUDE_PROJECT_DIR available?

A) Only in prompt-based hooks
B) Only in command-based hooks
C) In both command and prompt-based hooks
D) Only in SessionStart hooks

**Answer:** B

**Explanation:** CLAUDE_PROJECT_DIR is available in command-based hooks only, not in prompt-based hooks.

---

### Question 4
What is the default timeout for hook execution?

A) 30 seconds
B) 60 seconds
C) 120 seconds
D) No timeout

**Answer:** B

**Explanation:** The default timeout is 60 seconds, but it can be configured per hook using the "timeout" field.

---

### Question 5
Which hook event fires when a user submits a prompt?

A) PreToolUse
B) PromptSubmit
C) UserPromptSubmit
D) SessionStart

**Answer:** C

**Explanation:** UserPromptSubmit fires when the user submits a prompt, before Claude processes it.

---

### Question 6
What matcher pattern matches ALL tools?

A) "all"
B) "*" or ""
C) ".*"
D) "any"

**Answer:** B

**Explanation:** Both "*" and "" (empty string) act as wildcards matching all tools.

---

### Question 7
Which hook event CANNOT block execution?

A) PreToolUse
B) PostToolUse
C) Notification
D) Stop

**Answer:** C

**Explanation:** Notification hooks are non-blocking by design - they're for alerts and logging only.

---

### Question 8
What is the correct way to quote a path with CLAUDE_PROJECT_DIR in a hook command?

A) $CLAUDE_PROJECT_DIR/script.sh
B) "$CLAUDE_PROJECT_DIR/script.sh"
C) "\"$CLAUDE_PROJECT_DIR\"/script.sh"
D) '$CLAUDE_PROJECT_DIR/script.sh'

**Answer:** C

**Explanation:** Proper quoting requires both escaping inner quotes and quoting the variable: "\"$CLAUDE_PROJECT_DIR\"/script.sh"

---

### Question 9
Which settings file has the HIGHEST priority?

A) ~/.claude/settings.json
B) .claude/settings.json
C) .claude/settings.local.json
D) Enterprise policy settings

**Answer:** C

**Explanation:** Priority order (highest to lowest): .claude/settings.local.json, .claude/settings.json, ~/.claude/settings.json, enterprise policy.

---

### Question 10
What is the purpose of suppressOutput in hook responses?

A) Delete the tool output
B) Hide hook execution details from transcript
C) Prevent tool from running
D) Disable logging

**Answer:** B

**Explanation:** suppressOutput hides the hook's stdout output from the transcript, useful for auto-approval hooks that don't need visible feedback.

---

### Question 11
Which hook type uses natural language logic for decisions?

A) Command-based hooks
B) Prompt-based hooks
C) Script hooks
D) Function hooks

**Answer:** B

**Explanation:** Prompt-based hooks use LLM evaluation with natural language logic, while command-based hooks execute shell scripts.

---

### Question 12
What does the permissionDecision "ask" mean?

A) Auto-approve the operation
B) Block the operation
C) Show permission dialog to user
D) Log the decision

**Answer:** C

**Explanation:** "ask" displays a permission dialog to the user, letting them decide whether to approve or deny.

---

### Question 13
Which tool names require the "mcp__" prefix?

A) Core Claude Code tools
B) Custom user tools
C) MCP server tools
D) Python tools

**Answer:** C

**Explanation:** MCP (Model Context Protocol) server tools use the naming pattern: mcp__<server>__<tool>

---

### Question 14
What is the primary security risk of hooks?

A) They slow down Claude Code
B) They run with your full user credentials
C) They consume too much memory
D) They require internet access

**Answer:** B

**Explanation:** Hooks execute with full user credentials and can perform any action you can, making malicious hooks extremely dangerous.

---

### Question 15
Which NCSC principle emphasizes "deny by default"?

A) Know your system
B) Protect your supply chain
C) Control access
D) Secure by default

**Answer:** D

**Explanation:** "Secure by default" from UK Gov Secure by Design includes denying by default and requiring explicit allow lists.

---

### Question 16
What file should be used for team-shared hook configurations?

A) .claude/settings.local.json
B) .claude/settings.json
C) ~/.claude/settings.json
D) /etc/claude/settings.json

**Answer:** B

**Explanation:** .claude/settings.json should be committed to version control for team sharing, while .local.json is for personal configurations.

---

### Question 17
Which hook event is best for auto-formatting code after edits?

A) PreToolUse
B) PostToolUse
C) Stop
D) SessionEnd

**Answer:** B

**Explanation:** PostToolUse fires after tool execution, making it ideal for formatting code after Write/Edit operations.

---

### Question 18
What does CLAUDE_ENV_FILE enable?

A) Reading environment variables
B) Persisting environment variables across session
C) Deleting environment variables
D) Encrypting environment variables

**Answer:** B

**Explanation:** CLAUDE_ENV_FILE (available in SessionStart) allows writing exports that persist throughout the session.

---

### Question 19
Which validation should ALWAYS be performed on file paths in hooks?

A) File size check
B) Path traversal check (e.g., "..")
C) File extension check
D) Modified date check

**Answer:** B

**Explanation:** Path traversal vulnerabilities (e.g., "../../../../etc/passwd") are critical security risks that must always be checked.

---

### Question 20
What is the skill-rules.json file used for?

A) Defining hook permissions
B) Configuring skill auto-activation patterns
C) Storing skill credentials
D) Logging skill usage

**Answer:** B

**Explanation:** skill-rules.json defines patterns (file paths, keywords) that trigger automatic skill suggestions via UserPromptSubmit hooks.

---

## Part 2: True/False (10 questions, 1 point each)

### Question 21
PostToolUse hooks can modify the output of a tool before Claude sees it.

**Answer:** True

**Explanation:** PostToolUse hooks can add additionalContext to provide feedback or modify what Claude receives.

---

### Question 22
Hooks must be written in Python.

**Answer:** False

**Explanation:** Hooks can be any executable command - shell scripts, Python, Ruby, compiled binaries, etc.

---

### Question 23
A hook with exit code 1 will block tool execution.

**Answer:** False

**Explanation:** Only exit code 2 blocks execution. Exit 1 (or other non-zero, non-2 codes) is a non-blocking error.

---

### Question 24
PreToolUse hooks can modify tool inputs using the updatedInput field.

**Answer:** True

**Explanation:** The updatedInput field in hook responses allows modifying tool parameters before execution.

---

### Question 25
Prompt-based hooks are faster than command-based hooks.

**Answer:** False

**Explanation:** Prompt-based hooks are slower because they require API calls to the LLM, while command-based hooks execute locally.

---

### Question 26
The Infrastructure Showcase demonstrates 6 production hook examples.

**Answer:** True

**Explanation:** The repository showcases: skill-activation-prompt, post-tool-use-tracker, tsc-check, trigger-build-resolver, error-handling-reminder, stop-build-check-enhanced.

---

### Question 27
SessionEnd hooks can prevent Claude Code from exiting.

**Answer:** False

**Explanation:** SessionEnd hooks are non-blocking and cannot prevent session termination.

---

### Question 28
Matcher patterns support full regex syntax.

**Answer:** True

**Explanation:** Matchers support regex patterns like "Edit|Write", "Notebook.*", etc.

---

### Question 29
Hooks are evaluated in parallel when multiple matchers match.

**Answer:** True

**Explanation:** When multiple hooks match an event, they run in parallel (unless they're identical, which triggers deduplication).

---

### Question 30
The 500-line rule for skills also applies to hooks.

**Answer:** False

**Explanation:** The 500-line modular pattern applies to skills for context management, not to hooks which are external scripts.

---

## Part 3: Fill in the Blank (10 questions, 1 point each)

### Question 31
The hook event that fires after a tool completes is called _____________.

**Answer:** PostToolUse

---

### Question 32
To auto-approve a tool call in a PreToolUse hook, set permissionDecision to _____________.

**Answer:** allow (or "allow")

---

### Question 33
The environment variable containing the project root path is _____________.

**Answer:** CLAUDE_PROJECT_DIR

---

### Question 34
A hook should exit with code _____________ to block a tool execution.

**Answer:** 2

---

### Question 35
The three possible permission decisions are allow, deny, and _____________.

**Answer:** ask

---

### Question 36
Hooks for MCP tools use the naming pattern _____________.

**Answer:** mcp__<server>__<tool> (or mcp__*__* or similar valid answer)

---

### Question 37
The JSON field that contains tool-specific parameters in PreToolUse input is _____________.

**Answer:** tool_input

---

### Question 38
The hook type that uses LLM evaluation instead of scripts is called _____________.

**Answer:** prompt-based (or "prompt")

---

### Question 39
To hide hook output from the transcript, set _____________ to true.

**Answer:** suppressOutput

---

### Question 40
The file used for skill auto-activation configuration is _____________.

**Answer:** skill-rules.json

---

## Part 4: Short Answer (5 questions, 2 points each)

### Question 41
List three sensitive file patterns that should be protected by hooks.

**Answer (any 3 of the following):**
- .env
- .git/ (or .git/config)
- secrets.json (or any secrets file)
- credentials.yaml (or credentials file)
- id_rsa (or SSH keys)
- .aws/credentials
- package-lock.json (or dependency locks)

---

### Question 42
Explain the difference between PreToolUse and PermissionRequest hooks.

**Answer:**
PreToolUse fires before ANY tool execution and is used for validation, modification, and complex logic. PermissionRequest fires specifically when a permission dialog would be shown to the user, and is best for auto-approving known-safe operations to streamline workflow. PreToolUse is always-on validation, while PermissionRequest is for bypassing dialogs.

---

### Question 43
Name four of the ten hook event types.

**Answer (any 4 of the following):**
- PreToolUse
- PostToolUse
- PermissionRequest
- UserPromptSubmit
- Stop
- SubagentStop
- Notification
- SessionStart
- SessionEnd
- PreCompact

---

### Question 44
What are two advantages of command-based hooks over prompt-based hooks?

**Answer (any 2):**
- Faster execution (no API calls required)
- No token cost
- Deterministic/predictable behavior
- Can run offline
- Lower latency
- More precise control

---

### Question 45
List two UK Gov or NCSC security principles applicable to hooks.

**Answer (any 2):**
- Secure by default (deny by default, explicit allows)
- Principle of least privilege
- Defense in depth
- Fail securely
- Know your system
- Protect your supply chain
- Auditability

---

## Part 5: Code Analysis (3 questions, 5 points each)

### Question 46
Identify the security vulnerability in this hook code:

```python
import json, sys, os
input_data = json.load(sys.stdin)
file_path = input_data['tool_input']['file_path']
os.system(f"cat {file_path}")
```

**Answer:**
**Vulnerabilities:**
1. **Command injection:** file_path is not quoted, allowing shell injection with filenames containing spaces or special characters
2. **No path validation:** Missing checks for path traversal (../) or absolute paths
3. **No error handling:** Will crash if tool_input or file_path keys don't exist
4. **Using os.system:** Should use subprocess with proper argument passing
5. **No sensitive file checks:** Doesn't block access to .env, credentials, etc.

**Secure version:**
```python
import json, sys, subprocess
try:
    input_data = json.load(sys.stdin)
    file_path = input_data.get('tool_input', {}).get('file_path', '')

    # Validate path
    if '..' in file_path or not file_path:
        print("Invalid path", file=sys.stderr)
        sys.exit(2)

    # Use subprocess securely
    subprocess.run(['cat', file_path], check=True)
except Exception as e:
    print(f"Error: {e}", file=sys.stderr)
    sys.exit(1)
```

---

### Question 47
Complete this hook configuration to auto-approve Read operations on .md files:

```json
{
  "hooks": {
    "____________": [
      {
        "matcher": "____________",
        "hooks": [
          {
            "type": "command",
            "command": "____________"
          }
        ]
      }
    ]
  }
}
```

**Answer:**
```json
{
  "hooks": {
    "PermissionRequest": [
      {
        "matcher": "Read",
        "hooks": [
          {
            "type": "command",
            "command": "python3 -c \"import json,sys;d=json.load(sys.stdin);fp=d.get('tool_input',{}).get('file_path','');print(json.dumps({'hookSpecificOutput':{'hookEventName':'PermissionRequest','permissionDecision':'allow','permissionDecisionReason':'Markdown file'},'suppressOutput':True})) if fp.endswith('.md') else None;sys.exit(0)\""
          }
        ]
      }
    ]
  }
}
```

**Alternative (using external script):**
```json
{
  "hooks": {
    "PermissionRequest": [
      {
        "matcher": "Read",
        "hooks": [
          {
            "type": "command",
            "command": "\"$CLAUDE_PROJECT_DIR\"/.claude/hooks/auto-approve-md.py"
          }
        ]
      }
    ]
  }
}
```

---

### Question 48
Write a complete PreToolUse hook (in Python) that blocks Bash commands containing "rm -rf /".

**Answer:**

```python
#!/usr/bin/env python3
"""Block dangerous rm commands."""
import json
import sys

def main():
    # Load input safely
    try:
        input_data = json.load(sys.stdin)
    except json.JSONDecodeError as e:
        print(f"JSON error: {e}", file=sys.stderr)
        sys.exit(1)

    # Only check Bash tools
    tool_name = input_data.get('tool_name', '')
    if tool_name != 'Bash':
        sys.exit(0)

    # Get command
    command = input_data.get('tool_input', {}).get('command', '')

    # Check for dangerous pattern
    if 'rm' in command and '-rf' in command and ('/' in command or ' /' in command):
        # Check specifically for root deletion
        import re
        if re.search(r'rm\s+.*-rf\s+/(?!\w)', command) or re.search(r'rm\s+-rf\s+/(?!\w)', command):
            print("BLOCKED: Dangerous rm command targeting root filesystem", file=sys.stderr)
            sys.exit(2)  # Block execution

    # Allow safe commands
    sys.exit(0)

if __name__ == '__main__':
    main()
```

**Configuration:**
```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Bash",
        "hooks": [
          {
            "type": "command",
            "command": "\"$CLAUDE_PROJECT_DIR\"/.claude/hooks/block-rm-rf.py",
            "timeout": 5
          }
        ]
      }
    ]
  }
}
```

---

## Bonus Questions (Optional, 5 points total)

### Bonus Question 1 (3 points)
Explain the "progressive disclosure" pattern for skills and how hooks support it through skill-rules.json auto-activation.

**Answer:**
Progressive disclosure is a pattern where skills are split into:
1. A main SKILL.md file (< 500 lines) with overview and basic instructions
2. Resource files in subdirectories with detailed information

This prevents context window saturation by loading only relevant content. Hooks support this through:
- skill-rules.json defines activation patterns (file paths, keywords, context)
- UserPromptSubmit hook checks rules against user input
- When patterns match, hook suggests the skill to Claude
- Skill activates automatically without manual invocation
- Only necessary content loaded into context

This solves the problem: "skills don't activate automatically" by making them contextually responsive through hook-based rule matching.

---

### Bonus Question 2 (2 points)
Describe the monorepo TypeScript validation pattern (tsc-check.sh) from the Infrastructure Showcase.

**Answer:**
The tsc-check.sh hook is a Stop event hook that:
1. Runs TypeScript compiler (tsc --noEmit) across all packages
2. Checks for type errors after Claude makes changes
3. Blocks Claude from stopping if type errors exist
4. Forces Claude to fix errors before completing task
5. Works across multiple packages in monorepo structure
6. Provides guardrail ensuring type safety

This pattern ensures Claude doesn't leave TypeScript projects in a broken state, enforcing compilation success as a requirement for task completion.

---

## Answer Key Summary

### Part 1 (Multiple Choice): 20 points
1. B  2. C  3. B  4. B  5. C
6. B  7. C  8. C  9. C  10. B
11. B  12. C  13. C  14. B  15. D
16. B  17. B  18. B  19. B  20. B

### Part 2 (True/False): 10 points
21. True  22. False  23. False  24. True  25. False
26. True  27. False  28. True  29. True  30. False

### Part 3 (Fill in the Blank): 10 points
31. PostToolUse
32. allow
33. CLAUDE_PROJECT_DIR
34. 2
35. ask
36. mcp__<server>__<tool>
37. tool_input
38. prompt-based
39. suppressOutput
40. skill-rules.json

### Part 4 (Short Answer): 10 points (2 each)
41-45. See detailed answers above

### Part 5 (Code Analysis): 15 points (5 each)
46-48. See detailed answers above

### Bonus: 5 points
See detailed answers above

---

## Scoring Guide

**Total Possible:** 55 points (50 regular + 5 bonus)

**Passing Score:** 40/50 (80%) - Bonus points can help but aren't required

**Grade Scale:**
- **45-50 (90-100%):** Excellent - Deep understanding, ready for advanced topics
- **40-44 (80-89%):** Good - Solid understanding, ready for production use with review
- **35-39 (70-79%):** Fair - Basic understanding, needs more practice
- **30-34 (60-69%):** Poor - Significant gaps, revisit training materials
- **Below 30 (<60%):** Insufficient - Repeat training modules

---

## Score Breakdown by Topic

Calculate your score in each area:

**Hook Fundamentals (Q1-5, Q21-25, Q31-35):** _____ / 20

**PreToolUse/PermissionRequest (Q6-10, Q41-42, Q46-47):** _____ / 14

**Other Hook Types (Q11-15, Q43-44):** _____ / 8

**Security & Compliance (Q16-20, Q26-30):** _____ / 13

**Practical Implementation (Q36-40, Q45, Q48):** _____ / 10

**Bonus/Advanced (Bonus Q1-2):** _____ / 5

---

## Review Recommendations

Based on your score in each area:

### If you scored below 70% in Hook Fundamentals:
- Review Day 1 modules (1.1-1.4)
- Practice basic hook configuration
- Study exit codes and lifecycle

### If you scored below 70% in PreToolUse/PermissionRequest:
- Review Day 2 modules (2.1-2.3)
- Complete practical exercises for validation hooks
- Practice JSON input/output handling

### If you scored below 70% in Other Hook Types:
- Review Days 3-5 modules
- Practice PostToolUse, Stop, Session hooks
- Study prompt-based vs command-based differences

### If you scored below 70% in Security:
- **CRITICAL:** Review Day 7 security modules thoroughly
- Complete security checklist
- Study NCSC and UK Gov principles
- Do NOT deploy hooks to production

### If you scored below 70% in Practical Implementation:
- More hands-on coding practice needed
- Work through Infrastructure Showcase examples
- Build personal hook library
- Seek code review from experienced developer

---

## Certification Eligibility

To be eligible for certification, you must:

- [ ] Score 40/50 or higher (80%)
- [ ] Score at least 70% in EACH topic area
- [ ] Complete all 5 practical tasks in selfassessment.md
- [ ] Pass security module review
- [ ] Have deployed at least one production-ready hook

**Quiz Score:** _____ / 50 (____ %)

**Eligible for Certification:** [ ] Yes  [ ] No

**Areas Needing Improvement:**


---

## Retake Policy

If you did not pass:
- Study areas where you scored below 70%
- Complete additional practical exercises
- Review relevant lesson modules
- Retake quiz after 1 week minimum
- Maximum 3 attempts allowed

**Retake Scheduled:** _______________

---

**Quiz Version:** 1.0
**Last Updated:** 2025-12-10
**Next Review:** Quarterly or upon major Claude Code updates

---

*This quiz aligns with UK Government Secure by Design for AI and NCSC Secure Design Principles.*
