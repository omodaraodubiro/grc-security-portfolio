# AWS VPC Network Segmentation & Governance Control Evaluation
## Executive Summary
This project evaluates and strengthens network segmentation and access control within an AWS Virtual Private Cloud (VPC) environment.

The simulation focused on identifying excessive exposure risks, implementing least privilege controls, validating layered security enforcement, and comparing traditional versus modern administrative access mechanisms.

### The assessment demonstrates practical understanding of:

- VPC routing architecture
- Security group hardening
- Network ACL evaluation
- Bastion host risk analysis
- IAM-based secure administrative access
- Defense-in-depth design principles
- Cloud governance alignment
- Defense-in-depth design principles
- Cloud governance alignment

## Governance & Risk Alignment

This project aligns with the following governance and security principles:

- Least Privilege (NIST AC-6)

- Network Segmentation (NIST SC-7)

- Defense in Depth

- Zero Trust Architecture Concepts

- Secure Administrative Access Controls

- Auditability & Accountability (AU family controls)

### Key Governance Takeaways

- Security groups alone are insufficient without subnet-level controls.

- IP-based restrictions reduce risk but lack scalability.

- Security group referencing enables role-based segmentation.

- NACLs provide containment controls at the subnet boundary.

- Bastion hosts introduce exposure risk and operational overhead.

- Session Manager improves auditability and reduces attack surface.

