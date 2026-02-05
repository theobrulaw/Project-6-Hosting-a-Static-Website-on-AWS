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

User → Route 53 → CloudFront → S3 Bucket


### Core Components

- **Amazon S3:** Stores static website files (HTML, CSS, JS, assets)  
- **CloudFront CDN:** Caches and delivers content globally  
- **ACM Certificate:** Enables HTTPS security  
- **Route 53:** Routes custom domain traffic to CloudFront  

---

## Prerequisites

- AWS account with S3, CloudFront, Route 53, and ACM permissions  
- Registered domain name  
- Basic understanding of:
  - Static web hosting concepts  
  - DNS fundamentals  
  - CDN behavior  
- Website files ready for deployment  

---

## Steps Performed

1. Created S3 bucket for static website hosting  
2. Uploaded website files and configured permissions  
3. Enabled static website hosting in bucket settings  
4. Requested SSL certificate via ACM  
5. Created CloudFront distribution pointing to S3 origin  
6. Attached SSL certificate to CloudFront  
7. Configured Route 53 DNS alias to CloudFront  
8. Tested global access and HTTPS connectivity  

---

## Validation & Verification

The deployment was validated by:

- Website accessible via CloudFront domain  
- Custom domain resolving correctly  
- HTTPS connection verified with valid certificate  
- Fast load times from multiple locations
- Executed/tested multiple invalidations in CloudFront clearing cache at Edge Locations  

### Key Observations

- CloudFront caching reduced latency significantly  
- S3 provided durable, low-cost storage  
- SSL enabled secure content delivery  
- No server management required  

---

## Security & Operational Considerations

- HTTPS enforced for all traffic  
- Public access controlled through bucket policies  
- CloudFront origin access restrictions  
- Minimal attack surface (no compute layer)  

### Operational Trade-offs

- Static-only content (no server-side processing)  
- Cache invalidation required for updates  
- CDN introduces additional configuration  

---

## Lessons Learned

- Serverless hosting is cost-effective and scalable  
- CloudFront dramatically improves global performance  
- S3 simplifies static content management  
- DNS + CDN integration is powerful for production websites  

### Future Improvements

- Implement CI/CD pipeline for automatic deployments  
- Add AWS WAF for security filtering  
- Enable versioning and rollback strategies  
- Use Lambda@Edge for advanced routing  

---

## Project Summary

Hosted a secure, globally distributed static website using Amazon S3, CloudFront, and Route 53 with SSL/TLS encryption for fast and cost-effective content delivery.

This project demonstrates modern serverless web hosting architecture on AWS.
