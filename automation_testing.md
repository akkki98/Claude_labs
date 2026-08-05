# Lab: AI-Assisted Automation Testing using Claude Code

## Lab Overview

In this lab, you will use **Claude Code** as an AI-powered automation testing assistant to build and improve a Playwright automation framework for the **Inventory Management Application**.

Rather than writing automation scripts manually, you will use Claude Code to understand the application, generate test scenarios, write Playwright tests, debug failures, refactor code, and improve test coverage.

This lab simulates the daily responsibilities of an Automation Test Engineer working on a real development project.

---

# Application Under Test

Repository

https://github.com/akkki98/inventory_app.git

The application is an Inventory Management System that allows users to manage inventory items.

Typical features include:

- Dashboard
- Product Listing
- Add Product
- Edit Product
- Delete Product
- Search Products
- Inventory Details

---

# Business Scenario

You have recently joined the QA Automation team.

The development team has completed Sprint 5 and delivered several new inventory management features.

Your manager wants an automation regression suite before the production deployment.

Instead of writing hundreds of lines of automation code manually, your team will leverage **Claude Code** throughout the testing lifecycle.

Your responsibility is to:

- Understand the application
- Generate automation tests
- Execute the tests
- Debug failures
- Improve automation quality

---

# Learning Objectives

After completing this lab, you will be able to:

- Use Claude Code for automation testing
- Generate Playwright automation scripts
- Generate test scenarios
- Create reusable Page Objects
- Improve automation code quality
- Debug failed tests
- Generate test data
- Increase automation coverage
- Review automation framework using AI

---

# Prerequisites

- Claude Code
- Git
- Node.js LTS
- VS Code
- Playwright
- Basic JavaScript knowledge

---

# Lab Setup

## Clone the Repository

```bash
git clone https://github.com/akkki98/inventory_app.git

cd inventory_app
```

---

## Install Dependencies

```bash
npm install
```

---

## Start the Application

```bash
npm start
```

Verify the application launches successfully.

---

# Exercise 1 – Understand the Project

Open the project in Claude Code.

Prompt:

```
Analyze this repository and explain:

- Application architecture
- Folder structure
- Technologies used
- API calls
- Pages available
- Possible user workflows
```

Expected Outcome

Learners understand the application before beginning automation.

---

# Exercise 2 – Identify Testable Features

Prompt

```
Analyze the application and identify all features that require automation testing.
```

Expected Output

Claude should identify features such as

- Login (if available)
- Dashboard
- Product Management
- Add Product
- Edit Product
- Delete Product
- Search
- Validation Messages
- Navigation
- Error Handling

Deliverable

A complete automation scope document.

---

# Exercise 3 – Generate Manual Test Scenarios

Prompt

```
Generate positive, negative and boundary test cases for the Product Management module.
```

Expected Output

Examples

Positive

- Add valid product
- Edit product
- Delete product

Negative

- Empty product name
- Invalid quantity
- Duplicate product

Boundary

- Maximum product name length
- Quantity = 0
- Very large quantity

---

# Exercise 4 – Create Playwright Framework

Prompt

```
Generate a Playwright automation framework using Page Object Model for this application.
```

Claude should generate

- pages/
- tests/
- fixtures/
- utilities/
- configuration

---

# Exercise 5 – Automate Add Product

Prompt

```
Generate a Playwright test that automates adding a new inventory product.
```

Expected Validation

- Product created successfully
- Success message displayed
- Product appears in table

Run

```bash
npx playwright test
```

---

# Exercise 6 – Automate Edit Product

Prompt

```
Generate Playwright automation for editing an existing inventory item.
```

Validation

- Updated value visible
- Success notification displayed

---

# Exercise 7 – Automate Delete Product

Prompt

```
Generate Playwright automation for deleting an inventory item.
```

Validation

- Confirmation dialog
- Item removed
- Success notification

---

# Exercise 8 – Automate Search

Prompt

```
Generate automation tests for the search functionality.
```

Test Scenarios

- Exact match
- Partial match
- Invalid search
- Empty search
- Case insensitive search

---

# Exercise 9 – Generate Test Data

Prompt

```
Generate realistic inventory test data.
```

Expected

```
Electronics

Furniture

Books

Office Supplies

Medical Equipment

Food Products
```

Generate

- valid data
- invalid data
- edge case data

Store

```
test-data/products.json
```

---

# Exercise 10 – Refactor Automation Code

Provide an existing Playwright script.

Prompt

```
Improve this automation code by following Playwright best practices.
```

Expected Improvements

- Better locators
- Reusable methods
- Cleaner assertions
- Reduced duplication

---

# Exercise 11 – Debug Failed Tests

Run a failing automation test.

Copy the error into Claude.

Prompt

```
Explain why this Playwright test failed and provide the fix.
```

Expected Diagnosis

- Timing issue
- Locator issue
- Assertion issue
- Network issue
- Data issue

Apply the fix and rerun the tests.

---

# Exercise 12 – Increase Test Coverage

Prompt

```
Review my automation framework and identify missing automation scenarios.
```

Claude may suggest

- Validation testing
- Negative testing
- Boundary testing
- Session handling
- Browser refresh
- Accessibility
- Responsive testing

---

# Exercise 13 – Review Automation Framework

Prompt

```
Review this automation framework as a Senior QA Architect.
```

Expected Review

- Folder structure
- Maintainability
- Naming conventions
- Reusability
- Scalability
- Reporting
- Retry strategy
- Parallel execution

---

# Exercise 14 – Generate Automation Documentation

Prompt

```
Generate documentation for the automation framework.
```

Expected Sections

- Framework Architecture
- Folder Structure
- Running Tests
- Reporting
- Configuration
- Best Practices

---

# Bonus Challenge

Ask Claude Code to convert manual testing into automation.

Prompt

```
Convert all manual Product Management test cases into Playwright automation following the Page Object Model.
```

---

# Suggested Claude Code Prompts

- Explain this repository.
- Generate Playwright automation.
- Generate Page Object classes.
- Improve this locator strategy.
- Create reusable helper methods.
- Debug this failed test.
- Explain this Playwright error.
- Increase automation coverage.
- Review my framework.
- Generate realistic test data.
- Optimize execution time.
- Convert manual test cases into automation.

---

# Deliverables

By the end of this lab, participants should have:

- Complete Playwright automation framework
- Page Object Model implementation
- Automated CRUD test suite
- Search automation tests
- Test data repository
- AI-generated documentation
- Refactored automation code
- Automation framework review report
- Improved test coverage

---

# Learning Outcomes

After completing this lab, participants will understand how Claude Code can assist throughout the automation testing lifecycle, including:

- Understanding an unfamiliar codebase
- Designing automation strategies
- Generating Playwright scripts
- Creating reusable Page Objects
- Producing test data
- Debugging failures
- Refactoring test code
- Reviewing framework quality
- Increasing automation coverage
- Accelerating QA productivity with AI
