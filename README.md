# AWS VPC Peering Project

## Project Overview
This project demonstrates VPC Peering between two Amazon Virtual Private Clouds (VPCs), enabling private communication between EC2 instances using private IPv4 addresses.

## Architecture
- **VPC A:** `10.10.0.0/16`
- **VPC B:** `10.20.0.0/16`
- **Bastion Host:** Public subnet in VPC A
- **App-A:** Private subnet in VPC A
- **App-B:** Private subnet in VPC B
- **AWS Region:** Asia Pacific (Sydney) — `ap-southeast-2`

## AWS Services Used
- Amazon VPC
- VPC Peering
- Amazon EC2
- Route Tables
- Security Groups
- SSH and ICMP

## Implementation
1. Created two VPCs with non-overlapping CIDR blocks.
2. Created public and private subnets.
3. Launched one bastion host and two private EC2 instances.
4. Configured and activated VPC Peering.
5. Added routes for communication between both VPCs.
6. Configured security groups for SSH and ICMP traffic.
7. Tested connectivity using private IPv4 addresses.

## Verification
- Verified the VPC Peering connection.
- Tested connectivity between App-A and App-B using ping.
- Tested SSH access from the bastion host to App-B.
- Verified that both application instances had no public IPv4 addresses.
- Tested ICMP failure and recovery by modifying a security group rule.

## Security
Private application instances have no public IPv4 addresses. SSH access is intended to pass through the bastion host. No private keys, passwords, or AWS credentials should be committed to this repository.

## Author
Souraneel Biswas

