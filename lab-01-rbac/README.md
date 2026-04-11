# Lab 01 – Role-Based Access Control (RBAC)

## Overview
Configured Azure RBAC by creating users and security groups using three 
different methods: Azure Portal, PowerShell, and Azure CLI. Assigned the 
Virtual Machine Contributor role to a group scoped to a resource group.

## What I Did
- Created user accounts (Joseph Price, Isabel Garcia, Dylan Williams) via 
  Portal, PowerShell, and Azure CLI respectively
- Created three security groups: Senior Admins, Junior Admins, Service Desk
- Assigned the **Virtual Machine Contributor** role to the Service Desk group 
  scoped to resource group AZ500Lab01
- Verified access assignments using the "Check Access" tab in IAM

## Tools & Services Used
- Microsoft Entra ID (Azure AD)
- Azure Portal
- Azure Cloud Shell (PowerShell + Bash/CLI)
- Azure RBAC / IAM

## Key Concepts Demonstrated
- Principle of least privilege — scoping roles to a resource group, not the 
  entire subscription
- Three ways to manage identity in Azure (Portal vs PowerShell vs CLI)
- Difference between role assignment scope levels (subscription vs resource group)

## Real-World Relevance
In production, you'd use Entra ID groups + RBAC to manage access at scale 
rather than assigning roles to individual users. Scoping to resource groups 
instead of subscriptions limits blast radius if credentials are compromised.

## Screenshots
See `/screenshots` folder.
