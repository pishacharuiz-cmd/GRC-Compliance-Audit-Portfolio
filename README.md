# Enterprise GRC Audit Workflow & Framework Mapping Portfolio

## 📌 Project Overview
This project serves as a practical, hands-on demonstration of Governance, Risk, and Compliance (GRC) analyst workflows using the industry-standard **Eramba GRC Platform**. 

The core objective of this project is to simulate a real-world internal audit lifecycle: translating high-level regulatory compliance requirements down into specific, testable internal controls, executing user entitlement reviews, and maintaining an audit-ready posture for enterprise-scale software environments.

### 🔍 Key Competencies Demonstrated:
* **Compliance Framework Mapping:** Navigating and filtering compliance criteria libraries (CIS Controls v8 and ISO 27001:2022).
* **Internal Control Operationalization:** Utilizing Eramba to manage Control ID `IC-343` (Banking & Accounting Software Account Reviews) targeting Segregation of Duties (SoD) risks.
* **Audit Lifecycle Management:** Diagnosing expired controls, establishing continuous evidence collection workflows, and generating executive audit trails.
* **Evidence Validation:** Developing technical checking templates to audit system logs, access matrices, and change requests.

---

## 🎯 1. Scenario & Risk Analysis
* **System in Scope:** Enterprise ERP (SAP Production Database) and Corporate Banking Portals.
* **The Risk Profile:** High-risk profiles (specifically global administrative permissions like `SAP_ALL`) being inappropriately assigned or left active on standard business user accounts. This creates severe **Segregation of Duties (SoD)** violations and opens the organization up to financial fraud or unauthorized data modification.

---

## 🛡️ 2. Regulatory Alignment & Framework Filtering
To address this risk, the first objective was to map it back to recognized global security frameworks within Eramba to ensure regulatory alignment. 
* **Framework Library Used:** CIS Controls v8 / ISO 27002:2022.
* **Target Security Controls:**
  * **CIS Item 6.8:** Define and Maintain Role-Based Access Control (RBAC).
  * **CIS Item 6.2:** Establish an Access Revocation Process.

*Analyst Note: By filtering the framework library for "Access," we successfully isolated the exact compliance mandates required to justify our internal security workflows.*

---

## ⚙️ 3. Internal Control Definition (Control ID: IC-343)
Moving from the passive rulebook to active operations, I managed **Control ID IC-343: Banking & Accounting Software Account Reviews**. 

Per the system definition, the exact repeatable internal audit procedure consists of:

### 📥 A. Evidence Gathering
* Extract the authorized system **Access Matrix**.
* Gather active **System User Logs/Screenshots** directly from the target environments (e.g., SAP transaction code `RSUSR002`).
* Pull all approved **Change Requests** and provisioning tickets generated since the last audit cycle.

### 🔍 B. Technical Analysis
* Cross-reference every active system account against the master Access Matrix to detect "ghost accounts" or unapproved privilege escalations.
* Validate that all modifications to permissions correlate directly to an authorized, approved Change Request ticket following the corporate change management policy.

### 📤 C. Required Outputs
* System evidence screenshots.
* Completed reconciliation spreadsheets verifying each active account and change request history.

---

## 🔍 4. Audit Execution & Remediation Workflow
During verification of the Eramba dashboard, the status badge for **IC-343** displayed a critical warning: **`Last Audit Expired`** and **`Missing Evidence`**. This indicates that while the safeguard is defined, active validation has lapsed.

### 🛠️ Remediation Steps Taken:
1. **Executed the Test:** Simulated the reconciliation process utilizing a custom validation spreadsheet tracking user roles against the authorized matrix.
2. **Logged the Audit Trail:** Navigated to the Eramba Audits log sub-menu, generated a fresh audit record, established valid testing dates, and set the final status to **Passed**.
3. **Attached Evidence:** Linked the completed audit spreadsheets to the record to permanently resolve the system's "Missing Evidence" requirement, automatically returning the global control health status to green/compliant.
