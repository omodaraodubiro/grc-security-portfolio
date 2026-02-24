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

ProxyServer1PrivateIP/32
![Private Subnet NAT Routing](../screenshots/http-restricted-ip.png)

![Private Subnet NAT Routing](../screenshots/http-restricted-ip1.png)
