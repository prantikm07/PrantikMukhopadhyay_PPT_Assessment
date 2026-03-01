# Task 13: Start/Stop EC2 using Lambda + API Gateway

## Simple Definition

Automate starting and stopping EC2 instances using a serverless Lambda function triggered through API Gateway.

## Objective

To learn serverless automation by integrating Lambda with API Gateway to control EC2 instances.

## Architecture Overview

API Gateway  
↓  
Lambda Function  
↓  
EC2 Instance Control (Start / Stop)

## Steps

### Step 1: Create IAM Role for Lambda

1. Go to IAM → Roles → Create Role.
2. Select Trusted Entity: Lambda.
3. Attach policy: AmazonEC2FullAccess.
4. Create role.

### Step 2: Create Lambda Function

1. Go to Lambda → Create Function.
2. Runtime: Python.
3. Assign IAM role created above.
4. Write code to start or stop EC2 using boto3.
5. Deploy function.

### Step 3: Create API Gateway

1. Go to API Gateway → Create API.
2. Choose HTTP API.
3. Add integration with Lambda function.
4. Create route (e.g., /start or /stop).
5. Deploy API.

### Step 4: Test API

1. Copy API endpoint URL.
2. Open in browser or use curl.
3. Confirm EC2 instance state changes.

## Verification

* API endpoint accessible.
* Lambda execution logs show successful execution.
* EC2 instance state changes from stopped to running or vice versa.
* API response returns success message.

## Conclusion

Successfully automated EC2 start/stop operations using Lambda and API Gateway, demonstrating serverless infrastructure control and automation.