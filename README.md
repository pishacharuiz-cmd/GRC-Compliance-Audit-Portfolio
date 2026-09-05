# GRC Compliance & Audit Portfolio

## Project Overview

This project demonstrates hands-on GRC and internal audit work using the **Eramba GRC Platform**. The focus is on taking a security risk, mapping it to applicable controls, collecting evidence, testing the control, and documenting the result.

The project is designed to reflect the type of work a GRC analyst may support during access reviews, internal audits, and compliance activities.

### Skills Demonstrated
- Control and framework mapping
- Access review and Segregation of Duties (SoD) analysis
- Audit evidence collection and validation
- Control testing and documentation
- GRC platform workflows using Eramba
- Basic risk and remediation tracking
- Audit readiness and evidence management

---

## 1. Scenario & Risk

**Systems in scope:** SAP production environment and corporate banking applications.

The scenario focuses on users who have elevated permissions, such as `SAP_ALL`, when those permissions are not appropriate for their job responsibilities.

This can create access-control and SoD risks, including unauthorized transactions, inappropriate changes, or excessive access to financial systems.

As part of the review, the goal is to identify exceptions, validate whether access is approved, and document any issues that require remediation.

---

## 2. Framework & Control Mapping

The risk was mapped to applicable access-control requirements using:

- **CIS Controls v8**
- **ISO/IEC 27002:2022**

Relevant controls reviewed included:

- **CIS 6.8:** Define and Maintain Role-Based Access Control (RBAC)
- **CIS 6.2:** Establish an Access Revocation Process

The mapping provides a basis for connecting the business risk to specific security-control requirements.

---

## 3. Internal Control: IC-343

**Control:** Banking & Accounting Software Account Reviews

The control is intended to verify that user access to financial applications is appropriate, approved, and periodically reviewed.

### Evidence Reviewed

- Authorized user access matrix
- Active system user information
- Screenshots from the SAP environment, including `RSUSR002`
- Approved access or change requests

### Testing Approach

1. Compare active accounts against the authorized access matrix.
2. Identify users with excessive, inactive, or unapproved access.
3. Review supporting change or provisioning requests.
4. Confirm that access changes were approved and documented.
5. Record exceptions and determine whether follow-up is needed.

### Expected Result

Each active account should have an appropriate role, an identified business owner, and supporting approval where required.

---

## 4. Audit Execution

During the exercise, the Eramba control record showed **Last Audit Expired** and **Missing Evidence**.

I worked through the audit workflow by:

1. Reviewing the control and its evidence requirements.
2. Performing the access reconciliation using the supporting spreadsheet.
3. Documenting the audit activity in Eramba.
4. Recording the test result and audit dates.
5. Attaching the supporting evidence to the audit record.

This demonstrates the basic workflow from control review through evidence validation and audit documentation.

![Eramba Framework Filter](screenshots/01_compliance_framework_filter.png)

---

## 5. Finding & Remediation Example

A potential finding from this type of review would be an active privileged account that does not match the approved access matrix or lacks supporting approval.

A typical remediation record would capture:

- Finding description
- Affected system/account
- Risk or control impact
- Assigned owner
- Recommended corrective action
- Target completion date
- Remediation status
- Retest result

The purpose is to make the issue traceable from identification through corrective action and validation.

---

## 6. Portfolio Artifacts

- Eramba GRC screenshots
- Access review checklist
- Audit evidence examples
- Control and framework mapping
- Access reconciliation workflow

> **Note:** The systems, accounts, evidence, and audit results in this portfolio are simulated for learning and portfolio purposes. They do not represent access to or testing of a real production environment.

---

## What This Project Shows

This project demonstrates how I approach a GRC task at the analyst level: understand the risk, identify the relevant control, gather and validate evidence, perform the review, document the result, and follow up on exceptions.
