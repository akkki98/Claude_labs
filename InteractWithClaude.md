# Lab: Interacting with Claude Code and Refactoring a Spring Boot Application

## Lab Overview

**Duration:** 45 minutes

**Repository**

```text
https://github.com/akkki98/springcopilot.git
```

---

# Learning Objectives

By the end of this lab you will be able to:

- Interact effectively with Claude Code
- Understand the different editing modes
- Choose the appropriate mode for different tasks
- Analyze an existing codebase
- Refactor Java Spring Boot applications
- Generate documentation
- Improve code quality using AI

---


# Lab Setup

```bash
git clone https://github.com/akkki98/springcopilot.git

cd springcopilot

claude .
```

---

# Understanding Claude Code Modes

Before starting, familiarize yourself with the available interaction modes.

| Mode | Best Used For | Makes Changes? |
|--------|--------------|----------------|
| **Manual** | Reviewing every proposed change before applying it | Yes (after approval) |
| **Edit Automatically** | Refactoring a selected class or file with minimal interruption | Yes |
| **Plan** | Exploring the codebase, understanding architecture, and creating implementation plans before editing | No (planning only) |
| **Auto** | Multi-file refactoring and repetitive updates where low-risk edits can be applied automatically | Yes (automatically approves safe actions) |

> **Recommendation:** Always start with **Plan Mode** to understand the codebase before modifying it.

---

# Exercise 1 — Explore the Repository

## Recommended Mode

✅ **Plan**

## Objective

Understand the project before making changes.

### Prompt

```text
Analyze this Spring Boot application.

Explain:

- Architecture
- Folder structure
- Technology stack
- Important modules
- Build process
- Dependencies

Recommend the order in which I should understand this project.
```

---

# Exercise 2 — Understand the Application Flow

## Recommended Mode

✅ **Plan**

### Prompt

```text
Trace the execution flow of a REST request.

Explain:

Client

↓

Controller

↓

Service

↓

Repository

↓

Database

Identify every class involved.
```

---

# Exercise 3 — Generate Project Documentation

## Recommended Mode

✅ **Plan**

### Prompt

```text
Generate PROJECT_OVERVIEW.md.

Include:

- Application overview
- Folder structure
- Major components
- Technologies
- Important classes
```

---

# Exercise 4 — Review Code Quality

## Recommended Mode

✅ **Plan**

### Prompt

```text
Review this repository.

Identify:

- Code smells
- Technical debt
- Duplicate code
- Dead code
- Long methods
- Large classes

Rank findings from High to Low priority.
```

---

# Exercise 5 — Create a Refactoring Plan

## Recommended Mode

✅ **Plan**

### Prompt

```text
Create a refactoring plan.

Include:

- Files to refactor
- Why they need refactoring
- Expected improvements
- Risks
- Recommended order
```

---

# Exercise 6 — Refactor a Service Class

## Recommended Mode

✅ **Edit Automatically**

### Prompt

```text
Refactor this service class.

Apply:

- SOLID principles
- Constructor Injection
- Better naming
- Improved exception handling
- Remove duplicate code
- Improve readability

Explain each change.
```

---

# Exercise 7 — Refactor a Controller

## Recommended Mode

✅ **Edit Automatically**

### Prompt

```text
Improve this REST controller.

Focus on:

- Validation
- HTTP status codes
- ResponseEntity usage
- Exception handling
- Logging
- Clean Code practices
```

---

# Exercise 8 — Refactor Repository Layer

## Recommended Mode

✅ **Edit Automatically**

### Prompt

```text
Review this repository class.

Improve:

- Query performance
- Repository methods
- Pagination
- Naming
- Readability

Apply changes directly.
```

---

# Exercise 9 — Improve Exception Handling

## Recommended Mode

✅ **Manual**

### Why?

Exception handling often affects application behavior and should be reviewed carefully.

### Prompt

```text
Create:

- Global Exception Handler
- Custom Exceptions
- Standard Error Response

Show the changes before applying them.
```

---

# Exercise 10 — Improve Logging

## Recommended Mode

✅ **Manual**

### Prompt

```text
Improve logging.

Use:

- SLF4J
- Appropriate log levels
- Structured logging

Show proposed edits before modifying files.
```

---

# Exercise 11 — Multi-file Refactoring

## Recommended Mode

✅ **Auto**

### Objective

Apply safe refactoring across the project.

### Prompt

```text
Across the entire project:

- Remove unused imports
- Remove duplicate code
- Improve naming
- Apply constructor injection
- Format code consistently
- Remove commented code

Pause only if a risky change is required.
```

---

# Exercise 12 — Modernize Java Code

## Recommended Mode

✅ **Auto**

### Prompt

```text
Modernize this project using Java 17 best practices.

Apply:

- var where appropriate
- Switch expressions
- Optional improvements
- Better Stream API usage
- Records where applicable

Automatically apply safe improvements.
```

---

# Exercise 13 — Generate Documentation

## Recommended Mode

✅ **Plan**

### Prompt

```text
Generate:

- ARCHITECTURE.md
- REFACTORING_GUIDE.md
- TECHNICAL_DEBT.md
- ONBOARDING_GUIDE.md
```

---

# Exercise 14 — Final Code Review

## Recommended Mode

✅ **Manual**

### Prompt

```text
Review every modification made during this lab.

Summarize:

- Files modified
- Improvements made
- Remaining technical debt
- Suggested next steps

Do not make further changes.
```

---

# Challenge Lab

Use all four Claude Code modes appropriately:

| Task | Recommended Mode |
|------|-------------------|
| Understand the application | Plan |
| Generate documentation | Plan |
| Refactor one controller | Edit Automatically |
| Refactor one service | Edit Automatically |
| Improve exception handling | Manual |
| Improve logging | Manual |
| Clean the entire repository | Auto |
| Modernize Java code | Auto |

---

# Deliverables

Generate the following Markdown files:

- PROJECT_OVERVIEW.md
- ARCHITECTURE.md
- CODE_REVIEW.md
- TECHNICAL_DEBT.md
- REFACTORING_GUIDE.md
- TESTING_GUIDE.md
- ONBOARDING_GUIDE.md

---

# Key Takeaways

- **Plan** is ideal for understanding a codebase, designing changes, and generating documentation without modifying code.
- **Edit Automatically** is best for targeted refactoring of individual files or selected code.
- **Manual** provides full control by requiring approval before each edit, making it suitable for high-impact or sensitive changes.
- **Auto** is designed for safe, repetitive, and project-wide updates, automatically applying low-risk changes while pausing for anything that requires review.
