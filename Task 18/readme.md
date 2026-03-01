# Task 18: Azure Virtual Machine (Easy Task)

## Simple Definition

Azure Virtual Machine is a cloud-based compute service that allows running operating systems and applications in Microsoft Azure.

## Objective

To launch and configure a basic Azure Virtual Machine and access it using SSH or RDP.

## Architecture Overview

User  
↓  
Azure Virtual Machine  
↓  
Azure Virtual Network

## Steps

### Step 1: Create Azure VM

1. Go to Azure Portal.
2. Click Virtual Machines → Create.
3. Choose subscription and resource group.
4. Select image (Ubuntu or Windows).
5. Choose VM size.
6. Configure authentication (SSH/RDP).
7. Create VM.

### Step 2: Configure Networking

1. Ensure Public IP is enabled.
2. Configure NSG rules:
   - Allow SSH (22) or RDP (3389).

### Step 3: Connect to VM

For Ubuntu:
ssh azureuser@public-ip

For Windows:
Use Remote Desktop Connection.

## Verification

* VM status = Running.
* Successful SSH/RDP login.
* System information visible after login.

## Conclusion

Successfully launched and accessed Azure Virtual Machine, demonstrating understanding of Azure compute fundamentals.