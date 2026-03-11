# Lab: Deploying to the Cloud

**Objective:** Deploy the full-stack container you built on Day 4 to a real cloud environment, hook it up to a production database, and verify it live on the internet.

## Step 1: Provision a Production Database
We strongly recommend a serverless Postgres provider for speed:
- **Neon:** Generates connection strings instantly.
- **Supabase:** Full features, rapid Postgres provisioning.
- **Render:** Can spin up a Postgres instance alongside your app.

1. Create a database.
2. Under "Connection Details", copy the connection URL. Keep it secret.

## Step 2: Choose a Deployment Target
We recommend **Render**, **Railway**, or **Google Cloud Run** for Docker-based deployments.

**If using Render (Web Service):**
1. Connect your GitHub Repo.
2. Select "Docker" as the Runtime.
3. Under Environment Variables, add `DATABASE_URL` and paste your connection string.
4. Deploy!

## Step 3: Production Migrations
Your app is running, but the database schema is empty.

1. Ensure your deployment scripts or CI pipeline runs database migrations before your app starts up.
   - Using Prisma: `npx prisma migrate deploy` (Do not use `dev` in prod!)
   - You can add this to your Dockerfile CMD: `CMD npx prisma migrate deploy && npm run start:prod`
   
**Warning:** Be very careful running migrations on large production databases later in your career.

## Step 4: Verification
1. Open the public URL provided by your hosting platform.
2. Perform the exact same End-to-End test flow you wrote on Day 2.
3. Verify that data persists even if the container restarts.

## Step 5: Document the Architecture
Now that you've shipped a full-stack app, database, and CI/CD pipeline, it's time to document it.

Complete the `03_Architecture_Walkthrough_Template.md` provided in this directory and commit it to your repository. This earns your **Full-Stack Builder** badge!
