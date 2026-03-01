# Task 14: CloudWatch Alarm (70% CPU → Auto Stop + Email)

## Simple Definition

CloudWatch Alarm monitors EC2 CPU usage and automatically performs an action (such as stopping the instance) when the CPU crosses a defined threshold.

## Objective

To configure automated monitoring and response using CloudWatch alarms and SNS notifications.

## Architecture Overview

EC2 Instance  
↓  
CloudWatch Metric (CPUUtilization)  
↓  
CloudWatch Alarm  
↓  
SNS Notification + EC2 Stop Action

## Steps

### Step 1: Create SNS Topic

1. Go to SNS → Create Topic.
2. Select Standard.
3. Enter topic name.
4. Add email subscription.
5. Confirm subscription via email.

### Step 2: Create CloudWatch Alarm

1. Go to CloudWatch → Alarms → Create Alarm.
2. Select metric: EC2 → Per-Instance Metrics → CPUUtilization.
3. Choose your EC2 instance.
4. Set threshold:
   - Greater than 70%.
5. Configure Actions:
   - Send notification to SNS topic.
   - Add EC2 action → Stop instance.
6. Create alarm.

### Step 3: Test Alarm

1. Generate CPU load on EC2.
2. Monitor CloudWatch metrics.
3. Wait until CPU exceeds 70%.

## Verification

* Alarm state changes to ALARM.
* Email notification received.
* EC2 instance automatically stops.
* Alarm visible in CloudWatch dashboard.

## Conclusion

Successfully configured CloudWatch Alarm to monitor CPU utilization and automatically stop EC2 while sending email notification. Demonstrates automated monitoring and infrastructure control.