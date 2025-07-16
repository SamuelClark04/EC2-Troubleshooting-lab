# EC2-Troubleshooting-lab - SSH Connection Failure

## Scenario
I simulated a real-world issue where an EC2 instance launched successfully but could not be accessed via SSH.

This lab was designed to mirror the kinds of problems cloud support engineers solve daily.

## The Problem
- EC2 instance launched using a custom security group
- SSH connection attempt resulted in - "Operation Timeout"
- All settings (AMI, key pair, public IP) seemed correct

## Troubleshooting Performed
-  Confirmed instance was running
- Verified public IP was assigned
- Checked VPC/subnet and route table (Internet Gateway attached)
- Discovered that port 22 was not open in the Security Group

## Fix Implemented
- Edited the Security Group inbound rules
- Added SSH (port 22) access from my IP
- Re-attempted SSH — successfully connected

## What I Learned
- How to identify and fix common EC2 connectivity issues
- The layered relationship between security groups, route tables, and public IPs
- How to think like a cloud support engineer

## Tools Used
- AWS EC2
- AWS VPC & Security Groups
- SSH via Terminal
- Key pair management (.pem files)

This project proves I can troubleshoot AWS connectivity issues, use EC2 securely, and fix broken infrastructure with minimal guidance.
