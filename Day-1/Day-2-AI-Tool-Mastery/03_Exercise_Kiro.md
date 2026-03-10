# Exercise: Kiro (Spec-Driven Development)
**Time: 60 Minutes**

## Overview
Kiro enforces a "think before you code" workflow. The spec *is* the architecture document. In this exercise, you will connect Kiro to your repository and guide it from natural language to structured code.

## Pre-requisites
Connect Kiro to your GitHub repository.

## Part 1: Feature Request
1.  **Input:** Give Kiro the following feature request:
    > "Build a CLI tool that converts CSV files to JSON with filtering and validation."

2.  **Review the Specs:** Kiro translates your request into EARS notation (`requirements.md`), a design file (`design.md`), and an implementation plan (`tasks.md`).
    *   *Are the requirements complete?*
    *   *Is the design sound?*
    *   *Did it cover edge cases like empty CSV cells, mismatched headers, or invalid JSON encoding?*

## Part 2: Generate Code
Let Kiro generate the code based on the approved specifications.

**Verification Step (Crucial):**
Verify the generated code against the initial specs. Does the code fulfill the `requirements.md` exactly? If not, why?

## Part 3: Hooks
Test الكiro's Agent Hooks.
*   Setup a hook to auto-run your test suite on save.
*   Setup a hook to auto-update the documentation whenever the core logic changes.
