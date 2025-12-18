AWS 3-Tier Architecture Documentation

Project Overview
This project documents a standard 3-tier web application architecture deployed on Amazon Web Services (AWS).  
The purpose of this project is to demonstrate a clear understanding of cloud architecture fundamentals, the interaction between AWS services, and the ability to document technical systems in a structured, professional manner.

This project focuses on architecture understanding and documentation, not on application development or deep infrastructure configuration. It reflects the type of work typically performed by Cloud Project Coordinators, Cloud Analysts, and Technical Project Managers supporting cloud engineering teams.


Architecture Overview
The 3-tier architecture separates the application into three logical layers:

1. Presentation Layer – Handles incoming user traffic  
2. Application Layer – Processes business logic  
3. Data Layer – Stores and manages persistent data  

This separation improves scalability, availability, security, and maintainability.



Architecture Diagram
(Full visual diagram available in the "3 tier architecture-diagram.png" file)



Architecture Components

Application Load Balancer (ALB)
The ALB receives incoming HTTP/HTTPS requests from users and distributes traffic across multiple EC2 instances. This ensures high availability and fault tolerance while supporting secure HTTPS communication.



Amazon EC2 (Application Tier)
EC2 instances host the application logic and handle user requests. Instances are deployed across multiple Availability Zones to improve resilience.



Auto Scaling Group
The Auto Scaling Group automatically adjusts the number of EC2 instances based on traffic demand and performance metrics. This helps maintain performance during peak usage while optimizing costs during low traffic periods.



Amazon RDS (Database Tier)
Amazon RDS is used as the managed relational database service to store application data. It provides automated backups, patching, and high availability features such as Multi-AZ deployment.



Amazon S3 (Object Storage)
Amazon S3 stores static assets such as images, documents, and application backups. This reduces the load on EC2 instances and improves storage durability and cost efficiency.



Amazon CloudWatch
CloudWatch provides monitoring and logging capabilities by collecting metrics, logs, and health checks across AWS resources. It supports alerting and operational visibility.



AWS Identity and Access Management (IAM)
IAM controls access to AWS resources by defining roles and permissions based on the principle of least privilege. This ensures secure interaction between services.



Virtual Private Cloud (VPC)
The VPC provides a logically isolated network environment where all resources are deployed. It allows control over subnets, routing, and network security.


Security Groups
Security Groups act as virtual firewalls that control inbound and outbound traffic to AWS resources based on predefined rules.



Data Flow Description
1. A user sends a request through a web browser.
2. The request is received by the Application Load Balancer.
3. The ALB forwards traffic to healthy EC2 instances in the Auto Scaling Group.
4. EC2 instances process the request and retrieve or update data in Amazon RDS.
5. Static content and backups are accessed from Amazon S3.
6. The processed response is returned to the user.



Security & Governance Considerations
- Database instances are placed in private subnets
- S3 buckets have public access blocked
- IAM roles are used instead of hard-coded credentials
- HTTPS traffic is enforced through the load balancer
- Centralized logging and monitoring are enabled via CloudWatch

These controls support data protection, compliance, and operational governance.



Monitoring & Operational Visibility
- CloudWatch monitors EC2 CPU utilization and instance health
- ALB health checks ensure traffic is routed only to healthy instances
- RDS performance metrics support database monitoring
- Alerts can be configured for threshold breaches



Cost Awareness
This architecture includes cost-optimization considerations such as:
- Auto Scaling to match demand
- Use of managed services (RDS, ALB)
- Offloading static content to S3
- Monitoring usage to avoid overprovisioning

Exact cost figures are not calculated, as the focus is architectural understanding.




Author: Stella Ojiuba
AWS Certified Cloud Practitioner  
AWS Solutions Architect – Associate  



