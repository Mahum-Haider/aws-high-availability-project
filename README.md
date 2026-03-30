# AWS Highly Available Web Application Architecture

This project demonstrates the design and deployment of a highly available and scalable web application on AWS.

It leverages EC2, Auto Scaling, Application Load Balancer, RDS, CloudWatch, and SNS to simulate a real-world production architecture.

## Architecture Overview

The application is deployed across multiple Availability Zones to ensure high availability and fault tolerance.

Key components include:
- EC2 instances running a web application
- Auto Scaling Group for dynamic scaling
- Application Load Balancer for traffic distribution
- Amazon RDS (MySQL) for database
- CloudWatch for monitoring
- SNS for notifications

## Architecture Diagram

The following diagram illustrates the overall system design and how components interact:

![Architecture Diagram](./screenshots/architecture.png)

## Implementation Steps

1. Created a Launch Template with EC2 configuration and user data.
2. Configured an Auto Scaling Group across multiple Availability Zones.
3. Set up an Application Load Balancer with a Target Group.
4. Registered EC2 instances and configured health checks.
5. Deployed a MySQL database using Amazon RDS.
6. Configured CloudWatch monitoring and alarms.
7. Set up SNS notifications for alerting.
8. Simulated failure scenarios to test high availability.

## Screenshots

### Application Running
![App](./screenshots/app.png)
<img width="1461" height="562" alt="app" src="https://github.com/user-attachments/assets/690c488a-4bf9-425d-8319-a8497788b380" />

### Connected to EC2 Instance via SSH
![SSH to EC2](screenshots/ssh-ec2.png)
<img width="578" height="276" alt="ssh-ec2" src="https://github.com/user-attachments/assets/0b35e36e-9c69-4f08-b7bc-4fde6fb17274" />

### RDS Instance in Available State
![RDS Available](screenshots/rds-available.png)
<img width="1455" height="338" alt="rds-available" src="https://github.com/user-attachments/assets/24d0e78a-7381-4d3c-a63c-bf25e65a46c8" />

### MySQL Connection Successful
![MySQL Connection](screenshots/mysql-connection.png)
<img width="579" height="137" alt="mysql-connection" src="https://github.com/user-attachments/assets/14585f9f-6296-4d44-969d-efe32eb8170b" />

### CloudWatch Dashboard: CPU Utilization Metrics
![CPU Graph](screenshots/cpu-dashboard.png)
<img width="449" height="458" alt="cpu-dashboard" src="https://github.com/user-attachments/assets/72a89921-f533-4410-90b7-d579948d192e" />

### CloudWatch Alarms: EC2 and RDS High CPU
![Alarms](screenshots/cloudwatch-alarms.png)
<img width="1464" height="469" alt="cloudwatch-alarms png)" src="https://github.com/user-attachments/assets/b9350d89-c0d5-4ccb-bcd9-45d29e5ea6ea" />

### CloudWatch Alarm: CPU Utilization Exceeds Threshold
![CPU Alarm](screenshots/cpu-alarm.png)
<img width="574" height="481" alt="cpu-alarm" src="https://github.com/user-attachments/assets/a843d4bf-6be5-48b4-8ef9-f65047291947" />


### CloudWatch Alarm Notification via Amazon SNS
![SNS Email](screenshots/sns-email.png)
<img width="1062" height="643" alt="sns-email" src="https://github.com/user-attachments/assets/36e2f482-45c4-4e58-a86b-e5dfdf7686a4" />

### Auto Scaling Group Self-Healing in Action
![ASG Self Healing](screenshots/asg-self-healing.png)
<img width="1226" height="227" alt="asg-self-healing" src="https://github.com/user-attachments/assets/c783b457-f7f4-4ede-bc49-47e968de336d" />

### ALB Target Group: EC2 Instance Registered and Healthy
![ALB Health](screenshots/alb-health.png)
<img width="1178" height="220" alt="alb-health" src="https://github.com/user-attachments/assets/1b500bdb-6692-47ff-b90c-7d0dcd4b6d87" />










### Target Group Healthy
![Target Group](./screenshots/target-group.png)

### Auto Scaling Group
![ASG](./screenshots/asg.png)

### RDS Database
![RDS](./screenshots/rds.png)

### CloudWatch Monitoring
![CloudWatch](./screenshots/cloudwatch.png)

## Key Features

- High availability using Multi-AZ deployment
- Auto Scaling for handling traffic dynamically
- Load balancing across multiple EC2 instances
- Database integration using Amazon RDS
- Monitoring and alerting with CloudWatch and SNS
- Fault tolerance tested through simulated failures

## Outcome

Successfully built and tested a highly available and scalable AWS architecture capable of handling failures and distributing traffic efficiently.
