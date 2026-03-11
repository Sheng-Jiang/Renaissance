# Lab: Spec-Driven Application Build (Kiro Workflow)

**Objective:** Build a feature purely by writing requirements and letting an AI agent (Kiro/Antigravity) handle the design, planning, and execution phases.

## Step 1: Write Formal Requirements (EARS)
Create a file named `requirements.md` in a new directory.

We are building a **Rate Limiter Middleware** for an Express API.
Write the requirements using EARS notation.

**Example:**
- **Ubiquitous:** The system shall intercept all incoming HTTP requests.
- **Event-Driven:** WHEN a request is received, the system shall check the client IP address against the Redis cache.
- **State-Driven:** WHILE the client IP request count is below 100 within a 1-minute window, the system shall allow the request to proceed.
- **Unwanted (Error):** IF the client IP request count exceeds 100 within a 1-minute window, the system shall return an HTTP 429 Too Many Requests response.

## Step 2: Generate the Design
Open your AI terminal (e.g., Kiro).
Run the command to generate a design based *strictly* on the requirements document.

> "Read `requirements.md` and generate a formal `design.md`. Include the interface definition for the middleware and the exact Redis schema we will use to track IPs."

Review `design.md`. Does it capture the EARS logic perfectly? If not, fix the requirements, not the design.

## Step 3: Generate the Task List
> "Read `design.md` and generate a `tasks.md` checklist. Break the work down into atomic, test-driven steps."

## Step 4: Execute
Instead of coding, you are now the **Manager**.
Instruct your agent:
> "Execute the first task in `tasks.md`."

Review the code. If it passes, check the box and proceed to task 2.

**Takeaway:** The more time you spend in Phase 1 (Requirements), the faster and safer Phase 4 (Execution) becomes.
