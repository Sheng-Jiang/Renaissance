---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# 🏗 Module 4: System Design & Architecture
## Day 3: Writing Architecture Decision Records (ADRs)
**Renaissance Developer Academy**

---

<!-- Note: Cover image generation paused due to rate limits -->
## Overview

1. **The 'Why' Factor:** Code tells you how, ADRs tell you why.
2. **The ADR Lifecycle:** Proposed, Accepted, Deprecated.
3. **The Format:** Context, Decision, Consequences.
4. **ADR Workshop:** Writing records for ambiguous choices.

---

## 🧐 Why write ADRs?

Imagine joining a company and finding they use MongoDB to store relational financial ledgers.
- You think: *"Who made this terrible decision?"*
- But maybe 4 years ago, the start-up had to pivot in 3 days, and MongoDB was the only tool the 1 engineer knew.

**Context is lost instantly.** An Architecture Decision Record (ADR) captures the context *when the decision was made*.

---

## 🏛 The ADR Format

Keep it in version control (e.g., `docs/adr/0001-use-react.md`).

**1. Title:** Short noun phrase.
**2. Status:** Draft, Accepted, Deprecated, Superseded.
**3. Context:** What is the problem? What are the technological, business, and timeline constraints?
**4. Decision:** What are we doing?
**5. Consequences:** What becomes easier? What becomes harder? (No decision is free).

---

## 🪚 The Engineering Compromise

There are no silver bullets in system design.

- **Option A (Microservices):** High scalability, allows distinct teams. **Consequence:** Massive operational overhead, difficult local dev.
- **Option B (Monolith):** Easy deployments, easy debugging. **Consequence:** Slower build times, tight coupling.

*A good ADR explicitly lists the options considered and why they were rejected.*

---

## 🛠 Today's Mission

**ADR Workshop**

1. We will give you a contentious technical scenario.
2. You will draft an ADR using the provided template.
3. You must articulate the **Consequences** (the pain you are choosing to inherit).

*An undocumented decision is a liability.*
