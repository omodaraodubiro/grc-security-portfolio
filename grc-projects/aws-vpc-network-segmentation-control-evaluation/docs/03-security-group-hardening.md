# Security Group Hardening & Least Privilege
## 1. Baseline Security Group Assessment

Initial AppServerSG configuration:

Inbound:

HTTP (80)

Source: 0.0.0.0/0
![Private Subnet NAT Routing](../screenshots/appserver-open-http.png)

### Risk Analysis

Allowing inbound traffic from 0.0.0.0/0 increases attack surface.

Although the AppServer resides in a private subnet, overly permissive rules contradict least privilege principles.

## 2. IP-Based Restriction

Replaced 0.0.0.0/0 with:

ProxyServer1PublicIP/32
![Private Subnet NAT Routing](../screenshots/http-restricted-ip.png)

![Private Subnet NAT Routing](../screenshots/http-restricted-ip1.png)
Result:

ProxyServer1 → Access Granted

ProxyServer2 → Access Denied
### Governance Evaluation

Benefits:

- Reduced lateral movement risk

- Precise access control

Limitation:

- Not scalable

- Operationally rigid

- Vulnerable to IP changes
## 3. Security Group Referencing (Scalable Control)

Replaced IP rule with:

Allow HTTP from ProxySG

Assigned ProxySG to both proxy servers
![Private Subnet NAT Routing](../screenshots/security-group-reference-rule.png)
![Private Subnet NAT Routing](../screenshots/security-group-reference-rule1.png)

### Governance Strength

Security group referencing:

- Enables role-based segmentation

- Supports auto-scaling environments

- Eliminates static IP dependency

- Aligns with Zero Trust architecture

This represents mature cloud network design.
