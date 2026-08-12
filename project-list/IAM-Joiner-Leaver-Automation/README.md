
# IAM Joiner/Leaver Automation v1 (in Progress) 

An Identity and Access Management (IAM) workflow built in n8n to automate parts of the employee Joiner and Leaver lifecycle.

The workflow validates employee information, determines access using role-based access rules, requests manager approval, routes approved requests through the appropriate Grant or Revoke path, and records the outcome in an audit log.

## Why I Built This

Identity lifecycle processes involve repetitive tasks that can become time-consuming and prone to inconsistent access decisions when handled manually.

I built this project to explore how Joiner and Leaver processes could be automated while maintaining important IAM controls such as role-based access, approval and auditability.

## Workflow

The current workflow follows this process:

1. Receive employee lifecycle information.
2. Validate the employee data.
3. Determine required access based on the employee's role.
4. Send the access request for manager approval.
5. Process the approval decision.
6. Route the request based on the lifecycle event:
   - **Joiner** → Grant Access
   - **Leaver** → Revoke Access
7. Record the result in an IAM audit log.

### Workflow Overview

![IAM Workflow](screenshots/IAM-automate-overview.png)

## IAM & Security Controls

The workflow was designed around several IAM principles:

- Joiner and Leaver lifecycle management
- Role-Based Access Control (RBAC)
- Manager approval before access changes
- Least-privilege access assignment
- Structured access provisioning and deprovisioning
- Audit logging and traceability

## Technologies

- n8n
- Identity & Access Management (IAM)
- Role-Based Access Control (RBAC)
- Workflow automation
- Approval workflows
- Audit logging

## Current Limitations

This project is currently a proof of concept.

The Grant Access and Revoke Access stages represent provisioning and deprovisioning actions within the workflow. They do not currently make changes to a production identity platform.

The employee and access information used within the workflow is test data created for the project.

## Planned Improvements

The next stage of the project is to integrate the workflow with Microsoft Entra ID using Microsoft Graph.

Planned improvements include:

- Microsoft Graph API integration
- Entra ID group assignment and removal
- Automated provisioning and deprovisioning
- Verification of access changes
- Improved error handling
- Failed-action logging and alerts
- Duplicate request handling
- Mover lifecycle support

## What I Learned

Building this project gave me practical experience translating an IAM lifecycle process into an automated workflow.

It required me to think about how employee information moves through an identity process, where approval controls should exist, how role-based access decisions can be standardised, and how actions can be recorded for auditing.

The project also gave me hands-on experience with n8n and provided a foundation for integrating workflow automation with identity platforms and APIs.
