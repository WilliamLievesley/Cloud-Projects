
# Active Directory Deployment

Configured a Windows Server 2022 Domain Controller within Azure to simulate on-premises enterprise identity infrastructure and hybrid identity foundations.

---

# Objectives

- Deploy Windows Server infrastructure in Azure
- Install Active Directory Domain Services (AD DS)
- Promote a server to a Domain Controller
- Create an Active Directory forest and domain
- Begin organisational identity structure planning

---
# Windows Server Deployment

![Deployed VM](./screenshots/deployed-vm.png)

Deployed a Windows Server 2022 Datacenter: Azure Edition virtual machine within Azure to simulate on-premises enterprise identity infrastructure and hybrid identity foundations.

### VM Configuration

| Setting | Value |
|---|---|
| VM Name | DC01 |
| OS | Windows Server 2022 Datacenter: Azure Edition |
| Region | West Europe |
| VM Size | B2ts_v2 |
| Role | Domain Controller |
# Environment Overview

---

# Active Directory Installation

![AD Installation](./screenshots/ad-installation.png)

Installed the Active Directory Domain Services server role using Server Manager.

---

# Domain Controller Promotion

![Domain Controller Promotion](./screenshots/domain-controller-promotion.png)

Promoted the Windows Server VM to a Domain Controller and created a new Active Directory forest using the `corp.local` domain.

---

# Key Concepts Demonstrated

- Active Directory Domain Services
- Domain Controller deployment
- Enterprise identity infrastructure
- Windows Server administration
- Hybrid identity foundations
- Identity governance architecture

---

# Issues Encountered

- Azure VM connectivity and RDP configuration
- Azure region quota limitations
- Understanding Active Directory deployment stages
- DNS delegation warnings during domain promotion

---

# Future Improvements

- Organisational Unit (OU) structure
- Group Policy Objects (GPOs)
- Domain users and security groups
- Hybrid identity synchronisation
- Microsoft Entra Connect
- Intune integration
