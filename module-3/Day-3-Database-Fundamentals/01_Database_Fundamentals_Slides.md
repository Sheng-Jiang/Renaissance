---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# 🚀 Module 3: Full-Stack Development at Speed
## Day 3: Database Fundamentals at Speed
**Renaissance Developer Academy**

---

![bg right:60% fit](cover.png)

## Overview

1. **Schema Design:** Getting it right the first time (mostly).
2. **Migrations:** Evolving your data layer without breaking apps.
3. **ORMs vs. Raw SQL:** Navigating the ecosystem.
4. **Query Optimization:** AI assistance with human judgment.

---

## 🏗 Schema Design First Principles

Your data structure outlives your application code.

- **Normalization:** Reduce redundancy (1NF, 2NF, 3NF).
- **Foreign Keys constraints:** Let the DB enforce data integrity.
- **Indexes:** Fast reads, slower writes. Don't index everything, only what you query by.
- **Soft Deletes:** `deleted_at` timestamp instead of `DELETE FROM`.

---

## 🔄 Migrations: The Time Machine

Never change your DB schema manually. Use migrations.

- **Idempotency:** Migrations should be repeatable.
- **Up / Down:** Every `up` (e.g., CREATE TABLE) needs a `down` (e.g., DROP TABLE).
- **State Management:** The database tracks which migrations have run (e.g., `_prisma_migrations` or `alembic_version`).

*Migrations treat your database schema as code.*

---

## 🔨 ORMs: Pros, Cons, and Traps

Object-Relational Mappers (Prisma, TypeORM, SQLAlchemy)

**The Good:**
- Type safety out of the box.
- Rapid iteration.
- Easy to read for basic CRUD.

**The Bad:**
- The N+1 Query Problem (e.g., fetching a post, then running a separate query for every author).
- Abstracting away slow SQL.

---

## 🏎 Query Optimization

When the ORM fails, you need raw SQL and `EXPLAIN ANALYZE`.

1. **Identify the bottleneck:** Slow query logs.
2. **Analyze the execution plan:** Look for Sequential Scans.
3. **Add Indexes:** B-Trees on heavily filtered columns.
4. **AI Assistance:** Paste the `EXPLAIN` output to an AI—but ALWAYS verify the suggested index makes sense.

---

## 🛠 Today's Mission

**Database Lab & Optimization Guide**

1. **Lab:** Design a schema for a new feature, write a migration, and apply it.
2. **Guide:** Go through the Query Optimization scenarios using AI tools to interpret `EXPLAIN` plans.

*Let's harden the data layer!*
