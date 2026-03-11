# Lab: Matrix Builds & Docker Publishing

**Objective:** Write an advanced CI pipeline using GitHub Actions that lints, tests (using a matrix strategy), builds a Docker container, and publishes it to the GitHub Container Registry.

## Step 1: The Basic CI Pipeline
Create a file at `.github/workflows/ci.yml`.

Instruct your AI agent:
> "Write a GitHub Actions CI workflow for my Node/React monorepo. It should trigger on Pull Requests. It must include dependency caching, linting, and running unit tests."

## Step 2: Add a Matrix Build
Modify the testing job to use a matrix strategy to test across multiple Node versions.

```yaml
jobs:
  test:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        node-version: [18.x, 20.x]
    steps:
      - uses: actions/checkout@v4
      - name: Use Node.js ${{ matrix.node-version }}
        uses: actions/setup-node@v4
        with:
          node-version: ${{ matrix.node-version }}
          cache: 'npm'
      # Run tests here...
```

## Step 3: Write the Production Dockerfile
The Dockerfile should use a multi-stage build.

1. **Build Stage:** Use a heavy Node image to `npm install` and build the Vite frontend and compile the backend TypeScript.
2. **Production Stage:** Use a lightweight Alpine Linux image. Copy ONLY the compiled artifacts over.

*Use an AI agent to help draft this multi-stage Dockerfile safely.*

## Step 4: The Publish Pipeline
Create a second workflow `.github/workflows/publish.yml` that triggers only when code is merged into `main`.

1. Log into the GitHub Container Registry (`ghcr.io`) using the `GITHUB_TOKEN`.
2. Build the Docker image.
3. Tag the image with the Git Commit SHA (`${{ github.sha }}`).
4. Push the image to GHCR.

**Verify:** Merge a PR to main, watch the Actions tab, and confirm a new package appears in your GitHub repository packages section!
