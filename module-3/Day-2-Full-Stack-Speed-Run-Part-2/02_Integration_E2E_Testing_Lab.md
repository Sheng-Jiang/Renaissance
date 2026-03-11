# Lab: Front/Back Integration & End-to-End Testing

**Objective:** Connect the frontend and backend built on Day 1, hook up a real database, and write an End-to-End (E2E) test to prove it works.

## Step 1: Database Hookup
On Day 1, the backend returned static mockup data. Now, we connect it to a database.

1. Create a `docker-compose.yml` for Postgres if you don't have it running locally.
```yaml
version: '3.8'
services:
  db:
    image: postgres:15
    environment:
      POSTGRES_USER: dev
      POSTGRES_PASSWORD: dev
      POSTGRES_DB: appdb
    ports:
      - "5432:5432"
```
2. Run `docker-compose up -d`.
3. Instruct your backend AI Agent to replace the static mocks with a real DB connection (using an ORM like Prisma or SQLAlchemy) that adheres to `contract.md`.

## Step 2: Resolve CORS and Proxies
1. Open `vite.config.ts` in your frontend directory.
2. Configure a strict proxy so the frontend treats API calls as same-origin during local development.

**Example Vite Proxy:**
```typescript
export default defineConfig({
  plugins: [react()],
  server: {
    proxy: {
      '/api': 'http://localhost:3000' // Target your backend port
    }
  }
})
```

## Step 3: Frontend Integration
1. Remove the mock service layer in React.
2. Ensure your fetch calls point to `/api/...`.
3. Start both servers:
   - Backend: `npm run start:dev` (or Python equivalent)
   - Frontend: `npm run dev`
4. Load the app in your browser and verify the data flows from DB -> API -> React UI.

## Step 4: End-to-End Testing (E2E)
Write one "golden path" test to prove the system works. We recommend Playwright.

1. In the root of your project: `npm init playwright@latest`
2. Create `tests/integration.spec.ts`.
3. Instruct your agent to write a simple test: "Navigate to localhost:5173, verify the page title, and verify that the data payload from the API is successfully rendered in the DOM list."

## Step 5: Verification Task
Run `npx playwright test`. If it passes, your 2-day Full-Stack Speed Run is complete! 🎉
