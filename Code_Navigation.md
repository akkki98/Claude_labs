# Code Navigation and Understanding using Claude Code

## Lab Overview

**Duration: ** 60 Minutes  
**Audience:** Developers, QA Engineers, Technical Leads, Solution Architects

---

# Objectives

By the end of this lab, you will be able to:

- Navigate a new codebase using Claude Code
- Understand project architecture
- Identify application entry points
- Trace request execution flow
- Explore APIs and database interactions
- Understand dependencies between modules
- Generate architecture and onboarding documentation
- Become productive in an unfamiliar project faster

---

# Prerequisites

- Claude Code installed and authenticated
- Git installed
- Visual Studio Code (recommended)
- Basic knowledge of Git and software development
- Internet connection to clone the sample repository

---

# Sample Repository

Throughout this lab, you will use the following GitHub repository:

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

---

## Step 2 – Navigate to the Project

```bash
cd inventory_app
```

---

## Step 3 – Open the Project in Claude Code

```bash
claude .
```

---

## Step 4 – Verify the Repository

Ask Claude Code:

```text
Show me the folder structure of this project and briefly explain what each folder contains.
```

---

# Lab Scenario

You have recently joined a development team that maintains an **Inventory Management Application**.

Your first task is **not to write code**, but to understand the project so you can confidently work on new features and bug fixes.

Instead of manually opening dozens of files, you will use **Claude Code** to explore the repository, understand the architecture, trace application flows, and generate useful documentation.

---

# Exercise 1 – Understand the Repository

## Objective

Gain a high-level understanding of the project.

### Prompt

```text
Analyze this Inventory App repository and explain:

- What is the purpose of this application?
- Which programming language and framework are used?
- Which architectural pattern does it follow?
- Explain the folder structure.
- Identify the major modules.
- Highlight important configuration files.
- Explain how the different modules interact.
```

### Expected Outcome

You should understand:

- Technology stack
- Overall architecture
- Major components
- Project organization

---

# Exercise 2 – Repository Tour

## Objective

Learn which files are most important for new developers.

### Prompt

```text
Give me a guided tour of this repository.

Start with the files that every new developer should understand first.

Explain why each file is important.
```

---

# Exercise 3 – Find the Application Entry Point

## Objective

Understand how the application starts.

### Prompt

```text
Identify the application's entry point.

Explain:

- Startup sequence
- Configuration loading
- Dependency initialization
- How the application begins execution
```

---

# Exercise 4 – Explain the Folder Structure

## Objective

Understand the responsibility of each folder.

### Prompt

```text
Explain the responsibility of every major folder.

For each folder include:

- Purpose
- Important files
- Dependencies
- Interaction with other folders
```

---

# Exercise 5 – Trace a Business Feature

## Objective

Understand the execution flow of a feature.

Choose one inventory feature such as:

- Add Product
- Update Product
- Delete Product
- View Inventory

### Prompt

```text
Trace the complete execution flow for the selected feature.

Include:

UI

↓

Route

↓

Controller

↓

Service

↓

Repository

↓

Database

Explain every step.
```

---

# Exercise 6 – Locate Business Logic

## Objective

Find where business rules are implemented.

### Prompt

```text
Locate the business logic responsible for inventory management.

Explain:

- Which files contain the business logic?
- Which methods perform validation?
- Which modules invoke these methods?
```

---

# Exercise 7 – Understand Database Operations

## Objective

Learn how the application interacts with the database.

### Prompt

```text
Identify all database interactions.

Explain:

- Database technology
- ORM or data access framework
- Repository pattern
- CRUD implementation
- Transaction handling
```

---

# Exercise 8 – Understand API Flow

## Objective

Explore the REST APIs.

### Prompt

```text
List every API endpoint in this project.

For each endpoint explain:

- Purpose
- Request
- Response
- Controller
- Service
- Repository
```

---

# Exercise 9 – Generate a Dependency Map

## Objective

Understand relationships between components.

### Prompt

```text
Generate a dependency map showing:

Controllers

↓

Services

↓

Repositories

↓

Database

Highlight any tightly coupled components.
```

---

# Exercise 10 – Understand Error Handling

## Objective

Explore exception management.

### Prompt

```text
Explain how errors are handled.

Include:

- Global exception handling
- Validation errors
- Custom exceptions
- Logging strategy
```

---

# Exercise 11 – Generate Architecture Documentation

## Objective

Automatically generate project documentation.

### Prompt

```text
Generate ARCHITECTURE.md containing:

- Application overview
- Folder structure
- Components
- Data flow
- External integrations
- Technology stack
```

---

# Exercise 12 – Generate an Onboarding Guide

## Objective

Create documentation for new developers.

### Prompt

```text
Create ONBOARDING_GUIDE.md containing:

- Project overview
- Folder explanation
- Important classes
- APIs
- Database flow
- Build instructions
- Debugging tips
- Coding conventions
- Recommended learning order
```

---

# Exercise 13 – Create a Learning Roadmap

## Objective

Learn the repository efficiently.

### Prompt

```text
If I had only one hour to understand this repository, create a learning roadmap.

Tell me:

- Which files to read first
- Which modules to study next
- Recommended debugging path
- Suggested learning order
```

---

# Exercise 14 – Identify Technical Debt

## Objective

Review the quality of the project.

### Prompt

```text
Review the repository and identify:

- Large classes
- Long methods
- Duplicate code
- Dead code
- Missing tests
- Circular dependencies
- Potential security issues

Suggest improvements.
```

---

# Bonus Challenge

Generate a complete developer onboarding package.

### Prompt

```text
Assume I am joining this project today.

Generate documentation including:

- Repository overview
- Architecture
- Folder structure
- API documentation
- Database design
- Deployment overview
- Coding standards
- Build process
- Testing strategy
- Debugging guide
- Frequently modified files
- Suggested learning path

Save it as:

DEVELOPER_GUIDE.md
```

---

# Deliverables

At the end of this lab, participants should have generated:

- Repository Overview
- Architecture Documentation (`ARCHITECTURE.md`)
- API Documentation
- Dependency Map
- Database Summary
- ONBOARDING_GUIDE.md
- DEVELOPER_GUIDE.md
- Technical Debt Report
- Learning Roadmap

---

# Learning Outcomes

After completing this lab, participants will be able to:

- Navigate an unfamiliar codebase using Claude Code
- Understand software architecture quickly
- Trace feature execution across multiple layers
- Explore APIs and database interactions
- Generate developer documentation automatically
- Improve onboarding efficiency
- Identify technical debt and potential improvements
- Become productive in an existing project significantly faster
