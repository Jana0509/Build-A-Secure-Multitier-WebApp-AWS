# Build-A-Secure-Multitier-WebApp-AWS
Building and Hosting a Secure Multi-tier Web Application using various Security Services and following security protocols on AWS


## Introduction:
This Project demonstrates building and hosting a multi-tier web application by following good security practices and integrating with various AWS security services to identity and fix the security issues without compromising the website by internal attacks. Implemented the security best practices from CDN to the DB layer so there are very less chances for the man in the middle attack. Leveraged Public SSL certificates at the Cloudfront and ALB for the secure transfer of request and response, build a inbound and outbound rules with security group and NACL and followed the security group chaining such as only the SG of public subnet can reach to the private subnet such as EC2 and only EC2 can talk with DB layer. Leveraged AWS Config to Cloudfront and S3 to identity the compliance, Amazon Inspector to identity the vulnerability present across EC2, Created the customer managed KMS key to encrypt the blog storage volume in EC2.

## Architecture Overview: 

<img width="865" alt="Screenshot 2025-02-22 at 11 49 42 AM" src="https://github.com/user-attachments/assets/b7efac90-43e0-4192-8389-adaef8d27861" />

##
