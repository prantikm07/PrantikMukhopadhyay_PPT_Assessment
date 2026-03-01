# Task 21: Entra ID (Users, Roles, Basic Identity Management)

## Simple Definition

Azure Entra ID (formerly Azure Active Directory) is a cloud-based identity and access management service.

## Objective

To create users and assign roles using Azure Entra ID for managing identity and access control.

## Architecture Overview

Azure Entra ID  
↓  
Users  
↓  
Roles & Permissions

## Steps

### Step 1: Create User

1. Go to Azure Portal.
2. Search Entra ID → Users.
3. Click New User.
4. Enter username and password.
5. Create user.

### Step 2: Assign Role

1. Go to Subscriptions.
2. Select subscription.
3. Click Access Control (IAM).
4. Click Add role assignment.
5. Select role (e.g., Reader).
6. Assign to created user.

## Verification

* User visible in Entra ID.
* Role assignment visible under IAM.
* User can log in with assigned permissions.

## Conclusion

Successfully created users and assigned roles in Azure Entra ID, demonstrating identity and access management.