# AWS VPC Endpoint Architecture

This project demonstrates a secure AWS network setup that allows EC2 instances in a private subnet to access Amazon S3 using a VPC Endpoint, without traversing the public internet.

## Architecture Overview

![Event driven (1)](https://github.com/user-attachments/assets/a79116ec-26a3-409a-a5ef-3ea0c166a47f)


### Components:

- VPC (Virtual Private Cloud): Custom network for AWS resources.
- Public Subnet: Contains a Bastion Host used to connect to private EC2 instances via SSH.
- Private Subnet: Contains an EC2 instance with no direct internet access.
- Internet Gateway: Allows the Bastion Host in the public subnet to access the internet.
- VPC Endpoint (Gateway Type): Connects the private EC2 instance to Amazon S3 privately.
- S3 Bucket: Target AWS service accessed through the VPC endpoint.

## How It Works

1. Users SSH into the Bastion Host (public subnet) to securely reach the EC2 instance (private subnet).
2. The EC2 instance in the private subnet has no internet access.
3. It accesses S3 through a Gateway VPC Endpoint, keeping traffic within AWS' private network.
4. This setup improves security, performance, and cost efficiency by avoiding NAT gateways or internet routing.

## Use Case

- Secure data transfers from private EC2 to S3
- Avoiding internet exposure for sensitive workloads
- Reducing cost by removing NAT Gateway dependencies

## Prerequisites

- AWS account with IAM permissions
- VPC with at least one public and private subnet
- Basic knowledge of EC2, subnets, and endpoints

