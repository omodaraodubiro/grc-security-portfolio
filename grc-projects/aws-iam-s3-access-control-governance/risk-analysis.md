## AWS IAM & S3 Governance Risk Assessment
## 1. Identified Control Weaknesses
## Risk 1: Overreliance on Resource-Based Policies

Observation:
Access to bucket2 was granted through a bucket policy even though the IAM role policy did not explicitly grant s3:PutObject.
Risk:
If bucket policies are loosely managed, they can unintentionally expand access beyond intended role permissions.

Impact:

Unauthorized data upload

Data exfiltration

Accidental exposure

Compliance violations (GLBA, SOC 2, ISO 27001 Annex A.9)
Mitigation:

Centralized review of bucket policies

Enforce explicit deny statements where necessary

Implement Service Control Policies (SCPs) at the org level

Use AWS Access Analyzer for policy validation
