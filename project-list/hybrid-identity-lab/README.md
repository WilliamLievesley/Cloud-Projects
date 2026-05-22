# Hybrid Identity Lab

Enterprise-style hybrid identity environment integrating Active Directory and Microsoft Entra ID.

## Technologies
- Microsoft Entra ID
- Active Directory
- Entra Connect
- MFA
- Conditional Access
- RBAC
- Windows Server
- Azure

## Objectives
- Configure hybrid identity between Active Directory and Microsoft Entra ID
- Implement MFA and Conditional Access policies
- Configure RBAC and administrative role separation
- Simulate enterprise onboarding and identity governance workflows



## Resource Groups

![Resource Groups](screenshots/Resource-groups.png)

Branch-based Azure Resource Groups used to simulate infrastructure segmentation and RBAC scope boundaries.

---

## Security Groups

![Security Groups](screenshots/Security-groups.png)

Microsoft Entra security groups used to implement branch-based and administrative access control.

---

## RBAC Assignment

![RBAC Assignment](screenshots/Branch-role-assignment.png)

Configured Azure RBAC assignments using group-based inheritance and least-privilege principles.

---

## Storage Resources

![Storage Accounts](screenshots/Storage-accounts.png)

Deployed Azure Storage Accounts inside branch resource groups to demonstrate RBAC inheritance and scoped resource access.
