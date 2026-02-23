# AWS IAM & S3 Governance Risk Assessment
### 1. Identified Control Weaknesses
**Risk 1: Overreliance on Resource-Based Policies**

**Observation:**
Access to bucket2 was granted through a bucket policy even though the IAM role policy did not explicitly grant s3:PutObject.
**Risk:**
If bucket policies are loosely managed, they can unintentionally expand access beyond intended role permissions.

**Impact:**

Unauthorized data upload

Data exfiltration

Accidental exposure

Compliance violations (GLBA, SOC 2, ISO 27001 Annex A.9)

**Mitigation:**

Centralized review of bucket policies

Enforce explicit deny statements where necessary

Implement Service Control Policies (SCPs) at the org level

Use AWS Access Analyzer for policy validation

**Risk 2: Privilege Escalation via Role Assumption**

**Observation:**
Assuming BucketsAccessRole significantly altered permissions.

**Risk:**
If trust policies are overly broad, malicious users could assume privileged roles.

**Impact:**

Horizontal privilege escalation

Access to sensitive data

Regulatory breach

**Mitigation:**

Restrict trust relationships to specific principals

Use MFA for role assumption

Enable CloudTrail monitoring for AssumeRole events

Implement conditional access controls

**Risk 3: Lack of Explicit Deny Controls**

**Observation:**
No explicit deny policies were present to prevent unintended access expansion.

**Risk:**
Implicit allow through resource-based policies may override governance intent.

**Impact:**

Policy misalignment

Control circumvention

**Mitigation:**

Implement explicit deny conditions for sensitive buckets

Periodic policy review audits

Continuous monitoring using AWS Config

### 2. Control Evaluation Summary
| Control Area              | Status             | Observation                              |
| ------------------------- | ------------------ | ---------------------------------------- |
| Least Privilege           | Partially Enforced | Identity policy limited object actions   |
| Role Trust Governance     | Controlled         | Trust policy restricted to specific user |
| Resource Policy Oversight | Weak               | Bucket2 policy expanded access           |
| Monitoring & Logging      | Assumed Enabled    | CloudTrail records API attempts          |

### 3. Governance Lessons Learned
Effective access = identity policy + resource policy + trust policy

Resource-based policies require strict governance oversight

Role assumption significantly alters risk posture

Cloud environments require layered control validation
