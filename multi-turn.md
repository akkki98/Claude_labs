# Lab: Understanding Multi-turn Conversations in Claude

## Lab Overview

### Objective
In this lab, you will learn the difference between **Single-turn** and **Multi-turn** conversations in Claude. You will observe how Claude maintains context across multiple interactions and uses previous responses to generate more relevant and accurate answers.

---

## Learning Objectives

By the end of this lab, you will be able to:

- Understand the difference between single-turn and multi-turn conversations
- Observe how Claude remembers context
- Build conversations incrementally
- Ask follow-up questions without repeating previous information
- Experience how context improves response quality

---

## Prerequisites

- Access to Claude (Web/Desktop)
- Basic understanding of Azure services
- No programming knowledge required

---

## Estimated Duration

**20–30 Minutes**

---

# Exercise 1 – Single-turn Conversation

In a single-turn conversation, every prompt is treated independently. Claude only answers the current question without any additional context.

### Step 1

Open a new chat in Claude.

### Prompt

```text
Explain Azure Kubernetes Service.
```

### Expected Output

Claude explains:

- What Azure Kubernetes Service (AKS) is
- Key features
- Benefits
- Common use cases

### Observation

Notice that the conversation ends after Claude answers the question. If you ask another unrelated question in a new chat, Claude has no knowledge of the previous discussion.

---

# Exercise 2 – Multi-turn Conversation

Now experience how Claude maintains context throughout a conversation.

### Step 1 – Provide Initial Context

Enter the following prompt:

```text
I am building an e-commerce application on Azure.
```

### Expected Output

Claude recognizes that you are working on an Azure-based project and may ask follow-up questions to better understand your requirements.

---

### Step 2 – Continue the Conversation

Enter:

```text
Microservices using Java Spring Boot.
```

### Expected Output

Claude understands that:

- The application is an e-commerce platform.
- It is hosted on Azure.
- It uses a microservices architecture.
- The services are built using Java Spring Boot.

Based on this context, Claude may recommend deployment options such as:

- Azure Container Apps
- Azure Kubernetes Service (AKS)

---

### Step 3 – Ask a Follow-up Question

Without repeating any previous information, enter:

```text
Which one is cheaper?
```

### Observe

Claude understands that **"Which one"** refers to the previously discussed deployment options:

- Azure Container Apps
- Azure Kubernetes Service (AKS)

It compares the two services without requiring you to restate the earlier conversation.

---

### Step 4 – Add a New Requirement

Enter:

```text
We expect around 1 million users.
```

### Observe

Claude updates its recommendation based on the increased scale.

Instead of restarting the discussion, it considers the earlier context and may explain why AKS could be a better choice for large-scale workloads.

---

### Step 5 – Request Infrastructure as Code

Enter:

```text
Now generate Terraform code.
```

### Observe

Claude understands that you are requesting Terraform code for the Azure architecture discussed throughout the conversation.

There is no need to repeat:

- Azure
- E-commerce application
- Java Spring Boot
- Microservices
- Deployment platform

Claude uses the accumulated context to generate relevant Terraform code.

---

# What Happened?

Throughout this exercise, Claude continuously remembered the conversation.

The context evolved as follows:

```text
Turn 1
↓
Azure E-commerce Application

Turn 2
↓
Java Spring Boot Microservices

Turn 3
↓
Compare Azure Container Apps vs AKS

Turn 4
↓
Scale Requirement (1 Million Users)

Turn 5
↓
Generate Terraform for the Recommended Architecture
```

Each new prompt built upon the previous one, resulting in increasingly personalized and context-aware responses.

---

# Reflection Questions

1. Did you have to repeat your project details in every prompt?
2. How did Claude interpret the phrase **"Which one"**?
3. Why did Claude change its recommendation after you mentioned **1 million users**?
4. What information did Claude use when generating the Terraform code?
5. How does maintaining context improve productivity?

---

# Key Takeaways

- **Single-turn conversations** treat each prompt independently and do not rely on previous context.
- **Multi-turn conversations** build on earlier interactions, allowing Claude to remember context and provide more relevant responses.
- Follow-up questions become more natural because you do not need to repeat previous information.
- As new requirements are introduced, Claude refines its recommendations instead of starting over.
- Multi-turn conversations are ideal for tasks such as solution design, code generation, troubleshooting, documentation, and project planning.

---

# Challenge Exercise

Start a new conversation in Claude and use a different scenario, such as:

- Banking application
- Healthcare system
- Inventory management system
- Travel booking platform

Build a conversation over at least **6 turns**, gradually adding new requirements and observing how Claude maintains context and adapts its responses.

---

## Conclusion

You have successfully explored the difference between **Single-turn** and **Multi-turn** conversations. By progressively adding information and asking follow-up questions, you experienced how Claude leverages conversational context to deliver more accurate, consistent, and efficient responses.
