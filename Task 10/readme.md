# Task 10: VPC 3-Tier Architecture

## Simple Definition

A 3-tier architecture divides an application into three layers: Web layer (Public), Application layer (Private), and Database layer (Private). This improves security, scalability, and network isolation.

## Objective

To design and implement a secure 3-tier network architecture using VPC, subnets, Internet Gateway, NAT Gateway, route tables, NACLs, and SSH tunneling.

## Architecture Overview

Internet  
↓  
Internet Gateway  
↓  
Public Subnet (Web Server / Bastion Host)  
↓  
Private Subnet (Application Server via NAT)  
↓  
Private Subnet (Database Server)

## Steps

### Step 1: Create Custom VPC

1. Go to VPC → Create VPC.
2. Name the VPC.
3. CIDR Block: 10.0.0.0/16.
4. Create VPC.

### Step 2: Create Subnets

1. Create Public Subnet:
   - CIDR: 10.0.1.0/24
2. Create Private App Subnet:
   - CIDR: 10.0.2.0/24
3. Create Private DB Subnet:
   - CIDR: 10.0.3.0/24

### Step 3: Create Internet Gateway

1. Go to Internet Gateways → Create.
2. Attach to the VPC.

### Step 4: Create NAT Gateway

1. Allocate Elastic IP.
2. Create NAT Gateway in Public Subnet.
3. Associate Elastic IP.

### Step 5: Configure Route Tables

1. Public Route Table:
   - Add route 0.0.0.0/0 → Internet Gateway.
   - Associate with Public Subnet.

2. Private Route Table:
   - Add route 0.0.0.0/0 → NAT Gateway.
   - Associate with Private Subnets.

### Step 6: Launch EC2 Instances

1. Launch Web Server in Public Subnet.
2. Launch App Server in Private Subnet.
3. Launch Database Server in Private Subnet.

### Step 7: Configure SSH Tunneling

1. SSH into Public EC2.
2. From Public EC2, SSH into Private EC2.

## Verification

* Public instance accessible via Internet.
* Private instances not accessible directly from Internet.
* Private instances can access Internet through NAT Gateway.
* SSH tunneling works via Bastion host.

## Conclusion

Successfully designed and implemented a secure 3-tier VPC architecture demonstrating network segmentation, routing configuration, and secure access control.