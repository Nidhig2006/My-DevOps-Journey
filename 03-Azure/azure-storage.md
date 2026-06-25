# Azure Storage

Azure Storage is Microsoft's cloud-based storage solution that provides highly available, scalable, secure, and durable storage for a wide variety of data. It is designed to store structured, unstructured, and semi-structured data and can be accessed from anywhere in the world.

Azure Storage is one of the core services of Microsoft Azure and is commonly used to store:

- Images
- Videos
- Documents
- Virtual Machine Disks
- Application Logs
- Database Backups
- Big Data

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

Azure Storage is Microsoft's cloud storage service that provides highly available, secure, scalable, and durable storage for cloud applications.

Unlike traditional storage, Azure Storage automatically handles replication, scalability, maintenance, and high availability.

## Features

- High Availability
- Scalability
- Durability
- Security
- Automatic Replication
- Encryption
- Global Accessibility

## Benefits

- Accessible from anywhere
- Pay only for what you use
- Supports structured and unstructured data
- Multiple redundancy options
- Easy integration with Azure services

---

# Azure Storage Architecture

```text
                   Azure Storage

                         │
     ┌───────────────────┼───────────────────┐
     │                   │                   │
     ▼                   ▼                   ▼
 Blob Storage      File Storage      Queue Storage
     │                   │                   │
     ▼                   ▼                   ▼
Table Storage     Data Lake Gen2     Managed Disks
```

Azure Storage offers multiple services designed for different types of data and workloads.

---

# Azure Storage Account

A **Storage Account** is the primary Azure resource used to access Azure Storage services.

Think of it as a container that holds all your Azure storage resources.

Example:

```text
devopsstorage001
```

Inside a Storage Account, you can create:

- Blob Containers
- File Shares
- Queues
- Tables

---

## Storage Account Naming Rules

A Storage Account name:

- Must be globally unique
- Must contain 3–24 characters
- Can contain only lowercase letters and numbers
- Cannot contain spaces or special characters

Example:

```text
mydevopsstorage01
```

---

## Performance Tiers

Azure Storage provides two performance options.

| Standard | Premium |
|-----------|----------|
| HDD-based storage | SSD-based storage |
| Lower Cost | Higher Cost |
| General workloads | High-performance workloads |

Use **Standard** for learning and general applications.

Use **Premium** for production applications requiring high IOPS and low latency.

---

# Azure Storage Redundancy

Azure automatically creates multiple copies of your data to prevent data loss.

---

## Local Redundant Storage (LRS)

Stores **3 copies** of data within a single Azure datacenter.

Best For

- Development
- Testing
- Low-cost applications

```text
Datacenter

Disk 1
Disk 2
Disk 3
```

---

## Zone Redundant Storage (ZRS)

Stores copies across multiple Availability Zones within the same Azure region.

Advantages

- Better availability
- Protection against datacenter failure

---

## Geo-Redundant Storage (GRS)

Replicates data to a secondary Azure region.

```text
Primary Region
      │
Replication
      │
      ▼
Secondary Region
```

Provides protection against regional outages.

---

## Read-Access Geo-Redundant Storage (RA-GRS)

Similar to GRS but also allows read access from the secondary region.

Useful for business continuity.

---

## Geo-Zone Redundant Storage (GZRS)

Combines the benefits of:

- Zone Redundant Storage
- Geo-Redundant Storage

Provides the highest durability and availability.

---

## Redundancy Comparison

| Type | Copies | Region Protection |
|------|--------|-------------------|
| LRS | 3 | ❌ |
| ZRS | Multiple Zones | ❌ |
| GRS | 6 | ✅ |
| RA-GRS | 6 + Read Access | ✅ |
| GZRS | Zones + Region | ✅ |

---

# Azure Blob Storage

Blob Storage stores **unstructured data**.

Examples include:

- Images
- Videos
- PDFs
- Documents
- ISO Files
- Backups
- Application Logs

Blob Storage is the most commonly used Azure Storage service.

---

## Blob Types

Azure Blob Storage provides three blob types.

### Block Blob

Used for storing:

- Documents
- Images
- Videos
- Backups

Most commonly used blob type.

---

### Append Blob

Optimized for data that is continuously appended.

Examples

- Log Files
- Monitoring Data

---

### Page Blob

Designed for random read/write operations.

Primarily used for:

- Azure Virtual Machine Disks

---

## Blob Access Tiers

Azure provides four access tiers based on how frequently data is accessed.

### Hot Tier

- Frequently accessed data
- Highest storage cost
- Lowest access cost

Examples

- Website Images
- Application Files

---

### Cool Tier

- Infrequently accessed data
- Lower storage cost
- Higher access cost

Examples

- Monthly Reports
- Archived Project Files

---

### Cold Tier

- Rarely accessed data
- Lower storage cost than Cool
- Suitable for long-term storage

---

### Archive Tier

- Lowest storage cost
- Highest retrieval time
- Long-term backups

---

## Access Tier Comparison

| Tier | Best For |
|------|----------|
| Hot | Frequently accessed files |
| Cool | Monthly accessed data |
| Cold | Rarely accessed files |
| Archive | Long-term backup |

---

# Azure File Storage

Azure Files provides fully managed cloud file shares.

Supported protocols:

- SMB
- NFS

Common Uses

- Shared folders
- Application data
- Lift-and-shift applications
- Shared storage between VMs

```text
Windows VM
      │
      ▼
Azure File Share
      ▲
      │
Linux VM
```

---

# Azure Queue Storage

Queue Storage stores messages between applications.

Useful for asynchronous communication.

Example:

```text
Website

↓

Queue

↓

Background Worker

↓

Database
```

Example Use Cases

- Order Processing
- Email Notifications
- Background Jobs

---

# Azure Table Storage

Azure Table Storage is a NoSQL key-value database.

Suitable for storing:

- User Profiles
- Sensor Data
- Metadata
- Configuration Data

Unlike SQL databases, it does not support relationships between tables.

Example:

```text
Student

RowKey: 101

Name: Nidhi

Department: CSE
```

---

# Azure Data Lake Storage Gen2

Azure Data Lake Storage Gen2 is designed for big data analytics.

Common Uses

- Apache Spark
- Hadoop
- Machine Learning
- Data Analytics
- AI Workloads

It combines the scalability of Blob Storage with advanced analytics capabilities.

---
# Azure Storage Security

Azure Storage provides multiple security features to protect your data from unauthorized access.

---

## Access Keys

Every Storage Account contains two access keys.

These keys provide full administrative access to the Storage Account.

Features:

- Full access to all storage services
- Can regenerate one key without affecting the other
- Should never be shared publicly

---

## Shared Access Signature (SAS)

A Shared Access Signature (SAS) is a secure URL that provides temporary and limited access to Azure Storage resources.

Instead of sharing access keys, you can generate a SAS Token with specific permissions.

Example:

```text
Storage Account
        │
Generate SAS Token
        │
        ▼
Temporary Access Link
        │
        ▼
User Downloads File
```

Advantages

- Temporary access
- Fine-grained permissions
- More secure than sharing access keys

---

## Microsoft Entra ID Authentication

Azure Storage supports Microsoft Entra ID (formerly Azure Active Directory) authentication.

Benefits:

- No need to share storage keys
- Supports Role-Based Access Control (RBAC)
- More secure authentication

---

## Encryption

Azure automatically encrypts all data before storing it.

Supported options:

- Microsoft-managed keys
- Customer-managed keys (CMK)

Encryption protects data both:

- At Rest
- In Transit

---

# Azure Storage Explorer

Azure Storage Explorer is a free desktop application provided by Microsoft to manage Azure Storage resources.

Using Storage Explorer, you can:

- Upload files
- Download files
- Delete blobs
- Create containers
- Manage file shares
- Generate SAS Tokens
- View Storage Accounts

Example:

```text
Azure Storage Explorer

        │

        ▼

Storage Account

        │

 ┌──────┼──────┐

 ▼      ▼      ▼

Blobs  Files  Queues
```

---

# Azure CLI Commands

## Login to Azure

```bash
az login
```

Authenticates your Azure account.

---

## List Storage Accounts

```bash
az storage account list --output table
```

Displays all Storage Accounts.

---

## Create a Storage Account

```bash
az storage account create \
    --name mystorage123 \
    --resource-group DevOps-RG \
    --location centralindia \
    --sku Standard_LRS
```

Creates a new Storage Account.

---

## Create a Blob Container

```bash
az storage container create \
    --name images
```

Creates a Blob Container.

---

## List Containers

```bash
az storage container list
```

Displays all Blob Containers.

---

## Upload a Blob

```bash
az storage blob upload
```

Uploads a file to Blob Storage.

---

## Download a Blob

```bash
az storage blob download
```

Downloads a blob from Azure Storage.

---

## Delete a Blob

```bash
az storage blob delete
```

Deletes a blob from a container.

---

## Delete Storage Account

```bash
az storage account delete
```

Deletes a Storage Account.

---

# Best Practices

- Use meaningful Storage Account names.
- Use Standard storage for development and Premium for production.
- Enable HTTPS only.
- Choose the correct redundancy option.
- Prefer SAS Tokens over sharing access keys.
- Use Microsoft Entra ID authentication whenever possible.
- Enable soft delete for important data.
- Organize files into Blob Containers.
- Monitor storage usage regularly.
- Delete unused Storage Accounts to reduce costs.

---

# Hands-on Lab

## Objective

Create a Storage Account, upload a file to Blob Storage, generate a SAS URL, and clean up resources.

---

### Step 1

Create a Resource Group.

Example:

```text
DevOps-RG
```

---

### Step 2

Create a Storage Account.

Example:

```text
devopsstorage001
```

---

### Step 3

Create a Blob Container.

Example:

```text
images
```

---

### Step 4

Upload any image or document into the container.

---

### Step 5

Verify that the uploaded file appears in the Blob Container.

---

### Step 6

Generate a SAS URL for the uploaded file.

Open the generated URL in your browser to verify access.

---

### Step 7

Download the file.

---

### Step 8

Delete the uploaded Blob.

---

### Step 9

Delete the Storage Account.

---

# Interview Questions

<details>
<summary><strong>1. What is Azure Storage?</strong></summary>

Azure Storage is Microsoft's cloud storage service used to store structured, semi-structured, and unstructured data. It provides high availability, scalability, durability, and security.

</details>

---

<details>
<summary><strong>2. What is a Storage Account?</strong></summary>

A Storage Account is the primary Azure resource that provides a unique namespace for storing data. It can contain Blob Containers, File Shares, Queues, and Tables.

</details>

---

<details>
<summary><strong>3. What are the different Azure Storage services?</strong></summary>

Azure Storage provides:

- Blob Storage
- Azure Files
- Queue Storage
- Table Storage
- Data Lake Storage Gen2

</details>

---

<details>
<summary><strong>4. What is Blob Storage?</strong></summary>

Blob Storage is used to store unstructured data such as images, videos, documents, backups, and log files.

</details>

---

<details>
<summary><strong>5. What are the different Blob types?</strong></summary>

There are three Blob types:

- Block Blob
- Append Blob
- Page Blob

</details>

---

<details>
<summary><strong>6. What are Blob Access Tiers?</strong></summary>

Azure Blob Storage supports four access tiers:

- Hot
- Cool
- Cold
- Archive

These tiers help optimize storage costs based on access frequency.

</details>

---

<details>
<summary><strong>7. What is Azure File Storage?</strong></summary>

Azure Files provides fully managed cloud file shares that can be accessed using SMB or NFS protocols.

</details>

---

<details>
<summary><strong>8. What is Azure Queue Storage?</strong></summary>

Queue Storage stores messages between different components of an application, enabling asynchronous communication.

</details>

---

<details>
<summary><strong>9. What is Azure Table Storage?</strong></summary>

Azure Table Storage is a NoSQL key-value data store used for storing large amounts of structured, non-relational data.

</details>

---

<details>
<summary><strong>10. What is Azure Data Lake Storage Gen2?</strong></summary>

Azure Data Lake Storage Gen2 is designed for big data analytics and workloads such as Apache Spark, Hadoop, and Machine Learning.

</details>

---

<details>
<summary><strong>11. What is LRS?</strong></summary>

Local Redundant Storage (LRS) stores three copies of data within a single Azure datacenter.

</details>

---

<details>
<summary><strong>12. What is ZRS?</strong></summary>

Zone Redundant Storage (ZRS) stores copies of data across multiple Availability Zones within the same Azure region.

</details>

---

<details>
<summary><strong>13. What is GRS?</strong></summary>

Geo-Redundant Storage (GRS) replicates data to a secondary Azure region for disaster recovery.

</details>

---

<details>
<summary><strong>14. What is a SAS Token?</strong></summary>

A Shared Access Signature (SAS) Token provides temporary and limited access to Azure Storage resources without exposing access keys.

</details>

---

<details>
<summary><strong>15. What is Azure Storage Explorer?</strong></summary>

Azure Storage Explorer is a desktop application used to manage Azure Storage resources, upload/download files, and generate SAS Tokens.

</details>

---

<details>
<summary><strong>16. How is Azure Storage secured?</strong></summary>

Azure Storage can be secured using:

- Microsoft Entra ID
- Access Keys
- SAS Tokens
- Encryption
- RBAC

</details>

---

<details>
<summary><strong>17. Which storage service would you use for images and videos?</strong></summary>

Azure Blob Storage is the recommended service for storing images, videos, documents, and other unstructured data.

</details>

---

<details>
<summary><strong>18. Which redundancy option provides the highest durability?</strong></summary>

Geo-Zone Redundant Storage (GZRS) provides the highest durability by combining Zone Redundancy with Geo-Replication.

</details>

---

<details>
<summary><strong>19. Why should you use SAS Tokens instead of Access Keys?</strong></summary>

SAS Tokens provide temporary and limited access, making them more secure than sharing full Storage Account access keys.

</details>

---

<details>
<summary><strong>20. Which Azure Storage service is best for shared folders?</strong></summary>

Azure Files is best for creating shared folders that can be accessed from multiple virtual machines.

</details>

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
- Azure Storage Security
- Azure Storage Explorer
- Azure CLI Commands
- Best Practices
- Hands-on Lab
- Interview Questions

Azure Storage is one of the most fundamental Azure services and is widely used in cloud applications, DevOps pipelines, backup solutions, and enterprise workloads. Understanding its storage services, redundancy options, security features, and management tools is essential for Azure administrators, cloud engineers, and DevOps professionals.