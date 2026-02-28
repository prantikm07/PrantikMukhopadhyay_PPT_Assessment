# Task 4: Auto Scaling Group and Load Balancer in EC2

## Simple Definition

Auto Scaling Group (ASG) automatically adjusts the number of EC2 instances based on demand. A Load Balancer distributes incoming traffic across multiple instances.

## Objective

To understand high availability and scaling concepts by configuring an Auto Scaling Group attached to a Load Balancer.

## Steps

### 1. Create Launch Template
- Select AMI and instance type.
- Configure security group with HTTP and SSH.
- Add user data to install Nginx.

### 2. Create Target Group
- Protocol: HTTP
- Port: 80
- Configure health checks.

### 3. Create Application Load Balancer
- Internet-facing.
- Select at least two subnets.
- Attach target group.

### 4. Create Auto Scaling Group
- Select launch template.
- Choose VPC and subnets.
- Attach to load balancer.
- Set desired capacity to 2 instances.

## Verification

- Load Balancer status: Active.
- Two EC2 instances running under ASG.
- Access ALB DNS in browser.
- Web page loads successfully.
- Health checks show healthy instances.

Screenshots Submitted:
1. Launch Template details.
2. Load Balancer active with DNS name.
3. Auto Scaling Group showing running instances.

## Conclusion

Successfully configured an Auto Scaling Group with a Load Balancer. This demonstrates high availability and automatic scaling in AWS EC2.