---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# 🚀 Module 3: Full-Stack Development at Speed
## Day 5: Cloud-Agnostic Containerized Deployment
**Renaissance Developer Academy**

---

![bg right:60% fit](cover.png)

## Overview

1. **The Cloud Agnostic Dream:** Write once, run anywhere.
2. **Container runtimes:** Why Docker won.
3. **PaaS vs. IaaS:** Vercel vs. AWS EC2 vs. Cloud Run.
4. **Deploying the Speed Run:** Shipping your app.
5. **The Capstone Architecture:** Documenting what you built.

---

## ☁️ Why Cloud-Agnostic?

Vendor lock-in is expensive. If you rely on 14 proprietary AWS services, you can never leave AWS.

**The Container:**
Docker standardizes the environment. An Alpine Linux container running Node 20 behaves exactly the same on your laptop, on a Raspberry Pi, on Azure, and on Google Cloud.

If it runs in Docker, it's portable.

---

## 🚢 Where to Deploy?

Evaluating your targets:

1. **Vercel / Netlify (PaaS):** Amazing for Frontend. Difficult for complex Backend state/WebSockets.
2. **Heroku / Render / Railway (PaaS):** Extremely easy. Link GitHub and deploy. Slightly more expensive at scale.
3. **AWS EC2 / DigitalOcean Droplets (IaaS):** Total control. Maximum pain configuring Linux directly.
4. **Google Cloud Run / AWS Fargate:** The sweet spot. Serverless container execution. Give it a Docker image, it handles scaling and SSL automatically.

---

## ⚡ Connecting the Database in Prod

Your app needs to talk to a Production Database, not `localhost:5432`.

1. Provision a managed DB (Supabase, Neon, AWS RDS, Render DB).
2. Get the Connection String (e.g., `postgres://user:pass@host:5432/db`).
3. Inject the connection string securely as an **Environment Variable** into your container at runtime.
4. Set up an automated way to run Migrations against production.

---

## 🛠 Today's Mission

**Cloud Deployment & Documentation**

1. Deploy the Docker container built on Day 4 to a cloud provider (e.g., Render, Railway, or Google Cloud Run).
2. Hook it up to a live, managed PostgreSQL database.
3. Fill out the **Architecture Walkthrough Document** template to submit your Module 3 capstone.

*Congratulations on surviving the Full-Stack Speed Run!*
