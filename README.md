# README

## Description

This Terraform configuration sets up an Application Load Balancer (ALB) and an Auto Scaling Group (ASG) in AWS. The ALB distributes traffic to the instances in the ASG, which automatically scales based on CPU utilization.

## Prerequisites

- AWS account with appropriate permissions.
- Terraform installed locally.

## Usage

1. Clone this repository to your local machine.
2. Modify the `provider "aws"` block in the `main.tf` file with your AWS region if needed.
3. Run `terraform init` to initialize the working directory.
4. Run `terraform apply` to create the resources.
5. After verifying the plan, type `yes` to apply the changes.

## Configuration Details

- **ALB:** 
  - Type: Application Load Balancer.
  - Target Groups: Configured to forward traffic to a specific instance.
  - Listeners: HTTP and HTTPS listeners configured.

- **Auto Scaling Group (ASG):**
  - Launch Configuration: Uses a predefined AMI and instance type.
  - Scaling Policies: Automatically scales based on CPU utilization.
  - Instance Refresh: Configured for rolling updates.

## Notes

- Make sure to review the Terraform plan before applying changes to avoid unexpected costs or resource changes.
- This configuration is basic and may need modifications based on your specific requirements and best practices.
