# Task 8: Create IAM Users and Groups

## Simple Definition

IAM (Identity and Access Management) allows creation of users and groups and assigning permissions to securely control access to AWS resources.

## Objective

To create IAM users and groups and attach policies to manage access control and security permissions in AWS.

## GUI Steps

### Step 1: Create IAM Group
1. Go to AWS Console → IAM.
2. Click User Groups → Create group.
3. Name the group: developers.
4. Attach policy: AmazonS3ReadOnlyAccess.
5. Create group.

### Step 2: Create IAM Users
1. Go to IAM → Users → Create user.
2. Enter user name: user1.
3. Enable AWS Management Console access.
4. Set custom password and require password reset.
5. Add user to group: developers.
6. Repeat same steps for user2.

### Step 3: Verify Permissions
1. Check group developers → Policies tab.
2. Confirm AmazonS3ReadOnlyAccess attached.
3. Confirm both users are members of the group.

## Verification

- developers group exists.
- AmazonS3ReadOnlyAccess policy attached.
- user1 and user2 created.
- Users successfully added to group.
- Console login enabled.

Screenshots Submitted:
1. Group showing attached policy and users.
2. Users list showing user1 and user2.

## Conclusion

Successfully created IAM users and group and attached appropriate policies. This demonstrates understanding of AWS access control and security management.