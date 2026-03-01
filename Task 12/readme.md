# Task 12: Website Down Alert using Lambda (Canary) + SNS

## Simple Definition

Monitor a website’s availability and automatically send alerts when the website becomes unreachable.

## Objective

To implement automated monitoring and alerting using CloudWatch Synthetics Canary and SNS notifications.

## Architecture Overview

CloudWatch Canary  
↓  
CloudWatch Alarm  
↓  
SNS Topic  
↓  
Email Alert

## Steps

### Step 1: Create SNS Topic

1. Go to SNS → Create Topic.
2. Choose Standard topic.
3. Add email subscription.
4. Confirm email subscription.

### Step 2: Create CloudWatch Canary

1. Go to CloudWatch → Synthetics.
2. Click Create Canary.
3. Choose blueprint: Heartbeat monitoring.
4. Enter website URL.
5. Configure schedule.
6. Create Canary.

### Step 3: Create CloudWatch Alarm

1. Go to CloudWatch → Alarms.
2. Create Alarm based on Canary failure metric.
3. Set threshold for failure.
4. Add SNS topic as notification action.
5. Create alarm.

## Verification

* Stop website or simulate failure.
* Alarm state changes to ALARM.
* Email notification received from SNS.
* Canary execution logs visible in CloudWatch.

## Conclusion

Successfully implemented automated website monitoring and alert system using AWS CloudWatch Canary and SNS, ensuring proactive uptime management.