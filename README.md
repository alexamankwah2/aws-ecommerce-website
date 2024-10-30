# Dynamic eCommerce Website on AWS
This repository contains the deployment scripts and reference architecture for a dynamic eCommerce website hosted on AWS. This project utilizes various AWS services to ensure high availability, scalability, and security.


## Project Overview
The dynamic eCommerce website is hosted in a highly available and scalable infrastructure setup on AWS. The architecture is designed to leverage multiple AWS services to provide an optimized, fault-tolerant solution with secure connectivity and automated management.

## Architecture Diagram
Refer to the architecture diagram in the diagrams folder for a visual overview of the deployment.


## AWS Resources and Configuration


**1. Virtual Private Cloud (VPC)**
Configured a VPC with both public and private subnets across two Availability Zones to ensure network isolation and resilience.

**2. Internet Gateway**
Deployed an Internet Gateway to enable communication between resources within the VPC and the internet.

**3. Security Groups**
Created Security Groups to serve as a network firewall, allowing only necessary traffic to specific resources.

**4. Availability Zones**
Leveraged two Availability Zones to enhance reliability and fault tolerance.

**5. Public Subnets**
Public subnets were designated for the NAT Gateway and Application Load Balancer to facilitate secure internet connectivity and load distribution.

**6. EC2 Instance Connect Endpoint**
Configured an EC2 Instance Connect Endpoint to securely connect to resources in both public and private subnets.

**7. Web Servers (EC2 Instances)**
Deployed EC2 instances within private subnets to host the website, enhancing the security of application components.

**8. NAT Gateway**
Configured a NAT Gateway for secure internet access for instances located in private subnets.

**9. Application Load Balancer**
Set up an Application Load Balancer with a target group to evenly distribute traffic to an Auto Scaling Group across multiple Availability Zones.

**10. Auto Scaling Group**
Configured an Auto Scaling Group to dynamically manage EC2 instances, ensuring optimal performance, availability, and fault tolerance.

**11. Certificate Manager**
Secured application communications with SSL/TLS certificates using AWS Certificate Manager.

**12. Simple Notification Service (SNS)**
Configured SNS to send alerts about activities in the Auto Scaling Group for real-time monitoring.

**13. Domain Registration and DNS (Route 53)**
Registered the domain name and configured DNS records using Amazon Route 53.

**14. Amazon S3**
Used S3 to store and manage application code and other assets.


## Getting Started
To set up this project in your own AWS environment, follow these steps:

***Clone the Repository:***
bash
Copy code
git clone <repository-url>
cd <repository-directory>


***AWS Configuration:***
Ensure your AWS CLI is configured with appropriate credentials and permissions.
Update the variables in the deployment scripts as necessary for your AWS setup.

***Run Deployment Scripts:***
Execute the deployment scripts in the scripts folder to provision the AWS resources and deploy the application.


## Monitoring and Alerts
The system uses AWS SNS to send notifications related to Auto Scaling activities. You can customize alert thresholds and notification preferences based on your monitoring requirements.


## Additional Information
For further details on each AWS service used in this architecture, refer to the AWS documentation linked below:
Amazon VPC
Amazon EC2
Amazon Route 53
Amazon S3


## License
This project is licensed under the MIT License. See LICENSE for more information.
