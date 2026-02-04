# 🚀 HunterCloudTech — Secure, Scalable Cloud Platform on AWS

**HunterCloudTech** is a real-world, production-style cloud infrastructure project built on AWS, designed to demonstrate **secure architecture, high availability, scalability, monitoring, and automation** — just like enterprise environments.

---

## 🌐 Live Demo

🔗 **Main Website:** [https://huntercloudtech.online](https://huntercloudtech.online)
🔗 **App Subdomain:** [https://app.huntercloudtech.online](https://app.huntercloudtech.online)
🔗 **API Subdomain:** [https://api.huntercloudtech.online](https://api.huntercloudtech.online)
🔗 **Admin Panel:** [https://huntercloudtech.online/admin](https://huntercloudtech.online/admin)

---

## 🏗️ High-Level Architecture

```
User
  ↓
Route 53 (DNS)
  ↓
CloudFront (Global CDN)
  ↓
AWS WAF (Security Layer)
  ↓
Application Load Balancer (HTTPS + Routing)
  ↓
Nginx (Reverse Proxy)
  ↓
Apache (Web Server)
  ↓
Application Layer
  ↓
S3 (Storage & Logs)
```

---

## ✨ Key Features

* 🔐 **End-to-End HTTPS (SSL via ACM)**
* 🌍 **Global Content Delivery using CloudFront**
* 🛡️ **Web Security with AWS WAF & Shield**
* ⚖️ **Load Balancing with ALB (Host & Path-Based Routing)**
* 📈 **Auto Scaling Group (ASG)**
* 📊 **Monitoring & Alerts using CloudWatch + SNS**
* 🤖 **Automation using Lambda & EventBridge**
* 🧾 **Centralized Logs in Amazon S3**
* 🧠 **Reverse Proxy Architecture (Nginx + Apache)**

---

## 🌐 Routing Strategy

### 🔹 Host-Based Routing

| Domain                       | Target           |
| ---------------------------- | ---------------- |
| `app.huntercloudtech.online` | App Target Group |
| `api.huntercloudtech.online` | API Target Group |

### 🔹 Path-Based Routing

| Path          | Target                |
| ------------- | --------------------- |
| `/admin/*`    | Admin Target Group    |
| `/` (default) | Frontend Target Group |

---

## 🧰 Tech Stack

| Layer           | Technology                      |
| --------------- | ------------------------------- |
| DNS             | AWS Route 53                    |
| CDN             | AWS CloudFront                  |
| Security        | AWS WAF, AWS Shield, ACM        |
| Load Balancer   | Application Load Balancer (ALB) |
| Compute         | EC2 (Auto Scaling Group)        |
| Reverse Proxy   | Nginx                           |
| Web Server      | Apache                          |
| Monitoring      | CloudWatch, SNS                 |
| Automation      | Lambda, EventBridge             |
| Storage         | Amazon S3                       |
| IaC (Optional)  | Terraform                       |
| Version Control | GitHub                          |

---

## 📸 Screenshots

All screenshots are stored in:

```
docs/Screenshots/
```
---

## 🎥 Demo Videos

Stored in:

```
docs/Demo/
```

| Demo                       | File       |
| -------------------------- | ---------- |
| Infrastructure Walkthrough | `demo.mp4` |
| Auto Scaling Test          | `ASG.mp4`  |

---

## 📁 Project Structure

```
huntercloudtech-cloud-platform/
│
├── admin/              # Admin panel frontend
├── api/                # API frontend
├── app/                # App frontend
├── docs/
│   ├── Screenshots/   # Architecture & AWS screenshots
│   └── Demo/          # Demo videos
├── index.html         # Main frontend
├── logo.svg
├── .gitignore
└── README.md
```

---

## ⚙️ Infrastructure Highlights

### 🔹 Auto Scaling

* Minimum Instances: 1
* Maximum Instances: 2
* Scale Trigger: CPU Utilization via CloudWatch

### 🔹 Monitoring

| Metric     | Threshold | Action           |
| ---------- | --------- | ---------------- |
| CPU > 10%  | Scale Out | SNS Alert + ASG  |
| Disk > 25% | Warning   | SNS Notification |

### 🔹 Logging

* Application logs → Amazon S3
* ALB Access Logs → S3
* Metrics → CloudWatch

---

## 🔐 Security Model

* SSL Certificates via AWS ACM
* HTTPS enforced at ALB & CloudFront
* AWS WAF Rules:

  * Rate Limiting
  * IP Allowlist
  * Common Web Exploit Protection
  * Layer 7 DDoS Protection

---

## 🚀 Deployment Flow

1. User hits domain
2. Route 53 resolves DNS
3. CloudFront caches and accelerates content
4. WAF filters malicious traffic
5. ALB routes request based on Host/Path
6. Nginx reverse proxies request
7. Apache serves content
8. Logs stored in S3
9. Metrics monitored in CloudWatch

---

## 🧪 Load Testing

CPU stress test:

```bash
sudo yum install stress -y
stress --cpu 2 --timeout 300
```

Triggers Auto Scaling + CloudWatch Alarm

---

## 🎯 Learning Outcomes

* Real-world AWS production architecture
* Zero Trust Security Implementation
* DNS, CDN, WAF, ALB integration
* Monitoring & Observability
* Auto Scaling & High Availability
* Logging & Auditing
* Infrastructure Automation

---

## 🧠 Resume-Ready Project Statement

Designed and deployed a **production-grade secure cloud platform on AWS** using Route 53, CloudFront, WAF, ALB, Auto Scaling, EC2, and S3. Implemented **end-to-end HTTPS, host and path-based routing, centralized logging, real-time monitoring with CloudWatch & SNS, and automated scaling policies**, demonstrating enterprise-level security, scalability, and high availability.

---

## Author
Mahaboob Basha  
Cloud Engineer | AWS | DevOps | Security

---

## ⭐ If you like this project

Give it a **star ⭐** — this helps showcase real-world cloud engineering skills to recruiters and hiring managers.

---





