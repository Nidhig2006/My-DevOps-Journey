# CI/CD Interview Questions

This document contains commonly asked CI/CD and Azure DevOps interview questions with detailed answers.

---

<details>
<summary><strong>1. What is DevOps?</strong></summary>

DevOps is a combination of **Development (Dev)** and **Operations (Ops)**. It is a culture, set of practices, and tools that improve collaboration between development and operations teams by automating software development, testing, deployment, and monitoring.

Benefits include:

- Faster software delivery
- Better collaboration
- Automation
- Continuous feedback
- Improved reliability

</details>

---

<details>
<summary><strong>2. What is CI/CD?</strong></summary>

CI/CD stands for:

- Continuous Integration (CI)
- Continuous Delivery (CD)
- Continuous Deployment

CI/CD automates the process of building, testing, and deploying software, enabling faster and more reliable releases.

</details>

---

<details>
<summary><strong>3. What is Continuous Integration (CI)?</strong></summary>

Continuous Integration is the practice of automatically integrating code changes into a shared repository.

Whenever a developer pushes code:

- Source code is downloaded
- Dependencies are restored
- Application is built
- Automated tests are executed

If everything succeeds, the build is marked successful.

</details>

---

<details>
<summary><strong>4. What is Continuous Delivery?</strong></summary>

Continuous Delivery automatically prepares applications for deployment after a successful build.

The deployment to production usually requires manual approval.

</details>

---

<details>
<summary><strong>5. What is Continuous Deployment?</strong></summary>

Continuous Deployment automatically deploys every successful build directly to production without requiring manual approval.

This requires extensive automated testing to ensure reliability.

</details>

---

<details>
<summary><strong>6. What is the difference between Continuous Delivery and Continuous Deployment?</strong></summary>

| Continuous Delivery | Continuous Deployment |
|---------------------|----------------------|
| Manual approval before production | No manual approval |
| Human intervention required | Fully automated |
| Lower deployment risk | Faster releases |

</details>

---

<details>
<summary><strong>7. Why is CI/CD important?</strong></summary>

CI/CD provides several benefits:

- Faster releases
- Better code quality
- Automated testing
- Reduced manual effort
- Faster feedback
- Reliable deployments

</details>

---

<details>
<summary><strong>8. What is Azure DevOps?</strong></summary>

Azure DevOps is Microsoft's cloud platform for planning, developing, testing, and deploying applications.

It provides integrated services such as:

- Azure Boards
- Azure Repos
- Azure Pipelines
- Azure Test Plans
- Azure Artifacts

</details>

---

<details>
<summary><strong>9. What are Azure DevOps Services?</strong></summary>

Azure DevOps provides five major services:

- Azure Boards
- Azure Repos
- Azure Pipelines
- Azure Test Plans
- Azure Artifacts

These services support the complete software development lifecycle.

</details>

---

<details>
<summary><strong>10. What is Azure Repos?</strong></summary>

Azure Repos is Microsoft's Git repository service used for storing and managing source code.

Features include:

- Git repositories
- Branching
- Pull Requests
- Code Reviews
- Merge Policies

</details>

---

<details>
<summary><strong>11. What is Azure Pipelines?</strong></summary>

Azure Pipelines is the CI/CD service of Azure DevOps.

It automates:

- Build
- Test
- Package
- Deploy

It supports Windows, Linux, and macOS.

</details>

---

<details>
<summary><strong>12. What is a Build Pipeline?</strong></summary>

A Build Pipeline automatically:

- Restores dependencies
- Builds the application
- Runs tests
- Publishes build artifacts

It represents the Continuous Integration (CI) stage.

</details>

---

<details>
<summary><strong>13. What is a Release Pipeline?</strong></summary>

A Release Pipeline deploys build artifacts to different environments such as:

- Development
- Testing
- Production

It represents the Continuous Delivery process.

</details>

---

<details>
<summary><strong>14. What is a Multi-stage Pipeline?</strong></summary>

A Multi-stage Pipeline combines build and deployment stages into a single pipeline.

Example stages:

- Build
- Development
- Testing
- Production

This simplifies pipeline management.

</details>

---

<details>
<summary><strong>15. What is an Artifact?</strong></summary>

An Artifact is the output generated after a successful build.

Examples include:

- ZIP files
- DLL files
- Executables
- Docker Images

Artifacts are deployed by Release Pipelines.

</details>

---

<details>
<summary><strong>16. What is an Agent in Azure DevOps?</strong></summary>

An Agent is a machine that executes pipeline jobs.

It performs tasks such as:

- Building
- Testing
- Deploying

Agents can be Microsoft-hosted or Self-hosted.

</details>

---

<details>
<summary><strong>17. What is a Microsoft-hosted Agent?</strong></summary>

A Microsoft-hosted Agent is a temporary virtual machine managed by Microsoft.

Advantages:

- No maintenance
- Always updated
- Easy to use

</details>

---

<details>
<summary><strong>18. What is a Self-hosted Agent?</strong></summary>

A Self-hosted Agent runs on your own machine or server.

Advantages:

- Full control
- Custom software installation
- Better for private environments

</details>

---

<details>
<summary><strong>19. What is an Agent Pool?</strong></summary>

An Agent Pool is a collection of agents used to execute pipelines.

Pipelines automatically select an available agent from the pool.

</details>

---

<details>
<summary><strong>20. What are Environments in Azure DevOps?</strong></summary>

Environments represent deployment targets.

Examples include:

- Development
- Testing
- Staging
- Production

They also support approvals and deployment history.

</details>

---

<details>
<summary><strong>21. What are Approvals in Azure DevOps?</strong></summary>

Approvals require authorization before deploying to an environment.

For example, production deployment may require manager approval before execution.

</details>

---

<details>
<summary><strong>22. What are Variables?</strong></summary>

Variables store reusable values used by pipelines.

Examples:

- Build Number
- Version
- Resource Group
- Environment Name

They reduce duplication and simplify pipeline configuration.

</details>

---

<details>
<summary><strong>23. What are Variable Groups?</strong></summary>

Variable Groups allow multiple pipelines to share the same set of variables.

This centralizes configuration and improves maintainability.

</details>

---

<details>
<summary><strong>24. What are Secret Variables?</strong></summary>

Secret Variables securely store sensitive information such as:

- Passwords
- API Keys
- Access Tokens
- Connection Strings

Their values are hidden during pipeline execution.

</details>

---

<details>
<summary><strong>25. What is a Service Connection?</strong></summary>

A Service Connection securely connects Azure DevOps to external services such as:

- Azure Subscription
- GitHub
- Docker Hub
- Kubernetes
- AWS

It allows pipelines to authenticate and deploy resources without exposing credentials.

</details>
---

<details>
<summary><strong>26. What is an Artifact in Azure DevOps?</strong></summary>

An Artifact is the output produced after a successful build. It contains the files required for deployment.

Examples:

- ZIP files
- DLL files
- Executables
- Docker Images
- JAR/WAR files

Artifacts ensure that the same build is deployed across all environments.

</details>

---

<details>
<summary><strong>27. Why are Artifacts important?</strong></summary>

Artifacts provide a stable and reusable build output.

Benefits:

- Build once, deploy many times
- Consistent deployments
- Easy rollback
- Faster releases

</details>

---

<details>
<summary><strong>28. What is a YAML Pipeline?</strong></summary>

A YAML Pipeline defines the CI/CD process using a YAML configuration file stored in the repository.

Advantages:

- Version controlled
- Easy to review
- Reusable
- Infrastructure as Code approach

</details>

---

<details>
<summary><strong>29. What is a Classic Pipeline?</strong></summary>

A Classic Pipeline is created using the Azure DevOps graphical interface instead of YAML.

It is suitable for beginners but is less flexible than YAML pipelines.

</details>

---

<details>
<summary><strong>30. What is the difference between YAML and Classic Pipelines?</strong></summary>

| YAML Pipeline | Classic Pipeline |
|---------------|------------------|
| Pipeline as Code | GUI Based |
| Version Controlled | Stored in Azure DevOps |
| Easy to reuse | Less reusable |
| Preferred for modern DevOps | Suitable for beginners |

</details>

---

<details>
<summary><strong>31. What are Pipeline Triggers?</strong></summary>

Pipeline Triggers define when a pipeline should execute automatically.

Common triggers include:

- CI Trigger
- Pull Request Trigger
- Scheduled Trigger
- Manual Trigger

</details>

---

<details>
<summary><strong>32. What is a CI Trigger?</strong></summary>

A CI Trigger automatically starts a pipeline whenever code is pushed to the repository.

Benefits:

- Immediate feedback
- Automatic builds
- Faster bug detection

</details>

---

<details>
<summary><strong>33. What is a Pull Request (PR) Trigger?</strong></summary>

A PR Trigger runs the pipeline whenever a Pull Request is created or updated.

It verifies that the changes build successfully before they are merged into the main branch.

</details>

---

<details>
<summary><strong>34. What is a Scheduled Trigger?</strong></summary>

A Scheduled Trigger executes a pipeline automatically at a specified date and time.

Common Uses:

- Nightly Builds
- Automated Testing
- Database Backups

</details>

---

<details>
<summary><strong>35. What is a Manual Trigger?</strong></summary>

A Manual Trigger starts a pipeline only when a user selects **Run Pipeline** in Azure DevOps.

It provides complete control over pipeline execution.

</details>

---

<details>
<summary><strong>36. What is the difference between Build Pipeline and Release Pipeline?</strong></summary>

| Build Pipeline | Release Pipeline |
|----------------|------------------|
| Builds the application | Deploys the application |
| Compiles source code | Uses build artifacts |
| Executes tests | Deploys to environments |
| Represents CI | Represents CD |

</details>

---

<details>
<summary><strong>37. What is the purpose of a Service Connection?</strong></summary>

A Service Connection allows Azure DevOps to securely connect with external services such as:

- Azure Subscription
- GitHub
- Docker Hub
- Kubernetes
- AWS

Without a Service Connection, Azure DevOps cannot deploy resources.

</details>

---

<details>
<summary><strong>38. Why are Secret Variables used?</strong></summary>

Secret Variables securely store sensitive information.

Examples include:

- Passwords
- API Keys
- Access Tokens
- Connection Strings

Their values are hidden during pipeline execution.

</details>

---

<details>
<summary><strong>39. What happens when a Build Pipeline fails?</strong></summary>

If the Build Pipeline fails:

- The pipeline stops immediately.
- Artifacts are not published.
- Deployment does not occur.
- Developers review the logs, fix the issue, and rerun the pipeline.

</details>

---

<details>
<summary><strong>40. What happens if automated tests fail?</strong></summary>

If automated tests fail:

- The build is marked as failed.
- Deployment is stopped.
- Developers analyze the failed tests, fix the issue, and rerun the pipeline.

This prevents defective code from reaching production.

</details>

---

<details>
<summary><strong>41. Why should production deployments require approvals?</strong></summary>

Approvals add an additional layer of control before production deployments.

Benefits:

- Prevent accidental deployments
- Ensure quality checks
- Meet organizational compliance requirements

</details>

---

<details>
<summary><strong>42. What is the difference between Microsoft-hosted and Self-hosted Agents?</strong></summary>

Microsoft-hosted Agents:

- Managed by Microsoft
- Temporary virtual machines
- Automatically updated

Self-hosted Agents:

- Managed by the organization
- Installed on local servers or virtual machines
- Fully customizable

</details>

---

<details>
<summary><strong>43. Explain a typical CI/CD workflow.</strong></summary>

A typical workflow is:

1. Developer writes code.
2. Code is pushed to GitHub or Azure Repos.
3. CI Pipeline builds the application.
4. Automated tests run.
5. Build artifacts are generated.
6. CD Pipeline deploys to Development.
7. Application is tested.
8. After approval, it is deployed to Production.

</details>

---

<details>
<summary><strong>44. What are the advantages of CI/CD?</strong></summary>

Advantages include:

- Faster software delivery
- Better collaboration
- Automated testing
- Reduced manual effort
- Higher software quality
- Reliable deployments
- Faster feedback

</details>

---

<details>
<summary><strong>45. Why is automation important in DevOps?</strong></summary>

Automation reduces manual work and improves consistency.

It helps teams:

- Build faster
- Test automatically
- Deploy reliably
- Reduce human errors
- Increase productivity

</details>

---

<details>
<summary><strong>46. Which Azure DevOps service stores source code?</strong></summary>

**Azure Repos** stores Git repositories and source code.

It supports:

- Branches
- Pull Requests
- Code Reviews
- Merge Policies

</details>

---

<details>
<summary><strong>47. Which Azure DevOps service is responsible for CI/CD?</strong></summary>

**Azure Pipelines** is responsible for Continuous Integration and Continuous Delivery/Deployment.

It automates:

- Build
- Test
- Package
- Deploy

</details>

---

<details>
<summary><strong>48. What is the purpose of Environments?</strong></summary>

Environments represent deployment targets.

Examples:

- Development
- Testing
- Staging
- Production

They help organize deployments and provide deployment history and approvals.

</details>

---

<details>
<summary><strong>49. What is the difference between CI and CD?</strong></summary>

| Continuous Integration | Continuous Delivery |
|-------------------------|--------------------|
| Integrates code changes | Deploys applications |
| Focuses on Build & Test | Focuses on Deployment |
| Generates Artifacts | Deploys Artifacts |

</details>

---

<details>
<summary><strong>50. Explain the complete CI/CD pipeline in simple terms.</strong></summary>

A CI/CD pipeline automates the software delivery process.

Workflow:

1. Developer writes code.
2. Code is committed and pushed to the repository.
3. CI Pipeline restores dependencies.
4. The application is built.
5. Automated tests are executed.
6. Build artifacts are created.
7. CD Pipeline deploys the artifacts to Development.
8. Testing is performed.
9. After approval, the application is deployed to Production.

This process ensures faster, reliable, and consistent software delivery with minimal manual intervention.

</details>