# Function & Tool Calling with Claude

## Overview


1. **Tool Calling in Claude Code (No API Required)** – Learn how Claude Code uses its built-in capabilities to interact with your local development environment.
2. **Function Calling with the Claude API (API Required)** – Build an AI application that integrates with the Anthropic API and executes custom functions.

By completing both sections, you will understand the difference between using Claude Code as a development assistant and building applications powered by Claude.

---

# Section 1 – Tool Calling in Claude Code (No API Required)

## Objective

Learn how Claude Code automatically uses built-in tools and local resources to complete development and operational tasks without writing API integration code.

> **Note:** This section **does not require an Anthropic API key**.

---


## Prerequisites

- Claude Code installed and configured
- Anthropic account with Claude Code access
- Git installed
- Python or Node.js installed
- A local sample project

---

## Learning Outcomes

After completing this section, you will be able to:

- Understand Claude Code's built-in tool capabilities.
- Work with local files and folders.
- Execute local Python or Node.js scripts.
- Chain multiple tool invocations together.
- Understand permission requests and approval workflows.
- Observe how Claude automatically selects the appropriate tool.

---

## Business Scenario

You are building an **IT Service Desk Assistant** using Claude Code.

The assistant should be able to:

- Read application logs
- Search knowledge base documents
- Check server health
- Create support tickets
- Restart services (simulation)

Instead of relying solely on its knowledge, Claude Code should determine when to use available tools to complete the task.

---

## Tool Calling Workflow

```text
User Request
      │
      ▼
Claude Code
      │
      ▼
Determines Required Tool
      │
      ▼
Executes Local Tool
      │
      ▼
Processes Result
      │
      ▼
Returns Final Response
```

---

## Project Structure

```text
claude-tools-lab/

├── tools/
│   ├── check_server.py
│   ├── create_ticket.py
│   ├── restart_service.py
│   └── search_kb.py
│
├── logs/
│   └── application.log
│
├── docs/
│   ├── vpn.md
│   ├── password_reset.md
│   └── mfa.md
│
└── README.md
```

---

## Hands-on Exercise 1 – Analyze Application Logs

Prompt Claude Code:

```text
Read the application.log file and summarize the critical errors.
```

Expected Outcome

- Opens the log file
- Reads the contents
- Identifies critical errors
- Generates a concise summary

---

## Hands-on Exercise 2 – Search Project Documentation

Prompt:

```text
Search every markdown document for password reset instructions.
```

Expected Outcome

- Searches all Markdown files
- Finds matching documents
- Summarizes the relevant information

---

## Hands-on Exercise 3 – Execute a Server Status Tool

Create:

```text
tools/check_server.py
```

Sample output:

```text
Server Name : Web-01
Status      : Running
CPU Usage   : 42%
Memory      : 63%
Disk        : Healthy
```

Prompt:

```text
Use the server status tool and tell me whether the application server is healthy.
```

---

## Hands-on Exercise 4 – Search a Knowledge Base

Create:

```text
tools/search_kb.py
```

Sample knowledge base:

- Password Reset
- VPN Access
- Email Configuration
- MFA Setup

Prompt:

```text
Search the knowledge base for VPN connection troubleshooting.
```

---

## Hands-on Exercise 5 – Create an Incident Ticket

Create:

```text
tools/create_ticket.py
```

Example output:

```text
Ticket ID : INC10245

Priority : High

Assigned To : Infrastructure Team
```

Prompt:

```text
Create a high-priority incident ticket because the production server is unavailable.
```

---

## Hands-on Exercise 6 – Restart a Service

Create:

```text
tools/restart_service.py
```

Prompt:

```text
Restart the Tomcat service.
```

---

## Hands-on Exercise 7 – Chain Multiple Tool Calls

Prompt:

```text
The production application is slow.

Check server health.

Search the knowledge base.

Create an incident ticket.

Provide a final summary.
```

Observe how Claude performs multiple tool invocations to complete a single task.

---

## Hands-on Exercise 8 – Permission & Approval Flow

Perform operations that require approval, such as:

- Reading files
- Executing scripts
- Modifying files

Observe:

- When Claude requests permission
- What actions require approval
- How approvals improve security

---

## Key Takeaways

By the end of this section you should understand:

- Built-in tool usage
- Local file access
- Local script execution
- Automatic tool selection
- Multi-step workflows
- Permission and approval mechanisms

---

# Section 2 – Function Calling with the Claude API (API Required)

## Objective

Build an AI application that uses the Anthropic API to enable Claude to invoke custom functions (tools) defined by your application.

Unlike Claude Code, **your application is responsible for executing the tools and returning the results to Claude.**


---

## Prerequisites

- Anthropic API Key
- Python or Node.js
- Anthropic SDK
- VS Code or preferred IDE
- Internet connectivity

---

## Learning Outcomes

After completing this section, you will be able to:

- Configure an Anthropic API key.
- Use the Anthropic Messages API.
- Define custom tools.
- Execute tool requests.
- Return structured tool results.
- Build a complete AI assistant.

---

## Function Calling Workflow

```text
User
   │
   ▼
Application
   │
   ▼
Anthropic Messages API
   │
   ▼
Claude selects a tool
   │
   ▼
Application executes the tool
   │
   ▼
Tool returns structured output
   │
   ▼
Claude generates the final response
```

---

## Hands-on Exercise 1 – Configure the API

- Create an Anthropic API key.
- Store it securely using environment variables.
- Install the Anthropic SDK.

---

## Hands-on Exercise 2 – Send Your First API Request

Create a simple application that sends a prompt to the Anthropic Messages API and displays Claude's response.

---

## Hands-on Exercise 3 – Define a Custom Tool

Create a tool such as:

- Check Server Status
- Search Knowledge Base
- Create Incident Ticket

Define the tool using a JSON schema.

---

## Hands-on Exercise 4 – Execute Tool Requests

When Claude requests a tool:

- Parse the request
- Execute the corresponding function
- Capture the result

---

## Hands-on Exercise 5 – Return Tool Results

Send the structured tool response back to Claude and observe how it incorporates the result into its final answer.

---

## Hands-on Exercise 6 – Support Multiple Tools

Register multiple tools and allow Claude to choose the appropriate one based on the user's request.

---

## Hands-on Exercise 7 – Build an IT Service Desk Assistant

Create an assistant capable of:

- Checking server health
- Searching documentation
- Creating incident tickets
- Restarting services (simulation)
- Producing an incident summary

---

## Claude Code vs Claude API

| Feature | Claude Code | Claude API |
|----------|-------------|------------|
| Anthropic API Key | ❌ Not Required | ✅ Required |
| Local File Access | ✅ Built-in | Managed by Your Application |
| Execute Local Scripts | ✅ Supported | Managed by Your Application |
| Tool Definitions | Built-in and Local Workflows | Fully Customizable |
| Tool Execution | Claude Code | Your Application |
| Best For | Developer Productivity | AI Application Development |

---

# Final Challenge

Build an **Enterprise IT Operations Assistant** capable of:

- Reading application logs
- Checking server health
- Searching a knowledge base
- Restarting services
- Creating incident tickets
- Producing a management-ready incident report

### Example Prompt

```text
The payroll application is unavailable.

Investigate the issue.

Check server health.

Search the knowledge base.

Restart services if required.

Create a high-priority incident ticket.

Provide a management-ready summary.
```

---

# Success Criteria

You have successfully completed this workshop if you can:

- Explain the difference between Claude Code tool calling and Claude API function calling.
- Use Claude Code to execute local workflows and chain multiple tool invocations.
- Build an application that integrates with the Anthropic Messages API.
- Define and execute custom functions.
- Return structured tool results to Claude.
- Build an end-to-end AI assistant capable of solving real-world enterprise scenarios.
