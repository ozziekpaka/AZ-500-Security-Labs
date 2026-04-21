# Microsoft Sentinel Login Detection Lab

## Overview
This lab demonstrates how to use Microsoft Sentinel and Azure Entra ID sign-in logs to build and validate a basic login detection workflow.

## Oobjective
The goal of this lab was to:
- ingest sign-in logs into a Log Analytics workspace
- query authentication activity with KQL
- create a scheduled analytics rule in Microsoft Sentinel
- configure alert-to-incident generation in Microsoft Defender

## Tools Used
- Microsoft Sentinel
- Azure Entra ID
- Log Analytics Workspace
- Microsoft Defender Portal
- KQL (Kusto Query Language)

## Detection Logic

### Brute Force Detection Query
```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts = count() by IPAddress, UserPrincipalName
| where FailedAttempts >= 1
Test Query Used to Validate Alert Pipeline
SigninLogs
| take 1
What I Configured
Created a Log Analytics workspace for Sentinel
Connected Entra ID sign-in logs
Verified log ingestion using SigninLogs
Built a scheduled analytics rule named Brute Force
Configured the rule to create incidents in Microsoft Defender
Tested the detection pipeline with a simple query returning sign-in data
Validation Notes

Microsoft sign-in protections limited repeated failed login simulation during testing. Because of that, I validated the rule pipeline using existing sign-in data to confirm:

log ingestion was working
the analytics rule executed
incidents could be generated from alerts
Outcome

This lab helped me practice:

SIEM setup and configuration
KQL query writing
detection engineering basics
Microsoft Sentinel alert and incident workflow
Suggested Screenshots

Add screenshots to this folder later if you want:

sign-in logs query results
Sentinel analytics rule configuration
Defender incidents page
Key Takeaway

This project shows hands-on experience with building and validating a basic Microsoft Sentinel detection workflow using Entra ID sign-in telemetry.
