# aws-ec2-s3-mini-project
# Deploying a web server on EC2 and serving static assets from S3 with monitoring using CloudWatch.

## Overview
This mini project demonstrates how to deploy, secure, and monitor a basic web application using core AWS services.
An Apache web server is hosted on an EC2 instance, while static assets (images) are stored and served from Amazon S3.
Monitoring is performed using Amazon CloudWatch.

This project was built using AWS Free Tier resources with cost-awareness and proper cleanup.

## Services Used
- Amazon EC2
- Amazon S3
- AWS IAM
- Security Groups
- Amazon CloudWatch
- AWS Systems Manager (Session Manager)

## Architecture
- User accesses the website via the EC2 public IPv4 address
- EC2 runs an Apache web server
- Static image files are stored in Amazon S3
- EC2 website references the image using the S3 object URL
- Security Groups control inbound HTTP and SSH access
- CloudWatch monitors EC2 CPU utilization

## Implementation Summary
1. Launched an EC2 instance using Amazon Linux (Free Tier eligible)
2. Configured Security Groups to allow HTTP access
3. Installed and started Apache web server on EC2
4. Created an S3 bucket to store static assets
5. Configured S3 bucket policy for controlled public read access
6. Integrated S3-hosted image into the EC2-hosted website
7. Monitored EC2 performance using CloudWatch metrics
8. Stopped the EC2 instance after verification to avoid billing

## Screenshots
All screenshots related to this project are available in the `screenshots/` folder, including:
- EC2 instance running
- Apache test page
- EC2 website loading image from S3
- S3 bucket and object upload
- S3 bucket policy
- CloudWatch CPUUtilization metrics
- EC2 instance stopped (cost control)

## Key Learnings
- Practical understanding of EC2 and S3 integration
- Importance of Security Groups in controlling access
- Difference between compute and object storage
- Basics of cloud monitoring using CloudWatch
- Cost awareness and proper cleanup of cloud resources

## Cleanup
After completing the project and taking screenshots:
- EC2 instance was stopped
- No unnecessary resources were left running

This ensures zero or minimal cost usage under AWS Free Tier.
