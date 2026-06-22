# AWS Monitoring & Observaibility Platform

## Project Overview

This project demonstrates the implementation of a cloud-native monitroing and observability platform on AWS. The solution hosts an Nginx web application on Amazon EC2 and implements monitoring, alerting, log aggregation and reliability engineering practices using Amazon Cloudwatch. 
The project folloes Site Reliability Engineering (SRE) principles and focuses on the four Golden Signals:
- Latency
- Traffic
- Errors
- Saturation

## Architecture

```text
User
   │
   ▼
Amazon EC2 (Nginx Web Server)
   │
   ▼
CloudWatch Agent
   │
   ├── System Metrics Collection
   │       ├── CPU Utilization
   │       ├── Memory Utilization
   │       └── Disk Usage
   │
   ├── Application Logs
   │       ├── Nginx Access Logs
   │       └── Nginx Error Logs
   │
   ▼
Amazon CloudWatch
   │
   ├── Metrics Dashboard
   ├── Log Groups
   └── CloudWatch Alarms
             │
             ▼
        Amazon SNS
             │
             ▼
      Email Notifications
```
  ## AWS Services Used

| Service | Purpose |
|----------|----------|
| EC2 | Hosted Nginx web application |
| IAM | Managed permissions for CloudWatch Agent |
| CloudWatch | Metrics monitoring, dashboards and alarms |
| CloudWatch Agent | Collected system metrics and application logs |
| SNS | Email alert notifications |
| Security Groups | Controlled network access |

## Project Objectives

- Implement a production-style monitoring solution.
- Collect infrastructure metrics from EC2.
- Centralize application logs.
- Create automated alerting mechanisms.
- Follow Site Reliability Engineering (SRE) monitoring principles.
- Improve observability and troubleshooting capabilities.

## Implementation Summary

1. Launched Amazon EC2 instance running Amazon Linux.
2. Installed and configured Nginx web server.
3. Created a custom web page for testing.
4. Installed CloudWatch Agent.
5. Attached IAM Role with CloudWatch permissions.
6. Configured CloudWatch Agent to collect:
   - CPU Metrics
   - Memory Metrics
   - Disk Metrics
   - Nginx Access Logs
   - Nginx Error Logs
7. Created CloudWatch Log Groups.
8. Configured CloudWatch Alarms.
9. Integrated SNS email notifications.
10. Validated alerts using simulated failures.

## Results

Successfully implemented a cloud-native monitoring platform capable of:

- Real-time infrastructure monitoring
- Centralized log aggregation
- Automated alert generation
- Email-based incident notifications
- Improved visibility into application health

The solution achieved complete monitoring coverage for defined observability requirements.
