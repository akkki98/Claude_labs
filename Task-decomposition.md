# Lab: Task Decomposition with Claude

## Lab Overview

### Objective

In this lab, you will learn how to use **Task Decomposition** in Claude to solve complex problems by breaking them into smaller, logical tasks. Instead of asking Claude to complete an entire project in one prompt, you will guide it through a series of focused steps to produce higher-quality, more accurate results.

---

## Learning Objectives

By the end of this lab, you will be able to:

- Understand the concept of Task Decomposition
- Break a complex problem into smaller tasks
- Guide Claude through a structured workflow
- Improve the quality and accuracy of AI-generated responses
- Build a complete solution iteratively

---

## Prerequisites

- Claude Web or Claude Desktop
- Basic understanding of software development concepts
- No coding experience required (recommended for better understanding)

---

## Estimated Duration

**40–50 Minutes**

---

# Scenario

You are a Cloud Solution Architect designing a new **E-commerce application** to be deployed on Azure.

Instead of asking Claude to generate the complete solution in one prompt, you will decompose the project into smaller tasks and solve them one at a time.

---

# Exercise 1 – Solve Everything in One Prompt

Start a new conversation in Claude.

### Prompt

```text
Build a complete cloud-native e-commerce application using Java Spring Boot on Azure.

Include:
- Architecture
- Database
- Microservices
- Security
- CI/CD
- Terraform
- Monitoring
- Documentation
```

---

### Observe

Notice that Claude attempts to answer everything in one response.

Discuss:

- Was the response too large?
- Was every section detailed?
- Would it be easy to review or modify one part?

---

# Exercise 2 – Decompose the Task

Instead of solving everything at once, break the project into smaller tasks.

### Prompt

```text
We will build this solution step by step.

Act as a Senior Cloud Architect.

Do not solve everything at once.

Wait for my next instruction after completing each task.
```

---

### Expected Outcome

Claude acknowledges the workflow and waits for individual tasks.

---

# Exercise 3 – Task 1: Gather Requirements

### Prompt

```text
Task 1:

Identify the functional and non-functional requirements for an e-commerce application.
```

---

### Expected Outcome

Claude lists:

- Functional requirements
- Non-functional requirements
- Assumptions
- Constraints

---

# Exercise 4 – Task 2: Design the Architecture

### Prompt

```text
Task 2:

Based on the requirements, design a high-level Azure architecture.

Do not generate code yet.
```

---

### Expected Outcome

Claude recommends Azure services such as:

- Azure Container Apps or AKS
- Azure SQL Database
- Azure Cache for Redis
- Azure Storage
- Azure Key Vault
- Azure Monitor

---

# Exercise 5 – Task 3: Identify Microservices

### Prompt

```text
Task 3:

Identify the microservices required for this application.

For each microservice, describe its responsibility.
```

---

### Expected Outcome

Example services:

- Product Service
- Order Service
- User Service
- Payment Service
- Inventory Service
- Notification Service

---

# Exercise 6 – Task 4: Design the Database

### Prompt

```text
Task 4:

Design the database schema for the application.

Include the main tables and relationships.
```

---

### Expected Outcome

Claude generates:

- Customers
- Products
- Orders
- Order Items
- Payments
- Inventory

with relationships between them.

---

# Exercise 7 – Task 5: Generate APIs

### Prompt

```text
Task 5:

Generate REST APIs for the Product Service.

Include:

- Endpoints
- HTTP Methods
- Request
- Response
```

---

### Expected Outcome

Claude creates a structured API specification for the Product Service.

---

# Exercise 8 – Task 6: Infrastructure as Code

### Prompt

```text
Task 6:

Generate Terraform code for deploying the Azure infrastructure designed earlier.
```

---

### Expected Outcome

Claude generates Terraform for:

- Resource Group
- Azure Container Apps or AKS
- Azure SQL Database
- Storage Account
- Key Vault
- Monitoring resources

---

# Exercise 9 – Task 7: CI/CD Pipeline

### Prompt

```text
Task 7:

Generate an Azure DevOps YAML pipeline for building, testing, and deploying the application.
```

---

### Expected Outcome

Claude creates a pipeline including:

- Build
- Unit Tests
- Docker Build
- Push Image
- Infrastructure Deployment
- Application Deployment

---

# Exercise 10 – Task 8: Monitoring and Security

### Prompt

```text
Task 8:

Recommend monitoring and security best practices for this solution.
```

---

### Expected Outcome

Claude suggests:

- Azure Monitor
- Application Insights
- Log Analytics
- Microsoft Defender for Cloud
- Azure Key Vault
- Managed Identity
- Role-Based Access Control (RBAC)

---

# Exercise 11 – Final Summary

### Prompt

```text
Summarize all the completed tasks.

Include:

- Requirements
- Architecture
- Microservices
- Database
- APIs
- Terraform
- CI/CD
- Security
- Monitoring

Present the summary as a project design document.
```

---

### Expected Outcome

Claude consolidates all previous work into a well-structured project document.

---

# Visualizing Task Decomposition

```text
Goal
│
├── Task 1 → Gather Requirements
│
├── Task 2 → Design Architecture
│
├── Task 3 → Identify Microservices
│
├── Task 4 → Design Database
│
├── Task 5 → Generate APIs
│
├── Task 6 → Create Terraform
│
├── Task 7 → Build CI/CD Pipeline
│
├── Task 8 → Configure Security & Monitoring
│
└── Final → Project Summary
```

---

# Reflection Questions

1. How did breaking the problem into smaller tasks improve the responses?
2. Which task benefited the most from focused prompting?
3. Was it easier to review and refine individual outputs?
4. How would you modify one task without affecting the others?
5. In what real-world scenarios would Task Decomposition be useful?

---

# Best Practices

- Start with the overall goal before defining individual tasks.
- Keep each prompt focused on a single objective.
- Complete one task before moving to the next.
- Reuse outputs from earlier tasks instead of repeating information.
- Review and refine each step before proceeding.
- Ask Claude to summarize progress periodically during long conversations.

---

# Challenge Exercise

Choose one of the following projects and decompose it into at least **10 tasks** before asking Claude to solve them:

- Banking Application
- Hospital Management System
- Learning Management System (LMS)
- Food Delivery Platform
- Travel Booking Application
- Inventory Management System

After completing all tasks, ask Claude to generate:

- Architecture Diagram (Mermaid)
- Project Timeline
- Risk Assessment
- Cost Optimization Recommendations
- Deployment Checklist

---

# Key Takeaways

- **Task Decomposition** is the process of breaking a complex problem into smaller, manageable tasks.
- Claude produces more focused and detailed responses when each task has a clear objective.
- Solving one task at a time makes it easier to review, refine, and reuse outputs.
- Task Decomposition is particularly effective for software development, cloud architecture, documentation, project planning, and infrastructure automation.
- Combining **Task Decomposition** with **Multi-turn Conversations** enables Claude to build comprehensive, context-aware solutions step by step.
