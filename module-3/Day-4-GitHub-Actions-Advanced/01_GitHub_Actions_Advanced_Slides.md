---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# 🚀 Module 3: Full-Stack Development at Speed
## Day 4: GitHub Actions Advanced
**Renaissance Developer Academy**

---

![bg right:60% fit](cover.png)

## Overview

1. **Continuous Integration:** The heartbeat of modern software.
2. **Matrix Builds:** Test across multiple environments simultaneously.
3. **Dependency Caching:** Speed up your build times.
4. **Docker Publishing:** From source code to a consumable artifact.

---

## 🏗 Continuous Integration (CI)

If it isn't in `main`, it doesn't exist. If `main` doesn't build, you have a crisis.

- **Linting:** Enforce code style automatically.
- **Unit Testing:** Run fast, isolated tests on every commit.
- **E2E Testing:** Run browser tests via Playwright/Cypress on PRs.
- **Blocking PRs:** Protect the `main` branch. A PR cannot merge if the CI pipeline fails.

---

## 🔀 Matrix Builds

Does your code work on Node 18? What about Node 20? Windows vs. Ubuntu?

Instead of writing five workflows, use a **Matrix Strategy**.

```yaml
strategy:
  matrix:
    node-version: [18.x, 20.x]
    os: [ubuntu-latest, windows-latest]
```
GitHub Actions will automatically spin up 4 parallel jobs to test every combination.

---

## ⚡ Dependency Caching

Downloading `node_modules` or Python `pip` packages repeatedly wastes time and money.

**Action:** `actions/setup-node` or `actions/cache`
- Cache key relates to `package-lock.json` or `requirements.txt`.
- If the file hasn't changed, the CI restores the cached dependencies in seconds.

*Speed is a feature of your development workflow.*

---

## 🐳 Docker Publishing

The final step of CI is creating the immutable artifact: the Docker Image.

1. **Build:** Run `docker build` using the Dockerfile.
2. **Tag:** Tag it with the Git commit hash (e.g., `myapp:a1b2c3d`).
3. **Push:** Upload it to GitHub Container Registry (ghcr.io) or Docker Hub.

*Tomorrow, we deploy this image to the cloud.*

---

## 🛠 Today's Mission

**Matrix Builds & Docker Lab**

1. Write a GitHub Action to test your Full-Stack app.
2. Implement caching to get the build time under 2 minutes.
3. Write a Dockerfile for the production build.
4. Automate the process of building and pushing that Docker image to the registry upon merge to `main`.
