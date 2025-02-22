# Build-A-Secure-Multitier-WebApp-AWS
Building and Hosting a Secure Multi-tier Web Application using various Security Services and following security protocols on AWS


## Introduction:
This Project demonstrates building and hosting a multi-tier web application by following good security practices and integrating with various AWS security services to identity and fix the security issues without compromising the website by internal attacks. Implemented the security best practices from CDN to the DB layer so there are very less chances for the man in the middle attack. Leveraged Public SSL certificates at the Cloudfront and ALB for the secure transfer of request and response, build a inbound and outbound rules with security group and NACL and followed the security group chaining such as only the SG of public subnet can reach to the private subnet such as EC2 and only EC2 can talk with DB layer. Leveraged AWS Config to Cloudfront and S3 to identity the compliance, Amazon Inspector to identity the vulnerability present across EC2, Created the customer managed KMS key to encrypt the blog storage volume in EC2.

## Architecture Overview: 

<img width="865" alt="Screenshot 2025-02-22 at 11 49 42 AM" src="https://github.com/user-attachments/assets/b7efac90-43e0-4192-8389-adaef8d27861" />

## Project Highlights:

1. VPC
   * Created the VPC from scratch with public, private, and database subnets across multiple Availability Zones.

2. ALB:
   * Leveraged Application Load balancer for the high availability and for the efficient traffic distribution across multiple Azs

3. EC2:
   * Used as Compute for the static and dynamic application and present across multiple AZs for High availability.

4. RDS:
   * RDS Mysql is used as database for the application with primary and standby for Multi-Az deployment.

5. S3:
   * Stored the static web pages in the S3 for high durability.

6. KMS:
   * Created the customer managed KMS key for efficient security and used to encrypt the block storage volume.

7. Inspector:
   * Configured AWS Inspector  to EC2 instances for efficiently identifying the vulnerability across Multi-Azs

8. Config:
   * To identity Complaince status for the CDN and S3, leveraged AWS Config.
  
9. ASG:
    * Created the ASG for the EC2 instances for automatic scaling of instances if the instances goes down or high demand of traffic.

10. Launch Template:
    * Leveraged Launch template by configuring the OS, installing the web server and copying the Static files from S3 to reduce the application installing time once the instances are launched.

11. ACM:
    * Created the public certificate in certificate manager for seamless certificate management and used in CDN and ALB.
   
12. Route 53:
    * Created the domain in public hosted zone and leveraged Route 53 for the resolving the Ip address from the internet.

