# Hybrid Identity Lab

## Overview

This project demonstrates the implementation of a hybrid identity environment using Active Directory, Microsoft Entra ID and Azure Role-Based Access Control (RBAC).

The objective was to simulate a common enterprise identity architecture where user identities are managed on-premises, synchronized to the cloud and used to access Azure resources through centralized identity and access management controls.

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
    │
    ▼
Azure Resources
```

## Project Components

### Active Directory

Implemented an on-premises Active Directory environment to provide centralized identity management.

Key activities:

* Deployed Active Directory Domain Services (AD DS)
* Configured DNS
* Created Organizational Units (OUs)
* Created users and security groups
* Joined CLIENT01 to the domain
* Configured Group Policy Objects (GPOs)

➡️ [View Active Directory Lab](./active-directory/README.md)

---

### Microsoft Entra Connect

Implemented hybrid identity synchronization between Active Directory and Microsoft Entra ID.

Key activities:

* Installed Microsoft Entra Connect
* Configured Password Hash Synchronization
* Connected Active Directory to Microsoft Entra ID
* Synchronized user identities
* Validated successful synchronization

➡️ [View Entra Connect Synchronization Lab](./entra-connect-sync/README.md)

---

### Azure RBAC

Configured Azure Role-Based Access Control to demonstrate authorization and access management within Azure.

Key activities:

* Created Azure user accounts
* Assigned Azure RBAC roles
* Validated role assignments
* Demonstrated authentication versus authorization concepts

➡️ [View Azure RBAC Lab](./azure-rbac/README.md)

---

## Key Concepts Demonstrated

### Authentication

User identities were managed through Active Directory and synchronized to Microsoft Entra ID.

### Authorization

Azure RBAC was used to control access to Azure resources through role assignments.

### Hybrid Identity

Microsoft Entra Connect synchronized identities between Active Directory and Microsoft Entra ID.

### Source of Authority

Active Directory remained the authoritative identity source while Microsoft Entra ID consumed synchronized identities.

## Skills Demonstrated

* Active Directory Administration
* Microsoft Entra ID Administration
* Microsoft Entra Connect Configuration
* Azure RBAC Administration
* Group Policy Management
* DNS Administration
* Hybrid Identity Architecture
* Identity Synchronization
* Windows Server Administration
* Identity and Access Management (IAM)

## Outcome

Successfully implemented a hybrid identity environment integrating Active Directory, Microsoft Entra ID and Azure RBAC. The project demonstrates core enterprise IAM concepts including authentication, authorization and identity synchronization.
