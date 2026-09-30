# GRC Compliance & Audit Portfolio

> **Hands-on GRC / internal audit simulation using Eramba, access-control testing, evidence validation, and remediation tracking.**

## Executive Summary

This project demonstrates an analyst-level GRC workflow from **risk identification through control testing and remediation**.

I built the exercise around a simulated financial-systems access review and used **Eramba** to document the control and audit workflow. The project combines manual evidence review with spreadsheet-based access reconciliation and framework mapping.

**Core workflow:**

**Risk → Control → Evidence → Test → Finding → Remediation → Retest → Evidence**

The environment is intentionally simulated for portfolio purposes; no real production systems, accounts, or confidential evidence were used.

---

## What I Demonstrated

- GRC control and framework mapping
- User access reviews
- Privileged-access review
- Segregation of Duties (SoD) analysis
- Evidence collection and validation
- Control testing
- Exception identification
- Audit documentation
- Risk and remediation tracking
- Eramba GRC workflow
- Audit readiness and evidence management

---

## Scenario

### Systems in Scope

- SAP production environment
- Corporate banking / accounting applications

### Risk

The review focuses on users receiving elevated permissions, such as `SAP_ALL`, that are not supported by their approved job responsibilities.

Excessive or unauthorized access can increase the risk of:

- Unauthorized financial transactions
- Inappropriate system changes
- Privilege misuse
- Segregation-of-Duties conflicts
- Inadequate accountability over sensitive financial systems

### Objective

Determine whether active user access is:

1. Appropriate for the user's role
2. Approved by the appropriate business owner
3. Supported by evidence
4. Consistent with the authorized access matrix
5. Properly documented when exceptions exist

---

## Framework Mapping

The scenario was mapped to:

- **CIS Controls v8**
- **ISO/IEC 27002:2022**

Relevant CIS Controls include:

| Framework | Control | Relevance |
|---|---|---|
| CIS Controls v8 | **6.8 – Define and Maintain Role-Based Access Control** | Supports appropriate access based on job responsibilities |
| CIS Controls v8 | **6.2 – Establish an Access Revocation Process** | Supports removal of access when it is no longer required |

The mapping demonstrates how a business risk can be connected to a defined security-control requirement.

---

## Internal Control

### IC-343 — Banking & Accounting Software Account Reviews

**Control objective:** Verify that user access to financial applications is appropriate, approved, and periodically reviewed.

### Evidence Reviewed

- Authorized user access matrix
- Active system-user information
- SAP screenshots, including `RSUSR002`
- Approved access/change requests
- Supporting access documentation

### Test Procedure

1. Obtain the population of active accounts.
2. Compare active accounts against the authorized access matrix.
3. Identify excessive, inactive, or unapproved access.
4. Review supporting provisioning/change requests.
5. Verify approval and business justification.
6. Document exceptions.
7. Determine whether remediation or additional evidence is required.
8. Record the audit activity and supporting evidence in Eramba.

### Expected Result

Each active account should have:

- An appropriate role
- A defined business owner
- Appropriate approval
- Supporting evidence where required

---

## Audit Execution in Eramba

The Eramba control record was used to work through the audit workflow, including the control's evidence requirements and audit status.

The exercise included:

1. Reviewing the control requirements
2. Reviewing required evidence
3. Performing access reconciliation
4. Documenting the audit activity
5. Recording the test result and audit dates
6. Attaching supporting evidence
7. Tracking exceptions for follow-up

![Eramba framework filter](Screenshot%20from%202026-06-09%2012-38-49.png)

![Eramba audit workflow](Screenshot%20from%202026-06-09%2012-41-19.png)

![Eramba control evidence](Screenshot%20from%202026-06-09%2012-43-26.png)

![Access review](Screenshot%20from%202026-06-09%2012-48-26.png)

![Audit documentation](Screenshot%20from%202026-06-09%2012-52-51.png)

![Eramba results](Screenshot%20from%202026-06-09%2013-03-13.png)

---

## Sample Finding & Remediation Workflow

The following is a **simulated finding example** showing how an exception would be documented. It is not presented as a real production finding.

### Finding ID

**GRC-001 — Privileged Access Not Supported by Approved Access Matrix**

| Field | Example |
|---|---|
| Control | IC-343 – Banking & Accounting Software Account Reviews |
| Exception | Active privileged access does not match the approved access matrix |
| Evidence | Active-account extract, access matrix, and approval/change documentation |
| Risk | Excessive privileges could permit unauthorized transactions or inappropriate changes |
| Severity | Determined using the organization's approved risk-rating methodology |
| Root Cause | To be established through management/process-owner investigation |
| Recommendation | Validate business need, remove unnecessary privileges, or obtain and document appropriate approval |
| Owner | System / application owner |
| Due Date | Assigned according to remediation requirements |
| Status | Open pending remediation and validation |
| Retest | Required after corrective action |

### Remediation Lifecycle

**Identify → Assign → Correct → Document → Retest → Close**

This demonstrates that a GRC analyst does more than identify an exception: the issue should remain traceable through corrective action and validation.

---

## Access Review Artifact

The accompanying spreadsheet demonstrates the reconciliation component of the exercise:

**[Banking and Accounting Software Account Review Checklist.xlsx](Banking%20and%20Accounting%20Software%20Account%20Review%20Checklist.xlsx)**

The spreadsheet supports the comparison between active access and approved access and provides a structured place to document review results.

---

## Analyst Workflow

This project reflects the way I approach a GRC task:

> **Assess → Verify → Remediate → Document**

### Assess
Understand the business process, risk, system, and control objective.

### Verify
Collect evidence and test whether the control is operating as intended.

### Remediate
Identify exceptions, determine the appropriate corrective action, and track ownership.

### Document
Maintain an auditable record of the test, evidence, finding, remediation, and retest.

---

## Tools & Concepts

**GRC:** Eramba  
**Access Management:** RBAC, privileged access, access reviews, SoD  
**Audit:** Control testing, evidence validation, exception tracking  
**Frameworks:** CIS Controls v8, ISO/IEC 27002:2022  
**Documentation:** Audit records, evidence, findings, remediation tracking  
**Analysis:** Spreadsheet-based access reconciliation

---

## Why This Project Matters

The goal of this portfolio is not to demonstrate that I can simply navigate a GRC platform.

It demonstrates that I understand the relationship between:

**Business Risk → Control Objective → Evidence → Testing → Exception → Remediation → Validation**

Eramba is the platform used to document the workflow; the underlying skill is understanding **why the control exists, what evidence proves it is working, how exceptions are evaluated, and how remediation is tracked to closure**.

---

## Portfolio Disclaimer

All systems, accounts, screenshots, evidence, findings, and audit results in this project are **simulated for learning and portfolio purposes**.

This project does not represent access to, testing of, or audit work performed against a real production environment.

---

## Interview Summary

If asked to explain this project:

> “I built a simulated GRC audit using Eramba around financial-system access reviews. I defined the control objective, mapped the risk to CIS and ISO requirements, reviewed simulated evidence, reconciled user access against an approved matrix, documented the audit workflow in Eramba, and built out the finding and remediation lifecycle. It was a portfolio environment rather than a production client environment, but it gave me hands-on experience with the way a GRC analyst connects risk, controls, evidence, testing, and remediation.”

