# Project 6: Hosting a Static Website on AWS

## Objective

This lab demonstrates how to host a highly available, cost-effective static website on AWS using Amazon S3, Amazon CloudFront, and Amazon Route 53 with SSL/TLS security.

The project reflects real-world cloud architecture used for fast global content delivery, minimal operational overhead, and secure access to static web applications.

---

## Architecture / Environment Overview

The environment consists of:

- Amazon S3 bucket configured for static website hosting  
- Amazon CloudFront distribution for global content delivery  
- AWS Certificate Manager (ACM) SSL/TLS certificate  
- Amazon Route 53 for custom domain DNS routing  
- Public DNS access to CloudFront endpoints  

### Content Delivery Flow



