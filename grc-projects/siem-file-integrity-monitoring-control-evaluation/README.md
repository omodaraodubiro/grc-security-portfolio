# SIEM-Based File Integrity Monitoring (FIM) Control Evaluation

*(Wazuh Implementation & Governance Assessment)*

## 1. Executive Overview

This project evaluates the effectiveness of a File Integrity Monitoring (FIM) detective control using Wazuh SIEM in a simulated financial environment.

The objective was to:

* Assess risk related to unauthorized modification of financial documents
* Validate the effectiveness of monitoring controls
* Evaluate governance reporting capability
* Demonstrate audit evidence generation
* Align technical detection with compliance expectations

This project bridges technical monitoring with governance oversight.

## 2. Risk Context

### Identified Risk

Unauthorized modification of sensitive financial documents.

### Potential Business Impacts

**Financial Impact**

* Loss of financial reporting integrity
* Budget discrepancies
* Direct financial loss

**Operational Impact**

* Decision-making disruption
* Audit inconsistencies
* Compliance violations

**Reputational Impact**

* Stakeholder trust erosion
* Regulatory scrutiny

## 3. Control Architecture

### Primary Control

Detective Control: File Integrity Monitoring (FIM) via Wazuh SIEM

The control monitors:

* File creation
* File modification
* File deletion

Each event is logged with:

* Timestamp
* File path
* User activity
* System agent status

This allows measurable monitoring of sensitive file activity.

## 4. Control Effectiveness Evaluation

Control performance was evaluated using:

* Total file change alerts
* Alert frequency & timing analysis
* Agent health and reporting continuity
* Centralized event visibility

The SIEM dashboard enabled trend analysis and identification of abnormal access patterns, supporting risk quantification.

## 5. Preventive, Detective & Corrective Alignment

### Preventive Controls

* Access Control Lists (ACLs)
* Role-Based Access Restrictions
* Active Directory Group Policies

These reduce likelihood of unauthorized modification.

### Detective Controls

* Wazuh FIM alert generation
* Real-time event monitoring

### Corrective Controls

Triggered when unauthorized activity is detected:

* Restore files from backup
* Revoke user access
* Initiate incident investigation
* Document control exception

This demonstrates full control lifecycle integration.

## 6. Governance & Audit Readiness

The centralized SIEM logs provide:

* Tamper-evident monitoring records
* Change history tracking
* Checksum validation evidence
* Time-bound reporting capability

This supports compliance evidence for regulatory frameworks such as:

* SOX (Change Control)
* PCI DSS (File integrity monitoring requirements)
* HIPAA (Data integrity safeguards)

Example audit scenario:

To demonstrate that a sensitive file was not modified during a given quarter, SIEM logs were filtered by file path and time range. Absence of modification alerts, combined with checksum verification, provided audit-ready proof of integrity.

## 7. Key Takeaways

* Technical monitoring must be tied to governance reporting
* Detective controls require preventive & corrective support
* Centralized log management strengthens compliance posture
* SIEM metrics enable risk quantification and trend analysis
* Audit readiness depends on structured evidence retention


# What This Project Demonstrates

* Understanding of control lifecycle (preventive, detective, corrective)
* Ability to translate technical alerts into risk language
* Governance-focused evaluation of monitoring effectiveness
* Practical SOC exposure aligned to compliance frameworks
