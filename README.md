AWS Multi-Branch Setup
Project Overview
This project involves migrating a multi-branch retail company's IT infrastructure from on-premises servers to AWS. The primary goal is to enhance scalability, reliability, and cost-effectiveness by leveraging AWS services. This repository contains all necessary configuration files and scripts.

Problem Statement
Company XYZ, a rapidly growing retail chain with branches in multiple cities, faced challenges in managing its on-premises IT infrastructure efficiently and securely as the company expanded. The IT team was tasked with migrating the company's servers and applications to the cloud.

Solution
Key Components
VPC (Virtual Private Cloud): Created separate VPCs for the main branch and additional branches.
Internet Gateway: Attached Internet Gateways to VPCs to enable internet access.
Subnets: Configured public and private subnets within each VPC.
Route Tables: Configured and associated route tables with the respective subnets.
NAT Gateway: Implemented NAT Gateways to allow private subnets to access the internet securely.
EC2 Instances: Launched and configured EC2 instances for various branches.
Security Measures: Applied security groups to control inbound and outbound traffic.
Transit Gateway: Deployed and configured Transit Gateway for efficient inter-branch communication.
Architecture Diagram
The architecture diagram illustrates the structure of the infrastructure, including VPCs, subnets, internet gateways, NAT gateways, route tables, security groups, and the Transit Gateway.

Prerequisites
An AWS account
Basic understanding of AWS services (VPC, EC2, NAT Gateway, Transit Gateway)
Familiarity with networking concepts
Setup Instructions
Step 1: Create VPCs
Open AWS Management Console.
Navigate to the VPC Dashboard.
Click on "Create VPC" and select "VPC only".
Enter the required IPv4 CIDR block and create the VPC.
Step 2: Attach Internet Gateway
Navigate to the Internet Gateway section in the VPC Dashboard.
Click on "Create Internet Gateway".
Name the gateway and attach it to the VPC created in Step 1.
Step 3: Create Subnets
In the VPC Dashboard, click on "Subnets".
Create public and private subnets within the VPC.
Ensure the public subnet is associated with a public IP address.
Step 4: Configure Route Tables
In the VPC Dashboard, click on "Route Tables".
Create route tables for public and private subnets.
Associate the subnets with the respective route tables.
Add routes for internet and NAT gateway access.
Step 5: Set Up NAT Gateway
In the VPC Dashboard, navigate to the NAT Gateways section.
Create a NAT Gateway and allocate an Elastic IP address.
Attach the NAT Gateway to the public subnet.
Step 6: Launch EC2 Instances
Navigate to the EC2 Dashboard.
Launch instances within the created subnets.
Configure instance details, storage, key pairs, and security groups.
Ensure public instances are assigned public IPs.
Step 7: Implement Security Measures
Define security groups to control inbound and outbound traffic.
Apply security groups to the EC2 instances based on the requirements.
Step 8: Deploy Transit Gateway
Navigate to the VPC Dashboard.
Select "Transit Gateway" and create a new Transit Gateway.
Name the Transit Gateway and configure necessary options.
Step 9: Create Transit Gateway Attachments
Attach the Transit Gateway to the VPCs.
Ensure all branches (VPCs) are connected to the Transit Gateway.
Step 10: Update Route Tables
Update route tables to direct traffic through the Transit Gateway.
Ensure proper routes are added to facilitate inter-branch communication.
Conclusion
By migrating to AWS, Company XYZ achieved enhanced scalability, improved reliability, and cost savings. The architecture provided by the Transit Gateway ensures robust security and efficient management of the network across multiple branches.

Author
P. Narendra

Acknowledgements
Instructor: Lavish Arora
