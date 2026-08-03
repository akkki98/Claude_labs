# Lab: Generate Project Documentation using Claude Code

## Lab Overview

**Duration:** 60 Minutes  
**Audience:** Developers, QA Engineers, Technical Leads, Solution Architects, Technical Writers

---

# Lab Objectives

By the end of this lab, you will be able to:

- Generate high-quality project documentation using Claude Code
- Create architecture and onboarding guides
- Generate API and module documentation
- Produce technical design documents
- Create developer and user documentation
- Keep documentation synchronized with the codebase

---

# Prerequisites

- Claude Code installed and authenticated
- Git installed
- Visual Studio Code (recommended)
- Basic understanding of software development
- Internet connection

---

# Sample Repository

This lab uses the following GitHub repository.

**Repository:** Inventory App

```text
https://github.com/akkki98/inventory_app.git
```

---

# Lab Setup

## Step 1 – Clone the Repository

```bash
git clone https://github.com/akkki98/inventory_app.git
```

## Step 2 – Navigate to the Project

```bash
cd inventory_app
```

## Step 3 – Launch Claude Code

```bash
claude .
```

---

# Lab Scenario

You have joined a development team responsible for maintaining the **Inventory App**. The application has evolved over time, but much of its documentation is missing or outdated.

Your task is to use **Claude Code** to automatically generate comprehensive project documentation directly from the source code, making it easier for developers, testers, and stakeholders to understand and maintain the application.

---

# Exercise 1 – Generate a Project Overview

## Objective

Create a high-level summary of the application.

### Prompt

```text
Analyze this repository and generate a PROJECT_OVERVIEW.md document.

Include:

- Project purpose
- Business problem solved
- Technology stack
- Architecture style
- Main modules
- Folder structure
- Key dependencies
```

### Deliverable

```
PROJECT_OVERVIEW.md
```

---

# Exercise 2 – Generate Architecture Documentation

## Objective

Document the application architecture.

### Prompt

```text
Generate ARCHITECTURE.md.

Include:

- High-level architecture
- Components
- Data flow
- Layer responsibilities
- Design patterns
- External integrations
- Deployment overview
```

### Deliverable

```
ARCHITECTURE.md
```

---

# Exercise 3 – Generate API Documentation

## Objective

Automatically document all REST APIs.

### Prompt

```text
Scan the repository and generate API_DOCUMENTATION.md.

For every API include:

- Endpoint
- HTTP Method
- Purpose
- Request Parameters
- Response
- Validation
- Error Codes
- Controller
- Service
```

### Deliverable

```
API_DOCUMENTATION.md
```

---

# Exercise 4 – Generate Module Documentation

## Objective

Explain every module in the project.

### Prompt

```text
Generate MODULE_GUIDE.md.

For each module include:

- Purpose
- Responsibilities
- Important classes
- Dependencies
- Related modules
```

---

# Exercise 5 – Generate Database Documentation

## Objective

Understand the data layer.

### Prompt

```text
Generate DATABASE_DOCUMENTATION.md.

Include:

- Database technology
- Entity relationships
- Models
- Tables
- Repositories
- CRUD operations
- Transactions
```

---

# Exercise 6 – Generate Developer Onboarding Guide

## Objective

Help new developers become productive quickly.

### Prompt

```text
Generate ONBOARDING_GUIDE.md.

Include:

- Project overview
- Setup instructions
- Folder explanation
- Build process
- Running the application
- Debugging tips
- Coding standards
- Common workflows
- Recommended learning path
```

---

# Exercise 7 – Generate Feature Documentation

## Objective

Document business functionality.

### Prompt

```text
Identify all business features.

Generate FEATURE_GUIDE.md.

For each feature include:

- Business purpose
- Workflow
- Files involved
- APIs
- Database interactions
- Business rules
```

---

# Exercise 8 – Generate Class Documentation

## Objective

Explain key classes and components.

### Prompt

```text
Generate CLASS_REFERENCE.md.

For each important class include:

- Responsibility
- Public methods
- Dependencies
- Usage
- Related classes
```

---

# Exercise 9 – Generate Sequence Diagrams

## Objective

Visualize application workflows.

### Prompt

```text
Generate Mermaid sequence diagrams for:

- User Login
- Add Product
- Update Product
- Delete Product

Save them in:

SEQUENCE_DIAGRAMS.md
```

---

# Exercise 10 – Generate Deployment Documentation

## Objective

Document deployment steps.

### Prompt

```text
Generate DEPLOYMENT_GUIDE.md.

Include:

- Prerequisites
- Environment variables
- Build commands
- Deployment process
- Configuration files
- Troubleshooting
```

---

# Exercise 11 – Generate Testing Documentation

## Objective

Understand the testing strategy.

### Prompt

```text
Generate TESTING_GUIDE.md.

Include:

- Test framework
- Unit tests
- Integration tests
- Test execution
- Coverage
- Best practices
```

---

# Exercise 12 – Generate Troubleshooting Guide

## Objective

Create operational documentation.

### Prompt

```text
Generate TROUBLESHOOTING.md.

Include:

- Common errors
- Root causes
- Resolution steps
- Debugging techniques
- Logging
```

---

# Exercise 13 – Generate Technical Debt Report

## Objective

Review the codebase for maintainability.

### Prompt

```text
Generate TECHNICAL_DEBT.md.

Identify:

- Large classes
- Long methods
- Duplicate code
- Dead code
- Missing tests
- Circular dependencies
- Code smells

Provide recommendations for improvement.
```

---

# Exercise 14 – Generate Complete Project Wiki

## Objective

Create a documentation package suitable for a GitHub Wiki.

### Prompt

```text
Generate a complete project wiki.

Include:

- Home
- Architecture
- API Guide
- Module Guide
- Database Guide
- Developer Guide
- Deployment Guide
- Testing Guide
- Troubleshooting
- FAQ
- Contributing Guide

Organize the content as Markdown files suitable for a GitHub Wiki.
```

---

# Bonus Challenge 1 – Improve Existing Documentation

### Prompt

```text
Review all existing Markdown documentation in this repository.

Identify:

- Outdated information
- Missing sections
- Inconsistent formatting
- Broken links

Suggest improvements and update the documentation where appropriate.
```

---

# Bonus Challenge 2 – Generate README.md

### Prompt

```text
Generate a professional README.md.

Include:

- Project description
- Features
- Architecture
- Installation
- Configuration
- Usage
- Folder structure
- API summary
- Testing
- Deployment
- Contribution guidelines
- License
```

---

# Deliverables

By the end of this lab, participants should have generated:

- `PROJECT_OVERVIEW.md`
- `ARCHITECTURE.md`
- `API_DOCUMENTATION.md`
- `MODULE_GUIDE.md`
- `DATABASE_DOCUMENTATION.md`
- `ONBOARDING_GUIDE.md`
- `FEATURE_GUIDE.md`
- `CLASS_REFERENCE.md`
- `SEQUENCE_DIAGRAMS.md`
- `DEPLOYMENT_GUIDE.md`
- `TESTING_GUIDE.md`
- `TROUBLESHOOTING.md`
- `TECHNICAL_DEBT.md`
- `README.md`
- GitHub Wiki documentation

---

# Learning Outcomes

After completing this lab, participants will be able to:

- Automatically generate comprehensive project documentation using Claude Code.
- Create architecture, API, module, and deployment guides directly from source code.
- Produce onboarding documentation for new developers.
- Generate technical documentation that stays aligned with the codebase.
- Improve documentation quality and maintainability with AI-assisted workflows.
- Build a complete documentation package suitable for project repositories and GitHub Wikis.
