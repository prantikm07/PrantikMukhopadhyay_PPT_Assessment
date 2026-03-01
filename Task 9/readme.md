# Task 9: Access S3 from Ubuntu using IAM Roles & Policies

## Simple Definition

IAM Roles allow EC2 instances to securely access AWS services without storing access keys. Instead of configuring AWS credentials manually, permissions are assigned to the instance through an IAM Role.

## Objective

To securely access Amazon S3 from an Ubuntu EC2 instance using an IAM Role instead of access keys, demonstrating role-based access control.

## Architecture Overview

EC2 Instance → IAM Role → S3 Bucket

No access keys are stored inside the instance.

## Steps

### Step 1: Create S3 Bucket

1. Go to AWS Console → S3.
2. Click Create bucket.
3. Provide unique name.
4. Select region.
5. Keep default settings.
6. Create bucket.

### Step 2: Create IAM Role

1. Go to IAM → Roles → Create Role.
2. Select Trusted Entity: EC2.
3. Attach policy: AmazonS3ReadOnlyAccess.
4. Name role: EC2S3Role.
5. Create role.

### Step 3: Attach Role to EC2

1. Go to EC2 → Instances.
2. Select Ubuntu instance.
3. Click Actions → Security → Modify IAM Role.
4. Choose EC2S3Role.
5. Save.

### Step 4: Test Access from Ubuntu

1. SSH into EC2.
2. Install AWS CLI.
3. Run:
   aws s3 ls
4. Confirm S3 bucket listing works without running aws configure.

## Verification

* IAM Role attached to EC2 instance.
* AmazonS3ReadOnlyAccess policy attached.
* S3 bucket list accessible.
* No AWS access keys configured.


## Conclusion

Successfully accessed S3 from EC2 using IAM Role, ensuring secure and keyless authentication. This demonstrates best practice for AWS access management.