# AWS Three-Tier Web Application with RDS MySQL Multi-AZ



## Project Overview



This is my hands-on AWS Cloud project implementing a scalable three-tier web application using AWS networking, compute, storage, load balancing, auto scaling, and managed database services.



The application separates the infrastructure into three layers:



1\. Web Tier â€“ React frontend served using Nginx.

2\. Application Tier â€“ Node.js backend managed using PM2.

3\. Database Tier â€“ Amazon RDS for MySQL with Multi-AZ deployment.



## Architecture



Internet â†’ Internet-facing Application Load Balancer â†’ Web Tier â†’ Internal Application Load Balancer â†’ Application Tier â†’ Amazon RDS for MySQL.



## AWS Services Used



\- Amazon VPC

\- Public and Private Subnets

\- Internet Gateway

\- NAT Gateways

\- Route Tables

\- Security Groups

\- AWS IAM

\- Amazon EC2

\- Amazon Machine Images (AMI)

\- Launch Templates

\- Auto Scaling Groups

\- Application Load Balancers

\- Target Groups

\- Amazon S3

\- Amazon RDS for MySQL

\- AWS Systems Manager Session Manager



## Network Configuration



**AWS Region:** Asia Pacific (Mumbai) â€“ `ap-south-1`



**VPC Name:** `awsthreetierworkshop`



**VPC CIDR:** `10.0.0.0/16`



### Subnets



| Subnet | CIDR | Availability Zone |

|---|---|---|

| Public-Subnet-AZ-1 | 10.0.0.0/24 | ap-south-1a |

| Public-Subnet-AZ2 | 10.0.1.0/24 | ap-south-1b |

| Private-Subnet-AZ1 | 10.0.2.0/24 | ap-south-1a |

| Private-Subnet-AZ2 | 10.0.3.0/24 | ap-south-1b |

| Private-DB-Subnet-AZ1 | 10.0.4.0/24 | ap-south-1a |

| Private-DB-Subnet-AZ2 | 10.0.5.0/24 | ap-south-1b |



## Web Tier



\- React frontend application.

\- Nginx web server.

\- Internet-facing Application Load Balancer.

\- Web Tier Target Group.

\- Web Tier Launch Template.

\- Web Tier Auto Scaling Group.



## Application Tier



\- Node.js backend application.

\- PM2 process manager.

\- Internal Application Load Balancer.

\- Application Tier Target Group.

\- Application Tier Launch Template.

\- Application Tier Auto Scaling Group.



## Database Tier



\- Amazon RDS for MySQL.

\- Multi-AZ DB instance deployment.

\- Database name: `webappdb`.

\- Table: `transactions`.

\- Private database subnets.



## Implementation Overview



1\. Created the VPC and network infrastructure.

2\. Configured public, private application, and database subnets.

3\. Created and attached the Internet Gateway.

4\. Created NAT Gateways and configured route tables.

5\. Configured security groups for the load balancers, EC2 instances, and database.

6\. Created an IAM role for EC2 instances.

7\. Created an S3 bucket and uploaded application files.

8\. Deployed the Amazon RDS for MySQL Multi-AZ database.

9\. Configured the Application Tier EC2 instance and Node.js application.

10\. Configured database connectivity.

11\. Created the Application Tier AMI, Target Group, internal ALB, Launch Template, and Auto Scaling Group.

12\. Configured the Web Tier EC2 instance with React and Nginx.

13\. Built and deployed the React frontend.

14\. Created the Web Tier AMI, Target Group, external ALB, Launch Template, and Auto Scaling Group.

15\. Performed application and database testing.



## Troubleshooting



During implementation, I worked through issues involving:



\- AWS CLI installation and authentication.

\- React build and ESLint errors.

\- MySQL authentication compatibility.

\- Nginx configuration.

\- Frontend JavaScript asset loading.

\- S3 deployment and EC2 file updates.

\- Application troubleshooting through AWS Systems Manager.



## Key Learning Outcomes



This project provided hands-on experience with:



\- AWS networking and VPC architecture.

\- EC2 provisioning and Linux administration.

\- Application Load Balancers and Auto Scaling.

\- S3-based application deployment.

\- Amazon RDS and MySQL connectivity.

\- React frontend and Node.js backend deployment.

\- Nginx configuration and PM2 process management.

\- Cloud infrastructure troubleshooting.



## Author



**Rushikesh Shirsath**



This repository documents my hands-on AWS three-tier architecture implementation and learning.



