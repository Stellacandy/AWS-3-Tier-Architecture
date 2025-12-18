1. Component: Load Balancer
   AWS Service: ALB (Application Load Balancer)
   Purpose: This distributes user traffic. The Application Load Balancer receives incoming user requests and distributes them across multiple EC2 instances to ensure high availability,
   fault tolerance, and efficient traffic management.
   
2. Component: Web/App Servers
   AWS Service: EC2 (Elastic Compute Cloud) Application Tier
   Purpose: This is used to run the appplication. Amazon EC2 provides scalable virtual servers that run the application’s business logic,
   allowing the system to adjust capacity based on demand while maintaining performance.
   
3. Component: Database
   AWS Service: RDS
   Purpose: This is used to store structured data. Amazon RDS is a managed relational database service that stores application data securely while handling backups, patching,
   and high availability through features like Multi-AZ.
   
4. Component: Object Storage 
   AWS Service: S3 
   Purpose: This is for storing static files. Amazon S3 stores static assets, backups, and media files in a highly durable and cost-effective manner,
   reducing the load on application servers.
   
5. Component: Monitoring
   AWS Service: CloudWatch
   Purpose: This is for logs and metrics. Amazon CloudWatch collects metrics, logs, and events to monitor application performance and trigger alerts when thresholds are exceeded.
   
6. Component: Security
   AWS Service: IAM
   Purpose: This is used for access control. AWS IAM controls who can access AWS resources by defining users, roles, and permissions, ensuring secure and least-privilege access.
   




