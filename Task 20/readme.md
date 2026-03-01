# Task 20: Azure VNet (Basic Networking Practical)

## Simple Definition

Azure Virtual Network (VNet) allows secure communication between Azure resources, the internet, and on-premises networks.

## Objective

To create a Virtual Network, configure subnets, and apply Network Security Group (NSG) rules.

## Architecture Overview

Azure VNet  
↓  
Subnet  
↓  
Network Security Group (NSG)

## Steps

### Step 1: Create Virtual Network

1. Go to Azure Portal.
2. Search Virtual Networks → Create.
3. Select Subscription and Resource Group.
4. Enter VNet name.
5. Address space: 10.0.0.0/16.
6. Create VNet.

### Step 2: Create Subnet

1. Open created VNet.
2. Add Subnet:
   - Subnet name.
   - CIDR block (e.g., 10.0.1.0/24).
3. Save.

### Step 3: Create Network Security Group

1. Go to Network Security Groups → Create.
2. Attach NSG to subnet.
3. Add inbound rule:
   - Allow SSH (22) or HTTP (80).

## Verification

* VNet created successfully.
* Subnet associated with VNet.
* NSG rule visible.
* Resources inside subnet follow NSG rules.

## Conclusion

Successfully configured Azure Virtual Network with subnet and NSG rules, demonstrating basic cloud networking principles.