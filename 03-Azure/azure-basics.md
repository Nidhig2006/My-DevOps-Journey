# Azure Basics

A beginner-friendly guide to Microsoft Azure covering cloud computing fundamentals, Azure architecture, and the core concepts every Azure and DevOps engineer should know.

---

# Table of Contents

- Introduction to Cloud Computing
- What is Microsoft Azure?
- Why Use Azure?
- Benefits of Cloud Computing
- Cloud Service Models
- Cloud Deployment Models
- Azure Global Infrastructure
- Azure Regions
- Availability Zones
- Region Pairs
- Azure Resource Manager (ARM)
- Azure Portal
- Azure Subscription
- Azure Resource Groups
- Azure Services
- Azure Free Account
- Azure Pricing
- Summary

---

# Introduction to Cloud Computing

Cloud computing is the delivery of computing services such as servers, storage, databases, networking, software, analytics, and artificial intelligence over the internet instead of using local computers or physical servers.

Instead of purchasing and maintaining hardware, users can access resources whenever required and pay only for what they use.

### Traditional Computing

```text
User
   │
   ▼
Own Physical Computer
   │
   ▼
Own Servers
   │
   ▼
Own Storage
   │
   ▼
Maintenance by Organization
```

### Cloud Computing

```text
User
   │
   ▼
Internet
   │
   ▼
Cloud Provider (Azure)
   │
   ▼
Virtual Machines
Storage
Networking
Databases
AI Services
```

---

# What is Microsoft Azure?

Microsoft Azure is Microsoft's cloud computing platform that provides more than 200 cloud services to build, deploy, and manage applications through Microsoft-managed data centers across the world.

Azure allows businesses and developers to:

- Build applications
- Host websites
- Create virtual machines
- Store data
- Manage databases
- Deploy containers
- Build AI solutions
- Secure cloud infrastructure

Official Website:

https://azure.microsoft.com/

---

# Why Use Azure?

Azure helps organizations reduce infrastructure costs while providing highly available and scalable cloud services.

Advantages include:

- High availability
- Global infrastructure
- Scalability
- Strong security
- Easy integration with Microsoft products
- Pay-as-you-go pricing
- Disaster recovery
- Automatic backups

---

# Benefits of Cloud Computing

## Cost Effective

No need to purchase expensive servers.

Example:

Instead of buying a ₹5,00,000 server, you can create a virtual machine for only the time you need.

---

## Scalability

Increase or decrease resources whenever required.

Example:

A shopping website receives heavy traffic during festivals.

Azure can automatically increase server capacity.

---

## High Availability

Applications remain available even if hardware fails.

---

## Flexibility

Resources can be created within minutes.

Example:

Need another VM?

Simply create it from the Azure Portal.

---

## Security

Microsoft provides enterprise-grade security features including encryption, identity management, monitoring, and compliance certifications.

---

# Cloud Service Models

Cloud services are mainly divided into three categories.

---

## Infrastructure as a Service (IaaS)

The cloud provider manages:

- Physical servers
- Storage
- Networking
- Virtualization

The customer manages:

- Operating System
- Applications
- Data

Examples:

- Azure Virtual Machines
- Azure Virtual Network

Use Case:

Hosting your own web server.

---

## Platform as a Service (PaaS)

The cloud provider manages:

- Infrastructure
- Operating System
- Runtime
- Middleware

The customer manages:

- Applications
- Data

Examples:

- Azure App Service
- Azure SQL Database

Use Case:

Deploying web applications without managing servers.

---

## Software as a Service (SaaS)

The cloud provider manages everything.

Users simply use the software.

Examples:

- Microsoft 365
- Outlook
- Teams
- OneDrive

Use Case:

Using Microsoft Teams directly from the browser.

---

## Comparison

| Feature | IaaS | PaaS | SaaS |
|----------|------|------|------|
| Servers Managed By | Microsoft | Microsoft | Microsoft |
| Operating System | Customer | Microsoft | Microsoft |
| Applications | Customer | Customer | Microsoft |
| Best For | Full Control | Developers | End Users |

---

# Cloud Deployment Models

## Public Cloud

Infrastructure is owned by the cloud provider and shared among customers.

Example:

Microsoft Azure

Advantages

- Low cost
- Easy deployment
- High scalability

---

## Private Cloud

Infrastructure is dedicated to a single organization.

Advantages

- Greater security
- Full control
- Better compliance

Example:

Private data center

---

## Hybrid Cloud

Combination of Public Cloud and Private Cloud.

Example:

Sensitive customer information stays in a private cloud while web applications run in Azure.

Advantages

- Flexibility
- Better disaster recovery
- Cost optimization

---

# Azure Global Infrastructure

Azure operates one of the world's largest cloud infrastructures.

It consists of:

- Regions
- Availability Zones
- Region Pairs
- Data Centers

These components provide reliability, fault tolerance, and disaster recovery.

---

# Azure Regions

An Azure Region is a geographical area containing one or more Azure data centers.

Examples:

- Central India
- South India
- East US
- West Europe
- Japan East

Benefits

- Lower latency
- Data residency
- High availability

Example:

If your customers are located in India, choosing the Central India region reduces response time.

---

# Availability Zones

Availability Zones are physically separate data centers within the same Azure Region.

Each zone has:

- Independent power
- Independent cooling
- Independent networking

If one zone fails, the application continues running from another zone.

Example

```
Region

Zone 1
Zone 2
Zone 3
```

---

# Region Pairs

Azure pairs every region with another region within the same geography.

Example:

- Central India ↔ South India

Benefits

- Disaster recovery
- Planned maintenance
- Data replication

---

# Azure Resource Manager (ARM)

Azure Resource Manager (ARM) is the deployment and management service for Azure.

It allows users to:

- Create resources
- Update resources
- Delete resources
- Manage permissions
- Organize infrastructure

Everything created in Azure is managed through ARM.

---

# Azure Portal

The Azure Portal is Microsoft's web-based interface used to manage Azure resources.

Using the portal, users can:

- Create Virtual Machines
- Create Storage Accounts
- Configure Networks
- Monitor Resources
- View Billing
- Manage Resource Groups

Portal URL:

https://portal.azure.com/

---

# Azure Subscription

A subscription is a billing account in Azure.

Every Azure resource belongs to a subscription.

A subscription helps manage:

- Billing
- Permissions
- Resource limits
- Access control

One Azure account can contain multiple subscriptions.

---

# Azure Resource Groups

A Resource Group is a logical container used to organize Azure resources.

Example:

```
Resource Group

├── Virtual Machine
├── Storage Account
├── Virtual Network
├── Public IP
└── Network Security Group
```

Benefits

- Easy management
- Access control
- Resource organization
- Delete all related resources together

---

# Azure Services

Some commonly used Azure services include:

| Service | Purpose |
|----------|----------|
| Azure Virtual Machines | Virtual Servers |
| Azure Storage | Cloud Storage |
| Azure Virtual Network | Networking |
| Azure SQL Database | Managed Database |
| Azure App Service | Web App Hosting |
| Azure Kubernetes Service (AKS) | Container Orchestration |
| Azure Monitor | Monitoring Resources |
| Azure Key Vault | Secure Secrets Management |

---

# Azure Free Account

Microsoft provides a free Azure account for new users.

It includes:

- Free credits (subject to Microsoft's current offer)
- Free popular services for a limited period
- Always-free services within usage limits

Ideal for learning and practice.

---

# Azure Pricing

Azure follows a Pay-As-You-Go pricing model.

You pay only for the resources you consume.

Pricing depends on:

- Virtual Machine size
- Storage usage
- Network traffic
- Database usage
- Service type

Cost optimization tips:

- Stop unused virtual machines
- Delete unused resources
- Use the Azure Pricing Calculator before deployment

---

# Summary

Microsoft Azure is one of the world's leading cloud computing platforms.

Key concepts covered in this guide include:

- Cloud Computing
- Microsoft Azure
- Cloud Service Models
- Deployment Models
- Azure Regions
- Availability Zones
- Region Pairs
- Azure Resource Manager
- Azure Portal
- Azure Subscription
- Resource Groups
- Azure Services
- Azure Pricing

Understanding these concepts provides a strong foundation for learning Azure Virtual Machines, Azure Storage, Networking, Security, Monitoring, Azure CLI, Infrastructure as Code, and DevOps.