# 🌍 Amazon CloudFront CDN Lab

**AWS Hands-On Project | Cloud Engineering Portfolio**

---

## 📖 Overview

This project demonstrates how to deliver content globally using **Amazon CloudFront**, AWS’s Content Delivery Network (CDN).

I built a simple architecture where an image stored in **Amazon S3** is delivered through CloudFront’s global edge locations for faster performance, lower latency, and secure origin access.

This simulates how real companies accelerate websites, media platforms, and static web applications for users worldwide.

---

## 🎯 What This Project Shows

* Understanding of CDN architecture
* Hands-on experience with AWS CloudFront
* Integration between S3 and CloudFront
* Performance optimization using caching
* Secure origin configuration

---

## 🧱 Architecture (Simple View)

```
User Browser
     │
     │ Request image
     ▼
CloudFront Edge Location
     │
     │ (Cached → Fast delivery)
     │
     └── If not cached
           ▼
        Amazon S3
        (Origin Storage)
```

**Flow:**

1. User requests content
2. CloudFront checks nearest edge server
3. If cached → delivered instantly
4. If not cached → fetched from S3 and stored at edge

---

## ⚙️ Technical Steps Completed

### 1️⃣ Created S3 Origin

* Created a private S3 bucket
* Uploaded a test image
* Verified direct access was blocked

**Skill:** Secure storage configuration

---

### 2️⃣ Created CloudFront Distribution

* Selected S3 bucket as origin
* Used default performance settings
* Waited for distribution deployment

**Skill:** CDN setup & origin integration

---

### 3️⃣ Delivered Content via CloudFront

CloudFront generated a public delivery domain such as:

```
a1bc2d3ef45g.cloudfront.net
```

This domain is used to serve files stored in S3.

---

### 4️⃣ Tested CDN Delivery

Created a simple HTML test file:

```html
<html>
  <head>
    <title>CloudFront Test</title>
  </head>
  <body>
    <p>Testing image delivery via CDN</p>
    <img src="https://YOUR-DOMAIN/YOUR-IMAGE.jpg">
  </body>
</html>
```

Observed:

* First load → fetched from S3
* Next loads → served faster via edge cache

**Skill:** Understanding caching & performance behavior

---

## 🧠 Cloud Concepts Learned

* Content Delivery Networks (CDN)
* Edge locations
* Caching strategy
* Origin-based architecture
* Latency reduction
* Secure storage + public delivery separation

---

## 🌍 Real-World Use Cases

CloudFront is used by companies for:

* Website acceleration
* Video streaming platforms
* Image hosting
* Global SaaS applications
* Static site delivery
* Software downloads

This same architecture is used by:

* E-commerce platforms
* Media companies
* Large global apps

---

## 🛠️ AWS Services Used

* Amazon CloudFront
* Amazon S3

---

## 💼 Why This Matters for Cloud Roles

This project demonstrates practical experience with:

* Global content distribution
* Performance optimization
* CDN design principles
* Secure origin architecture

It shows the ability to:

* Improve application speed
* Design scalable delivery systems
* Work with production-level AWS services

---

## 🚀 Future Improvements

Planned enhancements:

* Add custom domain + HTTPS
* Integrate Route 53
* Enable WAF protection
* Tune caching policies
* Host a full static website via CloudFront

---

## 👤 Author

**GitHub:** CloudWthAlex
**Path:** Cloud Engineer
**Focus:** AWS • Networking • Performance • Infrastructure
