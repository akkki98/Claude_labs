# Lab: DevOps and Automation with Claude

## Objective

In this lab, you will use **Claude** to automate common DevOps tasks across the software development lifecycle. You will learn how Claude can assist with infrastructure automation, CI/CD pipeline creation, Docker, Kubernetes, Infrastructure as Code (IaC), monitoring, troubleshooting, and documentation.

---

# Learning Outcomes

By the end of this lab, you will be able to:

- Use Claude to automate DevOps workflows
- Generate Infrastructure as Code (IaC)
- Create CI/CD pipelines
- Build Dockerfiles and Docker Compose configurations
- Generate Kubernetes manifests
- Troubleshoot deployment issues
- Create monitoring and alerting configurations
- Automate scripting tasks
- Review infrastructure for security best practices
- Generate DevOps documentation

---

# Prerequisites

- Claude (Web, Desktop, or Claude Code)
- Git installed
- Docker Desktop
- Kubernetes cluster (Kind, Minikube, or AKS)
- VS Code
- Azure DevOps or GitHub repository
- Basic knowledge of Git, Docker, and Kubernetes

---

# Lab Repository

Use any sample application, for example:

- Node.js Web Application
- Python Flask API
- Java Spring Boot Application
- .NET Web API

Repository structure:

```text
sample-app/
├── src/
├── tests/
├── Dockerfile
├── docker-compose.yml
└── README.md
```

---

# Exercise 1: Understand the Application

## Objective

Analyze an existing application before automating deployment.

### Tasks

Open the project in Claude and ask:

> Explain the architecture of this application.

> Identify the technology stack.

> List external dependencies.

> Recommend improvements for deployment readiness.

### Expected Outcome

Claude provides:

- Application architecture overview
- Technology stack summary
- Dependency analysis
- Deployment recommendations

---

# Exercise 2: Generate Docker Configuration

## Objective

Containerize the application.

### Tasks

Ask Claude:

> Create an optimized Dockerfile for this application.

> Generate a docker-compose.yml for local development.

> Recommend multi-stage builds.

> Reduce the Docker image size.

### Expected Outcome

Generated:

- Dockerfile
- Docker Compose configuration
- Build optimization recommendations

---

# Exercise 3: Create a CI Pipeline

## Objective

Automate application builds.

### Tasks

Ask Claude:

> Generate a GitHub Actions workflow.

> Create an Azure DevOps YAML pipeline.

Include:

- Restore dependencies
- Build
- Unit tests
- Code quality checks
- Publish build artifacts

### Expected Outcome

Working CI pipeline YAML.

---

# Exercise 4: Create a CD Pipeline

## Objective

Automate deployments.

### Tasks

Ask Claude:

> Extend the pipeline to deploy automatically after a successful build.

Include:

- Development deployment
- Staging deployment
- Production approval
- Rollback strategy

### Expected Outcome

Complete CI/CD pipeline.

---

# Exercise 5: Infrastructure as Code

## Objective

Provision infrastructure using IaC.

### Tasks

Ask Claude:

> Generate Terraform code to deploy:

- Resource Group
- Storage Account
- Virtual Network
- Kubernetes Cluster
- Container Registry

Then ask:

> Explain every Terraform resource.

### Expected Outcome

Terraform project with explanations.

---

# Exercise 6: Kubernetes Deployment

## Objective

Deploy the application to Kubernetes.

### Tasks

Ask Claude:

Generate:

- Deployment
- Service
- ConfigMap
- Secret
- Ingress
- Horizontal Pod Autoscaler

Then ask:

> Explain how these resources work together.

### Expected Outcome

Complete Kubernetes manifests.

---

# Exercise 7: Helm Chart Generation

## Objective

Package the application for Kubernetes.

### Tasks

Ask Claude:

> Create a Helm chart for this application.

Include:

- values.yaml
- deployment.yaml
- service.yaml
- ingress.yaml

### Expected Outcome

Deployable Helm chart.

---

# Exercise 8: Monitoring and Logging

## Objective

Improve application observability.

### Tasks

Ask Claude:

> Recommend monitoring for this application.

Generate:

- Prometheus configuration
- Grafana dashboard ideas
- Alert rules
- Logging strategy

### Expected Outcome

Monitoring configuration and recommendations.

---

# Exercise 9: Troubleshooting Production Issues

## Objective

Use Claude as a DevOps troubleshooting assistant.

### Scenario

The deployment fails because pods are in **CrashLoopBackOff**.

### Tasks

Ask Claude:

> Explain possible causes.

> Recommend debugging steps.

> Suggest kubectl commands.

> Recommend a permanent fix.

Repeat for:

- ImagePullBackOff
- Pending Pods
- Failed Liveness Probe
- Failed Readiness Probe
- High CPU Usage

### Expected Outcome

Root cause analysis and troubleshooting guidance.

---

# Exercise 10: Security Review

## Objective

Improve infrastructure security.

### Tasks

Ask Claude:

Review:

- Dockerfile
- Kubernetes manifests
- CI/CD pipeline
- Terraform code

Identify:

- Hardcoded secrets
- Excessive permissions
- Security risks
- Best practice violations

### Expected Outcome

Security review with remediation recommendations.

---

# Exercise 11: Automation Scripts

## Objective

Automate operational tasks.

### Tasks

Ask Claude to generate scripts for:

- Backup logs
- Rotate logs
- Deploy application
- Restart services
- Scale Kubernetes workloads
- Clean Docker images
- Validate deployments

Use:

- Bash
- PowerShell

### Expected Outcome

Reusable automation scripts.

---

# Exercise 12: Documentation Generation

## Objective

Generate DevOps documentation.

### Tasks

Ask Claude:

Generate:

- Deployment Guide
- Operations Runbook
- Disaster Recovery Plan
- Infrastructure Documentation
- Troubleshooting Guide

### Expected Outcome

Complete operational documentation.

---

# Exercise 13: Code and Pipeline Review

## Objective

Improve quality before deployment.

### Tasks

Ask Claude:

Review:

- YAML pipelines
- Dockerfile
- Kubernetes manifests
- Terraform modules

Recommend:

- Performance improvements
- Cost optimization
- Security enhancements
- Maintainability improvements

### Expected Outcome

Actionable review recommendations.

---

# Challenge Exercise

You have been assigned to automate the deployment of a web application.

Using Claude:

1. Analyze the application.
2. Containerize the application.
3. Generate Docker Compose.
4. Create a CI pipeline.
5. Create a CD pipeline.
6. Generate Terraform infrastructure.
7. Deploy to Kubernetes.
8. Package using Helm.
9. Configure monitoring.
10. Perform a security review.
11. Generate operational documentation.
12. Troubleshoot a simulated deployment failure.

---

# Best Practices

- Keep infrastructure in version control.
- Validate generated YAML before deployment.
- Review AI-generated code before production use.
- Never store secrets in source code.
- Use reusable Infrastructure as Code modules.
- Automate testing before deployment.
- Apply least privilege principles.
- Include rollback and disaster recovery plans in deployment workflows.

---

# Success Criteria

You have successfully completed this lab if you can:

- Analyze an application's deployment requirements
- Containerize applications with Docker
- Build CI/CD pipelines
- Generate Infrastructure as Code
- Deploy applications to Kubernetes
- Package applications using Helm
- Configure monitoring and logging
- Troubleshoot deployment failures
- Review infrastructure for security
- Generate production-ready DevOps documentation

---

# Skills Practiced

- AI-assisted DevOps
- Docker
- Kubernetes
- Helm
- Infrastructure as Code (Terraform)
- CI/CD pipelines
- GitHub Actions
- Azure DevOps Pipelines
- Monitoring and Observability
- Bash and PowerShell automation
- DevOps troubleshooting
- Security best practices
- Technical documentation
