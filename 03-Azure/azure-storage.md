# Azure Storage

Azure Storage is Microsoft's cloud-based storage solution that provides highly available, scalable, secure, and durable storage for a wide variety of data. It is designed to store structured, unstructured, and semi-structured data and can be accessed from anywhere in the world.

Azure Storage is one of the core services of Microsoft Azure and is commonly used to store application data, backups, virtual machine disks, media files, logs, and much more.

---

# Table of Contents

- Introduction to Azure Storage
- Azure Storage Account
- Azure Storage Redundancy
- Azure Blob Storage
- Azure File Storage
- Azure Queue Storage
- Azure Table Storage
- Azure Data Lake Storage Gen2
- Azure Storage Security
- Azure Storage Explorer
- Azure CLI Commands
- Best Practices
- Hands-on Lab
- Interview Questions
- Summary

---

# Introduction to Azure Storage

Azure Storage provides cloud storage that is:

- Highly Available
- Durable
- Secure
- Scalable
- Accessible from anywhere

It can store:

- Images
- Videos
- Documents
- Virtual Machine Disks
- Application Logs
- Database Backups
- Big Data

---

## Features of Azure Storage

- Highly Available
- Automatic Replication
- Scalable
- Secure
- Durable
- Cost Effective
- Encrypted by Default

---

## Benefits

- No physical storage maintenance
- Pay only for what you use
- Accessible worldwide
- Multiple redundancy options
- Easy integration with Azure services

---

# Azure Storage Architecture

```

```
                Azure Storage

                       │

       ┌───────────────┼───────────────┐

       ▼               ▼               ▼

 Blob Storage     File Storage    Queue Storage

       │               │               │

       ▼               ▼               ▼

 Table Storage      Data Lake      Managed Disks

```

---

# Azure Storage Account

A Storage Account is the primary resource used to access Azure Storage services.

Think of it as a container that holds all your storage resources.

Example

```
devopsstorage001
```

Inside a Storage Account you can create:

- Blob Containers
- File Shares
- Queues
- Tables

---

## Naming Rules

- Must be globally unique
- 3–24 characters
- Lowercase letters and numbers only
- No special characters

Example

```
mydevopsstorage01
```

---

## Performance Tiers

Azure Storage provides two performance options.

| Standard | Premium |
|-----------|----------|
| HDD Based | SSD Based |
| Lower Cost | Higher Cost |
| General Purpose | High Performance |

Choose Standard for learning and Premium for production workloads requiring low latency.

---

# Azure Storage Redundancy

Azure automatically replicates data to improve durability and availability.

## Local Redundant Storage (LRS)

Stores three copies of data within a single datacenter.

Best for:

- Development
- Testing
- Low-cost storage

---

## Zone Redundant Storage (ZRS)

Stores copies across multiple Availability Zones within the same region.

Provides better availability than LRS.

---

## Geo-Redundant Storage (GRS)

Replicates data to a secondary Azure region.

Protects against regional failures.

---

## Read-Access Geo-Redundant Storage (RA-GRS)

Similar to GRS but also allows read access to the secondary region.

---

## Geo-Zone Redundant Storage (GZRS)

Combines the benefits of ZRS and GRS.

Provides the highest durability.

---

## Redundancy Comparison

| Type | Copies | Region Protection |
|------|--------|-------------------|
| LRS | 3 | No |
| ZRS | 3 Zones | No |
| GRS | 6 | Yes |
| RA-GRS | 6 | Yes + Read Access |
| GZRS | Multi-Zone + Region | Yes |

---

# Azure Blob Storage

Blob Storage stores unstructured data.

Examples:

- Images
- Videos
- PDFs
- ISO Files
- Backups
- Documents

Blob Storage is the most commonly used Azure Storage service.

---

## Blob Types

### Block Blob

Used for:

- Documents
- Images
- Videos
- Backups

Most commonly used blob type.

---

### Append Blob

Designed for data that is continuously appended.

Examples:

- Logs
- Monitoring Data

---

### Page Blob

Used for random read/write operations.

Mostly used for:

- Azure Virtual Machine Disks

---

## Blob Access Tiers

Azure allows moving data between different access tiers to optimize costs.

### Hot Tier

- Frequently accessed data
- Highest storage cost
- Lowest access cost

---

### Cool Tier

- Infrequently accessed data
- Lower storage cost
- Higher access cost

---

### Cold Tier

- Rarely accessed data
- Lower storage cost than Cool
- Suitable for long-term storage

---

### Archive Tier

- Long-term backup
- Lowest storage cost
- Highest retrieval time

---

## Access Tier Comparison

| Tier | Best For |
|------|----------|
| Hot | Daily Access |
| Cool | Monthly Access |
| Cold | Rare Access |
| Archive | Long-term Backup |

---

# Azure File Storage

Azure Files provides fully managed file shares.

Protocols supported:

- SMB
- NFS

Common Uses

- Shared folders
- Lift and Shift applications
- Shared application data

---

# Azure Queue Storage

Queue Storage stores messages.

Used for communication between applications.

Example

```
Website

↓

Queue

↓

Background Worker

↓

Database
```

Useful for asynchronous processing.

---

# Azure Table Storage

Azure Table Storage is a NoSQL key-value database.

Suitable for:

- User Profiles
- Sensor Data
- Metadata
- Configuration Data

Unlike SQL databases, it does not use tables with relationships.

---

# Azure Data Lake Storage Gen2

Azure Data Lake Storage Gen2 is designed for analytics and big data workloads.

Common Uses

- Hadoop
- Apache Spark
- Data Analytics
- Machine Learning

---

# Azure Storage Security

Azure provides multiple security features.

## Access Keys

Every Storage Account has two access keys.

They provide full access to the Storage Account.

Keep them secure.

---

## Shared Access Signature (SAS)

A SAS Token provides temporary and limited access to storage resources.

Example

```
Generate SAS

↓

Valid for 1 Hour

↓

Share File Securely
```

---

## Microsoft Entra ID Authentication

Allows users and applications to authenticate using Microsoft Entra ID instead of storage keys.

More secure than sharing access keys.

---

## Encryption

Azure Storage encrypts data automatically using Microsoft-managed keys.

Customer-managed keys are also supported.

---

# Azure Storage Explorer

Azure Storage Explorer is a desktop application used to manage Azure Storage.

Features

- Upload Files
- Download Files
- Delete Files
- Manage Containers
- Generate SAS Tokens
- View Storage Accounts

---

# Azure CLI Commands

## Login

```bash
az login
```

---

## List Storage Accounts

```bash
az storage account list --output table
```

---

## Create Storage Account

```bash
az storage account create \
    --name mystorage123 \
    --resource-group DevOps-RG \
    --location centralindia \
    --sku Standard_LRS
```

---

## Create Blob Container

```bash
az storage container create \
    --name images
```

---

## Upload Blob

```bash
az storage blob upload
```

---

## Download Blob

```bash
az storage blob download
```

---

## List Blob Containers

```bash
az storage container list
```

---

## Delete Storage Account

```bash
az storage account delete
```

---

# Best Practices

- Use meaningful Storage Account names.
- Use Standard storage for development.
- Enable HTTPS only.
- Choose the correct redundancy option.
- Use SAS Tokens instead of sharing access keys.
- Enable soft delete for important data.
- Organize files into containers.
- Monitor storage usage regularly.
- Delete unused storage resources.
- Follow the principle of least privilege.

---

# Hands-on Lab

## Objective

Create a Storage Account, upload a file, generate a SAS URL, and clean up resources.

### Step 1

Create a Resource Group.

### Step 2

Create a Storage Account.

### Step 3

Create a Blob Container named:

```
images
```

### Step 4

Upload any image.

### Step 5

Download the uploaded image.

### Step 6

Generate a SAS URL.

### Step 7

Access the image using the SAS URL.

### Step 8

Delete the Blob.

### Step 9

Delete the Storage Account.

---

# Interview Questions

(Use the same `<details>` format as your Git and Linux interview files.)

1. What is Azure Storage?
2. What is a Storage Account?
3. What are the different Azure Storage services?
4. What is the difference between Standard and Premium Storage?
5. What is Blob Storage?
6. What are the different Blob types?
7. What are Blob Access Tiers?
8. What is Azure File Storage?
9. What is Queue Storage?
10. What is Table Storage?
11. What is Azure Data Lake Storage Gen2?
12. What is LRS?
13. What is ZRS?
14. What is GRS?
15. What is RA-GRS?
16. What is GZRS?
17. What is a SAS Token?
18. What is Azure Storage Explorer?
19. How is Azure Storage secured?
20. Which Azure Storage service would you use for storing images and videos?

---

# Summary

In this guide, we covered:

- Azure Storage Overview
- Storage Accounts
- Storage Redundancy
- Blob Storage
- Blob Types
- Blob Access Tiers
- Azure Files
- Queue Storage
- Table Storage
- Data Lake Storage Gen2
- Storage Security
- Azure Storage Explorer
- Azure CLI Commands
- Best Practices
- Hands-on Lab
- Interview Questions

Azure Storage is one of the most important Azure services and forms the foundation for many cloud applications. Understanding its services, redundancy options, security features, and management tools is essential for Azure administrators, cloud engineers, and DevOps professionals.
