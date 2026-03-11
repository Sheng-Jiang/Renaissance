# Lab: Schema Design & Migrations

**Objective:** Design a relational schema for a new application feature, write a migration script to implement it safely, and execute it against a local Postgres database.

## Step 1: Scenario
You are building the "Comments" feature for the Full-Stack app built on Day 1 and 2.

**Requirements:**
- A `Comment` belongs to a `Post` (or `Item`).
- A `Comment` belongs to an `Author` (User).
- We need the `content` (text) and standard timestamps (`created_at`, `updated_at`).
- We need a `soft_delete` mechanism.

## Step 2: AI-Assisted Schema Design
Instruct your AI agent to propose a Database Schema.

**Prompt to try:**
> "I need a PostgreSQL schema for a Comments feature. It needs to relate to an existing `users` table and `posts` table. Include `created_at`, `updated_at`, and a `deleted_at` timestamp for soft deletes. Provide the raw SQL CREATE TABLE statements with appropriate foreign key constraints."

Review the agent's output. Does it include `ON DELETE CASCADE`? Should it? (Discuss with your peer).

## Step 3: Implement via ORM/Migrations
Depending on your stack (Prisma for TS, Alembic for Python):

**If using Prisma:**
1. Update `schema.prisma` with the new models.
2. Run `npx prisma migrate dev --name add_comments`.
3. Check the generated SQL in the `migrations` folder. Is it what you expected?

**If using Raw SQL/Flyway/Goose:**
1. Create a file `V2__add_comments_table.sql`.
2. Paste the `CREATE TABLE` script.
3. Run your migration tool.

## Step 4: Verify the State
1. Open a DB visualizer (DBeaver, TablePlus, or psql).
2. Verify the new table exists.
3. Check the Foreign Key constraints via the DB UI.
4. Insert a row manually to confirm constraints work correctly.

**Success!** You've successfully evolved your data layer locally. In Day 4/5, we'll see how GitHub Actions automates this in production.
