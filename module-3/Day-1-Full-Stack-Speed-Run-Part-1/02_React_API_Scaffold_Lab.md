# Lab: React & API Scaffold

**Objective:** Set up the foundation for a full-stack application by scaffolding both the frontend and backend in parallel, and establishing a clear API contract.

## Prerequisites
- Node.js (v18+)
- Python (if using FastAPI, v3.10+)
- Postgres installed locally or via Docker
- Antigravity AI Assistant

## Step 1: The Monorepo Structure
Create a root directory for your project, and set up two main folders: `frontend` and `backend`.

```bash
mkdir my-fullstack-app
cd my-fullstack-app
mkdir frontend backend
```

## Step 2: Establish the API Contract
Before writing any code, define the communication protocol between the frontend and backend.

Create a file `contract.md` or `openapi.yaml` at the root.

**Example Contract:**
```json
// GET /api/v1/users
// Response:
{
  "status": "success",
  "data": [
    { "id": 1, "name": "Alice", "role": "admin" },
    { "id": 2, "name": "Bob", "role": "user" }
  ]
}
```

## Step 3: Scaffold the Frontend (React)
Instruct your AI agent to scaffold the frontend:
1. "Use Vite to create a React + TypeScript project in the `frontend` directory."
2. "Set up TailwindCSS for styling."
3. "Create a mock service layer that returns the exact JSON defined in `contract.md`."

## Step 4: Scaffold the Backend (API)
In a separate terminal (or using parallel agents):
1. "Set up an Express.js (or FastAPI) project in the `backend` directory."
2. "Create an endpoint for `GET /api/v1/users`."
3. "Return static data matching `contract.md` for now."

## Step 5: Verify Both Sides
1. Run the frontend (`npm run dev`) and ensure the UI renders the mock data.
2. Run the backend and hit the endpoint via `curl` or Postman to ensure it returns the correct payload structure.

**Ready for Part 2!** Tomorrow we integrate the true database and remove the mocks.
