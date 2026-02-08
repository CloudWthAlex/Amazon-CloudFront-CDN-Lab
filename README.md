# 🌍 Amazon CloudFront CDN Lab

**AWS Hands-On Project | Cloud Engineering Portfolio**

---

## 📌 Project Overview

This project demonstrates how to deliver content globally using **Amazon CloudFront**, a Content Delivery Network (CDN) service from AWS.

In this lab, I created a CloudFront distribution connected to an Amazon S3 bucket and used it to deliver an image through CloudFront’s global edge locations. This simulates how companies make websites and media load faster for users around the world.

This project focuses on performance, scalability, and real-world cloud architecture basics.

---

## 🎯 Objectives

By completing this lab, I learned how to:

* Create an Amazon S3 bucket to store content
* Upload and manage files in S3
* Create a CloudFront distribution
* Deliver content using a CloudFront domain
* Understand how caching improves performance

---

## 🧱 Architecture (Simple View)

```
User Browser
     │
     │ Requests image
     ▼
CloudFront (Edge Location)
     │
     │ If cached → delivered instantly
     │
     └── If not cached
           ▼
        Amazon S3
        (Origin Storage)
```

### Flow Explanation

1. A user requests an image
2. CloudFront checks the nearest edge location
3. If the image is cached → it is delivered immediately
4. If not cached → CloudFront retrieves it from S3 and stores it for future requests

---

## ⚙️ Technical Steps Completed

### 1️⃣ Created an S3 Bucket (Origin)

* Created a private S3 bucket
* Uploaded a test image file
* Verified direct public access was blocked

**Skill demonstrated:** Secure storage setup

---

### 2️⃣ Created a CloudFront Distribution

* Selected the S3 bucket as the origin source
* Used default CloudFront settings
* Waited for deployment to complete

**Skill demonstrated:** CDN configuration and origin integration

---

### 3️⃣ Delivered Content via CloudFront

CloudFront generated a public domain similar to:

```
a1bc2d3ef45g.cloudfront.net
```

This domain is used to securely deliver files stored in S3.

---

### 4️⃣ Tested CDN Performance

Observed behavior:

* First load → image fetched from S3
* Next loads → delivered faster from the nearest edge location

**Skill demonstrated:** Understanding caching and performance optimization

---

## 🧠 Cloud Concepts Learned

This project helped me understand:

* What a CDN is and why it is used
* How CloudFront reduces latency
* How edge locations improve speed
* How S3 works as an origin server
* How caching improves user experience

---

## 🌍 Real-World Use Cases

CloudFront is commonly used for:

* Website acceleration
* Image delivery for applications
* Video streaming platforms
* Static website hosting
* Global content distribution

This same architecture is used by:

* E-commerce websites
* SaaS platforms
* Media companies
* High-traffic global applications

---

## 🛠️ AWS Services Used

* Amazon CloudFront
* Amazon S3

---

## 🏆 Skills Gained

* CDN setup and configuration
* Origin and edge architecture understanding
* Performance optimization basics
* Secure content delivery design

---

## 💼 Why This Project Matters

This project shows hands-on experience with:

* Real AWS infrastructure
* Performance-focused architecture
* Global content delivery systems
* Core cloud networking concepts

It demonstrates the ability to understand how companies deliver fast, scalable web content worldwide.

---

## 🚀 Future Improvements

Planned next steps:

* Add custom domain with HTTPS
* Integrate Route 53
* Tune CloudFront caching policies
* Add AWS WAF for protection
* Host a full static website using S3 + CloudFront

---

## 👤 Author

**GitHub:** CloudWthAlex
**Career Path:** Cloud Engineer
**Focus Areas:** AWS • Networking • Performance • Infrastructure

---
