# Task 11: S3 Upload Email Notification (Lambda + SNS)

## Simple Definition

Automatically send an email notification when a file is uploaded to an S3 bucket using Lambda and SNS services.

## Objective

To implement event-driven architecture using S3 triggers, Lambda functions, and SNS email notifications.

## Architecture Overview

S3 Upload Event  
↓  
Lambda Function Trigger  
↓  
SNS Topic  
↓  
Email Notification

## Steps

### Step 1: Create SNS Topic

1. Go to SNS → Create Topic.
2. Choose Standard topic.
3. Enter topic name.
4. Create topic.
5. Add subscription:
   - Protocol: Email
   - Enter email address.
6. Confirm subscription from email.

### Step 2: Create Lambda Function

1. Go to Lambda → Create Function.
2. Choose Author from scratch.
3. Runtime: Python.
4. Create new execution role with basic Lambda permissions.

### Step 3: Add SNS Publish Permission

1. Go to Lambda Execution Role.
2. Attach AmazonSNSFullAccess policy.

### Step 4: Add Lambda Code

1. Write code to publish message to SNS topic.
2. Deploy function.

### Step 5: Configure S3 Trigger

1. Go to S3 → Select bucket.
2. Go to Properties → Event Notifications.
3. Create new event:
   - Event type: PUT (Object Created)
   - Destination: Lambda function.
4. Save.

## Verification

* Upload a file to S3 bucket.
* Lambda is triggered.
* Email notification is received.
* Lambda logs visible in CloudWatch.

## Conclusion

Successfully implemented S3 event-driven notification using Lambda and SNS, demonstrating serverless automation and real-time alerting.