# Azure Identity Lifecycle Automation

## Overview

A cloud-focused identity lifecycle automation project designed to automate Joiner, Mover, and Leaver (JML) processes using PowerShell.

The project begins with processing structured employee data locally and will progressively integrate Microsoft Entra ID, Microsoft Graph, Azure Automation, managed identities, and Infrastructure as Code.

The goal is to demonstrate how identity lifecycle processes can be automated securely while applying role-based access and maintaining an auditable record of changes.

---

## Architecture

> Architecture diagram will be added as the cloud components are implemented.

---

## Project Phases

### Phase 1 - PowerShell Automation
- Import employee data from CSV
- Process employee records as PowerShell objects
- Implement Joiner, Mover, and Leaver logic
- Create role-based access mappings
- Validate input data
- Add error handling
- Implement logging
- Generate audit reports

### Phase 2 - Microsoft Entra ID Integration
- Connect PowerShell to Microsoft Graph
- Create and manage Entra ID users
- Manage group memberships
- Apply role-based access
- Automate onboarding and offboarding actions

### Phase 3 - Azure Automation
- Deploy the PowerShell workflow to Azure Automation
- Configure a managed identity
- Authenticate to Microsoft Graph without stored credentials
- Run identity lifecycle processes from Azure

### Phase 4 - Infrastructure as Code
- Define supporting Azure resources using Terraform or Bicep
- Deploy and manage infrastructure through code

---

## Technologies

### Currently Used
- PowerShell
- CSV

### Planned
- Microsoft Azure
- Microsoft Entra ID
- Microsoft Graph
- Azure Automation
- Managed Identities
- Terraform or Bicep

---

## Project Structure

```text
azure-identity-lifecycle-automation/
├── config/
├── data/
│   └── users.csv
├── logs/
├── reports/
├── src/
│   └── Invoke-IdentityAutomation.ps1
└── README.md
