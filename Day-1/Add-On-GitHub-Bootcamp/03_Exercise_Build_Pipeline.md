# Guide: Build Your First Pipeline
**Time: 45 Minutes**

## Overview
You will build a GitHub Actions Continuous Integration (CI) pipeline from scratch (not copy-pasted). This pipeline will run automatically every time you push code to your repository or open a Pull Request.

## Instructions
1. In the root of your portfolio repo, create the workflow directory:
   `mkdir -p .github/workflows`
2. Create a file named `ci.yml`.

### Step 1: The Trigger
Configure the workflow to run `on: [push, pull_request]`.

### Step 2: The Job and Environment
Create a job called `build-and-test`. Set it to `runs-on: ubuntu-latest`.

### Step 3: The Steps
Add the following steps logically using YAML:
1.  **Checkout:** Use `actions/checkout@v4` to bring your code into the runner.
2.  **Setup Node (or Python):** Use `actions/setup-node@v4` (or setup-python) to install the necessary environment.
3.  **Install:** Run `npm install` (or `pip install -r requirements.txt`).
4.  **Lint:** Add a script to run a linter (e.g., `npm run lint`).
5.  **Test:** Add a script to run your test suite (e.g., `npm run test`).

### Step 4: Verification
1. Commit the `.github/workflows/ci.yml` file and push it.
2. Go to the **Actions** tab in your GitHub repository.
3. Watch the workflow execute. Debug it using the logs if it fails.
4. **Final Polish:** Add the workflow status badge markdown to your repository's `README.md`.
