# Lab Guide: GitHub MCP Server with Claude Code

## Lab Overview

In this lab, you will configure the **GitHub MCP (Model Context Protocol) Server** with Claude Code and use it to interact with GitHub repositories using natural language. You will learn how to view issues, review pull requests, inspect commits, and work with repository information directly from Claude Code.

> **Difficulty:** Intermediate  
> **Duration:** 30–40 Minutes

---

# Learning Objectives

By the end of this lab, you will be able to:

- Configure the GitHub MCP Server in Claude Code.
- Authenticate using a GitHub Personal Access Token (PAT).
- Connect Claude Code to a GitHub repository.
- View and manage GitHub Issues.
- Review Pull Requests.
- Inspect Commit history.

---

# Prerequisites

Ensure you have the following:

- Claude Code installed
- Git installed
- GitHub account
- GitHub Personal Access Token (PAT)

Recommended GitHub PAT permissions:

- Repository Contents
- Pull Requests
- Issues
- Metadata

---

# Exercise 1 – Create a GitHub Personal Access Token

1. Sign in to GitHub.
2. Navigate to:

```
Settings
→ Developer Settings
→ Personal Access Tokens
→ Fine-grained Token
```

3. Create a new token with the required repository permissions.
4. Copy the generated token securely.

---

# Exercise 2 – Configure the GitHub MCP Server

Open a terminal and run:

```bash
claude mcp add github \
  --transport stdio \
  --env GITHUB_TOKEN=YOUR_GITHUB_PAT \
  -- npx -y @modelcontextprotocol/server-github
```

Replace `YOUR_GITHUB_PAT` with your GitHub Personal Access Token.

Verify the configuration:

```bash
claude mcp list
```

Expected output:

```
github
Status: Enabled
Transport: stdio
```

---

# Exercise 3 – Start Claude Code

Navigate to a local Git repository.

```bash
cd <your-repository>
```

Launch Claude Code:

```bash
claude
```

---

# Exercise 4 – Working with GitHub Issues

### Prompt 1

```
List all open issues in this repository.
```

### Prompt 2

```
Summarize issue #15.
```

### Prompt 3

```
Create a new issue titled "Application timeout during file upload" with a description explaining that uploads larger than 100 MB fail with a timeout.
```

---

# Exercise 5 – Working with Pull Requests

### Prompt 1

```
List all open pull requests.
```

### Prompt 2

```
Summarize pull request #24.
```

### Prompt 3

```
Show the files changed in pull request #24.
```

---

# Exercise 6 – Review a Pull Request

Ask Claude:

```
Review pull request #24 and provide:

- Summary of changes
- Potential bugs
- Code quality improvements
- Security observations
- Suggested review comments
```

---

# Exercise 7 – View Commit History

### Prompt 1

```
Show the latest 10 commits.
```

### Prompt 2

```
Who last modified the authentication module?
```

### Prompt 3

```
Show all commits made during the last seven days.
```

---

# Challenge Exercise

Using a single prompt, ask Claude to:

```
1. List all open pull requests.
2. Identify the most recently updated PR.
3. Review that PR.
4. Show the latest commits related to it.
5. Summarize any linked GitHub issues.
```

---

# Security Best Practices

- Never hardcode GitHub Personal Access Tokens.
- Store tokens using environment variables or a secure secret manager.
- Grant only the permissions required for your tasks.
- Rotate tokens regularly.
- Revoke unused or compromised tokens.

---

# Troubleshooting

| Problem | Solution |
|----------|----------|
| GitHub MCP Server not detected | Verify the configuration using `claude mcp list`. |
| Authentication failed | Check that the GitHub PAT is valid and has the required permissions. |
| Permission denied | Ensure the PAT has access to the target repository. |
| Repository not found | Confirm you have access to the repository and are in the correct local Git repository. |

---

# Lab Summary

After completing this lab, you should be able to:

- Configure the GitHub MCP Server in Claude Code.
- Authenticate with GitHub using a Personal Access Token.
- View and manage GitHub Issues.
- View and review Pull Requests.
- Inspect repository Commit history.
- Use Claude Code to perform common GitHub workflows using natural language.
