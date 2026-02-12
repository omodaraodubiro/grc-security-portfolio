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
