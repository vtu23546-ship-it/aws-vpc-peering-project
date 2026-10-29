# aws-vpc-peering-project
AWS VPC Peering project: two VPCs, bastion host, route tables and security groups, tested with private ping and SSH. Report included.
# AWS VPC Peering Project

Connect two VPCs and prove private connectivity.

## Overview
- VPC A (10.10.0.0/16): public subnet with a bastion host, private subnet with App-A
- VPC B (10.20.0.0/16): private subnet with App-B
- VPC peering connection with routes on both sides
- Security groups allow only the required SSH and ICMP traffic
- Admin access with SSH ProxyJump through the bastion

## Tested
- Two-way ping between App-A and App-B over private IPs
- Private SSH to App-B through the bastion
- Controlled failure and recovery (ICMP rule removed, then restored)

## Report
[Glen_VPC_Peering.pdf](Glen_VPC_Peering.pdf)

**Region:** us-east-1 | **Author:** Glen Nitish
