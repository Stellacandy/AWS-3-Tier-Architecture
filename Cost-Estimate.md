Cost Breakdown by Component
1. Application Load Balancer (ALB)
   Purpose: Distributes incoming traffic

  Item Estimate
  ALB hourly cost: $0.025/hour
  Monthly cost: $18
  LCU(Load balancer capacity unit) usage (low traffic): $8
  Estimated ALB Cost: $25/month



2. EC2 Instances (Application Tier)
   2 × t3.micro instances (Auto Scaling Group)
   Purpose: Runs application logic


  Item	Estimate
  Cost per instance: $8.50/month
  Number of instances:	2
  Total EC2 cost: $17
  Estimated EC2 Cost: $17/month



3. Amazon RDS (Database Tier)
   db.t3.micro (Single AZ)
   Purpose: Stores relational data


  Item	Estimate
  RDS instance: $15
  Storage (20 GB): $2
  Backup storage: $1
  Estimated RDS Cost: $18/month



4. Amazon S3 (Object Storage)
   50 GB standard storage
   Purpose: Static assets & backups


  Item	Estimate
  Storage: $1.15
  Requests & data transfer: $1
  Estimated S3 Cost: $2/month



5. Amazon CloudWatch
  Purpose: Monitoring & logging
  
  Item	Estimate
  Metrics & alarms: $5
  Log ingestion: $3
  Estimated CloudWatch Cost: $8/month



6. Data Transfer (Outbound)
   Low traffic workload
   Purpose: User traffic leaving AWS

  
  Item	Estimate
  Data transfer: $5
  Estimated Data Transfer Cost: $5/month



Total Estimated Monthly Cost
Load Balancer: $25
EC2 Instances:	$17
RDS:	$18
S3:	$2
CloudWatch:	$8
Data Transfer:	$5
Estimated Total: $75 per month


Cost Optimization Considerations

The following measures can significantly reduce or increase costs:

1. Auto Scaling adjusts EC2 capacity based on demand

2. S3 lifecycle policies move infrequently accessed data to cheaper storage

3. RDS instance size can be adjusted based on usage

4. Reserved Instances or Savings Plans reduce EC2 and RDS costs

5. Monitoring usage prevents over-provisioning


Kindly note that the above cost estimates are based on my assumptions they are not actual costs. Each project varies in costs.
