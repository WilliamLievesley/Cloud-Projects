# Entra Connect Synchronization Lab

## Overview

This phase extends the Active Directory environment by integrating on-premises identities with Microsoft Entra ID using Microsoft Entra Connect synchronization.

## Objectives

* Configure Microsoft Entra Connect
* Synchronize on-premises Active Directory identities with Microsoft Entra ID
* Validate hybrid identity synchronization
* Demonstrate centralized identity lifecycle management

## Architecture Overview

```text
On-Premises Active Directory
            │
            ▼
Microsoft Entra Connect
            │
            ▼
Microsoft Entra ID
```

## Implementation

Microsoft Entra Connect was installed on the domain controller and configured to synchronize user identities between the on-premises Active Directory environment (`corp.local`) and Microsoft Entra ID.

During configuration, Microsoft Entra Connect identified that `corp.local` was a non-routable domain and generated a User Principal Name (UPN) warning. This highlighted a common hybrid identity consideration when integrating legacy Active Directory environments with cloud identity platforms.

Synchronization was configured using Password Hash Synchronization and enabled upon completion of the configuration process.

![Ready To Configure](../screenshots/ready-to-configure.png)

## Validation

Synchronization completed successfully and Active Directory identities were synchronized into Microsoft Entra ID.

Validation was performed by reviewing synchronized user accounts within Microsoft Entra ID and confirming that synchronized identities were marked with the **On-premises Sync** attribute.

![Synchronized Users](../screenshots/synced-users-entra.png)

Four Active Directory user accounts were successfully synchronized from the on-premises environment into Microsoft Entra ID.

## Key Concepts Demonstrated

### Hybrid Identity

Microsoft Entra Connect enables organizations to maintain identities within Active Directory while synchronizing them to Microsoft Entra ID, providing a unified identity across both environments.

### Source of Authority

Active Directory remained the authoritative identity source. User attributes and account changes performed on-premises would synchronize to Microsoft Entra ID through Microsoft Entra Connect.

### Identity Synchronization

Microsoft Entra Connect synchronizes users, groups and selected identity attributes while maintaining consistency across on-premises and cloud environments.


## Skills Demonstrated

* Microsoft Entra ID Administration
* Microsoft Entra Connect Configuration
* Hybrid Identity Architecture
* Active Directory Integration
* Identity Synchronization
* Troubleshooting Authentication and Synchronization Issues

## Outcome

Successfully implemented a hybrid identity environment by synchronizing on-premises Active Directory identities with Microsoft Entra ID using Microsoft Entra Connect. The implementation demonstrated how organizations can maintain Active Directory as the source of authority while extending identities to cloud services through centralized synchronization.
