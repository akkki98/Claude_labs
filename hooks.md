# Lab: Automating Development Workflows with Hooks in Claude Code

## Lab Overview

Claude Code Hooks allow you to automatically execute custom commands or scripts during different stages of Claude's execution lifecycle. Hooks enable teams to automate repetitive tasks, enforce coding standards, improve security, and integrate development tools without requiring manual intervention.

In this lab, you will configure project-level Hooks to automatically run validations, formatting, testing, and security checks based on Claude Code events.

---

# Lab Objectives

By the end of this lab, you will be able to:

- Understand the Claude Code Hook lifecycle
- Configure project-level Hooks
- Create PreToolUse Hooks
- Create PostToolUse Hooks
- Handle tool execution failures
- Process batch tool executions
- Respond to permission-denied events
- Automate code quality checks
- Enforce development guardrails

---

# Lab Scenario

Your organization has adopted Claude Code for software development. To ensure consistent quality and security, the engineering team wants every Claude Code session to automatically:

- Validate commands before execution
- Run linting after code changes
- Execute unit tests
- Handle failures gracefully
- Log denied operations
- Notify developers when automation completes

You will implement these automations using Claude Code Hooks.

---

# Estimated Duration

**60 Minutes**

---

# Prerequisites

Before starting this lab, ensure you have:

- Claude Code installed
- Git installed
- Node.js installed
- Visual Studio Code (recommended)
- A sample Git repository
- Basic knowledge of JSON
- Basic shell scripting knowledge

---

# Lab Architecture

```text
Project
│
├── .claude
│   └── settings.json
│
├── scripts
│   ├── lint.sh
│   ├── format.sh
│   ├── security-check.sh
│   ├── notify.sh
│   ├── error-handler.sh
│   └── permission-log.sh
│
├── src
└── package.json
```

---

# Exercise 1 - Understanding the Hook Lifecycle

## Objective

Understand when Claude Code executes Hooks during its workflow.

### Claude Code Hook Lifecycle

| Lifecycle Event | When It Runs | Typical Use Cases |
|-----------------|--------------|-------------------|
| **PreToolUse** | Before a tool is executed | Validate commands, enforce security policies, block dangerous operations |
| **PostToolUse** | After a tool successfully completes | Run formatters, lint code, execute tests, update documentation |
| **PostToolUseFailure** | After a tool execution fails | Log errors, notify developers, capture diagnostics, perform cleanup |
| **PostToolBatch** | After a batch of tool calls completes | Generate summary reports, run integration tests, execute post-processing tasks |
| **PermissionDenied** | After Claude's Auto Mode denies a tool call | Log denied requests, notify users, trigger approval workflows |

### Hook Lifecycle Flow

```text
User Request
      │
      ▼
PreToolUse
      │
      ▼
Claude Executes Tool
      │
      ├─────────────── Success ───────────────┐
      │                                       │
      ▼                                       ▼
PostToolUse                          PostToolUseFailure
      │                                       │
      └───────────────┬───────────────────────┘
                      ▼
             PostToolBatch
                      │
                      ▼
      (If a tool call is denied)
                      │
                      ▼
            PermissionDenied
```

### Expected Outcome

Understand the purpose of each Hook lifecycle event and when it should be used.

---

# Exercise 2 - Configure Project Hooks

## Objective

Create a project-level Hook configuration.

### Step 1

Create the following directory structure:

```text
.claude/
    settings.json
```

### Step 2

Add the following Hook configuration:

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|Write",
        "hooks": [
          {
            "type": "command",
            "command": "./scripts/lint.sh"
          }
        ]
      }
    ]
  }
}
```

### Expected Outcome

Claude automatically executes the configured script after modifying files.

---

# Exercise 3 - Configure a PreToolUse Hook

## Objective

Prevent unsafe commands before execution.

### Create

```text
scripts/security-check.sh
```

Example validations:

- Block `rm -rf`
- Block `git push --force`
- Block `sudo rm`
- Block accidental production file deletion

Configure the Hook to execute before every Bash tool invocation.

### Expected Outcome

Unsafe operations are stopped before execution.

---

# Exercise 4 - Configure a PostToolUse Hook

## Objective

Automatically validate source code after Claude edits files.

Example tasks:

- Run ESLint
- Execute Prettier
- Verify formatting
- Run static analysis

Sample command:

```bash
npm run lint
```

### Test

Ask Claude:

> Refactor the authentication service.

Observe the Hook executing automatically.

---

# Exercise 5 - Configure a PostToolUseFailure Hook

## Objective

Handle tool execution failures.

Create:

```text
scripts/error-handler.sh
```

Example actions:

- Log the failed command
- Capture the error output
- Write diagnostics to a log file
- Notify the developer

Example log:

```text
Timestamp : 2026-08-05 11:25
Tool      : Bash
Status    : Failed
Reason    : npm test exited with code 1
```

### Expected Outcome

Failures are automatically captured for troubleshooting.

---

# Exercise 6 - Configure a PostToolBatch Hook

## Objective

Run automation after multiple tool calls complete.

Example scenario:

Claude:

- edits several files
- formats code
- executes tests

Instead of running another validation after every tool call, use **PostToolBatch** to execute once after all operations complete.

Possible actions:

- Generate a summary report
- Run integration tests
- Create a build summary
- Display execution statistics

Example output:

```text
Batch Complete

Files Modified : 12
Tests Passed   : 84
Lint Errors    : 0
Duration        : 18 seconds
```

### Expected Outcome

A single automation executes after all related tool operations finish.

---

# Exercise 7 - Configure a PermissionDenied Hook

## Objective

Respond when Claude's Auto Mode denies a tool request.

Create:

```text
scripts/permission-log.sh
```

Example actions:

- Log denied requests
- Notify the user
- Create an audit trail
- Trigger an approval workflow

Example log:

```text
Permission Denied

Tool : Bash
Reason : Dangerous command detected
Time : 11:45 AM
```

### Expected Outcome

Permission denials are recorded for auditing and review.

---

# Exercise 8 - Build a Complete Automation Pipeline

Configure Hooks for the following workflow:

1. Validate commands before execution.
2. Automatically format modified files.
3. Run linting.
4. Execute unit tests.
5. Log any failures.
6. Generate a batch summary.
7. Record permission-denied events.

Ask Claude:

> Refactor the authentication module and improve code quality.

Observe each Hook executing automatically during the workflow.

---

# Best Practices

- Keep Hook scripts lightweight and fast.
- Use **PreToolUse** for validation and security.
- Use **PostToolUse** for formatting, linting, and testing.
- Use **PostToolUseFailure** for diagnostics and recovery.
- Use **PostToolBatch** for expensive operations that should run once.
- Use **PermissionDenied** for auditing denied requests.
- Store project Hooks in `.claude/settings.json`.
- Test scripts independently before integrating them into Hooks.

---

# Knowledge Check

1. When is a **PreToolUse** Hook executed?
2. What is the purpose of **PostToolUse**?
3. When would you use **PostToolUseFailure**?
4. Why is **PostToolBatch** more efficient than running the same script after every tool call?
5. What information should be captured by a **PermissionDenied** Hook?
6. Which Hook is best for running automated tests?
7. Which Hook should block dangerous commands?
8. Where are project-level Hooks configured?

---

# Summary

In this lab, you learned how to configure Claude Code Hooks across the complete tool execution lifecycle. You implemented Hooks to validate commands before execution, automate formatting and testing after successful tool usage, capture failures for troubleshooting, perform batch-level processing, and audit permission-denied events. These capabilities help teams build secure, automated, and consistent AI-assisted development workflows.
