
# AWS Static Website Deployment Project

## 📌 Project Overview
Deployed a fully functional static portfolio website using Amazon Web Services (AWS), implementing scalable cloud storage and global content delivery. This project demonstrates hands-on experience with core cloud infrastructure concepts including storage configuration, access control, and CDN-based performance optimization.

---

## ☁️ AWS Services Used
- **Amazon S3** – Hosted static website files and configured bucket policies for public access
- **Amazon CloudFront** – Distributed content globally using a CDN for low-latency delivery and HTTPS security
- **AWS IAM** – Configured least-privilege users, roles, and policies to control access to the bucket

---

## ⚙️ Key Implementations
- Configured an Amazon S3 bucket for static website hosting
- Implemented bucket policies and IAM least-privilege access controls to allow secure public read access
- Deployed a CloudFront distribution connected to the S3 origin
- Configured default root object (`index.html`) for proper site routing
- Verified global HTTPS-enabled access via the CloudFront endpoint

---

## 🐛 Troubleshooting & Fixes

**Issue 1 — Site wouldn't render after upload**
The uploaded index file had picked up a duplicated file extension during export from GitHub, so CloudFront didn't recognize it as a valid root object. Diagnosed by checking the file name directly in the S3 bucket, corrected the naming, and redeployed — resulting in a fully `Enabled` CloudFront distribution.

**Issue 2 — CloudFront served an outdated version after an update**
After updating the site's files in S3, the CloudFront URL kept displaying the previous version while the direct S3 object URL showed the change immediately — standard CDN edge-caching behavior, since CloudFront won't re-fetch from the origin until told to. Resolved by creating a CloudFront invalidation (`/*`) to force a refresh from S3.

---

## 🚀 Key Outcomes
- Successfully deployed a live, globally accessible website using AWS cloud infrastructure
- Improved performance and latency using CDN-based delivery via CloudFront
- Gained practical experience diagnosing and resolving real deployment issues — file naming, routing, and CDN caching behavior
- Built a working understanding of static web hosting, CDN cache invalidation, and cloud architecture fundamentals

---

## 🧠 Skills Demonstrated
- Cloud Infrastructure Deployment (AWS)
- Static Website Hosting
- Content Delivery Network (CDN) Configuration & Cache Invalidation
- Access Control & IAM Least-Privilege Policy Management
- Troubleshooting and Root-Cause Diagnosis
- Basic Cloud Architecture Design

---

## 🔗 Live Links
- **Live Site:** https://d128r20xpbuxt8.cloudfront.net/
- **GitHub Repo:** https://github.com/tylertbrice12-hue/aws-static-website-project

---

## 📖 Notes
This project was deployed using Amazon S3 for storage and Amazon CloudFront for global content delivery, with IAM controlling access. It serves as a foundational cloud project demonstrating real-world AWS deployment and troubleshooting skills — not just following a tutorial, but diagnosing and fixing the same kinds of issues that come up in production environments.
