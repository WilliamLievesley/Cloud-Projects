# Hybrid Identity Lab

## Overview

This project demonstrates core Identity and Access Management (IAM) concepts across Azure and on-premises environments.

The project began with Azure Role-Based Access Control (RBAC) to explore authorization, role assignments and resource access management. A Windows Server 2022 virtual machine was then deployed and configured as a Domain Controller to provide centralized identity management through Active Directory Domain Services (AD DS). Finally, Microsoft Entra Connect was implemented to synchronize on-premises identities with Microsoft Entra ID, creating a hybrid identity environment.

The completed lab demonstrates authentication, authorization and hybrid identity synchronization within a Microsoft enterprise ecosystem.

---

## Architecture Overview

```text
CLIENT01
    │
    ▼
Active Directory (DC01)
    │
    ▼
Microsoft Entra Connect
    │
    ▼
Microsoft Entra ID
```

---

## Project Progression

### Phase 1: Azure RBAC

Azure Role-Based Access Control (RBAC) was implemented to explore authorization and access management within Azure.

Key activities:

* Created Microsoft Entra security groups
* Assigned Azure RBAC roles
* Configured branch-based access governance
* Implemented group-based access control
* Explored role inheritance and scope boundaries
* Applied least-privilege access control principles

➡️ [View Azure RBAC Lab](./azure-rbac/README.md)

---

### Phase 2: Active Directory

A Windows Server 2022 virtual machine was deployed and configured as a Domain Controller to provide centralized identity management.

Key activities:

* Installed Active Directory Domain Services (AD DS)
* Configured DNS
* Created the `corp.local` domain
* Created Organizational Units (OUs)
* Created users and security groups
* Managed group memberships
* Joined CLIENT01 to the domain
* Configured Group Policy Objects (GPOs)

➡️ [View Active Directory Lab](./active-directory/README.md)

---

### Phase 3: Microsoft Entra Connect

Microsoft Entra Connect was deployed to synchronize on-premises identities with Microsoft Entra ID.

Key activities:

* Installed Microsoft Entra Connect
* Configured Password Hash Synchronization
* Connected Active Directory to Microsoft Entra ID
* Synchronized user identities
* Validated successful synchronization
* Confirmed synchronized identities using the **On-premises Sync** attribute

➡️ [View Entra Connect Synchronization Lab](./entra-connect-sync/README.md)

---

## Key Concepts Demonstrated

### Authentication

Active Directory was used to centrally manage and authenticate user identities within the domain environment.

### Authorization

Azure RBAC was used to control access to Azure resources through role assignments and scope inheritance.

### Hybrid Identity

Microsoft Entra Connect synchronized identities between Active Directory and Microsoft Entra ID, extending on-premises identities into the cloud.

### Source of Authority

Active Directory remained the authoritative identity source, while Microsoft Entra ID consumed synchronized identities through Microsoft Entra Connect.

---

## Skills Demonstrated

* Azure Role-Based Access Control (RBAC)
* Microsoft Entra ID Administration
* Microsoft Entra Connect Configuration
* Active Directory Administration
* Group Policy Management
* DNS Administration
* Windows Server Administration
* Identity Synchronization
* Hybrid Identity Architecture
* Identity and Access Management (IAM)
* Security Group Administration
* Troubleshooting Authentication and Synchronization Issues

---

## Outcome

Successfully implemented a hybrid identity environment integrating Azure RBAC, Active Directory and Microsoft Entra ID.

The project demonstrates how organizations can manage identities on-premises, synchronize them to the cloud and control access to resources through centralized identity and access management practices. Core IAM concepts including authentication, authorization, source of authority and hybrid identity synchronization were successfully implemented and validated throughout the project.
