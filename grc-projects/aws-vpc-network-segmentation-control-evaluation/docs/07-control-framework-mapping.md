# Control Framework Mapping (Light Alignment)

This section provides a high-level alignment between the controls evaluated in this project and recognized security governance frameworks.

The purpose is not full compliance certification, but demonstration of control awareness and governance alignment.
## 1. NIST SP 800-53 (Rev. 5) – Relevant Control Families
| Project Activity               | NIST Control               | Alignment Explanation                                     |
| ------------------------------ | -------------------------- | --------------------------------------------------------- |
| Security group least privilege | AC-6 (Least Privilege)     | Restricted inbound access to only required sources        |
| Network segmentation via VPC   | SC-7 (Boundary Protection) | Isolated private subnets from internet exposure           |
| NACL defense-in-depth          | SC-7(3)                    | Implemented layered subnet boundary control               |
| Bastion host evaluation        | AC-17 (Remote Access)      | Assessed risk of externally exposed administrative access |
| Session Manager implementation | AU-2 / AU-12               | Supports auditable, logged administrative sessions        |
| IAM-based access               | IA-2                       | Identity-based access control enforcement                 |

### NIST Alignment Summary

The project demonstrates application-level and infrastructure-level enforcement of access control and boundary protection mechanisms consistent with NIST guidance.

## 2. ISO/IEC 27001:2022 – Relevant Control Domains
| Project Activity                | ISO Control                    | Alignment Explanation                            |
| ------------------------------- | ------------------------------ | ------------------------------------------------ |
| Restricting inbound HTTP        | A.8.20 Network Security        | Network controls implemented to protect services |
| Segmented VPC design            | A.8.22 Segregation of Networks | Separation of public and private network zones   |
| Administrative access hardening | A.8.2 Privileged Access Rights | Controlled administrative access                 |
| Session Manager over SSH        | A.8.15 Logging                 | Enables auditable session monitoring             |
| Layered SG + NACL controls      | A.5.15 Defense in Depth        | Multiple security layers applied                 |

### ISO Alignment Summary

The evaluation supports network segregation, privileged access control, and layered defensive architecture consistent with ISO 27001 Annex A controls.

## 3. CIS AWS Foundations Benchmark (Light Mapping)
| Project Activity               | CIS Control Area      | Alignment                               |
| ------------------------------ | --------------------- | --------------------------------------- |
| Removal of 0.0.0.0/0 exposure  | 4.x – Security Groups | Minimized unrestricted inbound access   |
| Use of IAM for Session Manager | 1.x – IAM Controls    | Leveraged identity-based access         |
| Network segmentation           | 3.x – VPC Controls    | Isolated subnets and controlled routing |
| Avoidance of open SSH          | 4.x – EC2 Security    | Reduced administrative exposure risk    |

### CIS Alignment Summary

The hardening measures reflect adherence to AWS security best practices regarding network exposure and identity control.
