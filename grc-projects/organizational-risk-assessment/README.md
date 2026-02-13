# Organizational Risk Assessment

## 1. Objective
To identify and evaluate key information security risks within a simulated fintech organization and propose ISO 27001-aligned controls to mitigate those risks.

## 2. Organization Overview
The organization is a mid-sized fintech company providing digital payment services to customers globally. The company processes sensitive customer data, financial transactions, and stores data in a cloud-based infrastructure.

## 3. Scope
This assessment focuses on:
- Customer data handling systems
- Employee endpoints
- Cloud infrastructure
- Email systems
- Administrative access controls

## 4. Asset Inventory

| Asset | Description | Business Impact if Compromised |
|--------|-------------|--------------------------------|
| Customer Database | Stores customer personal and financial data | Regulatory fines, loss of trust |
| Cloud Infrastructure | Hosts production systems | Service outage, financial loss |
| Employee Laptops | Used for daily operations | Data leakage risk |
| Email System | Internal and external communication | Phishing compromise |
| Admin Accounts | Privileged system access | Full system compromise |

## 5. Risk Identification

| Asset | Threat | Impact | Likelihood | Risk Level |
|--------|--------|--------|------------|------------|
| Customer Database | SQL Injection | Data breach | High | High |
| Email System | Phishing attack | Credential compromise | High | High |
| Employee Laptops | Malware infection | Data exfiltration | Medium | Medium |
| Cloud Infrastructure | Misconfiguration | Service disruption | Medium | Medium |
| Admin Accounts | Privilege abuse | System takeover | Low | High |

## 6. Risk Evaluation Methodology

Risk levels were determined using a qualitative assessment approach:

- Likelihood: Low / Medium / High
- Impact: Operational, Financial, Reputational, Regulatory

Risk Level = Likelihood × Impact severity.

High risks require immediate mitigation.
Medium risks require monitored mitigation.
Low risks are accepted with periodic review.
## 7. ISO 27001 Control Mapping

The following controls were selected to mitigate identified risks:

| Risk | ISO 27001 Control Area | Control Description |
|------|------------------------|--------------------|
| SQL Injection | A.14 Secure Development | Secure coding & input validation |
| Phishing | A.7 Awareness & Training | Security awareness training |
| Malware | A.12 Malware Protection | Anti-malware controls |
| Cloud Misconfiguration | A.12 Change Management | Configuration management |
| Privilege Abuse | A.9 Access Control | Least privilege & access review |

## 8. Risk Treatment Plan

| Risk | Treatment Strategy | Action |
|------|-------------------|--------|
| SQL Injection | Mitigate | Implement WAF & secure coding review |
| Phishing | Mitigate | Enforce MFA & awareness training |
| Malware | Mitigate | Endpoint protection & patch management |
| Cloud Misconfiguration | Mitigate | Periodic configuration audits |
| Privilege Abuse | Mitigate | Quarterly access reviews |

## 9. Continuous Monitoring Concept

To reduce manual compliance effort and enable continuous validation:

- SIEM alerts will monitor suspicious login attempts.
- Logs will track privilege escalations.
- Configuration monitoring tools will detect cloud misconfigurations.
- Automated access review reports will validate least privilege enforcement.

This approach transitions compliance from periodic review to continuous assurance.

## 10. Governance Alignment

This risk assessment supports the organization’s broader Information Security Governance framework by:

- Aligning identified risks with ISO 27001 control domains.
- Establishing accountability for risk treatment actions.
- Supporting audit-readiness through documented evaluation methodology.
- Enabling measurable compliance through continuous monitoring.

This ensures that risk management is integrated into the company’s governance structure rather than treated as a one-time exercise.

## 11. Formal Risk Register Structure

A structured risk register was developed to support ongoing governance and audit readiness.
| Risk ID | Asset | Risk Description | Likelihood (1-3) | Impact (1-3) | Risk Score | Risk Owner | Treatment | Status | Review Date |
|---------|--------|-----------------|------------------|--------------|------------|------------|-----------|--------|-------------|
| R-001 | Customer Database | SQL Injection leading to data breach | 3 | 3 | 9 | Head of Engineering | Mitigate | Open | Quarterly |
| R-002 | Email System | Phishing credential compromise | 3 | 3 | 9 | IT Manager | Mitigate | In Progress | Quarterly |
| R-003 | Employee Laptops | Malware infection | 2 | 2 | 4 | IT Operations | Mitigate | Open | Quarterly |
| R-004 | Cloud Infrastructure | Misconfiguration | 2 | 3 | 6 | Cloud Admin | Mitigate | Open | Quarterly |
| R-005 | Admin Accounts | Privilege abuse | 1 | 3 | 3 | Security Lead | Mitigate | Monitoring | Quarterly |
