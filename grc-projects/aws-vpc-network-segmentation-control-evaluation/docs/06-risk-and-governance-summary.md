# Risk & Governance Summary
### Controls Demonstrated

- VPC Network Segmentation

- NAT-Controlled Egress

- Security Group Hardening

- Least Privilege Enforcement

- Security Group Referencing

- Network ACL Defense in Depth

- Bastion Risk Assessment

- IAM-Based Secure Administrative Access

- Zero Trust Segmentation Principles

### Overall Risk Reduction Achieved
| Area                  | Before       | After                    |
| --------------------- | ------------ | ------------------------ |
| HTTP Exposure         | Open to all  | Restricted to proxy role |
| Lateral Movement      | Possible     | Reduced                  |
| Administrative Access | SSH exposed  | IAM-controlled           |
| Subnet Protection     | Single layer | Layered SG + NACL        |
