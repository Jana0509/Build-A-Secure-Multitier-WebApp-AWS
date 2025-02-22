# Build-A-Secure-Multitier-WebApp-AWS
Building and Hosting a Secure Multi-tier Web Application using various Security Services and following security protocols on AWS


## Introduction:
The primary goal was to build a multi-tier architecture while following strong security principles across all layers—from the CDN and web tier to the database layer. I implemented strict security controls, encryption mechanisms, and continuous monitoring to prevent unauthorized access and ensure compliance with best practices. Implemented the security best practices from CDN to the DB layer so there are very less chances for the man in the middle attack. Leveraged Public SSL certificates at the Cloudfront and ALB for the secure transfer of request and response, build a inbound and outbound rules with security group and NACL and followed the security group chaining such as only the SG of public subnet can reach to the private subnet such as EC2 and only EC2 can talk with DB layer. Leveraged AWS Config to Cloudfront and S3 to identity the compliance, Amazon Inspector to identity the vulnerability present across EC2, Created the customer managed KMS key to encrypt the blog storage volume in EC2.

## Architecture Overview: 

![image](https://github.com/user-attachments/assets/ca06aefd-829a-4040-8d1a-d53112ec807f)


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
   

## Learnings:
1. Leveraged Various AWS Security Services such as AWS Config, Amazon Inspector, KMS key, Public Certificates, Custom Header setup and understand how security playes the vital role and 
   identifying the security gaps and fix using various AWS services.

2. Learned how to apply and what security services can be utilized across various layers of the architecture.

## Conclusion:
This project has significantly deepened my understanding of building a highly secure multi-tier web application by leveraging various AWS services. I’m excited to continue exploring the potential of AWS in delivering Highly secure solutions.

