Step 1: The User sends a request via a web browser and the request reaches the Application Load Balancer.
Step 2: Then the ALB routes traffic to available EC2 instances. The EC2 processes the request and retrieves data from the databse(RDS).
Step 3: Now all static files will be fetched from the S3 bucket and response is returned to the user.

