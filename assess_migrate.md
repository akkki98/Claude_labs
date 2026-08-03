# Lab: Assess and Migrate Legacy Java Applications using Claude Code

## Lab Overview

**Duration:** 1-2 Hours

**Audience:** Java Developers, Solution Architects, Cloud Engineers, Technical Leads, Application Modernization Teams

---

# Lab Objectives

By the end of this lab, participants will be able to:

- Assess a legacy Java application using Claude Code
- Understand the existing architecture and dependencies
- Identify modernization opportunities
- Analyze technical debt and migration blockers
- Plan cloud migration strategies
- Modernize legacy code with Claude Code
- Generate migration documentation and reports

---

# Prerequisites

- Claude Code installed and authenticated
- Git installed
- Java 17 or later
- Maven installed
- Visual Studio Code (recommended)
- Basic understanding of Java and Spring applications

---

# Sample Repository

This lab uses Microsoft's Java migration sample application.

**Repository**

```text
https://github.com/Azure-Samples/java-migration-copilot-samples.git
```

This repository contains sample applications designed to demonstrate Java modernization and migration scenarios to Azure using GitHub Copilot modernization guidance. :contentReference[oaicite:0]{index=0}

---

# Lab Setup

## Step 1 – Clone the Repository

```bash
git clone https://github.com/Azure-Samples/java-migration-copilot-samples.git
```

---

## Step 2 – Open the Repository

```bash
cd java-migration-copilot-samples
```

---

## Step 3 – Launch Claude Code

```bash
claude .
```

---

# Lab Scenario

Your organization has a legacy Java application that has been running for several years.

The application contains:

- Legacy Java code
- Older frameworks
- Hardcoded configurations
- Technical debt
- Cloud migration challenges

Your responsibility is to use **Claude Code** to assess the application, identify modernization opportunities, generate migration documentation, and create a phased migration plan before implementation.

---

# Exercise 1 – Understand the Legacy Application

## Objective

Gain a high-level understanding of the application.

### Prompt

```text
Analyze this Java application.

Explain:

- Business purpose
- Technology stack
- Java version
- Frameworks used
- Overall architecture
- Folder structure
- Build system
- Main application modules
```

### Deliverable

- Project Overview

---

# Exercise 2 – Perform Application Assessment

## Objective

Assess the application's current state.

### Prompt

```text
Perform a complete assessment of this legacy application.

Identify:

- Outdated frameworks
- Legacy libraries
- Deprecated APIs
- Unsupported dependencies
- Security concerns
- Performance issues
- Technical debt

Generate an assessment report.
```

### Deliverable

```
ASSESSMENT_REPORT.md
```

---

# Exercise 3 – Analyze Project Dependencies

## Objective

Identify dependency risks.

### Prompt

```text
Analyze every project dependency.

Identify:

- Current version
- Latest version
- Deprecated libraries
- Vulnerabilities
- Migration recommendations

Create a dependency upgrade roadmap.
```

---

# Exercise 4 – Identify Migration Blockers

## Objective

Discover issues that could delay modernization.

### Prompt

```text
Identify all migration blockers.

Examples include:

- Hardcoded file paths
- Local storage
- Environment-specific configuration
- Vendor lock-in
- Deprecated APIs
- Legacy authentication
- Unsupported Java features

Prioritize blockers by severity.
```

---

# Exercise 5 – Analyze Cloud Readiness

## Objective

Evaluate Azure migration readiness.

### Prompt

```text
Assess whether this application is cloud-ready.

Evaluate:

- Stateless design
- External configuration
- Session management
- File storage
- Database connectivity
- Messaging
- Logging
- Scalability

Provide a cloud readiness score from 1–10.
```

---

# Exercise 6 – Modernize Configuration

## Objective

Identify configuration improvements.

### Prompt

```text
Review all configuration files.

Suggest improvements including:

- Externalized configuration
- Environment variables
- Secrets management
- Azure Key Vault integration
- Application configuration improvements
```

---

# Exercise 7 – Database Migration Assessment

## Objective

Prepare the data layer for modernization.

### Prompt

```text
Analyze the database layer.

Identify:

- Database technology
- ORM framework
- SQL queries
- Transactions
- Connection management

Recommend Azure database services suitable for this application.
```

---

# Exercise 8 – Storage Migration Assessment

## Objective

Assess storage modernization opportunities.

### Prompt

```text
Identify all file storage operations.

Recommend migration strategies for:

- Local file storage
- Shared folders
- Blob storage
- Static assets

Explain code changes required.
```

---

# Exercise 9 – Messaging Assessment

## Objective

Review messaging components.

### Prompt

```text
Identify all messaging components.

Recommend migration to Azure messaging services.

Explain:

- Current implementation
- Proposed Azure service
- Required code changes
```

---

# Exercise 10 – Security Assessment

## Objective

Evaluate application security.

### Prompt

```text
Perform a security assessment.

Identify:

- Hardcoded credentials
- Weak authentication
- Secrets in source code
- Missing encryption
- Security vulnerabilities

Recommend remediation steps.
```

---

# Exercise 11 – Generate Modernization Roadmap

## Objective

Create a phased migration strategy.

### Prompt

```text
Generate a modernization roadmap.

Include:

Phase 1

Assessment

Phase 2

Dependency upgrades

Phase 3

Java upgrade

Phase 4

Cloud migration

Phase 5

Testing

Phase 6

Deployment

Estimate effort and risks for each phase.
```

### Deliverable

```
MODERNIZATION_ROADMAP.md
```

---

# Exercise 12 – Refactor Legacy Code

## Objective

Modernize selected components.

### Prompt

```text
Review this codebase and identify opportunities to refactor.

Focus on:

- Modern Java features
- Better exception handling
- Improved logging
- Dependency Injection
- Code readability
- Maintainability

Generate refactored code with explanations.
```

---

# Exercise 13 – Generate Migration Documentation

## Objective

Create comprehensive migration documentation.

### Prompt

```text
Generate MIGRATION_GUIDE.md.

Include:

- Current architecture
- Target architecture
- Required code changes
- Infrastructure changes
- Testing strategy
- Deployment strategy
- Rollback plan
```

---

# Exercise 14 – Executive Migration Summary

## Objective

Prepare documentation for stakeholders.

### Prompt

```text
Generate an executive migration report.

Include:

- Current state
- Business risks
- Technical risks
- Estimated migration effort
- Benefits of modernization
- Recommended migration approach
- Expected business outcomes
```

---

# Challenge Lab

Your management has approved the migration project.

Using Claude Code, prepare a complete modernization package containing:

- Application Assessment
- Technical Debt Report
- Dependency Analysis
- Cloud Readiness Report
- Security Assessment
- Migration Roadmap
- Refactoring Recommendations
- Target Architecture
- Migration Guide
- Executive Summary

Save each report as a separate Markdown document.

---

# Deliverables

Participants should generate:

- `PROJECT_OVERVIEW.md`
- `ASSESSMENT_REPORT.md`
- `DEPENDENCY_ANALYSIS.md`
- `TECHNICAL_DEBT.md`
- `CLOUD_READINESS.md`
- `SECURITY_ASSESSMENT.md`
- `MODERNIZATION_ROADMAP.md`
- `REFACTORING_GUIDE.md`
- `MIGRATION_GUIDE.md`
- `EXECUTIVE_SUMMARY.md`

---

# Best Practices

- Understand the existing application before proposing changes.
- Assess dependencies before upgrading frameworks.
- Prioritize security and cloud readiness early in the migration.
- Modernize incrementally using phased migration plans.
- Validate recommendations with testing before implementation.
- Generate documentation alongside code changes to keep modernization efforts traceable.

---

# Learning Outcomes

After completing this lab, participants will be able to:

- Assess legacy Java applications using Claude Code.
- Identify technical debt, outdated dependencies, and migration blockers.
- Evaluate cloud readiness and modernization opportunities.
- Refactor legacy code using AI-assisted recommendations.
- Generate comprehensive migration documentation and executive reports.
- Build phased migration plans for enterprise Java applications.
- Apply AI-assisted modernization techniques to accelerate legacy application migration projects.
