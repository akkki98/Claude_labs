# Understanding CLAUDE.md, Skills, and Subagents

Before creating a Skill, it's important to understand how **CLAUDE.md**, **Skills**, and **Subagents** differ in Claude Code. Although they all help Claude perform tasks more effectively, they serve different purposes.

| Feature | `CLAUDE.md` | Skill | Subagent |
|---------|-------------|--------|----------|
| Primary Purpose | Defines project-wide instructions and conventions | Defines reusable expertise for a specific type of task | Acts as an independent AI specialist for delegated work |
| Scope | Entire project | Specific task or domain | Independent task execution |
| When Used | Always loaded for every conversation in the project | Loaded when Claude determines it is relevant (or when explicitly invoked) | Created or delegated by Claude when specialized work is needed |
| Context | Shares the main conversation context | Uses the main conversation context with additional task-specific instructions | Has its own execution context while working on the assigned task |
| Independence | No | No | Yes |
| Best Used For | Coding standards, architecture, naming conventions, project guidelines | Code reviews, documentation generation, testing, security audits, SQL optimization | Large-scale analysis, architecture reviews, complex refactoring, parallel investigations |

---

## `CLAUDE.md` – Project Rulebook

`CLAUDE.md` contains instructions that Claude follows throughout the project. Think of it as the project's handbook.

Typical contents include:

- Programming language and framework
- Coding standards
- Architecture guidelines
- Naming conventions
- Testing requirements
- Documentation standards

Example:

```markdown
# Project Standards

- Use Java 21
- Use Spring Boot 3
- Follow SOLID principles
- Use constructor injection
- Write JUnit 5 tests
- Every public method should include JavaDoc
```

These instructions are automatically applied during every interaction in the project.

---

## Skills – Reusable Expertise

A Skill teaches Claude how to perform a particular kind of work consistently.

Examples include:

- Java Code Review
- API Documentation Generator
- Unit Test Generator
- SQL Query Optimizer
- Security Audit

Example:

```markdown
---
name: Java Code Review
description: Review Java applications for best practices.
---

When invoked:

- Review readability
- Review performance
- Review security
- Suggest improvements

Output Format:

1. Summary
2. Issues Found
3. Recommendations
```

Skills are only used when Claude determines they are relevant to the current request.

---

## Subagents – Specialized AI Workers

A Subagent is an independent AI assistant that Claude can delegate work to. Unlike a Skill, which provides reusable instructions, a Subagent performs an assigned task independently and returns its findings.

For example, if you ask Claude to analyze an enterprise application, it may delegate work to specialized subagents such as:

- Security Reviewer
- Performance Analyzer
- Documentation Expert
- Testing Specialist
- Database Expert

The main Claude instance collects the results from these subagents and combines them into a comprehensive response.

---

## Simple Analogy

Imagine a software development team:

- **`CLAUDE.md`** is the **company handbook** that every developer follows.
- **A Skill** is a **standard operating procedure (SOP)** or checklist for a specific activity, such as code review or API documentation.
- **A Subagent** is a **specialist team member** (for example, a security engineer or performance engineer) who is assigned a dedicated task and reports back with their findings.

---

## Key Takeaways

- **`CLAUDE.md`** defines **how Claude should behave throughout the project.**
- **Skills** define **how Claude should perform a specific type of task.**
- **Subagents** define **who performs specialized work** by delegating tasks to independent AI specialists.
