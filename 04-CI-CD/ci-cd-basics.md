# CI/CD Basics

CI/CD (Continuous Integration and Continuous Delivery/Deployment) is one of the most important DevOps practices. It automates the process of building, testing, and deploying applications, enabling development teams to deliver software faster, more reliably, and with fewer errors.

In modern software development, CI/CD helps teams continuously integrate code changes, automatically test applications, and deploy them to different environments with minimal manual intervention.

---

# Table of Contents

- Introduction to CI/CD
- What is DevOps?
- Software Development Life Cycle (SDLC)
- Problems Before CI/CD
- What is Continuous Integration (CI)?
- What is Continuous Delivery (CD)?
- What is Continuous Deployment
- CI vs Continuous Delivery vs Continuous Deployment
- Benefits of CI/CD
- CI/CD Workflow
- Azure DevOps Overview
- Azure DevOps Services
- Azure Repos
- Azure Pipelines

---

# Introduction to CI/CD

CI/CD is a software development practice that automates application delivery.

CI/CD stands for:

- Continuous Integration
- Continuous Delivery
- Continuous Deployment

The primary objective is to deliver software quickly while maintaining high quality.

Instead of manually building, testing, and deploying applications, CI/CD automates these tasks.

---

# What is DevOps?

DevOps is a combination of **Development (Dev)** and **Operations (Ops)**.

It is a culture and set of practices that improve collaboration between developers and operations teams by automating software delivery.

```text
Developer

↓

Build

↓

Test

↓

Release

↓

Deploy

↓

Monitor

↓

Feedback
```

DevOps focuses on:

- Automation
- Continuous Improvement
- Faster Delivery
- Collaboration
- Reliability

---

# Software Development Life Cycle (SDLC)

The Software Development Life Cycle (SDLC) defines the process of developing software from planning to maintenance.

```text
Planning

↓

Requirement Analysis

↓

Design

↓

Development

↓

Testing

↓

Deployment

↓

Maintenance
```

Each phase contributes to delivering a reliable software product.

---

# Problems Before CI/CD

Before CI/CD, software deployment was largely manual.

Common challenges included:

- Manual builds
- Manual testing
- Manual deployments
- Long release cycles
- Frequent integration conflicts
- Human errors
- Slow feedback
- Production failures

Example:

```text
Developer A

↓

Developer B

↓

Developer C

↓

Manual Merge

↓

Manual Testing

↓

Manual Deployment

↓

Production
```

This process was slow and error-prone.

---

# What is Continuous Integration (CI)?

Continuous Integration (CI) is the practice of automatically integrating code changes from multiple developers into a shared repository.

Whenever a developer pushes code, the CI pipeline automatically:

- Retrieves the latest code
- Restores dependencies
- Builds the application
- Executes automated tests
- Reports build status

```text
Developer

↓

Git Push

↓

Repository

↓

Build

↓

Test

↓

Success / Failure
```

Advantages

- Early bug detection
- Faster feedback
- Improved code quality
- Fewer merge conflicts
- Automated testing

Example

A developer commits new code to GitHub.

The CI pipeline automatically:

- Downloads the latest code
- Compiles the application
- Executes unit tests
- Reports the result

If any step fails, the developer is immediately notified.

---

# What is Continuous Delivery (CD)?

Continuous Delivery extends Continuous Integration by automatically preparing applications for deployment.

After a successful build and test, the application is deployed to environments such as Development, Testing, or Staging.

Deployment to Production usually requires manual approval.

```text
Build

↓

Test

↓

Artifact

↓

Development

↓

Testing

↓

Manual Approval

↓

Production
```

Advantages

- Faster releases
- Reliable deployments
- Reduced deployment risk
- Consistent release process

---

# What is Continuous Deployment?

Continuous Deployment goes one step further than Continuous Delivery.

Every successful build is automatically deployed to production without manual approval.

```text
Developer

↓

Build

↓

Test

↓

Deploy to Production

↓

Users
```

Advantages

- Fully automated releases
- Faster feature delivery
- No manual deployment

Disadvantages

- Requires extensive automated testing
- Higher risk if testing is insufficient

---

# CI vs Continuous Delivery vs Continuous Deployment

| Feature | Continuous Integration | Continuous Delivery | Continuous Deployment |
|----------|------------------------|---------------------|-----------------------|
| Build Automation | ✔ | ✔ | ✔ |
| Automated Testing | ✔ | ✔ | ✔ |
| Artifact Creation | ✔ | ✔ | ✔ |
| Deployment to Test Environment | ✘ | ✔ | ✔ |
| Manual Approval | ✘ | ✔ | ✘ |
| Automatic Production Deployment | ✘ | ✘ | ✔ |

---

# Benefits of CI/CD

Implementing CI/CD provides several advantages:

- Faster software delivery
- Automated testing
- Improved code quality
- Faster bug detection
- Consistent deployments
- Reduced manual effort
- Better collaboration
- Faster feedback
- Reliable releases
- Improved customer satisfaction

---

# CI/CD Workflow

A typical CI/CD workflow looks like this:

```text
Developer

↓

Git Push

↓

Azure Repos / GitHub

↓

Continuous Integration

↓

Build

↓

Test

↓

Publish Artifact

↓

Continuous Delivery

↓

Development Environment

↓

Testing Environment

↓

Approval

↓

Production
```

Each stage is automated to reduce manual intervention and improve reliability.

---

# Azure DevOps Overview

Azure DevOps is Microsoft's cloud platform for managing the entire software development lifecycle.

It provides tools for planning, source control, continuous integration, continuous delivery, testing, and package management.

Azure DevOps supports:

- GitHub
- Azure Repos
- Azure Pipelines
- Docker
- Kubernetes
- Terraform
- Jenkins
- Maven
- Gradle
- .NET
- Java
- Node.js
- Python

---

# Azure DevOps Services

Azure DevOps consists of five primary services.

| Service | Purpose |
|----------|----------|
| Azure Boards | Project management and work tracking |
| Azure Repos | Git repositories |
| Azure Pipelines | CI/CD automation |
| Azure Test Plans | Manual and exploratory testing |
| Azure Artifacts | Package management |

```text
Azure DevOps

│

├── Boards

├── Repos

├── Pipelines

├── Test Plans

└── Artifacts
```

---

# Azure Repos

Azure Repos provides Git repositories for source code management.

Features include:

- Unlimited private Git repositories
- Branch management
- Pull Requests
- Code Reviews
- Merge Policies

Typical workflow:

```text
Developer

↓

Commit

↓

Push

↓

Azure Repos

↓

Pull Request

↓

Merge

↓

Main Branch
```

---

# Azure Pipelines

Azure Pipelines is Azure DevOps' CI/CD service.

It automates:

- Build
- Test
- Package
- Deploy

Supported platforms include:

- Windows
- Linux
- macOS

Supported languages:

- .NET
- Java
- Python
- Node.js
- Go
- PHP
- C++
- Android
- iOS

Azure Pipelines can deploy applications to:

- Azure App Service
- Azure Virtual Machines
- Kubernetes
- Docker
- AWS
- Google Cloud
- On-premises Servers

Typical pipeline:

```text
Source Code

↓

Restore Dependencies

↓

Build

↓

Run Tests

↓

Publish Artifact

↓

Deploy
```

Azure Pipelines supports both:

- Classic Pipelines (GUI-based)
- YAML Pipelines (Code-based)

---

# Build Pipeline

A Build Pipeline is the Continuous Integration (CI) part of a CI/CD pipeline.

Its primary purpose is to automatically build, compile, test, and package an application whenever new code is pushed to the repository.

Instead of manually compiling code, Azure Pipelines performs these tasks automatically.

---

## Build Pipeline Workflow

```text
Developer

↓

Git Push

↓

Azure Repos / GitHub

↓

Restore Dependencies

↓

Build

↓

Run Tests

↓

Publish Artifact
```

---

## Stages of a Build Pipeline

### Restore Dependencies

Downloads all required packages and libraries.

Examples:

- NuGet Packages (.NET)
- npm Packages (Node.js)
- Maven Dependencies (Java)

---

### Build

Compiles the application source code.

Example:

```text
Source Code

↓

Compiler

↓

Application Build
```

---

### Test

Runs automated tests.

Examples:

- Unit Tests
- Integration Tests
- Functional Tests

If tests fail, the pipeline stops.

---

### Publish Artifact

After a successful build, Azure creates an Artifact.

Artifacts may include:

- ZIP files
- DLL files
- Executables
- Docker Images

These artifacts are later used by the Release Pipeline.

---

# Release Pipeline

A Release Pipeline is responsible for deploying the application to one or more environments.

Unlike the Build Pipeline, it focuses on deployment rather than compilation.

---

## Release Pipeline Workflow

```text
Build Artifact

↓

Development

↓

Testing

↓

Approval

↓

Production
```

Each stage can contain different deployment tasks.

---

## Why Use a Release Pipeline?

Advantages

- Automated deployments
- Reduced deployment errors
- Consistent release process
- Supports approvals
- Supports rollback strategies

---

# Multi-stage Pipeline

A Multi-stage Pipeline combines Build and Release into a single pipeline.

Instead of creating separate pipelines, all stages are defined together.

```text
Source Code

↓

Build

↓

Test

↓

Publish Artifact

↓

Development

↓

Testing

↓

Approval

↓

Production
```

Advantages

- Easier management
- Single YAML file
- Better visibility
- Faster deployments

---

# Pipeline Components

Azure Pipelines are built using several components.

```
Pipeline

│

├── Stages

├── Jobs

├── Steps

├── Tasks

├── Variables

├── Artifacts

└── Agents
```

---

## Stage

A Stage represents a major phase of the pipeline.

Examples

- Build
- Development
- Testing
- Production

---

## Job

Each Stage contains one or more Jobs.

A Job runs on an Agent.

Example

```
Stage

↓

Job

↓

Agent
```

---

## Step

A Job contains multiple Steps.

Each Step performs one action.

Examples

- Restore Packages
- Build
- Test
- Publish

---

## Task

A Task is the smallest executable unit inside a pipeline.

Examples

- Copy Files
- Publish Build Artifact
- Deploy Azure App Service
- Docker Build
- Kubernetes Deployment

---

# Microsoft-hosted Agents

Microsoft-hosted Agents are virtual machines managed by Microsoft.

Whenever a pipeline starts:

- Azure creates a temporary VM.
- Executes the pipeline.
- Deletes the VM after completion.

```text
Pipeline

↓

Microsoft-hosted Agent

↓

Execute Pipeline

↓

Delete VM
```

Advantages

- No maintenance
- Always updated
- Easy to use

Disadvantages

- Limited customization
- Usage limits on free plans

---

# Self-hosted Agents

Self-hosted Agents run on your own machine or server.

Example

```text
Azure DevOps

↓

Your Server

↓

Agent

↓

Pipeline Execution
```

Advantages

- Full control
- Custom software
- Faster builds for internal projects

Disadvantages

- Requires maintenance
- You manage updates
- Hardware responsibility

---

# Microsoft-hosted vs Self-hosted Agents

| Microsoft-hosted | Self-hosted |
|------------------|------------|
| Managed by Microsoft | Managed by User |
| Temporary VM | Permanent Machine |
| Automatically Updated | Manual Updates |
| Easy Setup | Requires Configuration |
| Limited Customization | Fully Customizable |

---

# Agent Pools

An Agent Pool is a collection of one or more agents.

Pipelines select an available agent from the pool.

Example

```text
Agent Pool

│

├── Agent 1

├── Agent 2

└── Agent 3
```

Benefits

- Better resource utilization
- Parallel builds
- Load balancing

---

# Environments

Environments represent deployment targets.

Examples

- Development
- Testing
- Staging
- Production

Example

```text
Build

↓

Development

↓

Testing

↓

Production
```

Environments help manage deployments and approvals.

---

# Approvals & Checks

Approvals ensure deployments occur only after authorization.

Example

```text
Deploy to Development

↓

Testing

↓

Manager Approval

↓

Production
```

Types of Checks

- Manual Approval
- Business Hours
- Azure Policy
- Branch Control

---

# Variables

Variables store reusable values.

Examples

```text
BuildNumber

Environment

Version

ResourceGroup

Subscription
```

Benefits

- Reusability
- Easy updates
- Cleaner pipelines

---

# Variable Groups

Variable Groups allow multiple pipelines to share variables.

Example

```text
Variable Group

│

├── Resource Group

├── Subscription

├── Environment

└── App Service Name
```

Advantages

- Centralized management
- Reuse across pipelines
- Easier maintenance

---

# Secret Variables

Secret Variables store sensitive information securely.

Examples

- Passwords
- API Keys
- Tokens
- Connection Strings

Secret values are masked during pipeline execution.

Example

```text
Password

↓

********
```

Never store sensitive information directly in YAML files.

---

# Service Connections

Service Connections allow Azure DevOps to authenticate with external services.

Common Service Connections

- Azure Resource Manager
- GitHub
- Docker Hub
- Kubernetes
- AWS
- ServiceNow

Example

```text
Azure DevOps

↓

Service Connection

↓

Azure Subscription

↓

Deploy Resources
```

Without a Service Connection, Azure DevOps cannot deploy resources to Azure.

---

# Artifacts

Artifacts are files generated during the Build Pipeline.

Examples

- ZIP Files
- DLL Files
- Docker Images
- JAR Files
- WAR Files

Workflow

```text
Build

↓

Artifact

↓

Release Pipeline

↓

Deployment
```

Artifacts ensure the exact same build is deployed across all environments.

---

# Pipeline Triggers

Pipeline Triggers define when a pipeline should start automatically.

Instead of manually running a pipeline, Azure DevOps can trigger it based on specific events.

---

## Types of Pipeline Triggers

- Continuous Integration (CI) Trigger
- Pull Request (PR) Trigger
- Scheduled Trigger
- Manual Trigger

---

## Continuous Integration (CI) Trigger

A CI Trigger automatically starts the pipeline whenever new code is pushed to the repository.

```text
Developer

↓

Git Push

↓

Azure Repos / GitHub

↓

Pipeline Starts Automatically
```

Benefits

- Immediate feedback
- Automatic builds
- Faster bug detection

---

## Pull Request (PR) Trigger

A PR Trigger runs whenever a Pull Request is created or updated.

```text
Feature Branch

↓

Create Pull Request

↓

Pipeline Runs

↓

Merge if Successful
```

Benefits

- Validates code before merging
- Prevents broken code from reaching the main branch

---

## Scheduled Trigger

Runs pipelines at a specified time.

Example

```text
Every Day

↓

10:00 PM

↓

Run Pipeline
```

Common Uses

- Nightly Builds
- Automated Testing
- Backup Jobs

---

## Manual Trigger

The pipeline starts only when a user manually clicks **Run Pipeline**.

Used when deployments require manual control.

---

# YAML Pipelines

YAML Pipelines define the entire CI/CD process using code stored in the repository.

Example

```yaml
trigger:
- main

pool:
  vmImage: ubuntu-latest

steps:

- script: echo "Building Application"

- script: echo "Running Tests"

- script: echo "Deploying Application"
```

Advantages

- Version controlled
- Easy to review
- Reusable
- Infrastructure as Code approach

---

# Classic Pipelines

Classic Pipelines use the Azure DevOps graphical user interface (GUI) instead of YAML.

Users create pipelines by dragging and configuring tasks.

```text
Azure DevOps

↓

Classic Pipeline

↓

Add Tasks

↓

Save

↓

Run
```

Advantages

- Easy for beginners
- No YAML knowledge required

Disadvantages

- Harder to version control
- Limited flexibility
- Difficult to maintain for large projects

---

# YAML vs Classic Pipelines

| YAML Pipelines | Classic Pipelines |
|----------------|------------------|
| Pipeline defined as code | Pipeline created using GUI |
| Version controlled | Configuration stored in Azure DevOps |
| Easy to review | Harder to review |
| Reusable | Less reusable |
| Preferred for modern DevOps | Good for beginners |

Microsoft recommends using **YAML Pipelines** for new projects.

---

# Azure CLI Commands

## Login to Azure

```bash
az login
```

Authenticates your Azure account.

---

## List Resource Groups

```bash
az group list --output table
```

Displays all Resource Groups.

---

## List App Services

```bash
az webapp list --output table
```

Displays all Azure App Services.

---

## List Virtual Machines

```bash
az vm list --output table
```

Displays all Virtual Machines.

---

## List Storage Accounts

```bash
az storage account list --output table
```

Displays all Storage Accounts.

---

## Show Current Subscription

```bash
az account show
```

Displays the active Azure subscription.

---

## List Azure Subscriptions

```bash
az account list --output table
```

Displays all available Azure subscriptions.

---

## Set Active Subscription

```bash
az account set --subscription "Subscription Name"
```

Changes the active Azure subscription.

---

# Common Pipeline Errors

## Build Failed

Possible Causes

- Compilation errors
- Missing dependencies
- Incorrect project configuration

Solution

- Review build logs
- Restore dependencies
- Fix compilation errors

---

## Test Failed

Possible Causes

- Unit test failures
- Integration issues
- Incorrect test configuration

Solution

- Analyze test reports
- Fix failing tests
- Re-run pipeline

---

## Authentication Failed

Possible Causes

- Expired credentials
- Invalid Service Connection
- Incorrect permissions

Solution

- Verify Service Connection
- Check Azure credentials
- Assign proper RBAC permissions

---

## Deployment Failed

Possible Causes

- Incorrect App Service
- Wrong Resource Group
- Invalid deployment package

Solution

- Verify deployment target
- Check deployment logs
- Confirm artifact availability

---

## Agent Not Available

Possible Causes

- No available agents
- Agent offline
- Agent pool issues

Solution

- Start the self-hosted agent
- Verify Agent Pool
- Retry pipeline execution

---

# Hands-on Lab

## Objective

Create a complete CI/CD pipeline using Azure DevOps.

---

## Prerequisites

- Azure Subscription
- Azure DevOps Project
- Git Repository
- Azure App Service
- Service Connection

---

## Step 1

Create an Azure DevOps Project.

---

## Step 2

Import or connect your GitHub repository.

---

## Step 3

Create a Build Pipeline.

Tasks:

- Restore dependencies
- Build application
- Run tests
- Publish artifacts

---

## Step 4

Run the Build Pipeline.

Verify that:

- Build succeeds
- Tests pass
- Artifact is generated

---

## Step 5

Create an Environment.

Example

```text
Development
```

---

## Step 6

Configure a Service Connection.

Grant Azure DevOps permission to deploy resources.

---

## Step 7

Create a Multi-stage Pipeline.

Stages

```text
Build

↓

Development

↓

Testing

↓

Production
```

---

## Step 8

Add an Approval before Production deployment.

Example

```text
Development

↓

Approval

↓

Production
```

---

## Step 9

Run the Pipeline.

Observe:

- Build
- Test
- Artifact
- Deployment
- Approval
- Production Deployment

---

## Step 10

Verify the deployed application.

Open the deployed Azure App Service in a browser and confirm that the latest version of the application is running.

---

# Real-World CI/CD Flow

```text
Developer

↓

Git Commit

↓

Git Push

↓

Azure Repos / GitHub

↓

CI Pipeline

↓

Restore Packages

↓

Build

↓

Run Tests

↓

Publish Artifact

↓

CD Pipeline

↓

Development

↓

Testing

↓

Approval

↓

Production

↓

Users
```

