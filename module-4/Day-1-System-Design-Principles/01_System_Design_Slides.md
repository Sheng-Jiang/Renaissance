---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# 🏗 Module 4: System Design & Architecture
## Day 1: System Design & Progressive Architecture
**Renaissance Developer Academy**

---

![bg right:60% fit](cover.png)

## Overview

1. **Why Specs Matter:** Moving beyond hackathons.
2. **Progressive Complexity:** Evolution of a system.
3. **The Single Node:** Start simple and monolithic.
4. **The Distributed System:** Scaling out dynamically.
5. **System Design Workshop:** Whiteboarding reality.

---

## 🛑 Stop Coding. Start Thinking.

In Module 3, we optimized for velocity (Full-Stack Speed Run). In Module 4, we optimize for **resilience and scale**.

- **The Problem:** Building fast without a spec leads to unmaintainable spaghetti code. AI amplifies this problem—it can write bad code *very* quickly.
- **The Solution:** Specs drive everything. You must be an architect before you are a coder.

---

## 📈 Progressive Architecture

You don't need Kubernetes for a blog with 10 visitors.

1. **Phase 1 (Monolith):** One server. App code and DB on the same machine.
2. **Phase 2 (Decoupled):** Web server separated from Managed Database.
3. **Phase 3 (Scaled):** Load Balancer -> Multiple Web Servers -> Primary DB + Read Replicas.
4. **Phase 4 (Distributed):** Microservices, Message Queues (Kafka/RabbitMQ), Caching layers (Redis).

*Architect for ONE scale phase ahead of where you are.*

---

## 🔑 Key Components of Scale

When drawing architectures, you must know your primitives:

- **Load Balancers:** Nginx, HAProxy, AWS ALB. (Distributes traffic).
- **Caches:** Redis, Memcached. (Saves DB round trips).
- **Object Storage:** Amazon S3, GCS. (For images/videos).
- **CDN:** Cloudflare, Fastly. (Caches static assets at the edge).
- **Message Queues:** SQS, Kafka. (Asynchronous processing).

---

## 🛠 Today's Mission

**System Design Workshop**

We are going back to the whiteboard. No code today.

1. We will evaluate 3 system prompts.
2. You will draw the architecture diagram for each.
3. You must identify the bottlenecks, Single Points of Failure (SPOF), and trade-offs.

*Let's design for scale!*
