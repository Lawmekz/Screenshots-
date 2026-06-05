# Microsoft Azure Onboarding Lab – Full Documentation
**Name:** Ajagu Nnaemeka Lawrence  
**Date:** June 4–5, 2026  
**GitHub:** Lawmekz/Screenshots-

---

## Table of Contents
1. [Account Creation](#1-account-creation)
2. [Azure Portal Navigation](#2-azure-portal-navigation)
3. [Dashboard Customization](#3-dashboard-customization)
4. [Governance Setup – Resource Group](#4-governance-setup--resource-group)
5. [Identity & Security (Entra ID + RBAC)](#5-identity--security-entra-id--rbac)
6. [Region Selection](#6-region-selection)
7. [Resource Deployment – Storage Account](#7-resource-deployment--storage-account)
8. [Billing & Cost Management](#8-billing--cost-management)
9. [Free Tier Limits & Summary](#9-free-tier-limits--summary)
10. [Security Considerations](#10-security-considerations)
11. [Completion Checklist](#11-completion-checklist)
12. [Troubleshooting](#12-troubleshooting)

---

## 1. Account Creation

### Step-by-Step Process
1. Visited [https://azure.microsoft.com/free](https://azure.microsoft.com/free)
2. Clicked **"Start free"** and signed in with a Microsoft account
3. Completed **identity verification:**
   - Entered full name and contact details
   - Verified phone number via SMS code
   - Added a credit/debit card for validation (not charged)
4. Agreed to the Azure terms and conditions
5. Account activated with **$200 free credit** valid for 30 days

### Verification Evidence
- Screenshot 1: Azure Portal Dashboard showing active subscription
- Screenshot 2: Subscription page showing free credits

---

## 2. Azure Portal Navigation

### Key Areas Explored

| Area | Description | How to Access |
|------|-------------|---------------|
| **Home** | Central hub with shortcuts to resources | Click "Home" in sidebar |
| **Dashboard** | Customizable overview of your resources | Click "Dashboard" |
| **All Services** | Full catalog of Azure services | Left sidebar → "All services" |
| **Search Bar** | Find any service instantly | Top bar (Ctrl + /) |
| **Notifications** | Deployment alerts and updates | Bell icon (top right) |
| **Settings** | Theme, language, timeout preferences | Gear icon (top right) |
| **Cloud Shell** | Browser-based CLI (Bash/PowerShell) | Terminal icon (top bar) |

### Key Service Locations

| Service | Location in Portal |
|---------|--------------------|
| Virtual Machines | Left sidebar → Virtual machines |
| Storage Accounts | Left sidebar → Storage accounts |
| Resource Groups | Left sidebar → Resource groups |
| Microsoft Entra ID | Search "Entra ID" |
| Cost Management | Left sidebar → Cost Management + Billing |
| Azure Monitor | Search "Monitor" |

### Search Functionality
- The **top search bar** supports searching by service name, resource name, or documentation
- Results are grouped into: Services, Resources, Marketplace, and Documentation

---

## 3. Dashboard Customization

### Steps to Customize Dashboard
1. Navigated to **Dashboard** from the left sidebar
2. Clicked **"Edit"** in the top toolbar
3. Added the following tiles from the tile gallery:
   - **All resources** – shows all deployed resources
   - **Resource groups** – quick access to resource groups
   - **Service health** – monitors Azure service status
   - **Cost Management** – tracks spending at a glance
4. Rearranged tiles by dragging to preferred positions
5. Clicked **"Save"** to apply customization

> 📸 Screenshot 3: Customized Azure Dashboard view

---

## 4. Governance Setup – Resource Group

### What is a Resource Group?
A Resource Group is a logical container that holds related Azure resources for a solution. It allows you to manage, monitor, and control access to resources collectively.

### Steps Taken
1. Searched **"Resource groups"** in the top search bar
2. Clicked **"+ Create"**
3. Filled in the following details:

| Field | Value |
|-------|-------|
| **Subscription** | Azure Subscription 1 |
| **Resource Group Name** | MyFirstResourceGroup |
| **Region** | West Europe |

4. Clicked **"Review + Create"** → Validated → **"Create"**
5. Resource group successfully created

> 📸 Screenshot 4: MyFirstResourceGroup overview page

---

## 5. Identity & Security (Entra ID + RBAC)

### Microsoft Entra ID (formerly Azure Active Directory)
Microsoft Entra ID is Azure's cloud-based identity and access management service.

### Steps Taken
1. Searched **"Microsoft Entra ID"** in the top search bar
2. Navigated to **Users** → reviewed the user list
3. Clicked on user profile: **Ajagu Nnaemeka Lawrence**
4. Navigated to **Assigned Roles**

### Assigned Role Discovered

| Field | Value |
|-------|-------|
| **User** | Ajagu Nnaemeka Lawrence |
| **Role** | Global Administrator |
| **Scope** | Directory (Organization-wide) |
| **Resource Type** | Organization |

> 🔑 **Global Administrator** is the highest privilege role — it can manage all aspects of Microsoft Entra ID and Microsoft services.

### Role-Based Access Control (RBAC)
RBAC allows fine-grained access management to Azure resources.

| Role | Permissions |
|------|-------------|
| **Owner** | Full access including access management |
| **Contributor** | Can create/manage resources, no access management |
| **Reader** | View-only access |
| **Global Administrator** | Manages all Entra ID and Microsoft services |

### How to Review RBAC on a Resource
1. Go to **Resource groups** → **MyFirstResourceGroup**
2. Click **"Access control (IAM)"** in the left menu
3. Click **"View my access"** to see current role assignments

> 📸 Screenshot 5: Microsoft Entra ID Users page  
> 📸 Screenshot 6: Assigned Roles – Global Administrator

---

## 6. Region Selection

### Research & Decision

| Region | Location | Approx. Distance from Nigeria |
|--------|----------|-------------------------------|
| **South Africa North** ⭐ | Johannesburg 🇿🇦 | ~3,200 km — **Closest** |
| **South Africa West** | Cape Town 🇿🇦 | ~4,800 km |
| **West Europe** | Netherlands 🇳🇱 | ~5,200 km |
| **UK South** | London 🇬🇧 | ~5,000 km |

### Decision
- **Primary Region Selected:** South Africa North (Johannesburg)
- **Reason:** Lowest latency for users in Nigeria/West Africa, ensuring faster response times and better performance
- **Backup Region:** West Europe (Netherlands) — used for Resource Group and Storage Account

### Availability Zones
South Africa North supports **Availability Zones**, which provide redundancy across physically separate data centers within the same region, protecting against datacenter-level failures.

---

## 7. Resource Deployment – Storage Account

### What is a Storage Account?
Azure Storage Account provides cloud storage for blobs (objects), files, queues, and tables. It is a core IaaS/PaaS service in Azure.

### Deployment Steps
1. Searched **"Storage accounts"** in the top search bar
2. Clicked **"+ Create"**
3. Filled in configuration:

| Field | Value |
|-------|-------|
| **Subscription** | Azure Subscription 1 |
| **Resource Group** | MyFirstResourceGroup |
| **Storage Account Name** | ajagustorage |
| **Region** | West Europe |
| **Performance** | Standard |
| **Redundancy** | Locally Redundant Storage (LRS) |

4. Clicked **"Review + Create"** → Validation passed → **"Create"**
5. Deployment completed successfully

### Shared Responsibility Model

For a Storage Account (PaaS), responsibilities are divided as follows:

| Responsibility | Microsoft | Customer |
|---------------|-----------|----------|
| Physical datacenters | ✅ | |
| Network infrastructure | ✅ | |
| Host operating system | ✅ | |
| Data stored in storage | | ✅ |
| Access control & IAM | | ✅ |
| Encryption key management | | ✅ |
| Firewall & network rules | | ✅ |

> Microsoft secures the underlying infrastructure. The **customer is responsible** for data protection, access management, and security configurations.

> 📸 Screenshot 7: Storage Account (ajagustorage) Overview page  
> 📸 Screenshot 8: Deployment complete screen

---

## 8. Billing & Cost Management

### Steps Taken
1. Searched **"Cost Management + Billing"** in the top search bar
2. Reviewed the **Overview** page:
   - Amount Due: **$0.00**
   - Free credit active
3. Navigated to **Cost Management → Budgets**
4. Created a new budget:

| Field | Value |
|-------|-------|
| **Budget Name** | MyFirstBudget |
| **Amount** | $5/month |
| **Reset Period** | Monthly |
| **Expiration** | May 31, 2028 |
| **Alert Threshold** | 80% ($4.00) |
| **Alert Email** | Lawmekz1@gmail.com |

5. Budget successfully created and active

> 📸 Screenshot 9: Cost Management – Budgets page showing MyFirstBudget

---

## 9. Free Tier Limits & Summary

### Azure Free Account Includes

| Service | Free Tier Limit |
|---------|----------------|
| **Free Credit** | $200 for 30 days |
| **Virtual Machines** | 750 hrs/month – B1s (Windows & Linux) for 12 months |
| **Blob Storage** | 5 GB locally redundant storage for 12 months |
| **SQL Database** | 250 GB – S0 instance for 12 months |
| **Cosmos DB** | 1,000 RU/s + 25 GB for 12 months |
| **Bandwidth** | 15 GB outbound data transfer/month |
| **Azure Functions** | 1 million requests/month (always free) |
| **App Service** | 10 web/mobile/API apps (always free) |
| **Azure DevOps** | 5 users + unlimited private repos (always free) |
| **Key Vault** | 10,000 transactions/month (always free) |

> ⚠️ Free credit expires in **30 days**. Monitor usage regularly via Cost Management.

---

## 10. Security Considerations

### Steps Taken to Secure the Account

#### Multi-Factor Authentication (MFA)
- MFA is enabled by default for Global Administrator accounts in Microsoft Entra ID
- To verify: **Entra ID → Users → [User] → Authentication methods**

#### Password Policy
- Azure enforces strong passwords for all accounts
- Recommended: Use a passphrase of 16+ characters

#### Principle of Least Privilege
- Only assign roles with the minimum permissions needed
- Avoid using Global Administrator for daily tasks — create a separate user with Contributor role instead

#### Security Recommendations
| Action | Status |
|--------|--------|
| MFA enabled | ✅ (Default for Global Admin) |
| Strong password set | ✅ |
| Budget alert configured | ✅ |
| Resource group scoped access | ✅ |
| LRS redundancy on storage | ✅ |

#### Microsoft Defender for Cloud
- Navigate to **"Microsoft Defender for Cloud"** in the portal
- Provides security score, recommendations, and threat protection
- Free tier available for basic security posture assessment

---

## 11. Completion Checklist

| Task | Description | Status |
|------|-------------|--------|
| ✅ Account Registration | Azure free account created with email, phone & payment verification | Done |
| ✅ Portal Exploration | Navigated dashboard, services, search, notifications, settings | Done |
| ✅ Dashboard Customization | Added custom tiles and saved dashboard layout | Done |
| ✅ Governance Setup | Created MyFirstResourceGroup in West Europe | Done |
| ✅ Identity Awareness | Reviewed Entra ID users and confirmed Global Admin role | Done |
| ✅ RBAC Review | Explored Access Control (IAM) on resource group | Done |
| ✅ Region Selection | Identified South Africa North as optimal region for Nigeria | Done |
| ✅ Resource Deployment | Deployed ajagustorage Storage Account successfully | Done |
| ✅ Cost Monitoring | Created MyFirstBudget with $5 limit and 80% alert | Done |
| ✅ Security Review | Confirmed MFA, reviewed Defender for Cloud | Done |

---

## 12. Troubleshooting

| Issue | Solution |
|-------|----------|
| Storage account name already taken | Names must be globally unique — add numbers (e.g., `ajagustorage2026`) |
| Region not available | Choose an alternative region (West Europe is widely available) |
| Budget alert not received | Check spam folder; verify email in alert settings |
| Can't find a service | Use the top search bar — type the service name |
| Deployment failed | Check the error message under "Notifications" (bell icon) |
| Free credit expired | Upgrade to Pay-As-You-Go or delete unused resources |
| Access denied to a resource | Check your role under Access Control (IAM) |

---

### Support Resources
- 📘 [Azure Documentation](https://docs.microsoft.com/azure)
- 🎓 [Microsoft Learn – Azure Fundamentals](https://learn.microsoft.com/en-us/training/paths/azure-fundamentals/)
- 💬 [Azure Community Support](https://techcommunity.microsoft.com/t5/azure/ct-p/Azure)
- 🆘 [Azure Support Portal](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade)

---

*Documentation prepared by Ajagu Nnaemeka Lawrence | Azure Onboarding Lab | June 2026*
