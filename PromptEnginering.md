# Lab: Prompt Engineering Fundamentals with Claude

## Lab Overview

**Duration:** 90–120 Minutes

**Audience:** Developers, QA Engineers, Product Managers, Business Analysts, Data Engineers, Solution Architects

---

# Lab Objectives

By the end of this lab, participants will be able to:

- Write effective prompts using prompt engineering best practices
- Understand the components of a high-quality prompt
- Apply Zero-Shot, One-Shot, and Few-Shot prompting techniques
- Use Persona-Based prompting for specialized responses
- Generate structured outputs in Markdown, JSON, CSV, and tables
- Build multi-step workflows using Prompt Chaining

---

# Prerequisites

- Claude Desktop or Claude Console
- Anthropic account
- Basic understanding of Generative AI

---

# Lab Scenario

You are an AI Engineer working on an **Inventory Management System**. Your team wants to use Claude to assist with software development, documentation, testing, architecture, and business analysis.

Your goal is to learn various prompt engineering techniques that improve response quality and consistency.

---

# Exercise 1 – Components of an Effective Prompt

## Objective

Learn the building blocks of a well-crafted prompt.

### Prompt Structure

An effective prompt typically includes:

- Role
- Goal
- Context
- Input
- Constraints
- Expected Output Format

---

### Poor Prompt

```text
Explain inventory.
```

---

### Improved Prompt

```text
You are a senior software architect.

Explain the purpose of an Inventory Management System to a junior developer.

Include:

- Business purpose
- Key modules
- Typical workflow
- Benefits

Use simple language and provide real-world examples.

Present the answer using Markdown headings and bullet points.
```

---

### Tasks

- Execute both prompts.
- Compare the responses.
- Identify how each prompt component improved the result.

---

# Exercise 2 – Zero-Shot Prompting

## Objective

Generate a response without providing examples.

### Prompt

```text
Generate a REST API design for an Inventory Management System.

Include:

- Endpoint
- HTTP Method
- Request
- Response
- Status Codes
```

---

### Discussion

Observe:

- Completeness
- Assumptions made by Claude
- Response quality

---

# Exercise 3 – One-Shot Prompting

## Objective

Guide Claude with a single example.

### Prompt

```text
Example

Feature: Customer Management

Endpoint:
POST /customers

Description:
Creates a new customer.

Request:
{
  "name": "John",
  "email": "john@example.com"
}

Response:
201 Created

Now create similar documentation for Product Management.
```

---

### Tasks

Compare the One-Shot response with the Zero-Shot response.

---

# Exercise 4 – Few-Shot Prompting

## Objective

Improve consistency using multiple examples.

### Prompt

```text
Example 1

Feature:
Create Customer

Endpoint:
POST /customers

Description:
Creates a customer.

--------------------------------

Example 2

Feature:
Delete Customer

Endpoint:
DELETE /customers/{id}

Description:
Deletes a customer.

--------------------------------

Now generate documentation for:

Inventory Management
Supplier Management
Order Management
```

---

### Discussion

Observe how formatting and consistency improve.

---

# Exercise 5 – Persona-Based Prompting

## Objective

Generate responses tailored to different audiences.

---

### Prompt 1

```text
You are a senior software architect.

Explain Microservices Architecture for an Inventory Management System.
```

---


### Prompt 2

```text
You are a product manager.

Explain the business benefits of Microservices Architecture.
```

---

### Prompt 3

```text
You are a QA Lead.

Explain how Microservices Architecture impacts testing.
```

---

### Tasks

Compare:

- Tone
- Level of detail
- Vocabulary
- Technical depth
- Intended audience

---

# Exercise 6 – Structured Output Generation

## Objective

Generate predictable, machine-readable outputs.

---

## Part A – Markdown

### Prompt

```text
Generate Markdown documentation for the Product module.

Include:

- Purpose
- APIs
- Database tables
- Business rules
```

---

## Part B – JSON

### Prompt

```text
Generate a JSON object describing a Product.

Fields:

- ProductId
- ProductName
- Category
- Quantity
- Price
```

---

## Part C – CSV

### Prompt

```text
Generate CSV data containing five sample inventory records.
```

---

## Part D – Table

### Prompt

```text
Generate a comparison table showing:

- Monolithic Architecture
- Microservices
- Serverless
```

---

## Part E – Mermaid Diagram

### Prompt

```text
Generate a Mermaid sequence diagram for adding a product to inventory.
```

---

### Discussion

Discuss when each output format is most appropriate.

---

# Exercise 7 – Prompt Chaining

## Objective

Break a complex task into multiple prompts.

---

## Step 1 – Requirements

```text
Generate functional requirements for an Inventory Management System.
```

---

## Step 2 – Architecture

```text
Using the functional requirements generated previously, design the application architecture.
```

---

## Step 3 – Database Design

```text
Based on the proposed architecture, generate the database schema.
```

---

## Step 4 – API Design

```text
Using the database schema, generate REST APIs.
```

---

## Step 5 – Test Cases

```text
Generate unit and integration test cases for the APIs.
```

---

## Step 6 – Documentation

```text
Generate developer documentation for the application using all previous outputs.
```

---

### Discussion

Observe how each response builds upon the previous one to produce a comprehensive solution.

---

# Exercise 8 – End-to-End Prompt Workflow

## Objective

Use multiple prompt engineering techniques together.

### Prompt

```text
You are a senior solution architect.

Design an Inventory Management System.

Follow these steps:

1. Generate business requirements.
2. Design the architecture.
3. Create the database schema.
4. Generate REST APIs.
5. Suggest security controls.
6. Generate unit tests.
7. Produce deployment documentation.
8. Create a developer onboarding guide.

Provide each section as a separate Markdown document.
```

---

# Challenge Lab

## Scenario

Your organization wants to build a **Warehouse Inventory Platform**.

Using the techniques learned in this lab:

- Use Persona-Based prompting.
- Apply Few-Shot prompting where appropriate.
- Generate structured outputs in Markdown and JSON.
- Chain prompts to move from requirements to architecture, APIs, testing, and documentation.

Prepare a complete AI-assisted project blueprint.

---

# Deliverables

Participants should generate:

- Effective Prompt Examples
- Zero-Shot Prompt Output
- One-Shot Prompt Output
- Few-Shot Prompt Output
- Persona-Based Responses
- Markdown Documentation
- JSON Output
- CSV Sample Data
- Comparison Tables
- Mermaid Diagrams
- Chained Prompt Workflow
- Complete Project Documentation

---

# Best Practices

- Clearly define the role or persona.
- State the goal explicitly.
- Provide relevant context.
- Specify constraints and assumptions.
- Request a structured output format.
- Break large tasks into smaller chained prompts.
- Use examples to improve consistency.
- Iterate and refine prompts based on results.

---

# Learning Outcomes

After completing this lab, participants will be able to:

- Design effective prompts using structured prompt components.
- Differentiate between Zero-Shot, One-Shot, and Few-Shot prompting.
- Tailor responses using Persona-Based prompting.
- Generate consistent structured outputs for documentation and automation.
- Apply Prompt Chaining to solve complex, multi-step problems.
- Build reusable prompt templates for software development, testing, documentation, and architecture using Claude.
