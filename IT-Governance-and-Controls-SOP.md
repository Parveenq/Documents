# IT Governance and Controls SOP

Standard operating procedure for conducting quarterly IT governance and access-control audits.

## Contents

- [Purpose](#purpose)
- [Introduction](#introduction)
- [Scope](#scope)
- [Definitions](#definitions)
- [Responsibilities](#responsibilities)
- [Procedure](#procedure)
  - [Audit frequency and sign-off](#audit-frequency-and-sign-off)
  - [G Suite](#g-suite)
  - [Employee exit](#employee-exit)
  - [Jarvis](#jarvis)
  - [Pennant](#pennant)
  - [AWS](#aws)
  - [DB roles](#db-roles)
  - [Jira](#jira)
  - [GitHub](#github)
  - [Qlik Sense](#qlik-sense)
  - [CLS releases](#cls-releases)
  - [Approvals on Jira](#approvals-on-jira)

---

## Purpose

This SOP walks through the process for conducting quarterly audits in the company.

## Introduction

The SOP covers a comprehensive review of the company's processes, tools, and access to critical systems, to ensure that IT policies and procedures are followed correctly. It also addresses key aspects of IT governance, access management, security, and compliance.

## Scope

This SOP provides a framework for auditing processes, tools, access, and compliance within the organisation. Its aim is to improve efficiency and security, and to keep day-to-day practice aligned with established policies and procedures.

## Definitions

| Term | Definition |
|------|------------|
| **AWS** | Amazon Web Services, a cloud computing services provider. |
| **CLS** | Core Lending System. CLS is a Jira project. |
| **DB release** | The process of deploying new changes to a database (DB). |
| **Jira** | A project and process management tool. |

## Responsibilities

The following teams and individuals are responsible for carrying out the quarterly audit:

| Role | Responsibility |
|------|----------------|
| **CoE** | Conducts the quarterly audit and prepares the audit report. |
| **People and Culture team** | Provides reviewers with the required documents and access to relevant information, and cooperates with the audit process. |
| **XYZ** | Oversees the quarterly audit and ensures that all audit procedures meet the required standards. |

## Procedure

The organisation runs internal audits of its processes and tools. Each section below describes the audit process, what is expected of the reviewer, and who is responsible for follow-up.

### Audit frequency and sign-off

| Audit frequency | Signed off by |
|-----------------|---------------|
| Quarterly | XYZ |
| Half-yearly | ABC |
| Annual | CxOs |

### G Suite

The reviewer cross-checks the G Suite user report against the exit employee report, which lists employees who left the company during the quarter. The People and Culture team shares the exit employee report.

When an employee leaves the company (India), the People and Culture team should deactivate their ID and revoke their G Suite access, and the change should appear in the records.

> **Action:** If the reviewer finds an exited employee's ID on the current G Suite user list, they must report it to the People and Culture team immediately. The issue must be fixed within 1–2 working days.

### Employee exit

The People and Culture team maintains lists of resigned and terminated users and new joiners, along with additional details. The employee exit report shows all employees who left the organisation during the quarter.

The reviewer compares this report with the G Suite user data.

> **Action:** If the two don't match, the reviewer follows up with the People and Culture team until the correction appears in the report.

### Jarvis

The reviewer cross-verifies active Jarvis users against two sources: Jarvis's quarterly user data report and Heimdall's quarterly user data report.

### Pennant

The reviewer cross-checks Pennant employee login IDs against exited user IDs:

1. Download the current Pennant user data from the system.
2. Get the Pennant exit user data from the People and Culture team.
3. Compare the two lists.

> **Action:** If an exited user still appears in the current Pennant records, the reviewer must report the discrepancy to the Pennant custodian (XYZ) for correction.

### AWS

AWS user approvals and access tickets are recorded in the Jira access management system. The reviewer compares these against each user's G Suite ID to confirm the user's identity and that their access was approved.

The audit covers the following AWS environments for both Jarvis and Pennant:

| Environment | Jarvis | Pennant | Jarvis and Pennant DB |
|-------------|:------:|:-------:|:---------------------:|
| Production | ✔ | ✔ | ✔ |
| UAT | ✔ | ✔ | ✔ |
| Development | ✔ | ✔ | ✔ |

### DB roles

Access to DB roles is restricted to a small number of employees. To make changes or raise a query on DB logs, an employee must raise a ticket, which their manager must approve.

The reviewer verifies these approval tickets and captures the following data:

- New user accounts, along with the roles assigned to each user
- Deleted users
- All generic user accounts
- Privileged and superuser roles

> **Action:** If the reviewer finds any unapproved access, they must report it to the admin.

### Jira

Jira user access is cross-checked by XYZ, who holds Jira admin rights.

### GitHub

When auditing GitHub, the reviewer inspects queries, logs, activities, and changes, along with the list of user login IDs.

### Qlik Sense

The reviewer cross-checks Qlik Sense users against the exit employee report.

### CLS releases

The reviewer examines Core Lending System releases for the quarter and submits proof of each release.

### Approvals on Jira

The reviewer checks user access approvals and captures the following evidence:

- Privileged access user accounts (admin and super admin), and any system user accounts (generic IDs) from DB and app servers to the in-scope applications
- A list of suspended, disabled, or deleted users for each tool
- Evidence of access revocation for each tool
- Evidence that employees' assigned roles fall within the scope of their business responsibilities
- Evidence of periodic user access rights reviews for users with access to Jarvis
- A system-generated list of application administrative activity logs for the audit period
- Evidence of periodic reviews of Jarvis's application administrative activity logs
