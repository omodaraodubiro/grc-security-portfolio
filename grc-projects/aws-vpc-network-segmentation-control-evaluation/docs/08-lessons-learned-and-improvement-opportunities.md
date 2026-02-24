# Lessons Learned & Improvement Opportunities

## 1. Lessons Learned

### Network Segmentation Alone Is Not Enough

Although the AppServer was placed in a private subnet, initial security group rules still allowed overly permissive inbound access (0.0.0.0/0).

**Insight:**
Segmentation must be paired with strict access control enforcement to be effective.

### Least Privilege Requires Scalability Consideration

Restricting access using a /32 IP address improved security but introduced operational rigidity.

**Insight:**
Security controls must balance precision with scalability. Security group referencing is superior to static IP restriction in dynamic environments.


### Defense in Depth Prevents Single-Point Control Failure

Even when security groups allowed traffic, NACL deny rules successfully blocked it.

**Insight:**
Layered security ensures that misconfiguration at one layer does not immediately result in exposure.

### Traditional Administrative Access Models Increase Attack Surface

The Bastion host model required:

* Open SSH port (22)
* Key management
* External exposure

**Insight:**
Legacy access models may function operationally but introduce avoidable risk.

### IAM-Based Access Improves Auditability

AWS Systems Manager Session Manager removed the need for open inbound SSH while enabling IAM-based session control.

**Insight:**
Modern cloud-native access mechanisms improve compliance defensibility and reduce exposure risk.

## 2. Improvement Opportunities

If this were a production environment, the following enhancements would be recommended:

### Implement AWS Config Rules

Automatically detect:

* Security groups allowing 0.0.0.0/0
* Unrestricted SSH exposure
* Missing NACL deny rules

### Enable VPC Flow Logs

To:

* Monitor anomalous traffic
* Support incident investigation
* Improve network visibility

### Centralized Logging Integration

Send:

* Session Manager logs
* Security group change logs
* NACL modification events

To:

* CloudWatch or SIEM platform for monitoring and alerting


### Implement Infrastructure as Code (IaC)

Use:

* AWS CloudFormation or Terraform

To:

* Enforce standardized secure configurations
* Reduce configuration drift
* Improve audit traceability


### Continuous Compliance Monitoring

Integrate:

* CIS AWS Foundations Benchmark automated checks
* Periodic security posture assessments

## 3. Professional Reflection

This project strengthened understanding of:

* The difference between stateful and stateless controls
* Operational versus governance-focused security design
* The importance of auditability in cloud environments
* How small misconfigurations can materially impact risk posture

It reinforced the principle that effective cloud governance requires both technical configuration awareness and structured risk evaluation.
