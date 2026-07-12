# Azure Virtual Machines (VM)

Azure Virtual Machines (VMs) are one of the most widely used Infrastructure as a Service (IaaS) offerings provided by Microsoft Azure. They allow users to create and run virtual computers in the cloud without purchasing or maintaining physical hardware.

A Virtual Machine behaves like a physical computer, complete with its own operating system, CPU, memory, storage, and networking. Users can install software, host applications, run databases, deploy websites, or perform development and testing just as they would on a physical server.

Azure manages the underlying physical infrastructure, while users have complete control over the virtual machine's operating system and installed applications.

---

# Table of Contents

- What is an Azure Virtual Machine?
- Why Use Azure Virtual Machines?
- Real-World Use Cases
- Azure VM Architecture
- Benefits of Azure Virtual Machines
- Types of Azure Virtual Machines
- Azure VM Size Series
- Components Required Before Creating a Virtual Machine

---

# What is an Azure Virtual Machine?

An Azure Virtual Machine (VM) is a virtualized computing resource that runs in Microsoft's Azure cloud.

Instead of purchasing a physical server, users can create a virtual server in Azure within a few minutes and pay only for the resources they consume.

Azure Virtual Machines provide complete control over:

- Operating System
- Installed Applications
- Storage
- Networking
- Security
- Configuration

Azure takes care of:

- Physical Servers
- Data Centers
- Networking Hardware
- Cooling Systems
- Power Supply
- Hardware Maintenance

Since Azure Virtual Machines belong to the Infrastructure as a Service (IaaS) model, users are responsible for managing the operating system and applications while Microsoft manages the underlying infrastructure.

---

# Why Use Azure Virtual Machines?

Azure Virtual Machines are useful whenever an application requires full control over the operating system or software environment.

Common reasons include:

- Hosting websites
- Running enterprise applications
- Deploying databases
- Software development
- Software testing
- Running Linux or Windows servers
- Backup servers
- Disaster recovery
- Machine learning workloads
- Container hosting

---

# Real-World Use Cases

## Website Hosting

A company hosts its e-commerce website on an Ubuntu Virtual Machine running Nginx.

```
Customer
      │
      ▼
 Internet
      │
      ▼
 Azure Virtual Machine
      │
      ▼
 Nginx Web Server
      │
      ▼
 Website
```

---

## Development Environment

Developers create temporary Virtual Machines for testing applications without affecting production systems.

Benefits:

- Easy to create
- Easy to delete
- Pay only while running

---

## Database Server

Organizations install:

- MySQL
- PostgreSQL
- SQL Server
- MongoDB

inside Azure Virtual Machines.

---

## Learning Linux

Students can create an Ubuntu Virtual Machine to practice:

- Linux Commands
- Docker
- Kubernetes
- Terraform
- Jenkins

without using their personal computers.

---

## Hosting Internal Applications

Companies often deploy:

- ERP Systems
- HR Portals
- Employee Applications

inside Virtual Machines.

---

# Azure VM Architecture

```
                    User
                      │
                      ▼
               Azure Portal / CLI
                      │
                      ▼
           Azure Resource Manager
                      │
                      ▼
              Azure Virtual Machine
        ┌─────────────┼─────────────┐
        │             │             │
        ▼             ▼             ▼
   Operating      Virtual Disk    Network
     System         (Storage)     Interface
        │             │             │
        └─────────────┼─────────────┘
                      │
                      ▼
            Azure Physical Hardware
      (Managed Completely by Microsoft)
```

---

# Benefits of Azure Virtual Machines

## 1. Scalability

Virtual Machines can be resized whenever additional CPU or memory is required.

Example:

A website initially receives 500 visitors per day.

Later it receives 50,000 visitors.

Instead of purchasing new hardware, simply resize the VM.

---

## 2. High Availability

Azure provides multiple options to keep applications running even if hardware fails.

Examples:

- Availability Zones
- Availability Sets
- Region Pairs

---

## 3. Cost Effective

Pay only for the resources you use.

If the Virtual Machine is stopped and deallocated, compute charges stop.

---

## 4. Flexibility

Choose any operating system.

Examples:

- Ubuntu
- Windows Server
- Debian
- CentOS
- Red Hat Enterprise Linux

---

## 5. Global Deployment

Virtual Machines can be deployed in Azure Regions across the world.

Examples:

- Central India
- East US
- West Europe
- Japan East

This reduces latency for users.

---

## 6. Security

Azure provides several security features:

- Encryption
- Microsoft Defender for Cloud
- Network Security Groups
- Azure Key Vault
- Azure Active Directory

---

## 7. Easy Backup

Azure Backup allows automatic backups of Virtual Machines.

Snapshots can also be created before making important changes.

---

# Types of Azure Virtual Machines

Azure offers different VM families optimized for different workloads.

---

## 1. General Purpose

Best for:

- Web Servers
- Small Databases
- Development
- Testing

Examples:

- B-Series
- D-Series

---

## 2. Compute Optimized

Designed for CPU-intensive applications.

Examples:

- Gaming Servers
- Scientific Simulations
- Media Encoding

Series:

- F-Series

---

## 3. Memory Optimized

Provides large amounts of RAM.

Suitable for:

- SAP
- SQL Server
- Redis
- Large Databases

Series:

- E-Series
- M-Series

---

## 4. Storage Optimized

Designed for applications requiring high disk throughput.

Examples:

- Big Data
- Data Warehousing
- NoSQL Databases

---

## 5. GPU Virtual Machines

Used for:

- Artificial Intelligence
- Machine Learning
- Video Rendering
- Graphics Processing

Series:

- N-Series

---

## 6. High Performance Computing (HPC)

Designed for:

- Engineering Simulations
- Weather Forecasting
- Scientific Research

---

# Azure VM Size Series

Azure categorizes Virtual Machines into different series.

| Series | Best For |
|----------|------------------------------|
| B-Series | Budget workloads |
| D-Series | General purpose |
| E-Series | Memory-intensive applications |
| F-Series | Compute-intensive applications |
| M-Series | Very large databases |
| N-Series | GPU workloads |

---

## B-Series

Designed for workloads that do not require continuous high CPU usage.

Examples:

- Personal projects
- Learning Azure
- Small web servers

Advantages:

- Lowest cost
- Burstable CPU

---

## D-Series

Most commonly used Virtual Machines.

Suitable for:

- Business Applications
- APIs
- Medium-sized websites

---

## E-Series

Provides more RAM than D-Series.

Suitable for:

- SQL Server
- SAP
- Enterprise Applications

---

## F-Series

Optimized for CPU-intensive applications.

Examples:

- Gaming
- Video Processing
- Scientific Applications

---

## M-Series

Largest Virtual Machines in Azure.

Suitable for:

- Enterprise databases
- SAP HANA

---

## N-Series

Contains NVIDIA GPUs.

Suitable for:

- Artificial Intelligence
- Deep Learning
- Graphics Rendering

---

# Components Required Before Creating a Virtual Machine

Before creating an Azure Virtual Machine, several Azure resources are required.

```
Azure Subscription
        │
        ▼
Resource Group
        │
        ▼
Region
        │
        ▼
Virtual Network (VNet)
        │
        ▼
Subnet
        │
        ▼
Network Security Group
        │
        ▼
Public IP
        │
        ▼
Network Interface
        │
        ▼
Storage Disk
        │
        ▼
Azure Virtual Machine
```

Each component plays an important role in the deployment and management of the VM.

The upcoming sections will explain each of these components in detail while creating an Azure Virtual Machine.

---

# Creating an Azure Virtual Machine

Azure Virtual Machines can be created using multiple methods:

- Azure Portal (Graphical User Interface)
- Azure CLI
- Azure PowerShell
- ARM Templates
- Bicep
- Terraform

For beginners, the Azure Portal is the easiest and most commonly used method.

---

# Creating a Virtual Machine Using Azure Portal

Follow these steps to create a Virtual Machine.

## Step 1: Sign in to Azure Portal

Open:

```
https://portal.azure.com
```

Log in using your Microsoft Azure account.

---

## Step 2: Search for Virtual Machines

In the search bar, type:

```
Virtual Machines
```

Click **Virtual Machines**.

Click **+ Create**

↓

**Azure Virtual Machine**

---

## Step 3: Basics Tab

This is where the main configuration is done.

You will configure:

- Subscription
- Resource Group
- Virtual Machine Name
- Region
- Availability Options
- Image
- Size
- Authentication

---

## Subscription

A subscription is the billing account under which Azure resources are created.

Example

```
Azure Subscription

↓

Pay-As-You-Go
```

Every Virtual Machine belongs to one subscription.

---

## Resource Group

Select an existing Resource Group or create a new one.

Example

```
Resource Group

↓

DevOps-RG
```

All related resources can be managed together inside the Resource Group.

---

## Virtual Machine Name

Give your VM a meaningful name.

Examples

```
Ubuntu-VM

Linux-Test

WebServer-01

DevOps-Lab
```

Avoid spaces and special characters.

---

## Region

Choose the Azure Region closest to your users.

Examples

- Central India
- South India
- East US
- West Europe

Choosing a nearby region reduces latency.

---

## Availability Options

Azure provides multiple options to improve availability.

Options include:

- No Infrastructure Redundancy Required
- Availability Zone
- Availability Set

For learning purposes, select:

```
No Infrastructure Redundancy Required
```

---

# Choosing an Image

An Image is the operating system that will be installed on the Virtual Machine.

Common Images

| Image | Use Case |
|---------|------------------------------|
| Ubuntu Server | Linux Administration |
| Windows Server | Windows Applications |
| Debian | Lightweight Linux |
| CentOS | Enterprise Linux |
| Red Hat Enterprise Linux | Enterprise Workloads |

Example

```
Image

↓

Ubuntu Server 24.04 LTS
```

---

# Choosing a VM Size

The VM size determines:

- CPU
- RAM
- Performance
- Cost

Example

```
Standard_B1s

↓

1 vCPU

1 GB RAM
```

Suitable for:

- Learning Azure
- Linux Practice
- Small Websites

Azure also provides a **See all sizes** option where different VM configurations can be selected.

---

# Administrator Account

Azure requires administrator credentials.

Two authentication methods are available.

- Password Authentication
- SSH Public Key Authentication

---

# Password Authentication

The simplest authentication method.

Required information:

```
Username

Password

Confirm Password
```

Example

```
Username

↓

azureuser

Password

↓

********
```

Advantages

- Easy to configure
- Beginner friendly

Disadvantages

- Less secure than SSH Keys
- Vulnerable to brute-force attacks if weak passwords are used

---

# SSH Key Authentication

Recommended for Linux Virtual Machines.

Instead of passwords, Azure uses a pair of cryptographic keys.

```
Public Key

↓

Stored inside Azure VM

Private Key

↓

Stored securely on your computer
```

Only the private key can access the VM.

Advantages

- More secure
- Faster authentication
- Preferred in production environments

---

# Generating an SSH Key

On Linux, macOS, or Windows PowerShell, run:

```bash
ssh-keygen
```

Example output:

```text
Generating public/private rsa key pair.
```

Files created:

```text
id_rsa

id_rsa.pub
```

- `id_rsa` → Private Key (Never share this)
- `id_rsa.pub` → Public Key (Upload this to Azure)

---

# Inbound Port Rules

Azure asks which ports should be opened.

Common ports are:

| Port | Protocol | Purpose |
|------|----------|----------|
| 22 | SSH | Linux Remote Login |
| 80 | HTTP | Web Server |
| 443 | HTTPS | Secure Website |
| 3389 | RDP | Windows Remote Desktop |

For Ubuntu Linux, select:

```
Allow selected ports

↓

SSH (22)
```

---

# Disks

Azure automatically creates an Operating System Disk.

Additional Data Disks can also be attached later.

Disk Types

- Standard HDD
- Standard SSD
- Premium SSD
- Premium SSD v2
- Ultra Disk

For learning purposes:

```
Standard SSD
```

is sufficient.

---

# Networking

Azure automatically creates or allows you to choose:

- Virtual Network
- Subnet
- Public IP Address
- Network Interface
- Network Security Group

These resources enable communication between the Virtual Machine and the internet or other Azure resources.

---

# Management

Optional settings include:

- Auto Shutdown
- Backup
- Boot Diagnostics
- Identity
- Monitoring

For learning, default settings are usually sufficient.

---

# Review + Create

Azure validates all settings.

If validation succeeds:

```
Validation Passed
```

Click:

```
Create
```

Azure begins provisioning the Virtual Machine.

Deployment usually takes 2–5 minutes.

---

# Connecting to a Linux Virtual Machine

After deployment completes:

Open the Virtual Machine.

Click:

```
Connect

↓

SSH
```

Azure displays an SSH command similar to:

```bash
ssh azureuser@20.204.xxx.xxx
```

Where:

- `ssh` → Secure Shell command
- `azureuser` → Username
- `20.204.xxx.xxx` → Public IP Address

Run the command in your terminal.

If using SSH keys:

```bash
ssh -i ~/.ssh/id_rsa azureuser@20.204.xxx.xxx
```

After successful authentication, you will see a Linux terminal connected to the Azure Virtual Machine.

---

# Connecting to a Windows Virtual Machine

For Windows VMs:

Click:

```
Connect

↓

RDP
```

Download the `.rdp` file.

Open it using Remote Desktop Connection.

Enter:

- Username
- Password

You will then access the Windows desktop running inside Azure.

---

# Difference Between Password and SSH Authentication

| Password Authentication | SSH Authentication |
|--------------------------|-------------------|
| Uses Username and Password | Uses Public and Private Keys |
| Easier for beginners | More secure |
| Suitable for testing | Recommended for production |
| Can be vulnerable to brute-force attacks | Strong encryption provides better security |

---

# Best Practices

- Use SSH keys instead of passwords for Linux VMs.
- Choose the Azure region closest to your users.
- Use meaningful names for Virtual Machines and Resource Groups.
- Open only the required inbound ports.
- Select an appropriate VM size based on your workload.
- Enable Auto Shutdown for development VMs to reduce costs.
- Regularly update the operating system and installed software.
---

# Azure Virtual Machine Components

When an Azure Virtual Machine is created, Azure automatically creates or associates several resources that work together to make the VM functional.

A Virtual Machine cannot communicate, store data, or be accessed without these supporting resources.

```
                    Azure Subscription
                            │
                            ▼
                    Resource Group
                            │
                            ▼
                   Virtual Machine
        ┌───────────┼────────────┬─────────────┐
        ▼           ▼            ▼             ▼
   Network      Public IP    Managed Disk    Image
   Interface         │              │            │
        │            ▼              ▼            ▼
        └──────► Virtual Network ◄──┴────── Operating System
                     │
                  Subnet
                     │
          Network Security Group
```

---

# Resource Group

A Resource Group is a logical container used to organize Azure resources.

Instead of managing every resource separately, Azure groups related resources together.

Example

```
Resource Group

DevOps-RG

├── Ubuntu-VM
├── Public IP
├── Virtual Network
├── Network Interface
├── Managed Disk
└── Network Security Group
```

Benefits

- Easy management
- Resource organization
- Permission management
- Delete all related resources together

---

# Virtual Network (VNet)

A Virtual Network (VNet) is a private network inside Azure.

It allows Azure resources to securely communicate with each other.

Think of it as your own private network inside Microsoft's cloud.

Example

```
Virtual Network

10.0.0.0/16

│
├── VM 1
├── VM 2
├── Database
└── Storage
```

Benefits

- Secure communication
- Isolation from other Azure customers
- Connect multiple Azure resources

---

# Subnet

A Subnet divides a Virtual Network into smaller logical networks.

Example

```
Virtual Network

10.0.0.0/16

│
├── Web Subnet
│      10.0.1.0/24
│
├── Application Subnet
│      10.0.2.0/24
│
└── Database Subnet
       10.0.3.0/24
```

Benefits

- Better organization
- Improved security
- Easier traffic management

---

# Public IP Address

A Public IP allows your Virtual Machine to communicate with the Internet.

Example

```
Internet

↓

20.197.xxx.xxx

↓

Azure VM
```

Without a Public IP:

- You cannot SSH into a Linux VM.
- You cannot use RDP for a Windows VM.
- The VM cannot be directly accessed from the internet.

---

# Private IP Address

Every Azure Virtual Machine also receives a Private IP.

Example

```
10.0.0.4
```

Private IPs are used for communication inside the Virtual Network.

Example

```
VM

↓

10.0.0.4

↓

Database

↓

10.0.0.5
```

Private IPs cannot be accessed from the Internet.

---

# Network Interface (NIC)

The Network Interface (NIC) connects the Virtual Machine to the Virtual Network.

Every Azure VM must have at least one Network Interface.

A NIC contains:

- Private IP
- Public IP (optional)
- Network Security Group
- MAC Address

Example

```
Virtual Machine

↓

Network Interface

↓

Private IP

↓

Virtual Network
```

---

# Network Security Group (NSG)

A Network Security Group (NSG) acts as a firewall for Azure resources.

It controls which network traffic is allowed or denied.

Example

| Port | Protocol | Action |
|------|----------|--------|
| 22 | SSH | Allow |
| 80 | HTTP | Allow |
| 443 | HTTPS | Allow |
| All Others | Any | Deny |

Without NSG rules, users cannot connect to the VM.

---

# Managed Disk

Every Azure Virtual Machine requires storage.

Azure provides Managed Disks.

Types

- Standard HDD
- Standard SSD
- Premium SSD
- Premium SSD v2
- Ultra Disk

Advantages

- High availability
- Automatic management
- Better performance
- Built-in redundancy

---

# Operating System Disk

Every VM has one Operating System Disk.

Example

Ubuntu Server

↓

Operating System Disk

↓

Linux Files

Applications

Configurations

Logs

---

# Data Disk

Additional Data Disks can be attached whenever extra storage is required.

Examples

- Database storage
- Backup storage
- Application data
- Media files

Unlike the OS Disk, Data Disks only store user data.

---

# Virtual Machine Image

An Image is a template used to create the Operating System.

Examples

- Ubuntu Server 24.04 LTS
- Windows Server 2022
- Debian
- Red Hat Enterprise Linux
- CentOS

Every time you create a VM, Azure copies the selected image to create the Operating System Disk.

---

# Availability Zone

Availability Zones protect Virtual Machines from hardware failures.

Each zone has:

- Independent power
- Independent cooling
- Independent networking

Example

```
Central India

│

├── Zone 1

├── Zone 2

└── Zone 3
```

If one zone experiences an outage, applications can continue running in another zone.

---

# How All Components Work Together

```
Internet
      │
      ▼
Public IP
      │
      ▼
Network Security Group
      │
      ▼
Network Interface
      │
      ▼
Virtual Machine
      │
      ▼
Operating System
      │
      ▼
Managed Disk
      │
      ▼
Virtual Network
      │
      ▼
Subnet
```

---

# Best Practices

- Organize related resources inside a single Resource Group.
- Use Virtual Networks to isolate resources.
- Divide large networks using Subnets.
- Expose only necessary services through Public IP addresses.
- Restrict inbound traffic using Network Security Groups.
- Use Managed Disks for better reliability and easier management.
- Choose Availability Zones for production workloads to improve availability.

---

# Quick Revision

| Component | Purpose |
|-----------|---------|
| Resource Group | Logical container for Azure resources |
| Virtual Network | Private network inside Azure |
| Subnet | Division of a Virtual Network |
| Public IP | Internet connectivity |
| Private IP | Internal communication |
| Network Interface | Connects VM to the network |
| Network Security Group | Firewall rules |
| Managed Disk | Storage for the VM |
| OS Disk | Stores the operating system |
| Data Disk | Stores user data |
| Image | Template used to create a VM |
| Availability Zone | Protects against data center failures |
---

# Azure Virtual Machine States

Every Azure Virtual Machine goes through different states during its lifecycle.

Understanding these states is important because some states continue to incur charges, while others do not.

```
Create
   │
   ▼
Starting
   │
   ▼
Running
   │
   ▼
Stopping
   │
   ▼
Stopped
   │
   ▼
Deallocated
   │
   ▼
Deleted
```

---

# 1. Creating State

This state occurs immediately after clicking **Create** in the Azure Portal.

During this phase Azure performs the following tasks:

- Creates the Virtual Machine
- Creates the Operating System Disk
- Creates the Network Interface
- Assigns an IP Address
- Configures Networking
- Installs the Operating System

```
User

↓

Create VM

↓

Azure starts provisioning resources
```

Duration:

Usually 2–5 minutes.

---

# 2. Starting State

The Virtual Machine is booting.

Azure starts:

- CPU
- Memory
- Operating System
- Network Services

```
Power On

↓

Operating System Boot

↓

Running
```

During this state the VM cannot yet be accessed.

---

# 3. Running State

The Virtual Machine is fully operational.

Users can:

- SSH into Linux VM
- RDP into Windows VM
- Install software
- Run applications
- Host websites

Example

```
Internet

↓

Public IP

↓

Ubuntu VM

↓

Nginx

↓

Website
```

Billing

✅ Compute charges apply.

✅ Storage charges apply.

---

# 4. Stopping State

Azure begins shutting down the Virtual Machine.

The Operating System closes running processes.

```
Running

↓

Shutdown

↓

Stopped
```

Usually lasts a few seconds.

---

# 5. Stopped State

The Operating System has shut down.

However...

The Virtual Machine is still reserved on Azure hardware.

This means Azure still reserves:

- CPU
- Memory

Because of this,

**Compute charges continue.**

```
VM

↓

Powered Off

↓

Still Reserved
```

Billing

✅ Compute charges apply.

✅ Storage charges apply.

---

# 6. Deallocated State

This is the recommended way to stop a Virtual Machine.

Azure releases:

- CPU
- RAM
- Physical Host

Only storage resources remain.

```
VM

↓

Stopped

↓

Resources Released

↓

Storage Remains
```

Billing

❌ Compute charges stop.

✅ Storage charges continue.

This is why development Virtual Machines should always be **Stopped (Deallocated)** when not in use.

---

# 7. Deleted State

When a Virtual Machine is deleted:

- Compute resources are removed
- VM configuration is deleted

However,

Managed Disks and Public IP addresses may still remain if they were configured to be retained.

Always verify associated resources after deleting a VM.

---

# VM Lifecycle

```
Create

↓

Provisioning

↓

Running

↓

Stop

↓

Stopped

↓

Deallocate

↓

Start Again

↓

Running

↓

Delete
```

---

# Billing Comparison

| VM State | Compute Charges | Storage Charges |
|-----------|-----------------|-----------------|
| Creating | Yes | Yes |
| Starting | Yes | Yes |
| Running | Yes | Yes |
| Stopped | Yes | Yes |
| Deallocated | No | Yes |
| Deleted | No | Depends on retained resources |

---

# Difference Between Stop and Deallocate

This is one of the most frequently asked Azure interview questions.

| Stop | Deallocate |
|------|------------|
| VM is powered off | VM is powered off |
| Azure still reserves hardware | Azure releases hardware |
| Compute charges continue | Compute charges stop |
| Storage charges continue | Storage charges continue |
| Suitable for temporary shutdown | Recommended for cost saving |

---

# Starting a Virtual Machine

Using Azure Portal:

```
Virtual Machine

↓

Start
```

Using Azure CLI

```bash
az vm start \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

---

# Stopping a Virtual Machine

Using Azure Portal:

```
Virtual Machine

↓

Stop
```

Using Azure CLI

```bash
az vm stop \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

---

# Deallocating a Virtual Machine

Azure Portal

```
Stop

↓

Azure automatically deallocates
```

Azure CLI

```bash
az vm deallocate \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

---

# Restarting a Virtual Machine

Restarting is similar to pressing the restart button on a physical computer.

Azure Portal

```
Restart
```

Azure CLI

```bash
az vm restart \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

---

# Deleting a Virtual Machine

Azure Portal

```
Delete
```

Azure CLI

```bash
az vm delete \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

Azure asks for confirmation before deletion.

---

# Best Practices

- Stop and deallocate development VMs when they are not in use.
- Delete unused Virtual Machines to avoid unnecessary charges.
- Check whether disks and Public IP addresses are still attached after deleting a VM.
- Monitor VM states using Azure Monitor.

---

# Interview Questions

### What is the difference between Stop and Deallocate?

Stopping shuts down the operating system, but Azure still reserves hardware and continues compute billing.

Deallocation releases the hardware resources, stopping compute charges while storage charges continue.

---

### Does deleting a VM always delete its disks?

No.

Managed disks may remain depending on the deletion settings.

---

### Which VM state stops compute billing?

**Deallocated** is the state where compute billing stops.

---

### Which VM state is best for development environments?

**Stopped (Deallocated)** because it minimizes costs while preserving the VM's data on its disks.
---

# Azure Managed Disks

Every Azure Virtual Machine requires storage to hold its operating system, applications, and data.

Azure provides **Managed Disks**, which are fully managed block-level storage volumes designed for Azure Virtual Machines.

Instead of manually managing storage accounts, Azure automatically handles:

- Storage provisioning
- Replication
- Availability
- Performance
- Scaling
- Maintenance

Managed Disks make storage management simpler, more reliable, and highly available.

---

# What is a Managed Disk?

A Managed Disk is a virtual hard disk (VHD) managed entirely by Azure.

Think of it as the hard drive of your Virtual Machine.

```
Azure Virtual Machine
        │
        ▼
   Managed Disk
        │
        ▼
 Azure Storage Infrastructure
```

Microsoft automatically manages:

- Storage Accounts
- Availability
- Data Replication
- Hardware Failures

Users only need to select the disk type and size.

---

# Types of Azure Managed Disks

Azure provides several disk types based on performance requirements.

```
Managed Disks

│

├── Standard HDD

├── Standard SSD

├── Premium SSD

├── Premium SSD v2

└── Ultra Disk
```

---

# 1. Standard HDD

Standard HDDs are traditional magnetic hard disks.

Suitable for:

- Backup storage
- Development environments
- Testing
- Infrequently accessed data

Advantages

- Lowest cost
- Large storage capacity

Disadvantages

- Lowest performance
- Higher latency

Example

```
Development VM

↓

Standard HDD
```

---

# 2. Standard SSD

Standard SSDs use solid-state storage.

Suitable for:

- Small web applications
- Light production workloads
- Development

Advantages

- Better performance than HDD
- Lower latency
- Affordable

Example

```
Ubuntu VM

↓

Standard SSD

↓

Linux Practice
```

---

# 3. Premium SSD

Premium SSDs provide high-performance storage.

Suitable for:

- Enterprise Applications
- Databases
- Production workloads

Advantages

- High IOPS
- Low latency
- High throughput

Example

```
SQL Server

↓

Premium SSD
```

---

# 4. Premium SSD v2

Premium SSD v2 provides improved performance with flexible configuration.

Features

- Higher IOPS
- Better throughput
- Lower latency
- Independent performance tuning

Recommended for demanding production workloads.

---

# 5. Ultra Disk

Ultra Disk is Azure's highest-performance storage option.

Suitable for:

- SAP HANA
- Large Databases
- High Transaction Systems
- Scientific Applications

Advantages

- Extremely high IOPS
- Very low latency
- Highest throughput

Disadvantages

- Most expensive

---

# Comparison of Disk Types

| Disk Type | Performance | Cost | Best For |
|------------|-------------|------|----------|
| Standard HDD | Low | Low | Backup, Development |
| Standard SSD | Medium | Medium | Small Applications |
| Premium SSD | High | High | Production |
| Premium SSD v2 | Very High | Higher | Enterprise Applications |
| Ultra Disk | Highest | Highest | Mission-Critical Workloads |

---

# Types of Disks Attached to a Virtual Machine

Every Azure VM contains different types of disks.

```
Azure VM

│

├── Operating System Disk

├── Temporary Disk

└── Data Disk(s)
```

---

# Operating System (OS) Disk

Every Virtual Machine requires exactly one Operating System Disk.

The OS Disk contains:

- Operating System
- Boot Files
- Installed Applications
- System Configuration
- System Logs

Example

```
Ubuntu Server

↓

OS Disk

↓

Linux Files

Applications

Packages
```

Without the OS Disk, the VM cannot boot.

---

# Data Disk

Data Disks provide additional storage.

Used for:

- Databases
- Application Files
- Media
- Backups
- User Data

One Virtual Machine can have multiple Data Disks.

Example

```
Azure VM

│

├── OS Disk

├── Data Disk 1

├── Data Disk 2

└── Data Disk 3
```

Advantages

- Easy to expand storage
- Better organization
- Separate operating system and application data

---

# Temporary Disk

Some Azure Virtual Machines include a Temporary Disk.

Purpose

- Temporary files
- Cache
- Swap files
- Scratch space

Important

Temporary Disks are **not persistent**.

Data stored on the Temporary Disk can be lost during:

- VM Restart
- VM Deallocation
- Host Maintenance

Never store important files on a Temporary Disk.

---

# Disk Encryption

Azure supports encryption to protect stored data.

Options include:

- Azure Disk Encryption
- Server-Side Encryption
- Customer-Managed Keys
- Platform-Managed Keys

Benefits

- Improved security
- Data protection
- Compliance

---

# Snapshots

A Snapshot is a read-only copy of a disk at a specific point in time.

Example

```
Disk

↓

Snapshot

↓

Restore Later
```

Use Cases

- Backup before updates
- Disaster Recovery
- Testing
- Rollback

---

# Managed Disk vs Unmanaged Disk

Earlier, Azure required users to manage storage accounts manually.

Now Azure recommends Managed Disks.

| Managed Disk | Unmanaged Disk |
|---------------|----------------|
| Azure manages storage | User manages storage accounts |
| Easy to use | More complex |
| Better reliability | Manual configuration |
| Recommended | Legacy option |

---

# Resizing a Disk

Azure allows disks to be expanded when more storage is required.

Example

```
Current Size

↓

128 GB

↓

Resize

↓

256 GB
```

Resizing does not affect the operating system.

---

# Best Practices

- Use Standard SSD for learning.
- Use Premium SSD for production workloads.
- Store databases on Data Disks instead of the OS Disk.
- Never store important data on Temporary Disks.
- Enable disk encryption for sensitive workloads.
- Take snapshots before performing major updates.
- Monitor disk performance using Azure Monitor.

---

# Interview Questions

### What is an Azure Managed Disk?

A Managed Disk is a block-level storage volume managed by Azure and attached to Virtual Machines.

---

### What is the difference between an OS Disk and a Data Disk?

The OS Disk stores the operating system and boot files, while Data Disks store user applications and data.

---

### Can a VM have multiple Data Disks?

Yes.

A Virtual Machine can have multiple Data Disks depending on its size.

---

### Is the Temporary Disk persistent?

No.

Data stored on a Temporary Disk can be lost during restart, deallocation, or maintenance.

---

### Which disk type is recommended for production workloads?

Premium SSD or Premium SSD v2 depending on performance requirements.

---

# Quick Revision

| Component | Purpose |
|-----------|----------|
| Managed Disk | Azure-managed storage |
| OS Disk | Stores operating system |
| Data Disk | Stores user data |
| Temporary Disk | Cache and temporary files |
| Snapshot | Point-in-time backup |
| Standard HDD | Low-cost storage |
| Standard SSD | General-purpose storage |
| Premium SSD | Production workloads |
| Premium SSD v2 | High-performance workloads |
| Ultra Disk | Mission-critical applications |


---

# Azure Networking for Virtual Machines

Networking is one of the most important components of an Azure Virtual Machine.

Without networking, a Virtual Machine cannot communicate with:

- The Internet
- Other Virtual Machines
- Azure Services
- Databases
- Users

Azure networking provides secure communication between resources while allowing administrators to control network traffic.

---

# Azure Networking Architecture

```
                      Internet
                          │
                          ▼
                    Public IP Address
                          │
                          ▼
               Network Security Group
                          │
                          ▼
                Network Interface (NIC)
                          │
                          ▼
                Azure Virtual Machine
                          │
                          ▼
                    Private IP Address
                          │
                          ▼
                       Subnet
                          │
                          ▼
                 Virtual Network (VNet)
```

Each component plays a specific role in enabling communication between Azure resources.

---

# Virtual Network (VNet)

A Virtual Network (VNet) is Azure's private network.

It allows Azure resources to securely communicate with one another.

Think of a VNet as your organization's private network inside Microsoft's cloud.

Example

```
Company Network

↓

Azure Virtual Network

↓

Web Server

↓

Database Server

↓

Application Server
```

A Virtual Network provides:

- Isolation
- Secure communication
- IP address management
- Connectivity between Azure resources

---

# Address Space

Every Virtual Network requires an IP address range.

Example

```
10.0.0.0/16
```

This address space defines all available private IP addresses within the Virtual Network.

Example

```
Virtual Network

Address Space

10.0.0.0/16
```

---

# Subnet

A Subnet divides a Virtual Network into smaller logical networks.

Instead of placing every resource in one large network, Azure allows you to organize them into multiple subnets.

Example

```
Virtual Network

10.0.0.0/16

│

├── Web Subnet

│      10.0.1.0/24

│

├── Application Subnet

│      10.0.2.0/24

│

└── Database Subnet

       10.0.3.0/24
```

Benefits

- Better organization
- Improved security
- Easier traffic management
- Network isolation

---

# Why Use Multiple Subnets?

Imagine an application consisting of:

- Frontend Website
- Backend API
- Database

Instead of placing all servers together, separate them.

```
Internet

↓

Web Subnet

↓

Application Subnet

↓

Database Subnet
```

This improves security because users can only access the web server directly.

---

# Public IP Address

A Public IP allows Azure resources to communicate with the Internet.

Example

```
Internet

↓

52.168.xx.xx

↓

Ubuntu VM
```

Uses

- SSH
- Remote Desktop
- Website Hosting
- Public APIs

Without a Public IP, users outside Azure cannot directly access the Virtual Machine.

---

# Private IP Address

Every Azure Virtual Machine receives a Private IP Address.

Example

```
10.0.1.4
```

Private IP addresses are used only inside the Virtual Network.

Example

```
Ubuntu VM

↓

10.0.1.4

↓

SQL Database

↓

10.0.2.5
```

Private IPs are faster and more secure because they are not exposed to the Internet.

---

# Public IP vs Private IP

| Public IP | Private IP |
|------------|------------|
| Accessible from the Internet | Accessible only within the Virtual Network |
| Used for SSH and RDP | Used for internal communication |
| Globally unique | Private to the VNet |
| Less secure if not protected | More secure |

---

# Network Interface (NIC)

Every Azure Virtual Machine requires a Network Interface.

A Network Interface connects the VM to the Virtual Network.

The NIC stores:

- Private IP Address
- Public IP Address (optional)
- Network Security Group
- MAC Address

```
Virtual Machine

↓

Network Interface

↓

Private IP

↓

Virtual Network
```

Without a NIC, a Virtual Machine cannot communicate with the network.

---

# Network Security Group (NSG)

A Network Security Group (NSG) acts as a firewall.

It controls which network traffic is allowed or denied.

Example

```
Internet

↓

Network Security Group

↓

Ubuntu VM
```

An NSG contains:

- Inbound Rules
- Outbound Rules

---

# Inbound Rules

Inbound rules control traffic entering the Virtual Machine.

Example

| Priority | Port | Protocol | Action |
|----------|------|----------|--------|
| 100 | 22 | TCP | Allow |
| 110 | 80 | TCP | Allow |
| 120 | 443 | TCP | Allow |
| 4096 | * | Any | Deny |

Meaning

- SSH allowed
- HTTP allowed
- HTTPS allowed
- Everything else blocked

---

# Outbound Rules

Outbound rules control traffic leaving the Virtual Machine.

Example

```
Ubuntu VM

↓

Internet

↓

Allowed
```

These rules help restrict communication with external services if required.

---

# Common Ports

| Port | Protocol | Purpose |
|------|----------|----------|
| 22 | SSH | Linux Remote Login |
| 80 | HTTP | Website |
| 443 | HTTPS | Secure Website |
| 3389 | RDP | Windows Remote Desktop |
| 3306 | MySQL | Database |
| 1433 | SQL Server | Database |
| 5432 | PostgreSQL | Database |

---

# Example: Hosting a Website

Suppose you deploy Nginx on an Ubuntu VM.

To access the website, Azure requires:

- Public IP
- NSG Rule for Port 80
- Running Nginx Service

```
Internet

↓

Public IP

↓

NSG

↓

Port 80

↓

Ubuntu VM

↓

Nginx

↓

Website
```

Without allowing Port 80, the website cannot be accessed.

---

# Example: Connecting Using SSH

```
Laptop

↓

Internet

↓

Public IP

↓

NSG

↓

Port 22

↓

Ubuntu VM
```

Only when Port 22 is allowed can SSH connections be established.

---

# Azure DNS

Azure automatically assigns DNS names if configured.

Example

Instead of

```
20.198.xxx.xxx
```

You can use

```
myserver.centralindia.cloudapp.azure.com
```

DNS makes servers easier to identify.

---

# Best Practices

- Use Private IPs whenever possible.
- Open only the required ports.
- Never allow unnecessary inbound traffic.
- Keep databases inside private subnets.
- Use NSGs to restrict access.
- Remove unused Public IP addresses.
- Regularly review firewall rules.

---

# Interview Questions

### What is a Virtual Network (VNet)?

A Virtual Network is a private network in Azure that enables secure communication between Azure resources.

---

### What is the difference between a VNet and a Subnet?

A VNet is the entire private network, while a Subnet is a smaller segment within the VNet used to organize and isolate resources.

---

### What is the difference between a Public IP and a Private IP?

A Public IP allows internet access, whereas a Private IP is used only for communication within the Azure Virtual Network.

---

### Why is a Network Interface (NIC) required?

A NIC connects the Virtual Machine to the Virtual Network and manages IP addresses, NSGs, and network communication.

---

### What is a Network Security Group (NSG)?

An NSG is a virtual firewall that controls inbound and outbound traffic to Azure resources.

---

### Which ports are commonly opened for Azure VMs?

- 22 → SSH
- 80 → HTTP
- 443 → HTTPS
- 3389 → RDP

---

# Quick Revision

| Component | Purpose |
|-----------|---------|
| Virtual Network (VNet) | Private Azure network |
| Address Space | IP range for the VNet |
| Subnet | Logical division of a VNet |
| Public IP | Internet connectivity |
| Private IP | Internal communication |
| Network Interface (NIC) | Connects VM to the network |
| Network Security Group (NSG) | Firewall for Azure resources |
| Inbound Rules | Control incoming traffic |
| Outbound Rules | Control outgoing traffic |
---

# Azure Snapshots

A Snapshot is a **read-only, point-in-time copy** of an Azure Managed Disk.

Snapshots are commonly used to create backups before making important changes to a Virtual Machine. They allow administrators to restore the disk to its previous state if something goes wrong.

Snapshots can be created from both:

* Operating System (OS) Disks
* Data Disks

```
Managed Disk
      │
      ▼
Create Snapshot
      │
      ▼
Read-only Snapshot
      │
      ▼
Restore Disk (if required)
```

---

## Why Use Snapshots?

Snapshots are useful in several situations:

* Before updating the operating system
* Before installing software
* Before changing server configurations
* Before database upgrades
* Before applying security patches
* Disaster recovery
* Testing new configurations

Example

Suppose you are planning to upgrade an Ubuntu server.

Instead of directly upgrading,

```
Ubuntu VM

↓

Create Snapshot

↓

Upgrade Ubuntu

↓

If upgrade fails

↓

Restore Snapshot
```

---

## Snapshot vs Backup

| Snapshot                     | Backup                               |
| ---------------------------- | ------------------------------------ |
| Point-in-time copy of a disk | Complete backup of the VM            |
| Faster to create             | Takes longer                         |
| Disk-level protection        | VM-level protection                  |
| Used for quick recovery      | Used for long-term recovery          |
| Read-only                    | Can contain multiple recovery points |

---

## Creating a Snapshot (Azure Portal)

1. Open **Azure Portal**
2. Navigate to **Virtual Machines**
3. Select your VM
4. Open **Disks**
5. Click the **OS Disk**
6. Select **Create Snapshot**
7. Enter a Snapshot Name
8. Select the Resource Group
9. Click **Review + Create**
10. Click **Create**

Azure creates a read-only copy of the selected disk.

---

## Restoring from a Snapshot

A snapshot cannot be directly attached to a VM.

The process is:

```
Snapshot

↓

Create Managed Disk

↓

Attach Disk to VM

↓

Recover Data
```

---

# Azure CLI Commands

Azure CLI (Command Line Interface) allows Azure resources to be managed directly from the terminal.

Instead of using the Azure Portal, administrators can automate tasks using commands.

---

## Login to Azure

```bash
az login
```

Opens the Azure login page and authenticates your account.

---

## Show Current Subscription

```bash
az account show
```

Displays information about the active Azure subscription.

---

## List All Resource Groups

```bash
az group list --output table
```

Lists all available Resource Groups.

---

## Create a Resource Group

```bash
az group create \
    --name DevOps-RG \
    --location centralindia
```

Creates a Resource Group named **DevOps-RG** in the Central India region.

---

## List Virtual Machines

```bash
az vm list --output table
```

Displays all Virtual Machines in the subscription.

---

## Show VM Details

```bash
az vm show \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

Displays detailed information about the Virtual Machine.

---

## Start a Virtual Machine

```bash
az vm start \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

Starts a stopped Virtual Machine.

---

## Stop a Virtual Machine

```bash
az vm stop \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

Stops the Virtual Machine.

---

## Deallocate a Virtual Machine

```bash
az vm deallocate \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

Stops the VM and releases compute resources, reducing costs.

---

## Restart a Virtual Machine

```bash
az vm restart \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

Restarts the Virtual Machine.

---

## Delete a Virtual Machine

```bash
az vm delete \
    --resource-group DevOps-RG \
    --name Ubuntu-VM
```

Deletes the Virtual Machine.

---

## Open Port 80

```bash
az vm open-port \
    --resource-group DevOps-RG \
    --name Ubuntu-VM \
    --port 80
```

Creates an NSG rule allowing HTTP traffic.

---

## Open Port 443

```bash
az vm open-port \
    --resource-group DevOps-RG \
    --name Ubuntu-VM \
    --port 443
```

Allows HTTPS traffic.

---

# Best Practices

When deploying Azure Virtual Machines, follow these recommendations:

### Use Meaningful Names

Choose descriptive names for resources.

Example

```
DevOps-RG

Ubuntu-Web-VM

Production-DB
```

Avoid generic names like:

```
VM1

Test123

Server
```

---

### Use SSH Keys

For Linux Virtual Machines, always prefer SSH key authentication instead of passwords.

Benefits:

* Better security
* Faster authentication
* Resistant to brute-force attacks

---

### Stop Development VMs

If a VM is not in use,

**Stop (Deallocate)** it to reduce costs.

---

### Use Availability Zones

Deploy production Virtual Machines across Availability Zones to improve availability.

---

### Open Only Required Ports

Do not expose unnecessary ports.

Allow only:

* 22 (SSH)
* 80 (HTTP)
* 443 (HTTPS)

Block all other inbound traffic unless required.

---

### Keep Operating Systems Updated

Regularly install security patches and operating system updates.

---

### Enable Backups

Use Azure Backup or Snapshots before making significant changes.

---

### Monitor Resource Usage

Track:

* CPU
* Memory
* Disk Usage
* Network Traffic

using Azure Monitor.

---

### Delete Unused Resources

Unused resources continue to incur charges.

Regularly remove:

* Virtual Machines
* Public IP Addresses
* Managed Disks
* Snapshots

---

# Hands-on Lab

## Objective

Create an Ubuntu Virtual Machine, connect using SSH, install Nginx, create a Snapshot, and clean up all resources.

---

## Lab Steps

### Step 1

Create a Resource Group.

```
Name

DevOps-RG

Region

Central India
```

---

### Step 2

Create an Ubuntu Virtual Machine.

Configuration:

* Ubuntu Server 24.04 LTS
* Standard_B1s
* SSH Authentication
* Allow Port 22

---

### Step 3

Connect to the VM.

```bash
ssh azureuser@<public-ip>
```

---

### Step 4

Update Ubuntu.

```bash
sudo apt update
sudo apt upgrade -y
```

---

### Step 5

Install Nginx.

```bash
sudo apt install nginx -y
```

---

### Step 6

Open Port 80.

```bash
az vm open-port \
    --resource-group DevOps-RG \
    --name Ubuntu-VM \
    --port 80
```

Open:

```
http://<public-ip>
```

You should see the default Nginx page.

---

### Step 7

Create a Snapshot of the OS Disk using the Azure Portal.

---

### Step 8

Stop (Deallocate) the Virtual Machine.

---

### Step 9

Delete the Resource Group after completing the lab.

---

# Azure Virtual Machine Interview Questions

---

<details>
<summary><strong>1. What is an Azure Virtual Machine?</strong></summary>

An Azure Virtual Machine (VM) is an Infrastructure as a Service (IaaS) offering that allows users to create and run virtual servers in the Microsoft Azure cloud. It provides complete control over the operating system, installed software, storage, and networking while Microsoft manages the underlying physical infrastructure.

</details>

---

<details>
<summary><strong>2. What is the difference between IaaS, PaaS, and SaaS?</strong></summary>

| IaaS | PaaS | SaaS |
|------|------|------|
| Provides virtual infrastructure | Provides a platform to build applications | Provides ready-to-use software |
| User manages OS and applications | User manages only applications | Provider manages everything |
| Example: Azure VM | Example: Azure App Service | Example: Microsoft 365 |

</details>

---

<details>
<summary><strong>3. What resources are created when you create an Azure Virtual Machine?</strong></summary>

When an Azure VM is created, Azure typically creates or associates:

- Resource Group
- Virtual Machine
- Virtual Network (VNet)
- Subnet
- Network Interface (NIC)
- Public IP Address (optional)
- Network Security Group (NSG)
- Managed Disk (OS Disk)
- Data Disk (optional)

These resources work together to provide networking, storage, and connectivity for the VM.

</details>

---

<details>
<summary><strong>4. What is the difference between Stop and Deallocate?</strong></summary>

**Stop**

- Operating system shuts down.
- Azure still reserves the physical hardware.
- Compute charges continue.
- Storage charges continue.

**Deallocate**

- Operating system shuts down.
- Azure releases CPU and RAM resources.
- Compute charges stop.
- Storage charges continue.

For development VMs, always choose **Stop (Deallocate)** to reduce costs.

</details>

---

<details>
<summary><strong>5. What is a Managed Disk?</strong></summary>

A Managed Disk is Azure-managed block storage attached to a Virtual Machine. Azure automatically handles storage provisioning, replication, scalability, and availability, making storage management much simpler than unmanaged disks.

</details>

---

<details>
<summary><strong>6. What is a Network Security Group (NSG)?</strong></summary>

A Network Security Group (NSG) is a virtual firewall in Azure that controls inbound and outbound traffic using security rules.

Example:

- Port 22 → SSH
- Port 80 → HTTP
- Port 443 → HTTPS

Any traffic not explicitly allowed can be denied.

</details>
