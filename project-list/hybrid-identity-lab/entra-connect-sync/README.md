# Entra Connect Synchronization Lab

## Overview

This phase extends the Active Directory environment by integrating on-premises identities with Microsoft Entra ID using Microsoft Entra Connect synchronization.

## Objectives

- Configure Microsoft Entra Connect
- Synchronize on-prem Active Directory identities with Microsoft Entra ID
- Validate hybrid identity synchronization
- Demonstrate centralized identity lifecycle management

## Architecture Overview

```text
On-Premises Active Directory
        │
        │ Entra Connect Sync
        ▼
Microsoft Entra ID
```
## Environment

* DC01 (Active Directory Domain Controller)
* Microsoft Entra Connect
* Microsoft Entra ID

## Implementation

Microsoft Entra Connect was installed and configured to synchronize identities between the on-premises `corp.local` Active Directory environment and Microsoft Entra ID.

During configuration, a warning was presented because `corp.local` is a non-routable domain. Synchronization was configured using Password Hash Synchronization and completed successfully.

![Ready To Configure](images/ready-to-configure.png)

## Validation

Synchronization was validated by reviewing user accounts within Microsoft Entra ID. Synchronized users were identified using the **On-premises Sync** attribute.

![Synced Users](images/synced-users-entra.png)

## Key Takeaways

* Active Directory remained the source of authority.
* Microsoft Entra Connect synchronized identities between on-premises and cloud environments.
* Hybrid identity provides a single identity lifecycle across Active Directory and Microsoft Entra ID.
* Azure RBAC permissions remain managed separately from identity synchronization.
